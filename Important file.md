# Important file
#FORENSICS #MetaRed2022
## Objetivo
	A file with important research has been infected by a virus, you must perform a forensic analysis of the file to find the flag that has been placed on it.
## Solución
Se descarga el archivo, mediante el comando file se descubre que es un documento de word 2007. Se extrae mediante el comando unzip...
```bash
┌──(kali㉿kali)-[~/metared2022/forensic/importantfile]
└─$ unzip Xoloitzcuintle.docx\?token=eyJ1c2VyX2lkIjoxNjIyLCJ0ZWFtX2lkIjo1MDAsImZpbGVfaWQiOjE4fQ.Y09KOQ.CtKPWfsVRa9ertY6XLUPITItjUU    
Archive:  Xoloitzcuintle.docx?token=eyJ1c2VyX2lkIjoxNjIyLCJ0ZWFtX2lkIjo1MDAsImZpbGVfaWQiOjE4fQ.Y09KOQ.CtKPWfsVRa9ertY6XLUPITItjUU
  inflating: docProps/app.xml        
  inflating: docProps/core.xml       
  inflating: word/activeX/activeX1.bin  
  inflating: word/activeX/activeX1.xml  
  inflating: word/activeX/_rels/activeX1.xml.rels  
  inflating: word/document.xml       
  inflating: word/fontTable.xml      
 extracting: word/media/image1.png   
 extracting: word/media/image10.png  
  inflating: word/media/image11.jpg  
  inflating: word/media/image2.wmf   
 extracting: word/media/image3.jpeg  
 extracting: word/media/image4.jpeg  
 extracting: word/media/image5.jpeg  
 extracting: word/media/image6.png   
 extracting: word/media/image7.jpeg  
 extracting: word/media/image8.jpeg  
 extracting: word/media/image9.jpeg  
  inflating: word/numbering.xml      
  inflating: word/settings.xml       
  inflating: word/styles.xml         
  inflating: word/theme/theme1.xml   
  inflating: word/webSettings.xml    
  inflating: word/_rels/document.xml.rels  
  inflating: [Content_Types].xml     
  inflating: _rels/.rels  
```

Al hacer un grep -rl buscando algun archivo o cadena de texto que contuviera la cadena "flag" nos da los siguientes resultados.

```bash
┌──(kali㉿kali)-[~/metared2022/forensic/importantfile]
└─$ grep -rl flag
word/styles.xml
word/media/image11.jpg

```

Buscando en los metadatos de la imagen con el comando exiftool encontramos la bandera.

```bash
┌──(kali㉿kali)-[~/metared2022/forensic/importantfile]
└─$ xxd word/media/image11.jpg | head

00000000: ffd8 ffe0 0010 4a46 4946 0001 0101 0060  ......JFIF.....`
00000010: 0060 0000 ffed 0044 5068 6f74 6f73 686f  .`.....DPhotosho
00000020: 7020 332e 3000 3842 494d 0404 0000 0000  p 3.0.8BIM......
00000030: 0028 1c02 e600 1c66 6c61 674d 587b 4d33  .(.....flagMX{M3
00000040: 7831 6334 6e5f 6834 3172 6c33 3535 5f64  x1c4n_h41rl355_d
00000050: 3067 7d1c 0200 0002 0004 ffdb 0043 0002  0g}..........C..
00000060: 0101 0201 0102 0202 0202 0202 0203 0503  ................
00000070: 0303 0303 0604 0403 0507 0607 0707 0607  ................
00000080: 0708 090b 0908 080a 0807 070a 0d0a 0a0b  ................
00000090: 0c0c 0c0c 0709 0e0f 0d0c 0e0b 0c0c 0cff  ................
                   
```

==flagMX{M3x1c4n_h41rl355_d0g}==
## Notas adicionales

## Referencias
