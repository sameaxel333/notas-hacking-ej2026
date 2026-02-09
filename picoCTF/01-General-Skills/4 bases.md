
# Descripcion

What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.

# Solución 
## solución 1- Consola
```
sameaxel33-picoctf@webshell:~$ echo 'bDNhcm5fdGgzX3IwcDM1echo' | base64
YkROaGNtNWZkR2d6WDNJd2NETTFlY2hvCg==
sameaxel33-picoctf@webshell:~$ echo 'bDNhcm5fdGgzX3IwcDM1echo' | base64 -d
l3arn_th3_r0p35
```

flag: l3arn_th3_r0p35

## solución 2 cyberchef

https://cyberchef.org/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE

## solución 3 python

```
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1echo')
b'l3arn_th3_r0p35y\xc8h'
>>> 
```
# referencias
