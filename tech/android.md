## ADB CMD
 * adb reboot bootloader 
 
## fastboot CMD
  * fastboot flashing unlock    #6.0以上设备 设备必须解锁，开始刷机（这个不同的手机厂商不同）
  * fastboot erase {partition}  # 擦除分区
  * fastboot  erase  frp    # 擦除 frp 分区，frp 即 Factory Reset Protection，用于防止用户信息在手机丢失后外泄
  * fastboot  flash  boot  boot.img    # 刷入 boot 分区
  * fastboot  flash  system  system.img    # 刷入 system 分区
  * fastboot  flash  recovery  recovery.img    # 刷入 recovery 分区
  * fastboot flashall    #烧写所有分区，注意：此命令会在当前目录中查找所有img文件，将这些img文件烧写到所有对应的分区中，并重新启动手机。
  * fastboot  format  data    # 格式化 data 分区
  * fastboot  flashing lock    # 设备上锁，刷机完毕
  * fastboot  continue    # 自动重启设备
  * fastboot reboot# 重启手机
  * fastboot reboot-bootloader# 重启到bootloader 刷机用
  * fastboot devices  ## 发现手机，显示当前哪些手机通过fastboot连接了
  
  * 创建包含boot.img，system.img，recovery.img文件的zip包。
  * 执行：fastboot update {*.zip}
  
  * 华为手机解锁命令: fastboot oem unlock 解锁码
  
  * fastboot flash recovery recovery.img
  
  ##
	* https://dl.google.com/android/repository/platform-tools-latest-darwin.zip
	* https://dl.google.com/android/repository/platform-tools-latest-linux.zip
	* https://dl.google.com/android/repository/platform-tools-latest-windows.zip