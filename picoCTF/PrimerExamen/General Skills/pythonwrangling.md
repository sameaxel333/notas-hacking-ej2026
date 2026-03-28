

# reto
# Descripción

# Solución 
Python scripts are invoked kind of like programs in the Terminal...
Can you run ende.py using password.txt to get flag.txt.en?
## solución
kali-kali@:~/Desktop/retos/reto$ ls
ende.py  flag.txt.en  password.txt
kali-kali@:~/Desktop/retos/reto$ python3 ende.py 
Usage: ende.py (-e/-d) [file]
kali-kali@:~/Desktop/retos/reto$ cat password.txt 
720b6ad346f84cd483c60c7464dd95d4
kali-kali@:~/Desktop/retos/reto$ python3 ende.py -d flag.txt.en 
Please enter the password:720b6ad346f84cd483c60c7464dd95d4
picoCTF{4p0110_1n_7h3_h0us3_9c5f9bcf}

## solución 2




# referencias

