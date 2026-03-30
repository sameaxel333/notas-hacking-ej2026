

# reto
# Descripción
Now you DON’T see me.This report has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?



# Solución 
## solución
```
(kali㉿kali)-[~/picoctf/forensic/redactionGone]
└─$ binwalk Financial_Report_for_ABC_Labs.pdf

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PDF document, version: "1.7"
33166         0x818E          Zlib compressed data, default compression
34716         0x879C          Zlib compressed data, default compression

                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/redactionGone]
└─$ open Financial_Report_for_ABC_Labs.pdf    
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/redactionGone]
└─$ 



```
Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.
Breakdown - Just painted over in MS word.
Cost Benefit Analysis
Credit Debit
This is not the flag, keep looking
Expenses from the
picoCTF{C4n_Y0u_S33_m3_fully}
Redacted document.


## solución 2




# referencias

  