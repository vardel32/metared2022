# quemada broadcast
## Objetivo
We have intercepted a broadcast coming from the "La Quemada" in Zacatecas, Mexico. 
It appears to be** grouped in 7 bits bunches**, but we can't decode it. Can you help us to understand what do they trying to tell us? 
La Quemada represents the most important monumental settlement in northern central Mexico for its architecture.

In the place, there is a large hall of columns with its square, a field for the large ball game in the traditional form of “I”, and a pyramidal basement called Votive Pyramid.

Note> 1. run the docker container, instructions below, 2. access app at: http://127.0.0.1:5000

docker run --rm -it --name quemada -p 5000:5000 hackadvisermx/metaredctf-quemada-broadcast

## Solución
Se abre la pagina para poder observar un unico caracter **~**.
Se crea un programa en bash:

```bash
#!/bin/bash

bit=$(curl --s http://127.0.0.1:5000/seq/6bd3e1aa-8c7e-4cf6-94c1-2fbba1eb2f87)
salida='-'
while [ $bit==0 ] || [ $bit==1 ]
do
    echo $salida
    echo \n
    salida=$salida$bit
    bit=$(curl -s http://127.0.0.1:5000/seq/6bd3e1aa-8c7e-4cf6-94c1-2fbba1eb2f87)
done

echo $salida
```
Con el proposito de acceder a la pagina repetidas veces y obtener el siguiente codigo en binario:
*10110101101101111100011010001011010011000001100011011001110010111110101100100100001111000011011000101001010101001100100100011110001101110101101101010001111000110111100110110101000101110100011011001100010100100010000101010110110001101100011000010111001110110101010111100011011110101011010101100001100000111101*

al convertirlo en texto con un tamaño de 7 bytes, se obtiene :
*ZmxhZ01YezdCaXRTdGFuZGFyZEhlbHBVc1BsZWFzZX0=*

y eso, decodificarlo de base64 se optiene la bandera:
**flagMX{7BitStandardHelpUsPlease}**

## Notas adicionales
## Referencias
https://gchq.github.io/CyberChef/
