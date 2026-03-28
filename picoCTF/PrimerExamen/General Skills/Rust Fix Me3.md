

# reto
# Descripción
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code here.

# Solución 
## solución
```
                                                                                                             
┌──(kali㉿kali)-[~/…/examen/fixme2/fixme2/fixme3]
└─$ gunzip fixme3.tar.gz 
                                                                                                             
┌──(kali㉿kali)-[~/…/examen/fixme2/fixme2/fixme3]
└─$ tar xpf fixme3.tar      
                                                                                                             
┌──(kali㉿kali)-[~/…/examen/fixme2/fixme2/fixme3]
└─$ ls 
fixme3  fixme3.tar
                                                                                                             
┌──(kali㉿kali)-[~/…/examen/fixme2/fixme2/fixme3]
└─$ cd fixme3
                                                                                                             
┌──(kali㉿kali)-[~/…/fixme2/fixme2/fixme3/fixme3]
└─$ ls 
Cargo.lock  Cargo.toml  src
                                                                                                             
┌──(kali㉿kali)-[~/…/fixme2/fixme2/fixme3/fixme3]
└─$ cd src   

```
error[E0133]: call to unsafe function `std::slice::from_raw_parts` is unsafe and requires unsafe function or block
  --> src/main.rs:31:31
   |
31 |         let decrypted_slice = std::slice::from_raw_parts(decrypted_ptr, decrypted_len);
   |                               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ call to unsafe function
   |
   = note: consult the function's documentation for information on how to avoid undefined behavior

For more information about this error, try `rustc --explain E0133`.
error: could not compile `rust_proj` (bin "rust_proj") due to 1 previous error

vladi@911:~/Desktop/retos/reto/fixme3/src$ nano main.rs 
vladi@911:~/Desktop/retos/reto/fixme3/src$ cargo run main
   Compiling rust_proj v0.1.0 (/home/vladi/Desktop/retos/reto/fixme3)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.10s
     Running `/home/vladi/Desktop/retos/reto/fixme3/target/debug/rust_proj main`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{n0w_y0uv3_f1x3d_1h3m_411}

## solución 2




# referencias