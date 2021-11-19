# nvjdc


## 提示

由于我自己的环境是centos x86，arm不支持

这是打包过的 不要fork

不是热更新 每次修改配置需要重启容器


## 安装教程

如果你是装过NVjdc 先看看后面1.2以前如何更新之1.2升级说明

1拉源码
国内
```
git clone https://ghproxy.com/https://github.com/NolanHzy/nvjdcdocker.git /root/nolanjdc
```
国外
```
git clone https://github.com/NolanHzy/nvjdcdocker.git /root/nolanjdc
```


2 拉取基础镜像以后不需要拉取镜像了 如果需要拉取我会通知
```
sudo docker pull nolanhzy/nvjdc:latest
```

3 执行命令

```
yum install wget unzip -y
```

4创建一个目录放配置

```
 cd /root/nolanjdc
```
```
mkdir -p  Config && cd Config
```

5下载config.json 配置文件 并且修改自己的配置 不能缺少


```
wget -O Config.json  https://raw.githubusercontent.com/NolanHzy/nvjdc/main/Config.json
```
国内请使用
 ```
wget -O Config.json   https://ghproxy.com/https://raw.githubusercontent.com/NolanHzy/nvjdc/main/Config.json
```

6 回到nolanjdc目录创建chromium文件夹并进入

```
cd /root/nolanjdc && mkdir -p  .local-chromium/Linux-884014 && cd .local-chromium/Linux-884014
```

7下载 chromium 

```
wget https://mirrors.huaweicloud.com/chromium-browser-snapshots/Linux_x64/884
