# apache-serverstatus
A live CLI view on apache's mod_status.  Proof of concept version.

# screenshot
![screenshot](https://raw.githubusercontent.com/scarfboy/apache-serverstatus/main/screenshot.png)

# arguments


```
Usage: apache-serverstatus [options]

Options:
  -h, --help            show this help message and exit
  -i INTERVAL, --interval-sec=INTERVAL
                        Poll interval, in seconds. Defaults to 0.25
  -p, --no-chop-port    By default we chop post off vhost for readability. Use
                        this if you want to see those.
  -v VCHOP, --chop-vhost=VCHOP
                        Chop off parts from the end of vhost. Defaults to 1,
                        aiming to remove .com or such. Will refuse to remove
                        everything, so a high value shows the first part of
                        every name.
  -u HOST, --host=HOST  We basically fetch http://THIS/server-status  so this
                        defaults to 127.0.0.1
```

TODO:
- look at parsing outputs for other MPMs (it's currently aimed at prefork)
