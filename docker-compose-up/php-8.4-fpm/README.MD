### 一、dockerfile 制作镜像
    #### 1、 ../php/dockerfile 中，以官方发行版镜像作为基础镜像【这里用php:{version}-fpm,先拉取到本地】，最好linux是非alpine版本，因为alpine版本的php扩展安装比较麻烦，需要编译安装，而且alpine版本的php扩展安装后，需要重新编译安装 php 才能生效，所以最好使用非alpine版本的php镜像。
    #### 2、安装环境需要的 php 扩展
    #### 3、执行  `docker build -t php-{version}-fpm . ` 命令，制作镜像

### 二、编排 docker-compose
    #### 1、设置好服务的端口映射，环境变量，数据卷等，主要将各个服务的配置文件，日志文件，数据文件等挂载到宿主机上。方便随时更改配置，查看日志，查看数据。
    #### 2、执行  `docker-compose up -d` 命令，启动服务

### 三、使用
    #### 1、访问服务，观测是否正常响应，如果正常，说明服务已经启动成功。如果不正常，说明服务启动失败，需要查看日志，排查问题。查看日志可以使用  `docker-compose logs -f` 命令，查看服务的日志。
    
### 四、重启服务
    #### 1、执行  `docker-compose restart` 命令，重启服务