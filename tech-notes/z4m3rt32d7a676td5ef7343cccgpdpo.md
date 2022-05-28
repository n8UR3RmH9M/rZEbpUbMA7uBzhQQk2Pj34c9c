### Linux OS Commands Field Notes

|:---	|---:|
|commands |description|
|:---	|---:|
|`hashd-identifier` <br/> `hashid 'hashtext'`|identify hash type|
|:---	|---:|
|`john hash.txt --wordlist=/usr/share/wordlists/rockyou.txt --format=raw-sha256`|crack hash file|
|:---	|---:|
|`sed -n '45000,50000p' /usr/share/wordlists/rockyou.txt | hashcat -m3200 -a0 --force 'bcrypthash'` <br/> `john cred --wordlist=/usr/share/wordlists/rockyou.txt --format=bcrypt`|decrypting bcrypt|
|:---	|---:|
|`hashcat -m 1710 -a 0 hash:salt  /usr/share/wordlists/rockyou.txt`|decrypting sha512 salted password|
|:---	|---:|

