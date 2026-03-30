

# reto
# Descripción
Files can always be changed in a secret way. Can you find the flag?cat.jpg
# Solución 
## solución


## solución 2


```
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/infromation]
└─$ exiftool cat.jpg                   
ExifTool Version Number         : 13.36
File Name                       : cat.jpg
Directory                       : .
File Size                       : 878 kB
File Modification Date/Time     : 2025:12:12 14:21:14-05:00
File Access Date/Time           : 2026:03:29 23:33:49-04:00
File Inode Change Date/Time     : 2026:03:29 23:33:28-04:00
File Permissions                : -rw-rw-r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
                                        
                                        
                                        
```

Use el comando file para confirmar que es un jpg, revise con binwal para verificar si no tenia un zip oculto pero al parecer no, entonces revise los metadatos. Al ver la licencia hay un string extraño, lo desencripte en base64 con cyberchef y me dio la bandera.
# referencias

