# La enchilada
#MetaRed2022 #misc
## Objetivo
When a communication protocol is used that does not encrypt the information, it travels in plain text, putting the information at risk. Can you find the flag of this enchilada?
## Solución
Se da una captura de paquetes, buscando la palabra enchilada se encuentra un rastro de paquetes que poseen las siguientes características.
![[Pasted image 20221018211746.png]]
La linea resaltada en azul y letra blanca parece ser algún texto cifrado.
Al ponerlo en cyberchef podemos observar que se trata de un texto en base 64.
![[Pasted image 20221018211842.png]]
==flagMX{Ench1ladaR0jayVerd3}==
## Notas adicionales

## Referencias
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Wm14aFowMVllMFZ1WTJneGJHRmtZVkl3YW1GNVZtVnlaRE45Q2c9PQ