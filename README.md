# ElateLabs-task4
This displays the working through ufw firewall

1. Installation of ufw

For Archlinux :
```
    $ sudo pacman -Sy ufw
```

For Debian based distro :
```
    $ sudo apt install ufw
```

For Fedora based distro :
```
    $ sudo dnf install ufw
```

2. Initialization of ufw

To initialize the ufw wirewall enable the ufw services in systemd and enable the firewall using command

```
    $ sudo ufw enable
```

<img src="Data/Status.png">

As can be noticed the list is empty on checking the status of ufw

3. Adding a rule to block a port on the network

A port can be blocked from getting accessed using command 
> For all IP Address in the network 
```
    $ sudo ufw deny in <port_no>
```

> For a specefic IP to be blocked on your device
```
    $ sudo ufw deny in from <local_ip> to <remote_ip> port <port_no>
```

<img src="Data/Blocking_telnet.png">
