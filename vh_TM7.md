# 天敏 *TM7*

# 重新拉分支
- 从TM6拉出新的分支 
- [步骤](#newbranch)
	- 父分支名：TM6_20161110
- 出全量包
- 出差分升级包
- 测试升级
- 测试黑屏补丁

# 测试
- 升级固件
- 升级mac
- 测试固件升级功能
	- adb disconnect
	- adb connect 192.168.1.113
	- adb shell setprop persist.sys.log.debug true
	- adb shell getprop | grep "persist.sys.log.debug"
	- adb shell reboot
	- adb shell logcat -s otaservice
		- 过滤信息：[BaseRequest.java:parseData+262]...parseData ：{"data": {}, "error": 7}
		- [查看错误码含义](#errorcode)
- 查看黑屏补丁
	- adb shell dmesg | grep "nand version"
- 提测
- [ ] 状态




## errorcode
- 0   没有错误
- 1   参数有错误
- 2   没有查询到结果
- 3   服务器忙
- 4   超过最大并发下载数量限制
- 5   已经是最新版本了
- 6   版本不存在
- 7   正在生成差分包,稍后再查询，重启
- 8   新版本升级数量限制
- 9 盒子没有在TMS 报备，TMS 返回错误。
- 10 平台不对。

## newbranch  
在本地代码仓库
repo forall -c "git命令" 对仓库下所有git仓库操作
1. 将分支全部切换到要拉出分支的分支上
远端分支切换并追踪： repo forall -c "git checkout --track 远端分支"
2. 确保分支为最新代码：repo sync 
3. 从当前分支拉出新分支：repo forall -c "git checkout -b 新分支"
4. 将新拉分支推到远端：repo forall -c "git push 仓库 新分支"
5. 修改repo 创建仓库分支
cd .repo/manifests
git checkout -b 新分支
修改.repo/manifests/default.xml
git commit 
git push 仓库 新分支