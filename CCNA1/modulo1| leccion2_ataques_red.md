# CCNA1 – Módulo 1
## Ataques a la red

## Objetivo
Comprender los principales tipos de ataques informáticos que pueden afectar una red, incluyendo malware, ataques de reconocimiento, ataques de acceso y ataques de denegación de servicio.

## Conceptos clave

- Malware
- Virus
- Gusanos
- Troyanos
- Ataques de reconocimiento
- Barrido de ping
- Escaneo de puertos
- Ataques de acceso
- Man-in-the-Middle
- DoS
- DDoS

## Tipos de malware

El malware es software malicioso diseñado para dañar sistemas, robar información o comprometer la integridad de los datos.

### Virus
Un virus es un tipo de malware que se inserta dentro de un programa o archivo ejecutable y necesita que el usuario lo ejecute para activarse.

Puede:
- modificar software
- dañar archivos
- provocar interrupciones del sistema

### Gusanos
Los gusanos son malware autónomo. No necesitan un archivo host para propagarse.

Características:
- explotan vulnerabilidades del sistema
- se propagan automáticamente por la red
- no requieren interacción humana

### Troyanos
Un troyano es un malware que se disfraza como software legítimo para engañar al usuario.

A diferencia de virus o gusanos:
- no se replica
- engaña al usuario para ser ejecutado

## Diferencias clave entre malware

| Tipo | Característica principal |
|------|---------------------------|
| Virus | Necesita ejecutarse dentro de un programa |
| Gusano | Se propaga automáticamente por la red |
| Troyano | Se disfraza de software legítimo |

## Ataques de reconocimiento

Son la fase inicial de un ciberataque, donde el atacante recopila información sobre la red objetivo.

El objetivo es identificar:
- sistemas activos
- servicios disponibles
- vulnerabilidades

Principales técnicas:
- consultas en Internet
- barrido de ping
- escaneo de puertos

### Consultas en Internet
El atacante busca información pública del objetivo usando motores de búsqueda, sitios web y registros WHOIS.

### Barrido de ping
Se utiliza para descubrir qué direcciones IP están activas en una red.

Ejemplo:
El atacante envía solicitudes ping a un rango de IP para detectar dispositivos activos.

### Escaneo de puertos
El atacante analiza qué servicios están disponibles en un sistema.

Herramientas utilizadas:
- Nmap
- Masscan

Esto permite identificar servicios como:
- SSH
- DNS
- HTTP

## Ataques de acceso

Los ataques de acceso buscan obtener acceso no autorizado a sistemas o datos sensibles explotando vulnerabilidades.

Tipos principales:
- ataques de contraseña
- explotación de confianza
- redirección de puertos
- ataque Man-in-the-Middle

### Ataques de contraseña
El atacante intenta descubrir contraseñas mediante:

#### Fuerza bruta
Prueba todas las combinaciones posibles.

#### Ataque de diccionario
Usa listas de contraseñas comunes.

### Explotación de confianza
Un atacante aprovecha relaciones de confianza entre sistemas o usuarios para obtener acceso.

Ejemplo:
Un empleado con credenciales legítimas roba información sensible.

### Redirección de puertos
Un atacante utiliza un sistema comprometido como punto intermedio para atacar otros sistemas de la red.

### Man-in-the-Middle
El atacante se interpone entre dos sistemas que se comunican y puede:
- interceptar datos
- leer información
- modificar la comunicación

## Ataques de denegación de servicio

Los ataques DoS y DDoS buscan interrumpir el acceso a un servicio saturando el sistema con tráfico malicioso.

### DoS
Un solo sistema genera grandes cantidades de solicitudes para saturar un servidor.

Impacto:
- interrupción del servicio
- pérdida de disponibilidad

### DDoS
Un ataque distribuido utiliza múltiples dispositivos comprometidos para enviar tráfico al objetivo.

Impacto:
- caída de sitios web
- pérdidas económicas
- daño reputacional

## Conclusión

Los ataques a la red pueden tomar muchas formas, desde malware hasta ataques distribuidos que saturan servicios. Comprender estos ataques permite identificar riesgos y aplicar medidas de seguridad adecuadas en la infraestructura de red.

## Habilidades trabajadas

- Identificación de malware
- Comprensión de ataques de reconocimiento
- Comprensión de ataques de acceso
- Diferenciación entre DoS y DDoS
- Documentación técnica en Markdown
