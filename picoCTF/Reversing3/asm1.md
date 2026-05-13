# reto
# Descripción
What does asm1(0x295) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/2df9a8d7cf4a5aead6f62e9152fa816fecebd9e89385051b47b91e7c6d22582b/test.S)

# Solución 
## solución
**Explicación paso a paso (como si yo lo hubiera hecho):**

1. La función recibe el argumento `0x295` (661 en decimal).
    
2. En `+7` se compara `[ebp+8]` (el argumento) con `0x3ff` (1023). Como `0x295` no es mayor que `0x3ff`, no se salta a `+41`.
    
3. En `+16` se compara con `0x295`. Son iguales, por lo que `jne` (saltar si no igual) no se ejecuta.
    
4. En `+25` se mueve el argumento a `eax`: `eax = 0x295`.
    
5. En `+28` se suma `0xd` (13) a `eax`: `eax = 0x295 + 0xd = 0x2a2`.
    
6. Salta a `+64`, se restaura `ebp` y se retorna con `eax = 0x2a2`.

flag 0x2a2

## solución 2


# referencias

