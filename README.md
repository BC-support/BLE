# BLE Peripheral
These file updates allow the PHL using the current image (4.17.0) to run the BLE interface.

# Installation
1) Download updated files, ble_buster.tar.gz and mahalia-ble-peripherals.js.
[https://github.com/BC-support/BLE](https://github.com/BC-support/BLE)
2) Connect host computer to the PHL via WiFi.
3) ssh into the PHL and delete the existing node_module files with
```
/usr/share/mahalia-ble-peripheral/node_modules$ sudo rm -rf *
```
4) Copy files from host to PHL as root. Note the root user password is 'toor'.
```
scp mahalia-ble-peripheral.js root@10.0.0.1:/usr/share/mahalia-ble-peripheral
scp ble_buster.tar.gz root@10.0.0.1:/usr/share/mahalia-ble-peripheral/node_modules
```
5) On PHL, uncompress files. 
```
/usr/share/mahalia-ble-peripheral/node_modules$ sudo tar -xf ble_buster.tar.gz
```
6) Restart PHL.
7) Run BLE Server on host computer to connect to PHL.
