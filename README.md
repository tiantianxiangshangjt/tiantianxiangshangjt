- 👋 Hi, I’m @tiantianxiangshangjt
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
tiantianxiangshangjt/tiantianxiangshangjt is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Testkey的程序包括
  ChannelMap声明:layout_connect--pad_numbers--探针卡--测试板卡（一一对应）
  Signal声明：signal style:
                In/Out/InOut/Supply(DPS)
  Main program: 函数声明和调用（C++ & AItest API）
    Programing API
      theHW.PPMU() #<=6.5 V 设置电压
      thHW.DPS() #-10 to 10 V 设置电压
      theHW.DCL() # SetVIHH: 0-13 V 设置电压
      theHW.SignalMap.SetGroupName() #添加Signal group
      theHW.SignalMap.GetMember() #获取Signal group
      theMgr.SetCurTestName() #输出的字符串
      theMgr.SetCurTestNumber() #输出的数字
