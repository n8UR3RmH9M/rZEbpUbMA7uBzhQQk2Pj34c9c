### Field Notes for Linux Systems

|:---	|---:|
|commands |description|
|:---	|---:|
|`hash-identifier` <br/> `hashid 'hashtext'`|identify hash type|
|:---	|---:|
|`john hash.txt --wordlist=/usr/share/wordlists/rockyou.txt --format=raw-sha256`|crack hash file|
|:---	|---:|
|`sed -n '45000,50000p' /usr/share/wordlists/rockyou.txt | hashcat -m3200 -a0 --force 'bcrypthash'` <br/> `john cred --wordlist=/usr/share/wordlists/rockyou.txt --format=bcrypt`|decrypting bcrypt|
|:---	|---:|
|`hashcat -m 1710 -a 0 hash:salt  /usr/share/wordlists/rockyou.txt`|decrypting sha512 salted password|
|:---	|---:|
|`smbclient -N -L //10.10.114.22`|list remote smb shares|
|:---	|---:|
|`smbclient //10.10.114.22/C$ -U administrator` <br/> `smbclient //10.10.114.22/C$`|connect to remote smb shares|
|:---	|---:|
|`echo -n blloren.com | base64`|encode to base64|
|:---	|---:|
|`echo 'Ymxsb3Jlbi5jb20=' | base64 -d`|decode to base64|
|:---	|---:|
|`echo 'Ymxsb3Jlbi5jb20=' | base64 -d`|decode to base64|


