# 安卓安


## 升级固件
- 方法1：
 压缩包解压后得到Ada338Upgrade.bin文件，将其拷贝至U盘根目录下，插到主板上USB座上，拔掉电源再插上电源线，系统会自动升级。

- 方法2：
 压缩包解压后得到Ada338Upgrade.bin文件，将其拷贝至U盘根目录下，插到主板上USB座上，按遥控器上信号源键+数字键“3699”进入工厂菜单，选择系统升级选项升级

## 使用的电源为12V 4A
**********
## 待***测试***问题
- 给出最新的Launcher
	- 解决背景图片的问题
	- [x] 状态

- 开机动画
	- [x] 状态
	
- 系统属性->内部型号
	- [x] 状态
**********

## 20170214

### 上传开机视频 
- 链接：http://pan.baidu.com/s/1pKBvoUZ 密码：gq5n


##20170217
### 升级最新固件
### 测试
- 获取系统属性
	- adb shell getprop | grep {属性名}
- 测试开机动画
	- adb shell setprop persist.sys.log.debug true
	- 重启
	- ps | grep pm
	- logcat -s pm

