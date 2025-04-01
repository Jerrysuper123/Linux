# Linux

## boot volume
usually contain the os and necessary file systems to boot the instance.
often persistent and a type of block storage.

## block storage
general purpose storage for data, application and databases, just like ssd.

block storage also can be used as boot volume.

## in /etc/ contains the system-wide configuration file
for example in /etc/environment is the global proxy setting
```
http_proxy="http://proxy.example.com:8080"
https_proxy="http://proxy.example.com:8080"
ftp_proxy="http://proxy.example.com:8080"
//define address that should by pass the proxy, meaning if going to localhost, example.com, do not go thru proxy
no_proxy="localhost,127.0.0.1,.example.com"

```

## proxy also can be set in shell startup scrpts like /etc/profile (for logins shells) or /etc/bash.bashrc (for interactive shell)
```
export http_proxy="http://proxy.example.com:8080"
export https_proxy="http://proxy.example.com:8080"

```

## in /etc/hosts, host setting, map ip addresses to hostnames manually, overriding DNS
```
127.0.0.1   localhost
192.168.1.10   myserver.local

```

## /etc/hostname (System Hostname) Contains the system’s hostname (just the name, no domain).
```
my-computer
```

## /etc/resolv.conf (DNS Configuration) Defines DNS servers used for name resolution.
```
nameserver 8.8.8.8
nameserver 8.8.4.4
```
