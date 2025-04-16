# docker-dev-env
一个用于搭建本地docker开发环境的管理配置版本，达到到任何地方只要下载一个docker，就可以用docker-compose 立马启动本地开发环境

### 目录结构安排
`docker-compose-up` 服务构建配置目录：包含各种服务的 `docker-compose.yml` 文件
&nbsp;
`dockerfile`        镜像构建和镜像容器相关的配置目录：将镜像的构建和容器初始化的配置统一管理，包含dockerfile和conf以及ini之类配置
&nbsp;
`work`              工作目录：包含各种项目代码

### 更好的建议
1、可以在此基础上，重新更改配置，构建适合自己项目的新镜像以及配置文件
&nbsp;
2、构建完的镜像建议push到自己的docker镜像仓库，避免更换服务器环境或者本地开发电脑时，需要重新构建的问题，主要是耗时很长，甚至可能因为网络环境构建失败
