# Setup UART on Raspberry Pi

### Get rid of modem manager (can interfere with mavlink ports)
1. Run:
```bash
sudo apt purge modemmanager
```

### Activate `/dev/serial0`
1. Open `/boot/firmware/config.txt`:
```bash
vim /boot/firmware/config.txt
```

2. Add the following lines to the file
```bash
enable_uart=1
dtoverlay=disable-bt
```

3. Reboot

### Disable console login on serial port
1. Run:
```bash
sudo raspi-config
```
2.  Go to **Interface Options** → **Serial Port**
3. Answer:
    - “Login shell over serial?” → **No**
    - “Enable serial hardware?” → **Yes**
    - Then reboot.

### Run as sudo but with environment 
- (Only if you encounter permission errors)
```bash
sudo -E env "PATH=$PATH" mavproxy.py --master=/dev/serial0
# or
sudo -E env "PATH=$PATH" python monitor_incoming.py
```