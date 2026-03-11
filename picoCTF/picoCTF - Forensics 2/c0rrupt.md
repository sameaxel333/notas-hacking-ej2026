# reto
# Descripción
#### Description

We found this [file](https://challenge-files.picoctf.net/c_fickle_tempest/87bdc8ce30b177d033b3d68bca4647950bb07304032861baa912ebe08701d355/mystery). Recover the flag.

# Solución 


cambiamos `aa 00 16 25 00 00 16 25` por `00 00 16 25 00 00 16 25`

- lo corregimos con `hexeditor` , salimos y guardamos con `Ctrl+x`

`hexeditor mistery`

- corregir IHDR : 43 22 44 52 por 49 48 44 52
- instalamos `pngcheck` para auxiliarnos en en el análisis

`sudo apt install pngcheck`

- verificamos los erroes en el png

`pngcheck -v mistery`

- corregimos `pHys`, cambiamos `aa 00 16 25 00 00 16 25` por `00 00 16 25 00 00 16 25`
- verificamos errores de nuevo

`pngcheck -v mistery`

- corregimos el tamaño del chunk, cambiamos `AA AA FF A5` por `00 00 FF A5`
- corregir chunk anterior para que diga `IDAT` , cambiamos `AB 44 45 54` por `49 44 41 54`
- verificamos y abrimos el archivo para la flag

`file mistery open mistery`
## solución

## solución 2




# referencias

