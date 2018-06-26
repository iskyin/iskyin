# CentOS环境配置
```
> rpm/yum 适用于Redhat、CentOS、Suse等平台
> apt-get/dpkg 适用于Debian、Ubuntu等平台
> zypper 适合于Suse平台

$ ssh -p 22 root@ip地址

$ sudo yum install git vim openssl wget
   说明：
   	openssl  实现加解密和证书 开源的 专业系统
   	wget 下载文件的工具

> nvm 在同一台机器上安装和切换不同版本node
$ wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
或
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash

> 重启服务器
$ shutdown -r now

> nvm node 安装制定版本
$ nvm install 版本号

> 设置 node 当前版本
$ nvm use 需要使用的版本号

> 设置 node 默认版本
$ nvm alias default 版本号

```
