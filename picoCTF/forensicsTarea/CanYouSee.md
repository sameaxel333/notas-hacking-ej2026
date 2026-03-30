

# reto
# Descripción

# Solución 
## solución
```
┌──(kali㉿kali)-[~/picoctf/forensic/Canyouseeme]
└─$ unzip unknown.zip  
Archive:  unknown.zip
  inflating: ukn_reality.jpg         
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/Canyouseeme]
└─$ ls                                   
ukn_reality.jpg  unknown.zip
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/Canyouseeme]
└─$ binwalk ukn_reality.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.01
1813318       0x1BAB46        JBOOT STAG header, image id: 8, timestamp 0xAD56EFB0, image size: 1718551036 bytes, image JBOOT checksum: 0xE9BF, header JBOOT checksum: 0x3BBA

                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/Canyouseeme]
└─$ exiftool unknown.zip                          
ExifTool Version Number         : 13.36
File Name                       : unknown.zip
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:03:11 20:36:44-04:00
File Access Date/Time           : 2026:03:30 00:24:29-04:00
File Inode Change Date/Time     : 2026:03:30 00:24:18-04:00
File Permissions                : -rw-rw-r--
File Type                       : ZIP
File Type Extension             : zip
MIME Type                       : application/zip
Zip Required Version            : 20
Zip Bit Flag                    : 0
Zip Compression                 : Deflated
Zip Modify Date                 : 2024:03:12 00:05:52
Zip CRC                         : 0x42676dd7
Zip Compressed Size             : 2251928
Zip Uncompressed Size           : 2263756
Zip File Name                   : ukn_reality.jpg
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/Canyouseeme]
└─$ exiftool ukn_reality.jpg 
ExifTool Version Number         : 13.36
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:03:11 20:05:51-04:00
File Access Date/Time           : 2026:03:30 00:25:26-04:00
File Inode Change Date/Time     : 2026:03:30 00:24:29-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fM2I5MjA5YTJ9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
                                                                                          
┌──(
```
Extraje el contenido del zip, verifique que si fuera jpg, no tenia nada adentro, verifique los metadatos y en Attribution URL venia un texto encriptado, lo pase por cyberchef y me dio la bandera. 
## solución 2




# referencias

