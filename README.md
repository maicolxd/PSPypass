# PSPypass

Bypass PS4 update checker. Most of the code in this project is based on [inaz2/proxy2](https://github.com/inaz2/proxy2)


## Features

* bypass the update checker of PS4
* easy to customize
* require no external modules

This script works on Python 2.7. Tested on macOS 10.11 and Ubuntu 16.04 LTS

## Usage

Just run as a script:

```$ python pspypass.py```

Above command runs the proxy on tcp/8080.
To use another port, specify the port number as the first argument.

```$ python pspypass.py 8080```

If you want the script run as a deamon (Run the proxy in the backgroud), just run the shell script

```$ pspypass.sh start```

To stop:

```$ pspypass.sh stop```

## Customize

Change these values in pspypass.py

`region_id`: Your region. Possible values are: jp, us, au, uk, eu, kr, sa, tw, ru, mx, cn. 

Region ID is based on the region of PS4 hardware, not the region of your PSN account.


`fake_version`: Your firmware version. <b>NOT</b> the latest version of official firmware. 

For example: You are on FW 3.50 and 4.00 is released. Just set `fake_version` to 3.50 or below.


## Firewall

If you use iptables on your server, remember to allow connection from the port. 

Example:

```
iptables -A ufw-user-input -p tcp -m tcp --dport 8080 -j ACCEPT
```


## References

### [inaz2/proxy2](https://github.com/inaz2/proxy2)
