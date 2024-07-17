# 作用

内网穿透,实现多个设备在同一个局域网

# 安装

## 方法一

``` bash
sudo apt install zerotier-one
```

## 方法二

``` bash
curl -s https://install.zerotier.com | sudo bash
```

# 开机启动

``` bash
sudo systemctl start zerotier-one
```

# 连接网络

``` bash
sudo zerotier-cli join NETWORK_ID
```

# 开启共享屏幕

先安装vino用于设置共享桌面

```bash
sudo apt-get install vino
```

使用命令查看ubuntu IPv4地址

```bash
sudo zerotier-cli listnetworks
```

windows remote desktop中输入此ip地址
