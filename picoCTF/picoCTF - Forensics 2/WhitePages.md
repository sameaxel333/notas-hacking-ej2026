# reto
# Descripción
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.picoctf.net/c_fickle_tempest/ab5453de03105a8aab9c68b0b46e66a4fe0a781c3915ab519f7fab31b3ce6894/whitepages.txt) is all blank!

# Solución 
## solución
sed 's/\xe2\x80\x83/0/g' whitepages.txt
sed 's/\xe2\x80\x83/0/g' whitepages.txt | sed 's/\x20/1/g'

utilizamos esto despues de descargarlo 
## solución 2




# referencias

