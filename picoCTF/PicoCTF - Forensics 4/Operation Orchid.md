# reto
# Descripción


# Solución 
## solución
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ icat -o 0000411648 disk.flag.img 1782 > flag.txt.enc
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ openssl aes-256-cbc -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
40C7099C1F7F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ fls -o 0000411648 disk.flag.img      
d/d 460:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 81: proc
d/d 82: dev
d/d 83: tmp
d/d 84: lib
d/d 87: var
d/d 96: usr
d/d 106:        bin
d/d 120:        sbin
d/d 466:        media
d/d 470:        mnt
d/d 471:        opt
d/d 472:        root
d/d 473:        run
d/d 475:        srv
d/d 476:        sys
d/d 2041:       swap
V/V 51001:      $OrphanFiles
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ ls                                                  
disk.flag.img  flag.txt  flag.txt.enc
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ fls -o 0000411648 disk.flag.img 1875                
Error extracting file from image (ext2fs_dir_open_meta: Error reading directory contents: 1875
)
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ icat -o 0000411648 disk.flag.img 1875                                                    
touch flag.txt
nano flag.txt 
apk get nano
apk --help
apk add nano
nano flag.txt 
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ openssl aes-256-cbc -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
405706E4FC7E0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ openssl enc -aes-256-cbc -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567 -md md5
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
40B7CCE10F7F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ openssl enc -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ cat flag.txt                                                               
Salted__0��!�-6V����0��U��l��&�:�pj_1�0�|�h
                                           �Ȥ7� ���؎$�'%                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
40570D8F607F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ ls
disk.flag.img  flag.txt  flag.txt.enc
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ cat flag.txt
picoCTF{h4un71ng_p457_0a710765}                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ 
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]
└─$ 


## solución 2




# referencias

