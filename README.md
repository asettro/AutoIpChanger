
# Auto IP Changer with Tor
Script changes your IP address through the tor network at regular intervals which you can set

## Requirements:
- **Tor** must be installed on your system
- Root privileges to start and restart the tor service

## Installation:

1. ### Install Tor:
#### For Debian/Ubuntu based:
```bash
sudo apt update
sudo apt install tor
```
#### For Fedora based:
```bash
sudo dnf install tor
```
#### For Arch based:
```bash
sudo pacman -S tor
```

2. **Download the script**:
```
git clone https://github.com/asettro/AutoIpChanger.git
```

3. **Make script executable**:
```bash
chmod +x auto-ip-changer.sh
```
4. **Run script**:
```
sudo ./auto-ip-changer.sh
```

## Usage:
1. After running the script, it will check if tor is installed and running

2. You will be asked to enter how often you want the IP to change (in seconds)

3. The script will restart tor service and change your IP address at the specified interval

## Possible errors
**Proxy refused connection**
If you are changing your IP address too frequently you might get an error like "Proxy refused connection". This happens because tor is restarts and creats a new circuit or because the IP address change is happening too frequently.
**Solution**: If you get this error try to increase the time interval, the longer delay gives tor more time to properly establish a new connection the less chance of getting this error
## This script is okay for general browsing but not recommended for browsing like tor Browser

