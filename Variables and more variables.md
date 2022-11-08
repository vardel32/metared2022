# Variables and more variables
#MetaRed2022 #CRYPTO 
## Objetivo
Considere un sistema RSA con p=7, q= 11 and = e=13, encuentre el texto plano correspondiente a c=17. Encuentra el valor de m
## Solución
Para obtener el texto plano (m) se necesitan los siguientes valores:
- n = p * q, 77
- tn = (p-1) * (q-1), 60
- d = e mod inv tn / inverse(e,tn), 37
- m = c^d mod n / pow(c,d,n), 5
## Notas adicionales

## Referencias
