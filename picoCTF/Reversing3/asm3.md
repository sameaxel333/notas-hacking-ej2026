# reto
# Descripción
What does asm3(0xb58568e8,0xc63ab2a1,0xf9d33ef4) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/b3fee52f11c2963c3f6008623c66d7c0906ab439f927132ac7fbc1d53f83c4ee/test.S)


# Solución 
El análisis paso a paso de `asm3(0xb58568e8, 0xc63ab2a1, 0xf9d33ef4)` es el siguiente:

1. Se inicializa `eax = 0`.
    
2. `ah = byte en [ebp+0xb]` → corresponde al tercer byte (más significativo) del primer argumento: `0xb5`. Entonces `eax = 0x0000b500`.
    
3. `shl ax, 0x10` → desplaza `ax` 16 bits a la izquierda, dando `ax = 0`. Luego `eax = 0`.
    
4. `sub al, [ebp+0xd]` → resta el segundo byte del segundo argumento (`0xb2`) de `al` (que es 0). Resultado: `al = 0x4e` (por complemento a dos). `eax = 0x4e`.
    
5. `add ah, [ebp+0xc]` → suma el primer byte del segundo argumento (`0xa1`) a `ah` (que era 0). `ah = 0xa1`. Ahora `eax = 0x0000a14e`.
    
6. `xor ax, [ebp+0x10]` → hace XOR con la palabra de 16 bits del tercer argumento (bytes `0xf4` y `0x3e`, formando `0x3ef4`).  
    `0xa14e XOR 0x3ef4 = 0x9fba`.
    

El resultado final es `0x9fba`.
## solución

## solución 2


# referencias

