

# reto
# Descripción
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye here.

# Solución 
## solución
```
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ open flag.png                         
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ binwalk flag                             

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------

                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ binwalk flg.png                           

General Error: Cannot open file flg.png (CWD: /home/kali/picoctf/forensic) : [Errno 2] No such file or directory: 'flg.png'

                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ binwalk flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2869, uncompressed size: 3024, name: secret/flag.png
42908         0xA79C          End of Zip archive, footer length: 22

                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ unzip flag.png                                       
Archive:  flag.png
warning [flag.png]:  39739 extra bytes at beginning or within zipfile
  (attempting to process anyway)
   creating: secret/
  inflating: secret/flag.png         
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ cd secret 
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/secret]
└─$ ls 
flag.png
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/secret]
└─$ unzip flag.png 
Archive:  flag.png
  End-of-central-directory signature not found.  Either this file is not
  a zipfile, or it constitutes one disk of a multi-part archive.  In the
  latter case the central directory and zipfile comment will be found on
  the last disk(s) of this archive.
unzip:  cannot find zipfile directory in one of flag.png or
        flag.png.zip, and cannot find flag.png.ZIP, period.
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/secret]
└─$ binwalk flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 600 x 50, 16-bit grayscale, non-interlaced
134           0x86            Zlib compressed data, best compression

                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/secret]
└─$ explorer.exe flag.png              
explorer.exe: command not found
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/secret]
└─$ open flag.png                
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/secret]
```
al abrir escribi la bandera desde el la imagen a mano 
## solución 2




# referencias

