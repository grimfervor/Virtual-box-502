# 1: Add VirtualBox Repository Key
To add the repository key, run the commands below:
```
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
```

# 2: Add VirtualBox Repository
To add the repository to Ubuntu system run:
```
sudo sh -c 'echo "deb http://download.virtualbox.org/virtualbox/debian $(lsb_release -sc) contrib" >> /etc/apt/sources.list.d/virtualbox.list'
```

# 3: Installing VirtualBox
You may want to remove older versions of VirtualBox if you're still running it.
```
sudo apt remove virtualbox virtualbox-5.1
```

VirtualBox requires some packages, to install them run:
```
sudo apt update
sudo apt-get -y install gcc make linux-headers-$(uname -r) dkms
```

Finally, run:
```
sudo apt update
sudo apt-get install virtualbox-5.2
```
It's recommended to install the extention pack for some extra features like copy pasting between host and VM.
```
sudo apt install virtualbox-ext-pack
```

