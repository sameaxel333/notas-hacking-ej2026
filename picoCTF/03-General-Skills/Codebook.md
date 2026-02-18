# Reto: convertme.py

## Descripción


Run the Python script and convert the given number from decimal to binary to get the flag.

## Solución

El script de python contiene la siguiente línea:

```python
if ans_num == num:
    # imrpime la flag
```

Esta es la condición que nos limita si el programa imprime la flag o no. Si la cambiamos:

```python
if True:
    # imprime la flag
```

La flag es mostrada sin importar qué.

mea/OneDrive/Documents/Desktop/carlitos/convertme.py
If 43 is in decimal base, what is it in binary base?
Answer: 101011
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}