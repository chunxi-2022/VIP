# 📌 [News](./Log/News.md#news)


# 由 烟雨阁 和 Faker 联合维护的 一键系列
## 目前一键系列

### 全新 一键Dokcer
1：安装必要的系统工具。
2：安装GPG证书。
3：写入软件源信息。
4：更新并安装Docker-CE
5：下面是直接安装最新版本，查看一下Docker-CE的版本。
6：后查看Docker的状态，服务是启动状态，并且service是enabled开机自启的状态。到这Docker安装完成。
```
sudo apt-get update
sudo apt-get -y install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://mirrors.aliyun.com/docker-ce/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://mirrors.aliyun.com/docker-ce/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get -y update
sudo apt-get -y install docker-ce
apt-cache madison docker-ce
sudo systemctl status docker
```
### 一键青龙2.11.3版本青龙，注意只可以选择2.11.3版本

7.将当前用户账户添加到docker组并更新用户组
```
sudo usermod -aG docker $USER
newgrp docker
```
8.测试docker命令是否可以使用sudo正常使用
```
docker images
```

9.设置安装位置授权文件夹并安装qinglong
```
cd /usr/share
sudo chmod -R 777 /usr/share
wget -q https://mirror.ghproxy.com/https://raw.githubusercontent.com/chunxi-2022/VIP/main/Scripts/sh/ql.sh -O ql.sh && bash ql.sh
```

10. 如果无法进入qinglong界面或者其他安装（如网络原因无法安装 Ninga等等）错误，都请执行以下命令重新安装容器，不限制次数,直到成功（已安装成功请忽略）
```
wget -q https://mirror.ghproxy.com/https://raw.githubusercontent.com/chunxi-2022/VIP/main/Scripts/sh/ql.sh -O ql.sh && bash ql.sh
```

### 一键青龙2.12版本青龙
```
# wget -q https://git.metauniverse-cn.com/https://raw.githubusercontent.com/yanyuwangluo/VIP/main/Scripts/sh/ql12.sh -O ql12.sh && bash ql12.sh
```
### 已安装青龙2.11+的用户，一键拉库 没反应就是网络问题
```
docker exec -it qinglong bash -c "$(curl -fsSL https://git.metauniverse-cn.com/https://github.com/yanyuwangluo/VIP/blob/main/Scripts/sh/1customCDN.sh)"
```
