__关于matlab安装__
	__条件：__ xftp,xshell,镜像,在root权限下
	远程服务器环境下：

	• 挂载镜像 
	sudo mount -o loop R2018a_glnxa64_DVD1.iso /home/cese/cdrom

    • 创建matlab2018a,mat_2018,crack三个文件夹，分别用于安装，存放安装引导，存放破解文件
	
	• 将挂载后的镜像上installer_input.txt、activate.ini复制到本地，并做如下更改
	
	编辑installer_input.txt
	destinationFolder= /home/cese/matlab2018a #安装目录
	fileInstallationKey= 38699-60149-36808-21840-05491 #你的序列号
	agreeToLicense=yes #同意协议
	outputFile=/home/cese/mathwork_install.log #安装日志 （Optional）
	mode=silent #开启无人值守安装
	activationPropertiesFile=/home/cese/mat_2018/activate.ini #激活文件
	
	
	编辑activate文件
	isSilent=true #开启silent模式
	activateCommand=activateOffline #设置激活方式, 离线激活 无需联网
	licenseFile=/home/crack/lic_standalone.lic #license文件位置
	
	• 使用如下命令安装
	sudo /home/b304/matlab1/install  -inputFile /home/b304/crack/installer_input.txt
	安装过程中提示挂载第二个dvd时使用如下命令：
	sudo mount -o loop R2018a_glnxa64_DVD2.iso /home/cese/cdrom
	
	安装完成使用复制文件破解，将破解文件复制到指定目录
	
	• 解除挂载
	umount /home/cese/cdrom
	
	• 更改变量环境
	• 这里的早Ubuntu上后面的备注需要清除，影响读入命令
