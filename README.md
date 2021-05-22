# SSHPLUS

sudo apt-get update -y; apt-get upgrade -y; wget https://raw.githubusercontent.com/starrising321/SSHPLUS/master/Plus; chmod 777 Plus; ./Plus

===============
# TROUBLESHOOT

if badvpn or limitor and proxy socks not working use this cocmand:

sudo apt install screen

and than all DONE

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

===============

COMPLETAMENTE FREE! 

===============

By ☆ https://t.me/star_Jani ☆ https://t.me/StarZany
