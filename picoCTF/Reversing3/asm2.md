# reto
# Descripción
What does asm2(0xc,0x1d) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/03ef6d65b33a69a3aee644df1385c84ab7c9e3b45d81fe05ad144e1460a9eaaf/test.S)

# Solución 
Simulación:

Inicio: A = 0x1d (29 decimal), B = 0xc (12 decimal).

Entramos al bucle porque 12 <= 62927.

Iteración 1: A = 30, B = 12 + 228 = 240.

Iteración 2: A = 31, B = 240 + 228 = 468.

... y así sucesivamente hasta que B supere 0xf5cf.

Cálculo del número de iteraciones:

Cada iteración suma 228 a B.
Queremos la mayor cantidad de iteraciones n tal que el valor de B antes de la última iteración sea ≤ 62927.
El valor de B después de k iteraciones es: B_k = 12 + 228·k.
Antes de la iteración k+1, B_k debe ser ≤ 62927.
Buscamos el máximo n donde 12 + 228·(n-1) ≤ 62927:

text
228·(n-1) ≤ 62915
n-1 ≤ 62915 / 228 ≈ 275,94
n-1 ≤ 275  →  n ≤ 276
Por tanto, se ejecutan 276 iteraciones.

Valor final de A:

A comienza en 29 y se incrementa en 1 cada iteración:
A_final = 29 + 276 = 305.

Conversión a hexadecimal:

305 decimal → 0x131 (porque 1·256 + 3·16 + 1 = 256 + 48 + 1 = 305).

flag: 0x131
## solución

## solución 2


# referencias

