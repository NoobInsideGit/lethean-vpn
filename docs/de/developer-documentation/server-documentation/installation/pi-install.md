# install Proxy or VPN on PI3

Download Noobs Lite or Raspbian Lite

https://www.raspberrypi.org/downloads/

* Install on a SD Card
* Boot PI and setup all till getting to Linux Prompt

Login with default
```
user = pi
pass = raspberry
```
# (don’t forget to change default password )

Also enable ssh if using Noobs with:

`sudo raspi-config`

* Update Raspbian to lasted patch :

`sudo apt-get update && sudo apt-get upgrade`

* Update PI3 firmware:

`sudo rpi-update`


`sudo apt-get install python3 python3-pip haproxy`

`sudo apt install libboost-dev libboost-all-dev libminiupnpc-dev libunbound2`

`sudo user add vpnuser`
`sudo passwd vpnuser`
`sudo echo "vpnuser ALL=(ALL:ALL) NOPASSWD:ALL" >> /etc/sudoers`

Login with vpnuser

`wget https://gitlab.com/lethean.io/vpn/lethean-vpn/-/raw/master/server/easy-deploy-nodepi3.sh`

`chmod +x easy-deploy-nodepi3.sh`

`BRANCH=master ./easy-deploy-nodepi3.sh`


* Edit dispatcher.ini and sdp.json at /opt/lthn/etc


# Server instructions:

[Server instructions](/vpn/server-documentation)

Pay 10 LTHN and upload your sdp.json
 
`./lvmgmt --upload-sdp`

# Payment instructions:

# Node List:

https://nodes.lethean.io

https://lethean.zendesk.com/hc/en-us/articles/360013600571-Subscribing-to-the-Service-Discovery-Platform
