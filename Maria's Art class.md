## Descripción
For María’s art class the teacher ask for a MASTERPIECE that combains history and feelings, so María decided to créate a painting that describes an event in history close to her heart and her roots. She decided to paint a piece of Yucatán that everyone can relate to, so she paint the kukulkan pirámide. María says that she hide a Little message in the painting but I guess the teacher never find it because María got an F. Help María to pass de class, find the message and send it to the teacher:3

## Solución
1. Descargamos el archivo.
2. Aplicamos strings a la imagen y filtramos por flag.
``` bash
strings KUKULKAN.jpg\?token=eyJ1c2VyX2lkIjoxODg0LCJ0ZWFtX2lkIjo1MDAsImZpbGVfaWQiOjh9.Y09ECw.T-pMG57Jzxkfb_QLVgTTeD2SLQ8 | grep FLAG
_I LOVE FLAGS :3 
.MY FAVOURITE WORD IS FLAG 
THIS IS NOT THE FLAG, KEEP LOOKING BRO! 
/ FLAG Un PAso mas  BRO{Vm0weGQxTnRVWGxXYTFwUFZsZG9WRmxVU2xOalJsSlZVMnhPVlUxV2NEQlVWbEpUWVdzeFYxTnNhRmRpVkZaUVZrUktTMUl5VGtsaVJtUk9ZbTFvZVZadE1YcGxSbGw0Vkc1V2FsSnNXazlXYlRWRFYxWmFkR1JIUmxSTlZYQjVWR3hhYjFSc1duTmpSVGxhWWxoU1RGWnNXbUZXVmtaMFVteHdWMkpJUWpaV1ZFa3hWREZhV0ZOclpHcFNWR3hZV1ZSS1VrMUdWWGRYYlVacVZtdHdlbGRyV210VWJGcDFVV3R3VjJGcmJ6QlZla1pYVmpGa2NsWnNTbGRTTTAwMQ==}   x
```
3. Desencriptamos usando base64 y obtenemos. `Vm0xd1NtUXlWa1pPVldoVFlUSlNjRlJVU2xOVU1WcDBUVlJTYWsxV1NsaFdiVFZQVkRKS1IyTkliRmROYm1oeVZtMXplRll4VG5WalJsWk9WbTVDV1ZadGRHRlRNVXB5VGxab1RsWnNjRTlaYlhSTFZsWmFWVkZ0UmxwV2JIQjZWVEkxVDFaWFNrZGpSVGxYWVRKUk1GVXdXbUZqVmtweldrWmtUbFp1UWtwV2FrbzBVekZXVjFkclZsSldSM001`
4. Volvemos a desencriptar usando base 64  `Vm1wSmQyVkZOVWhTYTJScFRUSlNUMVp0TVRSak1WSlhWbTVPVDJKR2NIbFdNbmhyVm1zeFYxTnVjRlZOVm5CWVZtdGFTMUpyTlZoTlZscE9ZbXRLVlZaVVFtRlpWbHB6VTI1T1ZXSkdjRTlXYTJRMFUwWmFjVkpzWkZkTlZuQkpWako0UzFWV1drVlJWR3M5`
5. Volvemos a aplicar desencripción en base 64 y obtenemos `VmpJd2VFNUhSa2RpTTJST1ZtMTRjMVJXVm5OT2JGcHlWMnhrVmsxV1NucFVNVnBYVmtaS1JrNVhNVlpOYmtKVVZUQmFZVlpzU25OVWJGcE9Wa2Q0U0ZacVJsZFdNVnBJVjJ4S1VWWkVRVGs9`
6. Volvemos a aplicar desencripción en base 64 y obtenemos  `VjIweE5HRkdiM2ROVm14c1RWVnNObFpyV2xkVk1WSnpUMVpXVkZKRk5XMVZNbkJUVTBaYVZsSnNUbFpOVkd4SFZqRldWMVpIV2xKUVZEQTk=`
7. Volvemos a aplicar desencripción en base 64 y obtenemos `V20xNGFGb3dNVmxsTVVsNlZrWldVMVJzT1ZWVFJFNW1VMnBTU0ZaVlJsTlZNVGxHVjFWV1ZHWlJQVDA9`
8. Volvemos a aplicar desencripción en base 64 y obtenemos `Wm14aFowMVllMUl6VkZWU1RsOVVTRE5mU2pSSFZVRlNVMTlGV1VWVGZRPT0=`
9. Volvemos a aplicar desencripción en base 64 y obtenemos `ZmxhZ01Ye1IzVFVSTl9USDNfSjRHVUFSU19FWUVTfQ==`
10. Volvemos a aplicar desencripción en base 64 y obtenemos la bandera que es `flagMX{R3TURN_TH3_J4GUARS_EYES}`


## Notas
