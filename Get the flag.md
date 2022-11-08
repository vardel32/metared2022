# Get the flag
#MetaRed2022 #GeneralSkills 
## Objetivo
Inside this [file](https://drive.google.com/file/d/1HpgZluYnta1YEmYLaWGG6C5evIay9Upv/view?usp=sharing) find the flag
## Solución
Se observa que es un archivo de texto bastante grande.

```bash
┌──(root㉿kali)-[/home/kali/metared2022]
└─# file quinua 
quinua: ASCII text, with very long lines (4200)

```

Mediante el comando grep se puede encontrar la bandera.

```bash
┌──(root㉿kali)-[/home/kali/metared2022]
└─# cat quinua| grep flag
.cP5$er?y:H6Z9N]p3,XhB!;4.5.l.3Yv8tkz?!e#r5BlPT4167z_bCcQH<9G=0fBDVx=|BN flag{grep_is_a_good_tool}

```

## Notas adicionales

## Referencias
