### This is a guide to install vim-plugins(Ycm) for coder in Mac-OS

beside I offer a way to config terminal to use vpn

* install
brew install privoxy

* config
vim /usr/local/etc/privoxy/config

listen-address 0.0.0.0:8118
forward-socks5 / localhost:1080 .

u should config your vpn's socks port for forward-socks5, don't forget the litte point at the end

* launch
sudo /usr/local/sbin/privoxy /usr/local/etc/privoxy/config

* verify
netstat -na | grep 8118

* redirect your terminal's traffic to 8118

vim ~/.bash_profile
-----------------------------------------------------
export http_proxy='http://localhost:8118'
export https_proxy='http://localhost:8118'
----------------------------------------------------

source ~/.bash_profile

* check

curl ip.gs

* enjoy it by yourself
