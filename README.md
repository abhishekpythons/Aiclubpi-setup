# Aiclubpi-setup
Ai club raspberry pi setup

## Enabling required interfaces
Go to Menu > Preferences > Raspberry Pi Configuration > Interfaces
Enable required Interfaces like SSH(for CLI remote access), VNC(for GUI remote access), etc.

## Adding network to automatiically connect to that Wi-Fi
 add following lines in /etc/wpa_supplicant/wpa_supllicant.conf
'''
 network = {
 ssid="Your SSID"
 psk="Your Password"
 }
'''
 then add following lines in /etc/rc.conf
'''
 wpa_supplicant=YES
 wpa_supplicant_flags="-i iwn0 -c /etc/wpa_supplicant.conf"
'''

## Enabling boot in GUI mode even when HDMI is not coonnected

