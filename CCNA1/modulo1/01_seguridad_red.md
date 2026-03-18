# CCNA1 – Módulo 1: Fundamentos de seguridad de red

## Objetivo
Comprender los conceptos básicos de seguridad de red, identificar amenazas, reconocer vulnerabilidades y aplicar medidas básicas de protección en redes pequeñas.

## Conceptos clave
- Seguridad de red
- Amenazas informáticas
- Vulnerabilidades tecnológicas
- Vulnerabilidades de configuración
- Vulnerabilidades de política
- Seguridad física
- Protección contra ataques
- Solución básica de problemas de red

## Explicación clara

La seguridad de red consiste en proteger dispositivos, servicios, datos y comunicaciones frente a accesos no autorizados, alteraciones o interrupciones.

Una red puede verse afectada por distintos tipos de amenazas, no solo técnicas, sino también físicas y organizacionales. Por eso, la seguridad no depende únicamente de software o firewalls, sino también de buenas configuraciones, políticas internas y control físico del entorno.

## Amenazas principales

### Robo de información
Acceso no autorizado a sistemas o redes para obtener datos confidenciales.

### Manipulación de datos
Alteración o destrucción de información almacenada en sistemas.

### Robo de identidad
Uso indebido de datos personales o credenciales para hacerse pasar por otra persona.

### Interrupción del servicio
Ataques que impiden el acceso legítimo a un sistema o servicio, como un ataque DoS.

## Vulnerabilidades detectadas en el módulo

### Vulnerabilidades tecnológicas
- Protocolos inseguros como HTTP o FTP sin cifrado
- Sistemas operativos con fallos de seguridad
- Routers, switches o firewalls mal protegidos

### Vulnerabilidades de configuración
- Contraseñas débiles
- Configuraciones por defecto
- Servicios mal configurados
- Cuentas inseguras

### Vulnerabilidades de política
- Falta de políticas de seguridad
- Instalación de software no autorizado
- Ausencia de plan de recuperación ante desastres

### Vulnerabilidades físicas
- Daño al hardware
- Problemas ambientales
- Fallos eléctricos
- Mantenimiento deficiente

## Ejemplo real

En una empresa pequeña, un router con usuario y contraseña por defecto puede ser comprometido fácilmente. Si un atacante obtiene acceso al equipo, podría cambiar configuraciones, interceptar tráfico o dejar fuera de servicio la red.

## Medidas de protección

- Cambiar contraseñas predeterminadas
- Usar contraseñas seguras
- Restringir acceso físico a equipos
- Monitorear áreas sensibles
- Implementar cámaras de seguridad
- Mantener políticas internas de seguridad
- Aplicar configuraciones seguras en red

## Comandos y verificación básica

Herramientas comunes de diagnóstico:
- `ping`
- `traceroute`
- `ipconfig`
- `ifconfig`
- `netstat`

Ejemplo:

```bash
ping 8.8.8.8
