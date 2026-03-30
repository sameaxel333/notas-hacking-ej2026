
Download this image and find the flag.

Download image
# reto
# Descripción


# Solución 
## solución

```
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/stEgo]
└─$ binwalk pico.flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 585 x 172, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, default compression

                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/stEgo]
└─$ zsteg pico.flag.png  
b1,r,lsb,xy         .. text: "~__B>wV_G@"
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_96ae0ac1}$t3g0"
b1,abgr,lsb,xy      .. text: "E2A5q4E%uSA"
b2,b,lsb,xy         .. text: "AAPAAQTAAA"
b2,b,msb,xy         .. text: "HWUUUUUU"
b4,r,lsb,xy         .. file: Targa image data (16-273) 65536 x 4097 x 1 +4352 +4369 - 1-bit alpha - right "\021\020\001\001\021\021\001\001\021\021\001"                            
b4,g,lsb,xy         .. file: 0420 Alliant virtual executable not stripped
b4,b,lsb,xy         .. file: Targa image data - Map 272 x 17 x 16 +257 +272 - 1-bit alpha "\020\001\021\001\021\020\020\001\020\001\020\001"                                        
b4,bgr,lsb,xy       .. file: Targa image data - Map 273 x 272 x 16 +1 +4113 - 1-bit alpha "\020\001\001\001"                                                                        
b4,rgba,msb,xy      .. file: Applesoft BASIC program data, firs
```

Verifique que la imagen si sea png, revise con binwalk y al parecer no muestra archivos ocultos mas que Zlib del formato. Utilice la herramienta zsetg el cual detecta el canal rgb y extraje directamente la bandera entre los datos de color.

zsetg: Zsteg is also a tool like Jsteg but it is used to detect LSB steganography only in the case of PNG and BMP images.

## solución 2




# referencias

