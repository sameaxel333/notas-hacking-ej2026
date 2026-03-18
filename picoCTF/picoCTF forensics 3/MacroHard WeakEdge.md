
# reto
# Descripción

I've hidden a flag in this file. Can you find it? [Forensics_is_fun.pptm](https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm)
# Solución 
## solución
primero descomprimimos con uzip el documento
en el documento hidden
ya despues de ahi utilizamos el siguiente comando 
└─$ cat ppt/slideMasters/hidden | tr -d ' ' | base64 -d 
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}

## solución 2




# referencias

