

# reto
# Descripción
Why search for the flag when I can make a bookmarklet to print it for me?Browse here, and find the flag!

# Solución 
## solución
javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£Ö�ÓÚåÛÑ¢ÕÓ�Ó�Ç¡�¥Ìí";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
        Flag: picoCTF{p@g3_turn3r_1d1ba7e0}
Copee el metodo, lo pege en la consola de inspeccionar elemento y me dio la bandera.
## solución 2




# referencias
