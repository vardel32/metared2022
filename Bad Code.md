# Bad Code
#MetaRed2022 #GeneralSkills 
## Objetivo
help us review this code in this [file](https://drive.google.com/file/d/1gLEsMvKICvOyu1DsnKGLiKWujdbgYeIz/view?usp=sharing)
## Solución
La consola indica que la identación del archivo es incorrecta.
```bash
┌──(root㉿kali)-[/home/kali/metared2022]
└─# python3 badcode.py 
  File "/home/kali/metared2022/badcode.py", line 13
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
                                                                                                         ^
IndentationError: unindent does not match any outer indentation level

```

Al corregir la identación del programa y eliminar un par de errores de sintaxis se puede obtener la badnera.

```bash
┌──(root㉿kali)-[/home/kali/metared2022]
└─# python3 badcode.py
That is correct! Here's your flag: dOcpE$9.QM9TEiam

```

## Notas adicionales

## Referencias
