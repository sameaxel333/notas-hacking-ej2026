# reto
# Descripción
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/picopico.key). Recover the flag.

# Solución 
## solución
primero buscamos el tráfico de captura de paquetes https luego de ahi descargamos la imagen de vultures
picoCTF{honey.roasted.peanuts}


tambien podemos utilizar el mismo comando 
 ssldump -r capture.pcap -d -k picopico.key | grep pico -A 2,
## solución 2




# referencias

