

# reto
# Descripción
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:

challenge.zip
Additional details will be available after launching your challenge instance.

# Solución 
## solución
```
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ ls 
challenge.zip
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ unzip challenge.zip 
Archive:  challenge.zip
   creating: home/ctf-player/drop-in/
 extracting: home/ctf-player/drop-in/flag.png  
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ LS 
LS: command not found
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ ls 
challenge.zip  home
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ unzip challenge.zip 
Archive:  challenge.zip
replace home/ctf-player/drop-in/flag.png? [y]es, [n]o, [A]ll, [N]one, [r]ename: n
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ file home/ctf-player/drop-in/flag.png
home/ctf-player/drop-in/flag.png: PNG image data, 99 x 99, 1-bit colormap, non-interlaced
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ binwalk home/ctf-player/drop-in/flag.png


DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 99 x 99, 1-bit colormap, non-interlaced

                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ exiftool home/ctf-player/drop-in/flag.png
ExifTool Version Number         : 13.36
File Name                       : flag.png
Directory                       : home/ctf-player/drop-in
File Size                       : 346 bytes
File Modification Date/Time     : 2024:03:11 19:50:25-04:00
File Access Date/Time           : 2026:03:30 00:18:26-04:00
File Inode Change Date/Time     : 2026:03:30 00:17:28-04:00
File Permissions                : -rw-r--r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 99
Image Height                    : 99
Bit Depth                       : 1
Color Type                      : Palette
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Palette                         : (Binary data 6 bytes, use -b option to extract)
Transparency                    : 255 255
Pixels Per Unit X               : 2834
Pixels Per Unit Y               : 2834
Pixel Units                     : meters
Image Size                      : 99x99
Megapixels                      : 0.010
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ open flag.png
^C
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ explorer.exe  home/ctf-player/drop-in/flag.png
explorer.exe: command not found
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ open home/ctf-player/drop-in/flag.png
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/scansurprise]
└─$ 

```

## solución 2
Extraje el zip y verifique que la imagen no viniera con algo adentro y al parecer no, abri la imagen y es un qr, lo escanee con mi celular y me dio la bandera.



# referencias

