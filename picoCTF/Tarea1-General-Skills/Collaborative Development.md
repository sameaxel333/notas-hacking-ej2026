# 
# Descripción
#### Description

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/70/challenge.zip)

# Solución 
## solución
```
sameaxel33-picoctf@webshell:~$ ls
README.txt  challenge.zip  drop-in
sameaxel33-picoctf@webshell:~$ git branches
git: 'branches' is not a git command. See 'git --help'.
sameaxel33-picoctf@webshell:~$ cd drop-in/ 
sameaxel33-picoctf@webshell:~/drop-in$ git branches 
git: 'branches' is not a git command. See 'git --help'.
sameaxel33-picoctf@webshell:~/drop-in$ git branch   
sameaxel33-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
sameaxel33-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
sameaxel33-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
sameaxel33-picoctf@webshell:~/drop-in$ cat flag.py                
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')sameaxel33-picoctf@webshell:~/drop-in$ q
-bash: q: command not found
sameaxel33-picoctf@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
sameaxel33-picoctf@webshell:~/drop-in$ cat flag.p
cat: flag.p: No such file or directory
sameaxel33-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')sameaxel33-picoctf@webshell:~/drop-in$ q
-bash: q: command not found
sameaxel33-picoctf@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
sameaxel33-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("w0rk_7ffa0077}")
sameaxel33-picoctf@webshell:~/drop-in$ 
```

## solución 2




# referencias
