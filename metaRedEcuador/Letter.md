## Problema
the format the flag is: flag{WORDFIND}

The Dad wrote to the oldest son about the loss of the house pet. Using an encryption tool on the web, so that younger siblings don't find out and are affected, so they can enjoy summer vacation.

The Dad told his son that he apparently joined a pack.

## Solución
1. Descargamos el archivo y vemos el contenido.
``` text
Mcnq

W gp kxlhoqu zr hkoz eri zkoz rix ssz koy eskq zuvh. Ch vgys jrbk hjkumzkwtj hu vsguqn icx kws eiz zs ndjk qcz eskq ohos zr toqr g fvgpdorb.

Ch kooz hh kglhoqu lrf gqm thky lb zks yhoxfv.

Ikskug
```

2. Utilizamos el el algoritmo de Vigenere y como palabra clave usamos Dog y obtenemos el sisguiente texto decodificado.
``` text
John

I am writing to tell you that our pet has been lost. We have done everything to search for him but we have not been able to find a champion.

We will be waiting for any news in the search.

Cheers
```

3. La bandera es el nombre del perro que en este caso es Champio, por lo que la bandera es:  flag{CHAMPION}

## Notas
