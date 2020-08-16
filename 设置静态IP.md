1. 通过`ifconfig -a`命令查看设备情况，记录对应的网卡设备名（以eno1为例）。如果不存在对应的网卡设备（只有lo回环时），可能是Linux版本不足导致对应的网卡驱动不可用，则需要手动下载网卡驱动更新或安装更高版本的Linux。
2. 通过`sudo vim /etc/network/interfaces`更改网络配置，添加如下字段，保存退出：
    ```
    auto eno1
    iface eno1 inet static
    address 10.112.156.50
    gateway 10.112.0.1
    netmask 255.255.0.0
    nameserver 10.3.9.4
    ```
3. 通过`sudo vim /etc/resolv.conf`更改nameserver，写入以下两行，保存退出：
    ```
    nameserver 10.3.9.4
    nameserver 10.3.9.5
    ```
4. 通过命令`sudo /etc/init.d/network-manager restart`重启网络服务。如果报错，可以尝试其他命令如：`sudo /etc/init.d/networking restart`，或`sudo service network restart`等。
