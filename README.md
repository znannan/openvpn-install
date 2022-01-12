**New: [wireguard-install](https://github.com/Nyr/wireguard-install) is also available.**

## openvpn-install
OpenVPN [road warrior](http://en.wikipedia.org/wiki/Road_warrior_%28computing%29) installer for Ubuntu, Debian, AlmaLinux, Rocky Linux, CentOS and Fedora.

This script will let you set up your own VPN server in no more than a minute, even if you haven't used OpenVPN before. It has been designed to be as unobtrusive and universal as possible.

### Installation
Run the script and follow the assistant:

`wget https://raw.githubusercontent.com/znannan/openvpn-install/master/openvpn-install.sh -O openvpn-install.sh && sudo chmod +x openvpn-install.sh && sudo bash openvpn-install.sh`

Once it ends, you can run it again to add more users, remove some of them or even completely uninstall OpenVPN.

### view your ubuntu Firewall Rules (don't edit)
`sudo systemctl cat openvpn-iptables.service`

### view your openvpn server configration ( don't edit )
`sudo more /etc/openvpn/server/server.conf`

### stop the OpenVPN service
`sudo systemctl stop openvpn-server@server.service`

### start the OpenVPN service
`sudo systemctl start openvpn-server@server.service`

### restart the OpenVPN service
`sudo systemctl restart openvpn-server@server.service`

### View status of your OpenVPN systemd based service
`sudo systemctl status openvpn-server@server.service`

### I want to run my own VPN but don't have a server for that
You can get a VPS from just $1/month at [VirMach](https://billing.virmach.com/aff.php?aff=4109&url=billing.virmach.com/cart.php?gid=18).

### Client-end configuration
 - `sudo find / -type f -name "*.ovpn`
 - `scp [yourUser]@[yourServerIP]:~/[your openVpn client user name].ovpn .`
 - for iOS: https://itunes.apple.com/us/app/openvpn-connect/id590379981?mt=8
 - for MacOS: https://tunnelblick.net/
 - for Android: https://play.google.com/store/apps/details?id=net.openvpn.openvpn&hl=en
 - for linux, Windows8/10: https://www.cyberciti.biz/faq/howto-setup-openvpn-server-on-ubuntu-linux-14-04-or-16-04-lts/

