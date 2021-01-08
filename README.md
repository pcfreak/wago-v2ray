## V2Ray is based on Nginx's vmess+ws+tls one-click installation script

> Thanks to JetBrains for providing non-commercial open source software development authorization

> Thanks for non-commercial open source development authorization by JetBrains
### Telegram group
* telegram exchange group: https://t.me/wulabing_v2ray
* Telegram update announcement channel: https://t.me/wulabing_channel

### Ready to work
* Prepare a domain name and add the A record。
* V2ray official instructions , understand TLS WebSocket and V2ray related information
* Install wget

### Installation/update method (h2 and ws versions have been merged）
Vmess+websocket+TLS+Nginx+Website
```
wget -N --no-check-certificate -q -O install.sh "https://raw.githubusercontent.com/pcfreak/wago-v2ray/master/install.sh" && chmod +x install.sh && bash install.sh
```

### Precautions
* If you do not understand the specific meaning of each setting in the script, except for the domain name, please use the default values ​​provided by the scrip
* To use this script, you need to have Linux basics and experience, understand some knowledge of computer networks, and basic computer operations
* Currently Debian 9+ / Ubuntu 18.04+ / Centos7+ are supported. Some Centos templates may have difficult to handle compilation problems. It is recommended that when you encounter compilation problems, please change to other system templates
* The group owner only provides extremely limited support, if you have any questions, you can ask the group friends
* Every Sunday at 3 o'clock in the morning, Nginx will automatically restart to cooperate with the issuance of the certificate. During this period, the node cannot be connected normally, and the expected duration is several seconds to two minutes.

### Update log
> Please check CHANGELOG.md for updates

### Thanks
* Another branch version of this script (Use Host) address: https://github.com/dylanbai8/V2Ray_ws-tls_Website_onekey Please choose according to your needs The author may have stopped maintenance
* The MTProxy-go TLS version project in this script refers to https://github.com/whunt1/onekeymakemtg, thank you whot1
* In this script, the original project of Rui Speed ​​4 in 1 script is quoted https://www.94ish.me/1635.html Thanks here
* In this script, the Ruispeed 4-in-1 script modified version project is quoted https://github.com/ylx2016/Linux-NetSpeed, thank you ylx2016

### certificate
> If you already have the certificate file of the domain name you are using, you can name the crt and key files as v2ray.crt v2ray.key and place them in the /data directory (if the directory does not exist, please create the directory first). Please pay attention to the certificate file permissions and Validity period of the certificate, please renew after the validity period of the custom certificate expires

The script supports the automatic generation of let's encrypted certificate with a validity period of 3 months. In theory, the automatically generated certificate supports automatic renewal

### View client configuration
`cat ~/v2ray_info.txt`

### Introduction to V2ray

* V2Ray is an excellent open source network proxy tool that can help you experience the Internet smoothly. Currently, all platforms support the use of Windows, Mac, Android, IOS, Linux and other operating systems。
* This script is a one-key complete configuration script. After all the processes are running normally, you can directly set the client according to the output results to use
* Please note: We still strongly recommend that you have a full understanding of the workflow and principles of the entire program

### It is recommended that a single server only build a single agent
* This script installs the latest version of V2ray core by default
* The latest version of V2ray core is 4.22.1 (At the same time, please pay attention to the synchronization update of the client core, you need to ensure that the client kernel version>= server kernel version)
* It is recommended to use the default port 443 as the connection port
* The disguised content can be replaced by itself。

### Precautions
* It is recommended to use this script in a pure environment. If you are a novice, please do not use the Centos system。
* Please do not apply this program in a production environment until this script is actually available。
* have installed Nginx should pay special attention. Using this script may cause unpredictable errors (untested, if it exists, subsequent versions may deal with this problem) 。
* Some functions of V2Ray depend on the system time. Please ensure that the system UTC time error of the V2RAY program is within three minutes, regardless of the time zone。
* This bash relies on the official V2ray installation script and acme.sh to work。
* Centos For Centos system users, please allow the relevant ports of the program in the firewall in advance (default: 80, 443）


### Start method

Start V2ray：`systemctl start v2ray`

Stop V2ray：`systemctl stop v2ray`

Start Nginx：`systemctl start nginx`

Stop Nginx：`systemctl stop nginx`

### Related catalog

Web directory：`/home/wwwroot/3DCEList`

V2ray server configuration：`/etc/v2ray/config.json`

V2ray client configuration: `~/v2ray_info.inf`

Nginx directory： `/etc/nginx`

Certificate file: `/data/v2ray.key 和 /data/v2ray.crt` 请注意证书权限设置

### Donate

Currently supports accepting virtual currency donations through MugglePay

𝒘𝒖𝒍𝒂𝒃𝒊𝒏𝒈 invites you to use Muggle Treasure, a Telegram-based e-wallet, anonymous payment of 0 handling fee to the account in seconds. https://telegram.me/MugglePayBot?start=T3Y78AZ3

You can donate to me anonymously via Telegram: send /pay @wulabing xxx to @MugglePayBot and the default currency is USDT 

If you need to donate via Alipay/WeChat, please Telegram private chat @wulabing Thank you for your support


