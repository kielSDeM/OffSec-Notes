```
wpscan --url http://driftingblues.box/blog --detection-mode aggressive -e --passwords=/home/kali/rockyou.txt 
```

Scans for vulnerable plugins.
 ```
 wpscan --url http://192.168.1.101/blog/ --enumerate ap --plugins-detection aggressive --plugins-version-detection aggressive
 ```
 Scans for passwords
 ```
 wpscan --url http://10.10.67.77 --usernames c0ldd --passwords rockyou.txt
 ```

```
wpscan --url http://10.10.67.77 --enumerate u 
```
