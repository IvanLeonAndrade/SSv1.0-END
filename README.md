# Sistema de Sensado Versión 1.0 (SSv1.0)

**Copyright (C) 2023  Iván León Andrade Franco**  
**Empresa:** Silica Networks SA

**Mail Personal:** ivan.batapum@gmail.com  
**Mail Coorporativo:** Ivan.Andrade@datco.net

## Descripción:
El equipo sensa temperatura, humedad y corriente continua. Los valores se obtienen mediante SNMP V1.0. Hecho con Arduino Nano, PCB en KICAD y diseño de la caja en SolidWorks.

## Configuración del código

IP e informacion del dispositivo:
En IP establecer las direcciones IP correspondientes. La IP del DNS no es necesario cambiar, dejar por defecto. En
informacion del equipo: En location indicar la zona donde opera la Base (Los tecnicos)
y en Shelter el nombre del sitio. Se debe ingresar el ancho del
vector igual a la cantidad de numero de letras + 1.

```c
IPAddress ip(192, 168, 0, 95);
IPAddress ip_dns(192, 168, 1, 1);
IPAddress ip_gateway(192, 168, 0, 1);
IPAddress subnet(255, 255, 255, 0);

static char locShelter[7] = "Abasto";
static char locLocation[5] = "AMBA";
```

## Verificar Programa

Se deben importar librerias y drivers USB. En libs-zip se encuentran las librerías (y las dependencias) que no están por defecto en el IDE de Arduino. Tienen formato .zip para poder 
importarlas desde el IDE. Algunas librerías se pueden descargar en el IDE pero otras no. Las que están por defecto en el IDE son SPI y Ethernet. 

Tambien en la carpeta principal "libraries-SSv1.0" se encuentra un archivo .zip llamado CH341SER. Este es el driver USB para poder subir el programa al Arduino Nano. Se debe descomprimir y ejecutar el instalador. Dependiendo del Arduino Nano, puede cargar el programa con el Bootloader viejo o nuevo.


En el Link https://www.ireasoning.com/downloadmibbrowserfree.php descargar el MIB Browers. En este programa se ingresa la IP del equipo y el OID para obtener el valor obtenido
por los sensores o las descripciones del equipo definidas.
