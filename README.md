# MT7603U_LinuxSTA
Mediatek MT7603U LinuxSTA vendor driver 3.0.0.5_20140922

关于MT7603U驱动编译问题  
1. AP的驱动可以在Linux2.6和Linux3.2的内核上编译  
2. STA的驱动可以在Linux3.2的内核上编译，  
    但是在Linux2.6的内核上直接编译会出现错误，  
    需要将DPA/os/linux/目录下的config.mk文件中，  
    HAS_CFG80211_SUPPORT=y  
    修改为HAS_CFG80211_SUPPORT=n  
这样就可以在Linux2.6内核上编译
