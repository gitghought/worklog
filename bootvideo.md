#开机视频

##查看日志   
- 能够抓取的log  
	- setprop persist.sys.log.debug true  
	- getprop | grep "persist.sys.log.debug"  
	- adb shell reboot //重启设备  
	- logcat -s otaservice  

##查看进程  
- 手动启动进程  
	- adb shell am startservice -n com.cantv.pm/.ConfigService   
	- ps | grep "cantv"  
		- 能够看到pm开头的进程  