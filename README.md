# Wifi-Pineapple-MK7-Disconnect-client-on-reboot
Disconnects radio2 (client) after reboot

Add to your /etc/init.d/ directory

`chmod +x /etc/init.d/client_network_reset`

`/etc/init.d/client_network_reset enable`

This will create a symlink in /etc/rc.d To make sure it is enabled

`/etc/init.d/client_network_reset enabled && echo on`

If it returns `on` then

`reboot`

Client mode should be disconnected.

Remember this will be on EVERY reboot. If you want to reverse this then

`rm /etc/init.d/client_network_reset`
