## 一、申请微信企业公众号的团体号

参考链接：

http://blog.51cto.com/itnihao/1733245

## 二、配置微信告警
```
1、下载微信告警脚本

cd /tmp

git clone https://github.com/Lancger/Wechat-Alert-for-Zabbix.git

cp /tmp/Wechat-Alert-for-Zabbix/wechat_alert.py /usr/lib/zabbix/alertscripts

chown zabbix.zabbix /usr/lib/zabbix/alertscripts/wechat_alert.py

chmod +x /usr/lib/zabbix/alertscripts/wechat_alert.py

pip install requests

2、测试脚本是否能正常发送消息

python /usr/lib/zabbix/alertscripts/wechat_alert.py 2 test_message

k0YpqvW1EiJwK2N4znNpU3XFKNKDoUrvaeJQJE8oP1xf-tlof4aC9l0tBzN1_n0K__fKtqO3E6UsdrglmcCGP_iHOc4bfnWZ92XeEV6PVtcEfTs3-b8GJuo9qycBySuXl7DSzGyy9O-yrEzCw7QeVV2xv0ai4zHdbI2v1J8oRJ4LcC_shNEnqAgcrunHm731lD2J0RnQETTEB7JoyYkaeg

{"errcode":0,"errmsg":"ok","invaliduser":""}    ----这表示成功发送了消息

```

## 三、配置触发器告警


## 四、模拟告警
```
1、允许ping

echo 0 >/proc/sys/net/ipv4/icmp_echo_ignore_all

2、禁止ping

echo 1 >/proc/sys/net/ipv4/icmp_echo_ignore_all

```