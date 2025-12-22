# ZTE-MF289F-OpenWrt-24.10.05-by-ilblogdicristiangallo
This customized version of OpenWrt for ZTE MF286D is designed to deliver a complete, ready-to-flash firmware optimized for advanced LTE/5G modem support and post-install automation.
This build targets ipq40xx/generic and is specifically tuned for the ZTE MF289F, providing stable USB modem support, web-based management, and extended modem control tools out of the box.

# 🔑 Key Features

Native USB modem support
Built-in drivers for QMI, MBIM, USB serial, and CDC interfaces
Automatic support for /dev/cdc-wdm0 LTE WAN
LuCI Web Interface
Full LuCI support for:

QMI

ModemManager

MBIM

WireGuard VPN

Advanced LTE / WWAN support

# Integrated ModemManager

QMI & MBIM CLI tools

USB modeswitch for modem detection

# Preconfigured external feeds

Cristian Gallo repository
IceG Modem Extras repository
GPG keys automatically installed at first boot
Local LuCI applications bundled
Installed directly inside the firmware image
No post-flash installation required
Preconfigured system
LTE WAN already configured
Firewall rules ready
LAN bridge configured on LAN2 only
Included Packages
# Base system & LuCI
luci

# LTE / Modem support

modemmanager
uqmi
umbim
usb-modeswitch

# kernel modules (USB / WWAN)

kmod-usb-serial
kmod-usb-serial-option
kmod-usb-serial-wwan
kmod-usb-wdm
kmod-usb-net
kmod-usb-net-qmi-wwan
kmod-usb-net-cdc-mbim
kmod-mii

# LuCI protocol integrations

luci-proto-qmi
luci-proto-modemmanager
luci-proto-mbim

# VPN

luci-proto-wireguard
wireguard-tools

# Bundled LuCI applications (local .ipk)

luci-app-modemband – LTE band locking
luci-app-sms-tool-js – SMS management from LuCI
luci-app-3ginfo-lite – LTE signal & cell info
luci-app-atcommands – AT command interface

# 🔐 Trusted External Feeds

The firmware includes preconfigured and trusted external repositories:
Cristian Gallo OpenWrt Repository
IceG Modem Extras Repository
All required GPG public keys are:
Embedded into the firmware
Automatically added to opkg at first boot
No manual key installation required

# 🌐 Network Configuration (Default)

LAN
IP: 192.168.1.1
Bridge port: LAN2 only
WAN (LTE)
Protocol: QMI
Device: /dev/cdc-wdm0
APN: internet
IPv4 enabled
WAN6 via DHCPv6
Firewall
NAT enabled on WAN
LAN → WAN forwarding preconfigured
