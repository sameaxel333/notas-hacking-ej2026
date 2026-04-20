# reto
# Descripción
What happens if you have a small exponent? There is a twist though, we padded the plaintext so that (M ** e) is just barely larger than N. Let's decrypt this:

# Solución 
## solución
corremos el script sustituyendo
```
import gmpy2

n = 
c = 

print("Calculando la raíz cúbica de c...")

m, es_exacta = gmpy2.iroot(c, 3)

if es_exacta:
    print("\n¡Raíz cúbica perfecta encontrada!")
    print(f"Mensaje (entero): {m}")
    flag = bytes.fromhex(hex(m)[2:]).decode()
    print(f"FLAG: {flag}")
else:
    print("\nNo se encontró una raíz cúbica perfecta.")
    print("Este ataque (small e) no funcionó.")
```
picoCTF{e_sh0u1d_b3_lArg3r_92f4d5a5}
## solución 2




# referencias

