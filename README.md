# z-nomp-fail2ban
fail2ban filters for z-nomp

/etc/fail2ban/jails.d

```sh
[z-nomp]
enabled = true
protocol = tcp
filter = z-nomp
logpath = /path/to/log.log
action   = iptables-multiport[name=Z-NOMP, port=”0:65535″, protocol=all] 
maxretry = 30
# 1 hour
bantime = 3600
```
