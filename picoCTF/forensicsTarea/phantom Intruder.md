

# reto
# Descripción
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here Network Traffic PCAP file and try to get the flag.

# Solución 
## solución
```
┌──(kali㉿kali)-[~/picoctf/forensic/phantomIntruder]
└─$ tshark -r myNetworkTraffic.pcap
    1   0.000000  192.168.0.2 → 192.168.1.2  TCP 52 20 → 80 [SYN] Seq=0 Win=8192 Len=12
    2  -0.003973  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
    3  -0.003031  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
    4  -0.001386  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
    5  -0.003505  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
    6  -0.002316  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
    7  -0.000217  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=12
    8  -0.003265  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
    9  -0.002088  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
   10  -0.001618  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
   11   0.000775  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=12
   12  -0.001161  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
   13  -0.000717  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
   14  -0.000942  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
   15   0.000228  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=12
   16   0.000996  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=12
   17  -0.001854  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
   18   0.000558  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=12
   19  -0.002803  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
   20  -0.002544  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
   21   0.001211  192.168.0.2 → 192.168.1.2  TCP 44 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=4
   22  -0.000449  192.168.0.2 → 192.168.1.2  TCP 48 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=8
                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/phantomIntruder]
└─$ tshark -r myNetworkTraffic.pcap -x
0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 05 5b 00 00 65 7a 46 30 58 33 63 30   P. ..[..ezF0X3c0
0030  63 77 3d 3d                                       cw==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 9f 00 00 00 49 2b 7a 6e 43 4a 67 3d   P. .....I+znCJg=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 d6 dc 00 00 2f 39 51 5a 52 74 63 3d   P. ...../9QZRtc=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 a4 17 00 00 75 46 2b 32 55 54 73 3d   P. .....uF+2UTs=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 89 fd 00 00 70 44 57 37 72 6b 49 3d   P. .....pDW7rkI=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 dd dd 00 00 38 65 73 56 4f 4b 34 3d   P. .....8esVOK4=

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 fd 41 00 00 63 47 6c 6a 62 30 4e 55   P. ..A..cGljb0NU
0030  52 67 3d 3d                                       Rg==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 f8 ba 00 00 4b 57 45 68 32 6a 51 3d   P. .....KWEh2jQ=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 0d e2 00 00 42 47 41 56 43 65 38 3d   P. .....BGAVCe8=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 a0 25 00 00 52 41 2b 37 78 46 77 3d   P. ..%..RA+7xFw=

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 1b 1d 00 00 59 6d 68 66 4e 48 4a 66   P. .....YmhfNHJf
0030  5a 41 3d 3d                                       ZA==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 1c eb 00 00 43 4d 45 78 33 34 34 3d   P. .....CMEx344=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 aa 0d 00 00 50 47 62 36 6f 59 41 3d   P. .....PGb6oYA=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 3c e5 00 00 75 53 79 35 72 76 6f 3d   P. .<...uSy5rvo=

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 eb 52 00 00 62 6e 52 66 64 47 67 30   P. ..R..bnRfdGg0
0030  64 41 3d 3d                                       dA==

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 57 90 00 00 4d 54 41 32 4e 54 4d 34   P. .W...MTA2NTM4
0030  4e 41 3d 3d                                       NA==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 80 f3 00 00 78 49 4a 50 62 57 67 3d   P. .....xIJPbWg=

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 f6 5a 00 00 58 7a 4d 30 63 33 6c 66   P. ..Z..XzM0c3lf
0030  64 41 3d 3d                                       dA==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 c6 d8 00 00 6f 44 69 73 35 54 38 3d   P. .....oDis5T8=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 5e fe 00 00 76 32 58 67 6c 4c 73 3d   P. .^...v2XglLs=

0000  45 00 00 2c 00 01 00 00 40 06 f8 76 c0 a8 00 02   E..,....@..v....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 69 97 00 00 66 51 3d 3d               P. .i...fQ==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 8c c8 00 00 53 54 6e 65 65 62 59 3d   P. .....STneebY=

```

YmhfNHJfMg== : bh_4r_2
cGljb0NURg== : picoCTF
fQ== : }
bnRfdGg0dA== : nt_th4t
ZTFmZjA2\Mw== : e1ff063
ezF0X3c0cw== : {1t_w4s 
XzM0c3lfdA== : _34sy_t



picoCTF{1t_w4snt_th4t_34sy_tbh_4r_d1065384}



## solución 2




# referencias

