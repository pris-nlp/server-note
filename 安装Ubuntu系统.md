1. 从[Ubuntu官网](https://cn.ubuntu.com/download)下载镜像（建议下载服务器版）。
2. 下载UltraISO，制作U盘安装盘。
3. 插入U盘，启动服务器，进入BIOS，选择U盘启动。
4. 进入安装界面安装即可，其中安装语言建议选择English，磁盘分区需要设置：
    - `/`，主分区，ext4，固态剩余大小；
    - `/boot`，主分区，ext4，大小1024MB；
    - efi分区，逻辑分区，大小1024MB；
    - swap分区，逻辑分区，具体大小依内存而定。对于64G内存，可设置为8G；
    - `/home`，主分区，设置在机械硬盘上，用来存放各个用户的文件。
   参考：
    - [安装Ubuntu Linux系统时硬盘分区最合理的方法](https://blog.csdn.net/u012052268/article/details/77145427)
    - [ubuntu1804安装的自定义分区](https://blog.csdn.net/kan2016/article/details/102832169) 
