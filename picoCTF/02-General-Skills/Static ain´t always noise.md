
# Descripción
Can you look at the data in this binary? The bash script might help!

# Solución 
## solución
```

sameaxel33-picoctf@webshell:~$ ./ltdis.sh
-bash: ./ltdis.sh: Permission denied
sameaxel33-picoctf@webshell:~$ chmod +x ltdis.sh
sameaxel33-picoctf@webshell:~$ ./ltdis.sh
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
sameaxel33-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
sameaxel33-picoctf@webshell:~$ string static | grep pico
-bash: string: command not found
sameaxel33-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_20335e41}
sameaxel33-picoctf@webshell:~$ 
```
picoCTF{d15a5m_t34s3r_20335e41}

## solución 2




# referencias
