

# Descripción
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/505/big-zip-files.zip)

# Solución 
## solución

```
sameaxel33-picoctf@webshell:~$ grep -r pico
.bash_history:wget https://challenge-files.picoctf.net/c_wily_courier/11d04620d1b8e59680f745f5e3d3957d48628b1e3e7c56c74c0030e82a778d63/warm
.bash_history:wget https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/static
.bash_history:wget https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/ltdis.sh
.bash_history:string static | grep pico
.bash_history:strings static | grep pico
.bash_history:ssh picoplayer@saturn.picoctf.net -p55856
.bash_history:wget https://challenge-files.picoctf.net/c_wily_courier/56f53a4189949d066fe969e998769a4e0390123be59782c06e6c0a52c78403e2/Addadshashanammu.zip
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
sameaxel33-picoctf@webshell:~$ 
```
picoCTF{gr3p_15_m4g1c_ef8790dc}
## solución 2




# referencia