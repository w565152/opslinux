# 一、查看当前防火墙状态
```
查看当前防火墙状态
sudo ufw status

inactive状态是防火墙关闭状态 
active是开启状态。
```

# 二、开启防火墙
```
开启防火墙 
sudo ufw enable

查看开启防火墙后的状态
sudo ufw status

active 说明防火墙开启成功。
```

# 三、关闭防火墙
```
sudo ufw disable

sudo ufw status
如果是inactive 说明我们的防火墙已经关闭掉
```

# 四、常用指令
```
UFW 使用范例：

允许 53 端口

$ sudo ufw allow 53

禁用 53 端口

$ sudo ufw delete allow 53

允许 80 端口

$ sudo ufw allow 80/tcp

禁用 80 端口

$ sudo ufw delete allow 80/tcp

允许 smtp 端口

$ sudo ufw allow smtp

删除 smtp 端口的许可

$ sudo ufw delete allow smtp

允许某特定 IP

$ sudo ufw allow from 192.168.254.254

删除上面的规则

$ sudo ufw delete allow from 192.168.254.254

```
