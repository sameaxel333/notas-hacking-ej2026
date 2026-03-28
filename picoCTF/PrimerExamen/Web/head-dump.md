# Descripción
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.
The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.
Additional details will be available after launching your challenge instance.

# Solución 
## solución
~/Desktop/retos/reto$ wget http://verbal-sleep.picoctf.net:51368/heapdump descargar este archivo 
ile heapdump 
heapdump: ASCII text, with very long lines (64680)
vladi@911:~/Desktop/retos/reto$ strings heapdump | grep picoCTF
picoCTF{Pat!3nt_15_Th3_K3y_dcffa92e}

## solución 2




# referencias
