# CCNA1 – Módulo 2 – Sesión 2: Cisco IOS
## Objetivo de la sesión
Comprender los modos de comando de Cisco IOS, cómo identificarlos mediante el prompt y cómo navegar correctamente entre ellos para administrar y configurar dispositivos Cisco.
---
## Conceptos clave
- Cisco IOS
- Modo EXEC usuario
- Modo EXEC privilegiado
- Modo de configuración global
- Modos de subconfiguración
- Prompt
- enable
- disable
- configure terminal
- exit
- end
- line console 0
- line vty 0 15
- interface vlan 1
---
## Explicación simple
Cisco IOS funciona por **niveles o modos** dentro de la línea de comandos.
No todos los comandos sirven en cualquier lugar.  
Primero hay que mirar el **prompt** para saber en qué modo estás.
### Modos principales
- `Router>` → modo EXEC usuario
- `Router#` → modo EXEC privilegiado
- `Router(config)#` → modo de configuración global
- `Router(config-line)#` → modo de configuración de línea
- `Router(config-if)#` → modo de configuración de interfaz
---
## Explicación técnica
### 1. Modo EXEC usuario
Es el modo básico.  
Permite ejecutar comandos limitados, orientados principalmente al monitoreo del dispositivo.
Se identifica por el símbolo:
```text
>

Ejemplos:

Switch>
Router>

En este modo no se pueden hacer cambios de configuración.

⸻

2. Modo EXEC privilegiado

Es el modo con mayores capacidades de administración.
Desde acá se puede:

* inspeccionar más a fondo el dispositivo
* ejecutar pruebas y depuración
* acceder al modo de configuración global

Se identifica por el símbolo:

#

Ejemplos:

Switch#
Router#

Se accede con:

enable

⸻

3. Modo de configuración global

Desde el modo privilegiado, se entra con:

configure terminal

El prompt cambia a:

Router(config)#

Desde este modo se hacen configuraciones generales que afectan al dispositivo completo.

⸻

4. Modos de subconfiguración

Desde configuración global se puede entrar a modos más específicos.

Configuración de línea

Se usa para configurar accesos como consola, Telnet o SSH.

Ejemplo:

line console 0

Prompt:

Router(config-line)#

Otro ejemplo:

line vty 0 15

También lleva a:

Router(config-line)#

Configuración de interfaz

Se usa para configurar una interfaz física o lógica del dispositivo.

Ejemplos:

interface gigabitethernet 0/0/0
interface vlan 1

Prompt:

Router(config-if)#
Switch(config-if)#

⸻

Navegación entre modos

enable

Pasa de:

Router>

a:

Router#

⸻

disable

Pasa de:

Router#

a:

Router>

⸻

configure terminal

Pasa de:

Router#

a:

Router(config)#

⸻

exit

Sirve para salir un nivel.

Ejemplo:

Router(config-if)# → Router(config)#
Router(config-line)# → Router(config)#

⸻

end

Sirve para volver directamente al modo EXEC privilegiado.

Ejemplo:

Router(config-if)# → Router#
Router(config-line)# → Router#

⸻

Modelo mental

> = modo usuario
# = modo privilegiado
(config)# = configuración global
(config-line)# = configuración de líneas
(config-if)# = configuración de interfaz

Mnemotecnia

* enable = subir
* disable = bajar
* exit = salir un piso
* end = ascensor directo a Router#

⸻

Aplicación práctica

Cuando configurás un router o switch en Packet Tracer, seguís esta lógica:

Router> enable
Router# configure terminal
Router(config)# interface gigabitethernet 0/0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown

Esto muestra que:

* primero entrás al modo correcto
* después aplicás el comando correcto en ese nivel

⸻

Diferencias importantes

EXEC usuario vs EXEC privilegiado

* Usuario = acceso limitado
* Privilegiado = acceso amplio, administración avanzada y acceso a configuración

exit vs end

* exit = sube un solo nivel
* end = vuelve directamente a Router#

enable vs configure terminal

* enable = pasa a modo privilegiado
* configure terminal = entra a modo configuración global

⸻

Errores típicos

* Confundir > con #
* No mirar el prompt antes de escribir
* Querer usar ip address fuera de config-if
* Creer que end vuelve a Router>
* Confundir exit con end
* Escribir comandos correctos en el modo equivocado

⸻

Regla de oro

Antes de escribir un comando, mirá el prompt.

El prompt te dice:

* dónde estás
* qué podés hacer
* qué comandos tienen sentido en ese momento

⸻

Resumen final

Cisco IOS trabaja con distintos modos de comando.
Cada modo cumple una función específica.

* Router> = EXEC usuario
* Router# = EXEC privilegiado
* Router(config)# = configuración global
* Router(config-line)# = configuración de líneas
* Router(config-if)# = configuración de interfaz

La lógica operativa correcta es:

1. identificar el prompt
2. entrar al modo correcto
3. ejecutar el comando adecuado
4. salir con exit o end según corresponda

Idea final para recordar

Primero mirás el prompt, después escribís.
