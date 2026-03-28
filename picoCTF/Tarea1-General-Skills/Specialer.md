# reto
# Descripción

# Solución 
## solución
```
vladi@911:~/Desktop/retos/reto$ ssh -p 59796 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:59796 ([13.59.203.175]:59796)' can't be established.
ED25519 key fingerprint is: SHA256:lMXKIC17ONzyUJx7ZYBY5VSwoxCz20uq5/Nm+IhXKew
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:59796' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@saturn.picoctf.net's password: 
Specialer$ ls
-bash: ls: command not found
Specialer$ whoami 
-bash: whoami: command not found
Specialer$ cat
-bash: cat: command not found
Specialer$ 
!          bash       cd         declare    else       false      hash       let        pwd        shift      times      unalias    
./         bg         command    dirs       enable     fc         help       local      read       shopt      trap       unset      
:          bind       compgen    disown     esac       fg         history    logout     readarray  source     true       until      
[          break      complete   do         eval       fi         if         mapfile    readonly   suspend    type       wait       
[[         builtin    compopt    done       exec       for        in         popd       return     test       typeset    while      
]]         caller     continue   echo       exit       function   jobs       printf     select     then       ulimit     {          
alias      case       coproc     elif       export     getopts    kill       pushd      set        time       umask      }          
Specialer$ cd ../../           
bin/   home/  lib/   lib64/ 
Specialer$ cd ../../home
Specialer$ pwd
/home
Specialer$ ls            
-bash: ls: command not found
Specialer$ cd ctf-player/
.hushlogin  .profile    abra/       ala/        sim/        
Specialer$ cd ctf-player/
.hushlogin  .profile    abra/       ala/        sim/        
Specialer$ cd ctf-player/
Specialer$ cd   
.hushlogin  .profile    abra/       ala/        sim/        
Specialer$ cd ala/
Specialer$ echo $(<kazam.txt)
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_d5ef8b71
```

## solución 2




# referencias

