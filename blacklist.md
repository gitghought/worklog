#blacklist相关

##去掉媒体中心和文件管理
- 修改黑名单文件  
- 更新launcher  
	- 将/data/data/com.cantv.launcher删除，再重启  
	- 使用的launcher是单独拉出的分支，给朗国和海勤  
		- http://172.16.11.9:8009/dailybuild/launcher5.2_haiqin_5.2.6/2017-01-18_15-56-28/  
		
# 20170220
## 不能将黑名单文件放到data下，否则在回复出厂设置后黑名单功能会因为data下的内容被清除而失效