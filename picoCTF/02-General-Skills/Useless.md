
# Descripción
There's an interesting script in the user's home directory

Additional details will be available after launching your challenge instance.

# Solución 
## solución
```
sameaxel33-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p55856
The authenticity of host '[saturn.picoctf.net]:55856 ([13.59.203.175]:55856)' can't be established.
ED25519 key fingerprint is SHA256:DiJcS90U9QussLS8HLR6l6BGJb5eCA0vRmA18IvDvw8.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:55856' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 

picoplayer@challenge:~$ ls
useless
picoplayer@challenge:~$ file useless
useless: Bourne-Again shell script, ASCII text executable
picoplayer@challenge:~$ cat 
picoplayer@challenge:~$ file useless
useless: Bourne-Again shell script, ASCII text executable
picoplayer@challenge:~$ cat useless
#!/bin/bash

picoplayer@challenge:~$ man useless
```
picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_4151}
## solución 2




# referencias
