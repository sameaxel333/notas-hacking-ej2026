# reto
# Descripción

I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/75/challenge.zip)
# Solución 
```
sameaxel33-picoctf@webshell:~/drop-in$ git reflog

[2]+  Stopped                 git reflog
sameaxel33-picoctf@webshell:~/drop-in$ git checkout 6603cb4
Note: switching to '6603cb4'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 6603cb4 create flag
sameaxel33-picoctf@webshell:~/drop-in$ cat message.txtt
cat: message.txtt: No such file or directory
sameaxel33-picoctf@webshell:~/drop-in$ cat message.txt 
picoCTF{s@n1t1z3_9539be6b}
sameaxel33-picoctf@webshell:~/drop-in$ 
```

## solución 2




# referencias
