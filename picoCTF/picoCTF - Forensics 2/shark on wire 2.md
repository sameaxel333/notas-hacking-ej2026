# reto
# Descripción
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/ca7e8f9bb6b060dd724f90e3243aa3e36fc0d98c9b421cef0e860d1ff75f9ef0/capture.pcap). Recover the flag.

# Solución 
wireshark capture.pcap &   verificamos con esto, y el follow udo, no funciona entones 

`udp.stream eq 32 udp.stream eq 60`

- Ahora observamos que el puerto destino udp es 22, establecemos fitro

`udp.dstport == 22`


```
vemos que si le quitamos el 5  nos da >>> chr(112)
'p'
>>> chr(105)
'i'
>>> chr(99)
'c'
>>> chr(111)
'o'
>>> 

utilizamos el siguiente script y lo ejecutamos en la misma carpeta
from scapy.all import *

packets = rdpcap('capture.pcap')

flag=''

for p in packets:
    if UDP in p and p[UDP].dport == 22:
        if p[UDP].sport > 5000:
            flag+=chr(p[UDP].sport - 5000)

print(flag)
```
## solución 2




# referencias

