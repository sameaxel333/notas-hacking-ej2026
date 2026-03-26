# reto
# Descripción

 #### Description

Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory. [Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.

---
# Solución 
## solución
└─$ cd Sleuthkitintro 
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/Sleuthkitintro]
└─$ wget 'https://artifacts.picoctf.net/c/164/disk.img.gz'
--2026-03-23 10:25:26--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.105, 13.225.222.125, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                     100%[======================================================>]  28.34M   720KB/s    in 40s     

2026-03-23 10:26:07 (730 KB/s) - ‘disk.img.gz’ saved [29714372/29714372]

                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/Sleuthkitintro]
└─$ gzip -d disk.img.gz                                    
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/Sleuthkitintro]
└─$ mmls disk.img            
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/Sleuthkitintro]
└─$ nc saturn.picoctf.net 56263
What is the size of the Linux partition in the given disk image?
Length in sectors: ^C
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/Sleuthkitintro]
└─$ nc saturn.picoctf.net 56263
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/Sleuthkitintro]
└─$ 

## solución 2




# referencias

