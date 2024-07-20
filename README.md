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

Para verificar el programa importar todas las liberias en el IDE de arduino manualmente desde la carpeta lib-zip. En
la carpeta libreries se encuentra un archivo CH341SER, esto es el driver USB para cargar el codigo al Arduino Nano.
