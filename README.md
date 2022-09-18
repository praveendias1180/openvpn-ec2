# OpenVPN Access Server

https://openvpn.net/

![](web-openvpn.png)

![](openvpn.png)

# Setup Access Server

![](access-server.png)

![](setup-complete.png)

# OpenVPN Status

![](status.png)

# Connect to the OpenVPN Server

https://openvpn.net/vpn-server-resources/connecting/

```
apt install apt-transport-https
sudo wget https://swupdate.openvpn.net/repos/openvpn-repo-pkg-key.pub
sudo apt-key add openvpn-repo-pkg-key.pub
sudo wget -O /etc/apt/sources.list.d/openvpn3.list https://swupdate.openvpn.net/community/openvpn3/repos/openvpn3-jammy.list
sudo apt update
sudo apt install openvpn3
```
![](client.png)

```
openvpn3 config-import --config client.ovpn
openvpn3 session-start --config client.ovpn
openvpn3 sessions-list
```

![](connected.png)
