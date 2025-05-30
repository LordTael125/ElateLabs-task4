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

4. Adding rule to allow ssh port to be accessible 

It can be performed using the command

```
    $ sudo ufw allow in 22
```

5. Reseting the rules to default

```
    $ sudo ufw reset
    $ sudo ufw default deny incoming
```

Summary : the working of firewall
```
    -> Firewall works as filter based on rules declared to decide if the device can accessed or not by managing the iptables
```