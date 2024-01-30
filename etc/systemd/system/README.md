# Prologue

Systemd is a nice tool to start, stop and restart scripts on your linu machine. If your script crashes or the VPS does a system reboot your scripts will come back online.  
In order to use this you need to be on Linux, have systemd, the discord-twitter-bot has been properly installed and it has worked before.

# Setup and Configuration

## Prerequisites
- Linux OS
- systemd installed
- discord-twitter-bot properly installed and working

## Installation
1. Install necessary dependencies:
   - Dependency 1
   - Dependency 2
   - ...
2. Copy the dtb.service file to /etc/systemd/system: 
   `cp dtb.service /etc/systemd/system/dtb.service`
3. Edit dtb.service: 
   `nano /etc/systemd/system/dtb.service`
4. Adjust the `WorkingDirectory` in dtb.service to the path where the `discord-twitter-bot` folder/repository is cloned.

## Bot Configuration
- Adjust the path of your python executable (first parameter of `ExecStart`):
   - Run `which python3` to get the path to python3
   - Replace the path in the `ExecStart` line in dtb.service
- Adjust the path to main.py (second parameter of `ExecStart`):
   `<...>/discord-twitter-bot/bot/main.py`

## systemd commands
- Start the service: `sudo systemctl start dtb.service`
- Enable automatic startup: `sudo systemctl enable dtb.service`
- Disable automatic startup: `sudo systemctl disable dtb.service`
- Stop the service: `sudo systemctl stop dtb.service`
- Restart the service: `sudo systemctl restart dtb.service`

### Note:
`enable` means that the service is automatically started when your VPS boots up.

## Prerequisites
- Linux OS
- systemd installed
- discord-twitter-bot properly installed and working

## Installation
1. Copy the dtb.service file to /etc/systemd/system: 
   `cp dtb.service /etc/systemd/system/dtb.service`
2. Edit dtb.service: 
   `nano /etc/systemd/system/dtb.service`
3. Adjust the `WorkingDirectory` in dtb.service to the path where the `discord-twitter-bot` folder/repository is cloned.

## Bot Configuration
- Adjust the path of your python executable (first parameter of `ExecStart`):
   - Run `which python3` to get the path to python3
   - Replace the path in the `ExecStart` line in dtb.service
- Adjust the path to main.py (second parameter of `ExecStart`):
   `<...>/discord-twitter-bot/bot/main.py`

## systemd commands
- Start the service: `sudo systemctl start dtb.service`
- Enable automatic startup: `sudo systemctl enable dtb.service`
- Disable automatic startup: `sudo systemctl disable dtb.service`
- Stop the service: `sudo systemctl stop dtb.service`
- Restart the service: `sudo systemctl restart dtb.service`

### Note:
`enable` means that the service is automatically started when your VPS boots up.

Copy the dtb.service file and put it to /etc/systemd/system  
`cp dtb.service /etc/systemd/system/dtb.service`

Edit dtb.service  
`nano /etc/systemd/system/dtb.service`

Adjust the `WorkingDirectory` to the path you git cloned the `discord-twitter-bot` folder/repository.  

Adjust the path of your python executable (first parameter of `ExecStart`):   
```coffeescript
tin@Riftshadow:~# which python3
/usr/bin/python3
tin@Riftshadow:~# which python3.5
/usr/bin/python3.5
```

Adjust the path to main.py (second parameter of `ExecStart`)     
`<...>/discord-twitter-bot/bot/main.py`

# systemd commands

```coffeescript
sudo systemctl start dtb.service
sudo systemctl enable dtb.service
sudo systemctl disable dtb.service
sudo systemctl stop dtb.service
sudo systemctl restart dtb.service
```

`enable` means that the service is automatically started when your VPS boots up.