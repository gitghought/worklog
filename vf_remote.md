# 遥控器

## 修改kl文件 
> 此步骤用于创建一个全新的遥控器键值码的情况

- 文件绝对路径：[绝对路径](#kl_abs_path "good")   
	- customer_ir_{}.kl
- 将修改后的kl文件复制到“device/softwinner/dolphin-cantv-h2/configs/”下  
	- /home/gaihao/b_h2_allwinner/Allwinner-h2/device/softwinner/dolphin-cantv-h2/configs/
- 修改“/home/gaihao/b_h2_allwinner/Allwinner-h2/device/softwinner/dolphin-cantv-h2/dolphin_cantv_h2.mk”
	- 修改：PRODUCT_COPY_FILES，在后面添加源文件位置和目标文件位置
	
## 修改kl文件 

- 文件绝对路径：[绝对路径](#klAbaPath "good")   
	- customer_ir_{}.kl


## 修改fex文件

### 刷机&清除

- /home/gaihao/b_h2_allwinner/lichee/tools/pack/chips/sun8iw7p1/configs/dolphin-p2
	- sys_config.fex 
		- ir_recovery_key_code1       = 0x03 ** dpad_up **  
		- ir_addr_code1               = 0xff00 ** key code **
		- ir_wipe_key_code1           = 0x02 ** dpad_down **  


### 电源键唤醒
- /home/gaihao/b_h2_allwinner/lichee/tools/pack/chips/sun8iw7p1/configs/dolphin-p2
	- sys_config.fex 
			- ir_power_key_code9  = 0x14 ** POWER **
			- ir_addr_code9       = 0xff00 ** key code ** 


## 测试遥控器键值
### 测试直播和点播
> 在没有遥控器的情况下，使用其它遥控器
> 将当前遥控器对应的键值添加到kl文件中
- 手动修改/system/usr/keylayout下的kl文件
	- 将kl文件pull出来修改
	- 将修改后的kl文件push进去
- 重启设备

*****  

## kl_abs_path
/home/gaihao/b_h2_allwinner/Allwinner-h2/device/softwinner/common/configs/keylayout
