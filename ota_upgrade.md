#OTA 升级

##测试ota升级
- 添加系统属性
	- setprop persist.sys.log.debug true
- 重启设备
	- reboot //需要进入adb shell
	- adb shell reboot
- 打印log
	- logcat -s otaservice
- 查看log //可以将log内容定向到一个文件
	- 0   没有错误
	- 1   参数有错误
	- 2   没有查询到结果
	- 3   服务器忙
	- 4   超过最大并发下载数量限制
	- 5   已经是最新版本了
	- 6   版本不存在
	- 7   正在生成差分包,稍后再查询
	- 8   新版本升级数量限制
	- 9   盒子没有在TMS 报备，TMS 返回错误。
	- 10  平台不对。