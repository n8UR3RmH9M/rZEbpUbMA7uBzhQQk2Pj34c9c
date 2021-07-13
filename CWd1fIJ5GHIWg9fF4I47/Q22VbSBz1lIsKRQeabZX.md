## DC-5 Summary

In this article we will learn how to gain root access to DC-5 machine. 
This machine is exploited using a combination of web server access log poisoning and a local file inclusion vulnerability (LFI) in a web application resulting in remote code execution (RCE). The ultimate goal of this challenge is to get root and to read the one and only flag.

For more details see [DC Challenges](https://www.five86.com/dc-5.html).

### Enumeration

We start by running nmap scan against all ports:

```markdown
┌──(ramdac㉿virlnx)-[~]
└─$ nmap -sCV -Pn -p- -o nmap 192.168.120.57
Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times will be slower.
Starting Nmap 7.91 ( https://nmap.org ) at 2021-07-13 15:18 EDT
Nmap scan report for 192.168.120.57
Host is up (0.0018s latency).
Not shown: 65532 closed ports
PORT      STATE SERVICE VERSION
80/tcp    open  http    nginx 1.6.2
|_http-server-header: nginx/1.6.2
|_http-title: Welcome
111/tcp   open  rpcbind 2-4 (RPC #100000)
| rpcinfo: 
|   program version    port/proto  service
|   100000  2,3,4        111/tcp   rpcbind
|   100000  2,3,4        111/udp   rpcbind
|   100000  3,4          111/tcp6  rpcbind
|   100000  3,4          111/udp6  rpcbind
|   100024  1          42782/tcp   status
|   100024  1          48194/udp   status
|   100024  1          55162/udp6  status
|_  100024  1          60306/tcp6  status
42782/tcp open  status  1 (RPC #100024)

```



### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/n8UR3RmH9M/08gTNzCvTQrIiCN28YTn/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
