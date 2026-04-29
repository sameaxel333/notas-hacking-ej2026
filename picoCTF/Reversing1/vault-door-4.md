# reto
# Descripción
#### Description

This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://challenge-files.picoctf.net/c_fickle_tempest/f587295139ec9c3d23e1299b831596c3243b0e042bec63dd21168e996c0f7c8c/VaultDoor4.java)

# Solución 
## solución
Hay que descargar el programa y después tenemos que modificar el archivo para que se brinque los pasos de validacion del password
```
import java.util.*;

class VaultDoor4 {
    public static void main(String args[]) {
        VaultDoor4 vaultDoor = new VaultDoor4();
        //Scanner scanner = new Scanner(System.in);
        //System.out.print("Enter vault password: ");
        //String userInput = scanner.next();
    //String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
    if (vaultDoor.checkPassword()) {
        System.out.println("Access granted.");
    } else {
        System.out.println("Access denied!");
        }
    }

    // -Minion #7781
    public boolean checkPassword() {
        //byte[] passBytes = password.getBytes();
        byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 0143, 061 ,
            '9' , '4' , 'f' , '7' , '4' , '5' , '8' , 'e' ,
        };
    /*     for (int i=0; i<32; i++) {
            if (passBytes[i] != myBytes[i]) {
                return false;
            }
        } */
        String flag = new String(myBytes);
        System.out.println(flag);
        return true;
    }
}
```
ya en la salida nos da jU5t_4_bUnCh_0f_bYt3s_759600abc3
Access granted. picoCTF{jU5t_4_bUnCh_0f_bYt3s_759600abc3}

## solución 2




# referencias

