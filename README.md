# DockerInstall
Linux Docker install and android install scripts


Android 
1. need root magisk
download zip from coolapk@望月古川 or this https://www.123pan.com/s/6VlDVv-vGd7d提取码:ZgCV
面板访问：127.0.0.1:5700
ssh连接：
ip:127.0.0.1
用户:root
密码:123456

常用依赖
Nodejs：
ping3
canvas
requests
jieba
PyExecJS
httpxts-md5
@types/node
prettytable
node-telegram-bot-api
tslib
ql
common
fs
typescript
axios
png-js
axios
ws@7.4.3
crypto-js
jieba
global-agent
jsdom -g
moment
form-data
date-fns
node-jsencrypt
require
js-base64
tough-cookie
json5
jsdom
dotenv
qs

python3：
ping3
canvas
requests
jieba
PyExecJS
httpx

常用库：
FAKER3
ql repo https://git.metauniverse-cn.com/https://github.com/shufflewzc/faker3.git "jd_|jx_|gua_|jddj_|jdCookie" "activity|backUp" "^jd[^_]|USER|function|utils|sendNotify|ZooFaker_Necklace.js|JDJRValidator_|sign_graphics_validate|ql|JDSignValidator|magic|depend|h5sts" "main"
KR库：
ql repo https://github.com/KingRan/KR.git "jd_|jx_|jdCookie" "activity|backUp" "^jd[^_]|USER|utils|function|sign|sendNotify|ql|magic|JDJR"
my：
ql repo https://github.com/peaky2222/AutoTaskList.git





Linux
1. install docker centos8
#更新yum 安装依赖
yum install -y yum-utils device-mapper-persistent-data lvm2

#添加yum源
yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

#安装
yum install docker-ce

#启动并设置开机自启动
# 添加docker用户组，一般已存在，不需要执行
sudo groupadd docker     
# 将登陆用户加入到docker用户组中
sudo gpasswd -a $USER docker
# 更新用户组
newgrp docker   
# 测试docker命令是否可以使用sudo正常使用
docker version  



systemctl start docker
systemctl enable docker

#验证
docker version
2. install qinglong
docker run -dit --name ql --hostname ql --restart always -p 5700:5700 -v $PWD/ql/config:/ql/config -v $PWD/ql/log:/ql/log -v $PWD/ql/db:/ql/db -v $PWD/ql/scripts:/ql/scripts -v $PWD/ql/jbot:/ql/jbot whyour/qinglong:latest 
