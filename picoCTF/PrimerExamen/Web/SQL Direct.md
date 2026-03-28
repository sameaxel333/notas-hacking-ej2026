

# reto
# Descripción
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.

# Solución 
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 49653 -U postgres pico
Password for user postgres: 
                                                                                          
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 49653 -U postgres pico
Password for user postgres: 
psql: error: connection to server at "saturn.picoctf.net" (13.59.203.175), port 49653 failed: FATAL:  password authentication failed for user "postgres"
                                                                                          
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 49653 -U postgres pico
Password for user postgres: 
psql (18.1 (Debian 18.1-1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# help
You are using psql, the command-line interface to PostgreSQL.
Type:  \copyright for distribution terms
       \h for help with SQL commands
       \? for help with psql commands
       \g or terminate with semicolon to execute query
       \q to quit
pico=# /d
pico-# \d
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico-# select * from flags;
ERROR:  syntax error at or near "/"
LINE 1: /d
        ^
pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# 

## solución

## solución 2




# referencias
