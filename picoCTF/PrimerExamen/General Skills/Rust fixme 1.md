# reto
# Descripción
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code here.

# Solución 
```                             
┌──(kali㉿kali)-[~/picoctf/examen]
└─$ gunzip fixme1.tar.gz 
                                                                                                                
┌──(kali㉿kali)-[~/picoctf/examen]
└─$ ls           
fixme1.tar  RustFixme1┌──(kali㉿kali)-[~/picoctf/examen]
└─$ ls fixme1.tar   
fixme1.tar                                                      
┌──(kali㉿kali)-[~/picoctf/examen]
└─$ ls RustFixme1 
┌──(kali㉿kali)-[~/picoctf/examen]
└─$ tar xpf fixme1.tar
┌──(kali㉿kali)-[~/picoctf/examen]
└─$ ls           
fixme1  fixme1.tar  RustFixme1
┌──(kali㉿kali)-[~/picoctf/examen]
└─$ ls fixme1    
Cargo.lock  Cargo.toml  src

┌──(kali㉿kali)-[~/picoctf/examen]
└─$ cd fixme1/src                                   
                                
┌──(kali㉿kali)-[~/picoctf/examen/fixme1/src]
└─$ ls        
main.rs

┌──(kali㉿kali)-[~/picoctf/examen/fixme1/src]
└─$ nano main.rs  
                                                                                                                                                                                              
┌──(kali㉿kali)-[~/picoctf/examen/fixme1/src]
└─$ cargo run main
   Compiling rust_proj v0.1.0 (/home/kali/picoctf/examen/fixme1)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.23s
     Running `/home/kali/picoctf/examen/fixme1/target/debug/rust_proj main`
picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}
```
## solución

## solución 2




# referencias

