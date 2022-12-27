- 👋 Hi, I’m @tiantianxiangshangjt
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
tiantianxiangshangjt/tiantianxiangshangjt is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Testkey的程序概括：
  ChannelMap声明:layout_connect--pad_numbers--探针卡--测试板卡（对照文件，一一对应）
  Signal声明：signal style:
                In     (PPMU&DCL)
                Out    (PPMU&DCL)
                InOut  (PPMU&DCL)
                Supply (DPS)
  Main program: 函数声明和调用（C++ & AItest API）
    常用Programing API
      theHW.PPMU() // <=6.5 V 设置电压
      thHW.DPS() // -10 to 10 V 设置电压
      theHW.DCL() // SetVIHH: 0-13 V 设置电压
      theHW.SignalMap.SetGroupName() // 添加Signal group
      theHW.SignalMap.GetMember() // 获取Signal group
      theMgr.SetCurTestName() // 输出的字符串在Debug windows
      theMgr.SetCurTestNumber() //输出的数字在Debug windows
      theHw.Util().DisplayLog() // 输出显示字符串在Debug windows
      theHw.Util().Debug(); // 输出显示字符串在Debug windows
 Code内容：Debug windows
    头文件声明：
      #include "stdafx.h"
      #include "UserUnit.h"
      #include <string>
    函数声明：
    void(read_single_cell)
    void(read_by_WL)
    void(PGM_single_cell)
    void(ERS_single_cell)
    主函数：
    WX_FUNCTION(function name)  //为了wxFlow定义的，wxFlow中包含多个WX_FUNCTION
    {
    // 声明数组变量，用于抓取signal_group
    // 变量初始化，定义读、写、擦除操作的模式与条件
    // initial_read
        上电
        调用函数
        下电
    // program
        上电
        调用函数
        下电
    // read_after_program
        上电
        调用函数
        下电
    // erase 
        上电
        调用函数
        下电
    // read_after_eras
        上电
        调用函数
        下电
    }
    
