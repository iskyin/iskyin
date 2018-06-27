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

> (yarnpkg.com)
$ brew install yarn

$ npm install vue-cli pm2 -g


$ pm2 start server   .js

node 8.1.2
npm 5.0.3
pm2 2.5.0
yarn 0.24.6
vue 2.8.2
brew 1.2.2

```

# nginx 配置
```
删除Apache
  sudo service apache2 stop 停掉Apache
  update-rc.d -f apache2 remove 删除
  sudo apt-get remove apache2 彻底删除

  sudo apt-get update 更新包列表

安装nginx
  sudo apt-get install nginx
  nginx -v  
    1.4.6
  cd /etc/nginx/conf.d

   添加配置文件：
    sudo vim iskyin-h5-9000.conf

      # 负载均衡
      upstream iskyin {
        # ip_hash;
        # server xxx.xxx.xxx:xxx;
        server 127.0.0.1:9000;
      }
      #
      server{
        listen:80;
        server_name iskyin.com;
        ....

    重启nginx
      sudo service nginx restart


```
