# Server Setup Guide

## Getting started

You're likely wondering *Should I run this on my home PC?* The best answer: it depends. That is, it depends on your needs. For that, you will also need to be aware of the risks as well as the costs.

For most people who just want to play with their friends privately, you could easily run a private server on your PC. However, if you intend to run it 24-7 that tends to be a bit trickier but is still doable on your home PC. 

What we advise against is running a public server on your home PC unless you're prepared to expose your residential IP address to the public. If you have some spare cash and are familiar with the Linux command line, we recommend investing in a small virtual private server (VPS) from a reputable host:

| Host                                          |
| --------------------------------------------- |
| [DigitalOcean](https://www.digitalocean.com/) |
| [Linode](https://www.linode.com/)             |
| [OVHCloud](https://www.ovhcloud.com/)         |

Keep in mind, a small VPS will typically only run a Linux distribution like Ubuntu or CentOS and not Windows. **Expect to be investing a lot more for a Windows VPS or dedicated server.**

## Firewall

If you are running a server on a home PC, then port forwarding will be necessary if you do not plan on running the server in local area network (LAN) mode. If you do not port forward, anyone outside your local network will not be able to connect to your server.

!!! warning "Don't put yourself at risk"
    By exposing your residential IP address, you place yourself at significant risk of denial-of-service (DoS) attacks and other risks.

Residential routers can be different depending on your service provider. We recommend following the procedures (if any) laid out by your service provider or follow [this guide by No-IP](https://www.noip.com/support/knowledgebase/general-port-forwarding-guide/).

Also keep in mind of your operating system may have a local firewall such as Windows Firewall or Ubuntu's Uncomplicated Firewall (ufw) that may prohibit anyone from connecting to your server including your local network.

## Installation and setup

### with Linux

As mentioned earlier, this guide makes many assumptions about your technical know-how with Linux. While this guide makes no assumptions about your Linux distribution, this guide will be using Debian 11.

1. Uhm
```
wget https://files.rigsofrods.org/
```
2. Extract the .zip into your desired location (Do not merge with anything else!)
```
unzip
```
3. Open `server.cfg` with nano (or vim) and adjust things to your liking
```
nano server.cfg
```
4. Run and verify the changes you've made are working **Note: You can see other CLI args with the `-h` flag**
```
./rorserver -c server.cfg
```

Should you encounter an error,

### with Windows

This guide assumes that you are using Windows as your own home PC with Windows 10+ any edition or through the remote desktop protocol with Windows Server 2016+. This guide will be using Windows 11.

1. Uhm
2. Extract the .zip into your desired location (Do not merge with anything else!)
3. Open `server.cfg` with Notepad (or your preferred text editor) and adjust things to your liking
4. Double-click `StartServer.bat` and verify the changes you've made are working

Should you encounter an error,

## Additional setup and personalization