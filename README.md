# Trojan-GFW Script
## This script will help you set up a trojan-gfw server in an extremely fast way.
### Read The Fucking Manual: https://www.johnrosen1.com/trojan/ 

#### via wget
```
sudo bash -c "$(wget -O- https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/trojan.sh)"
```
#### or via curl
```
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/trojan.sh)"
```

### 中文GUI版本
```
apt-get update && apt-get install sudo whiptail curl -y | yum install sudo newt curl -y
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/trojangui.sh)"
```
### Shadowsocks Version (ws+tls+V2ray-plugin)
```
apt-get update && apt-get install sudo whiptail curl -y | yum install sudo newt curl -y
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/trojan-ss.sh)"
```
### Qbittorrent Version (No Centos8 Support)
```
apt-get update && apt-get install sudo whiptail curl -y | yum install sudo newt curl -y
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/trojangui-qbt.sh)"
```
#### Bash Features:

1. Auto install and config Trojan-GFW NGINX Dnsmasq V2ray Shadowsocks and Qbittorrent
3. Auto issue renew let's encrypt certificate and **auto reload Trojan-GFW after renewal**
4. Auto OS Detect **Support Centos Debian Ubuntu** (Centos not recommended)
5. Auto domain resolve verification
6. Auto iptables(includes ipv6) firewall config and iptables-persistent
7. Auto generate client config (includes both Trojan-GFW and V2ray )
8. Auto random vmess uuid generate
9. Auto TCP Turbo enable ( **TCP-BBR** included)
10. Auto Nginx Performance Optimization
11. Auto Trojan-GFW ***trojan://*** share link and QR code generate
12. Auto V2ray ***vmess://*** share link generate
13. Auto https 301 redirect without affecting certificate renew
14. Auto enable HSTS header
15. Auto enable ***TLS1.3 ONLY***
16. Auto ***Random Html Template Choose***
17. Auto enable ***Full IPv6 Support***
18. Auto enable ***time sync***
19. Auto enable ***Fail Restart*** 
19. Support auto ***vmess or ss + tls + websocket + nginx*** config
20. Support custom websocket path and alterid
21. Support manually check for update include both Trojan-gfw and v2ray
22. Support manually force renew certificate
23. Support Full Uninstall

#### Friendly Reminder:
1. Please Purchase a domain and finish a dns resolve before running this bash script!
2. Please manually change system dns to frequently updated dns like 1.1.1.1 instead of those who update slowly like aliyun lan dns !
```
echo "nameserver 1.1.1.1" > '/etc/resolv.conf'
```
3. Please ***choose option2 if you want to use v2ray or shadowsocks !***
5. Please do not use enter / in websocket option ,enter someting else like /secret !
6. For security reasons, system upgrade is not forced ,press [ENTER] to skip or manually enter y to upgrade system.
7. Trojan-GFW QR code generate will be skipped on os who do not support python3-qrcode!
8. Due to personal demands , Dnsmasq installation is not forced ,press [ENTER] to skip or manually enter y to install dnsmasq.
9. If "sudo command not found" , please manually install sudo from the command above !

#### Telegram Channel And Group

### https://t.me/johnrosen1

### https://t.me/trojanscript

Attachment: Trojan-GFW one-click script's function is basically complete. Stop Function-based updating from now on. **If you need more functions, please open a Github issue.**

## If you found it useful , please give a star ,thanks!

### Debug Guide

```
sudo systemctl status trojan
sudo systemctl status trojan6
sudo systemctl status nginx
sudo systemctl status v2ray
sudo systemctl status dnsmasq
sudo systemctl status qbittorrent
journalctl -e -u trojan.service
cat /var/log/v2ray/error.log
crontab -l
sudo ~/.acme.sh/acme.sh --cron
timedatectl
```
### Result Example
```
trojan://trojanscript@www.johnrosen.top:443
```
![Trojan-GFW QR code](https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/trojanscript.png)



