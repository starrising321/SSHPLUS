# SSHPLUS

sudo apt-get update -y; apt-get upgrade -y; wget https://raw.githubusercontent.com/starrising321/SSHPLUS/master/Plus; chmod 777 Plus; ./Plus


# SSHPLUS NEW COMMAND

apt-get update -y; apt-get upgrade -y; apt-get install curl -y; apt-get install sudo -y; wget https://raw.githubusercontent.com/starrising321/SSHPLUS/master/Plus; chmod 777 Plus; ./Plus

===============
# TROUBLESHOOT

============================================================

if badvpn or limitor and proxy socks not working use this cocmand:

sudo apt install screen

============================================================

OPENVPN FIXED FOR DEBIAN 9

sed -i 's|LimitNPROC|#LimitNPROC|' "/lib/systemd/system/openvpn@.service"

sed -i 's|/etc/openvpn/server|/etc/openvpn|' "/lib/systemd/system/openvpn@.service"

sed -i 's|%i.conf|server.conf|' "/lib/systemd/system/openvpn@.service"

systemctl daemon-reload

systemctl restart openvpn@openvpn.service

systemctl enable openvpn@openvpn.service

============================================================

DROPBEAR FIXED COMMAND

apt-get install dropbear -y

and than all DONE

============================================================

# SLOWDNS AFTER INSTALL COMMAND MANUAL

cd /usr/local

wget https://golang.org/dl/go1.16.2.linux-amd64.tar.gz

tar xvf go1.16.2.linux-amd64.tar.gz

export GOROOT=/usr/local/go 

export PATH=$GOPATH/bin:$GOROOT/bin:$PATH



nano /etc/ssh/sshd_config 

edit this

AllowTcpForwarding yes     find this and remove # from the file

iptables -I INPUT -p udp --dport 5300 -j ACCEPT

iptables -t nat -I PREROUTING -p udp --dport 53 -j REDIRECT --to-ports 5300

lsof -i :5300

# PORTS

SERVICE: OPENSSH PORT: 22

SERVICE: OPENVPN: PORT: 1194

SERVICE: PROXY SOCKS PORT: 8080

SERVICE: SSL TUNNEL PORT: 443

SERVICE: DROPBEAR PORT: 442 (111 is default automaticly..)

SERVICE: SQUID PORT: 5556 8799

SERVICE: SLOWDNS PORT: 5300

===============

COMPLETAMENTE FREE! 

===============

By ☆ https://t.me/star_Jani ☆ https://t.me/StarZany
