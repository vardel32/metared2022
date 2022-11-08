# Get your flag
#MetaRed2022 #FORENSICS 
## Objetivo
Through tools look for the flag in this [binary](https://drive.google.com/file/d/1YFNZwSLOduHnaJnvtUE5k9FkmQY6J7Nl/view?usp=sharing)
## Solución
Primeramente se observa que es un archivo binario y que es ejecutable. Se le dan los permisos adecuados para que pueda ser ejecutado y se obtiene la bandera.

```bash
┌──(root㉿kali)-[/home/kali/metared2022]
└─# chmod 555 /home/kali/metared2022/b1n@ri0
                                                                            
┌──(root㉿kali)-[/home/kali/metared2022]
└─# ./b1n@ri0                               
Hello user! Pass me a -h to learn what I can do!
                                                                            
┌──(root㉿kali)-[/home/kali/metared2022]
└─# ./b1n@ri0 -h
Oh, help? I actually don't do much, but I do have this flag here: flag{T3@m_H3rE_1s_yU0r_Fl@G_XD}"@@@@@

```
## Notas adicionales
chmod 555 ruta/de/Archivo 
le proporciona al archivo los permisos de lectura y ejecución para grupo, propietario y otros.

0 = --- = sin acceso
1 = --x = ejecución
2 = -w- = escritura
3 = -wx = escritura y ejecución
4 = r-- = lectura
5 = r-x = lectura y ejecución
6 = rw- = lectura y escritura
7 = rwx = lectura, escritura y ejecución

## Referencias
