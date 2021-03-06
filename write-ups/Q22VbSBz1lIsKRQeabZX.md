## vulnhub: dc-5

Purposely built vulnerable lab machine with the intent of gaining experience in the world of penetration testing. Susceptible to web server access log poisoning and a local file inclusion vulnerability (LFI) resulting in remote code execution (RCE). The ultimate goal is to get access to a root user and read the flag.

For more details see [DC Challenges](https://www.five86.com/dc-5.html).

### Enumeration

We start by running **nmap** scan against our target DC-5 192.168.120.57 running in virtual machine in my environment.

```javascript
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

From **nmap** result we found three available ports open **80,111,42782**.

#### Web Enumeration
Exploring the webpage for hints we notice a contact form which seems interesting. 

<img src="https://blloren.com/assets/img/8JCiWyCRbq579sarPEMX.PNG" width="1127" height="477">

We filled the form and submitted it.

<img src="https://blloren.com/assets/img/Ljo7xL1tCkrwY8a6XEHG.PNG" width="1127" height="477">

After submitting the form we are redirected to *Thankyou.php* page. Refreshing the page several times we notice the changes in **Copyright year** text 2020 or 2019.

### Exploitation

Layout

### Local Privilege Escalation

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.


### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
