# reto
# Descripción
Description
Download this disk image, find the key and log into the remote machine. Note: if you are using the webshell, download and extract the disk image into /tmp not your home directory.

Additional details will be available after launching your challenge instance


# Solución 
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ mmls disk.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ 
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ ┌──(kali㉿kali)-[~/picoctf/forensic/operation-orchid]                                       
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ fls -o 206848 disk.img 470-r        
Error stat(ing) image file (raw_open: image "470-r" - No such file or directory)
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ fls -o 206848 disk.img 470 -r
r/r 2344:       .ash_history
d/d 3916:       .ssh
+ r/r 2345:     id_ed25519
+ r/r 2346:     id_ed25519.pub
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ icat -o 206848 disk.img 2345 > key_file
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ file key_file                
key_file: OpenSSH private key
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ chmod 600 key_file 
                                                                                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ ssh -i key_file -p 56637 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:56637 ([13.59.203.175]:56637)' can't be established.
ED25519 key fingerprint is: SHA256:XBSvB1lk28EctsAVdKJtsl0A7C5bonqPrvHCYH8aEy4
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:56637' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1047-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt 
picoCTF{k3y_5l3u7h_b5066e83}ctf-player@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed
## solución

## solución 2




# referencias

