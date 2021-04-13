1.	win10开始上右键搜索Hyper-V 管理器
2.	右侧操作下点击虚拟交换机管理器，新建虚拟交换机，选择内部网络
3.	 
4.	右侧操作下点击新建-虚拟机，配置网络选择新建的hadoop虚拟机网络
5.	 
6.	控制面板\网络和 Internet\网络连接下找到新建的hadoop网络，因为使用定ip，需要设置固定ip地址
7.	 
8.	安装完linux以后，配置固定ip，修改/etc/sysconfig/network-scripts/ifcfg-eth0，注意需要配置BROADCAST而不需要配置GATEWAY,没有配置BROADCAST无法ping通内网其他机器ip，配置了GATEWAY以后无法ping外网
9.	 
10.	此时可以连接内网192.168.80.*ip，无法连接外网，在虚拟机下点击设置-添加硬件-旧版网络适配器-选择默认的Default Swiftch，此处选择网络适配器无法连接外网，具体原因未知，重启机器即可，如果不能编辑需要先停止虚拟机
11.	 
