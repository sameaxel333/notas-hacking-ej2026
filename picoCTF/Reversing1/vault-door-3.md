

# reto
# Descripción

This vault uses for-loops and byte arrays. The source code for this vault is here: VaultDoor3.java

# Solución 
## solución
```
import java.util.*;

class VaultDoor3 {
    public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
        String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
        if (vaultDoor.checkPassword(input)) {
            System.out.println("Access granted.");
        } else {
            System.out.println("Access denied!");
        }
    }

    // Our security monitoring team has noticed some intrusions on some of the
    // less secure doors. Dr. Evil has asked me specifically to build a stronger
    // vault door to protect his Doomsday plans. I just *know* this door will
    // keep all of those nosy agents out of our business. Mwa ha!
    //
    // -Minion #2671
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        return s.equals("jU5t_a_sna_3lpm11g54e_u_4_m4r042");
    }
}                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ nano flag 
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ nano flag
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ nano flag
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ javac flag         
error: Class names, 'flag', are only accepted if annotation processing is explicitly requested
1 error
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ java flag  
Error: Could not find or load main class flag
Caused by: java.lang.ClassNotFoundException: flag
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ nano VaultDoor3           
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ cat VaultDoor3.java 
import java.util.*;

class VaultDoor3 {
    public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
        String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
        if (vaultDoor.checkPassword(input)) {
            System.out.println("Access granted.");
        } else {
            System.out.println("Access denied!");
        }
    }

    // Our security monitoring team has noticed some intrusions on some of the
    // less secure doors. Dr. Evil has asked me specifically to build a stronger
    // vault door to protect his Doomsday plans. I just *know* this door will
    // keep all of those nosy agents out of our business. Mwa ha!
    //
    // -Minion #2671
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        return s.equals("jU5t_a_sna_3lpm11g54e_u_4_m4r042");
    }
}                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ nano VaultDoor3      
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ javac VaultDoor3      
error: Class names, 'VaultDoor3', are only accepted if annotation processing is explicitly requested
1 error
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ nano VaultDoor3.java
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ javac VaultDoor3.java
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ java VaultDoor3.java 
Enter vault password: jU5t_a_sna_3lpm11g54e_u_4_m4r042
Access denied!
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ java VaultDoor3.java
Enter vault password: jU5t_a_sna_3lpm11g54e_u_4_m4r042
Access denied!
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ nano VaultDoor3.java 
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ nano VaultDoor3.java
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ java VaultDoor3.java
Enter vault password: jU5t_a_sna_3lpm11g54e_u_4_m4r042
Access denied!
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ javac VaultDoor3.java
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ java VaultDoor3.java 
Enter vault password: jU5t_a_sna_3lpm11g54e_u_4_m4r042
Access denied!
}                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ nano VaultDoor3.java 
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ javac VaultDoor3.java
                                                                                          
┌──(kali㉿kali)-[~/picoctf/reversing/vaultdoorTraining3]
└─$ java VaultDoor3.java 
Enter vault password: picoCTF{jU5t_a_sna_3lpm11g54e_u_4_m4r042}
jU5t_a_s1mpl3_an4gr4m_4_u_e45012
Access denied!

```
jU5t_a_s1mpl3_an4gr4m_4_u_e45012
Access denied!


## solución 2




# referencias

