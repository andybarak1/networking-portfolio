# CCNA1 – Módulo 2 – Sesión 3: Estructura de comandos en Cisco IOS

## Objetivo de la sesión
Comprender cómo se construyen los comandos en Cisco IOS, cómo interpretar su sintaxis, cómo leer correctamente el prompt y cómo utilizar la ayuda contextual y los atajos de la CLI para trabajar con mayor precisión y eficiencia.

---

## Qué me quiere enseñar esta sesión
Esta sesión busca que pueda entender que en Cisco IOS no alcanza con “saber comandos”. También tengo que entender:

- en qué modo estoy
- qué acción quiero ejecutar
- qué argumento necesita el comando
- cómo leer la sintaxis de la documentación
- cómo usar la ayuda de IOS cuando no recuerdo algo
- cómo detectar errores de escritura o sintaxis

---

## Conceptos clave
- Prompt
- Comando
- Argumento
- Estructura de comandos
- Estructura jerárquica de Cisco IOS
- User EXEC
- Privileged EXEC
- Global Configuration
- Interface Configuration
- Line Configuration
- Ayuda contextual
- Verificación de sintaxis
- Atajos de teclado en CLI

---

## Explicación simple

En Cisco IOS, un comando no se escribe al azar.  
Siempre tiene una estructura.

La estructura básica es esta:

```text
[Prompt] comando argumento
````

### ¿Qué significa cada parte?

* **Prompt**: me dice dónde estoy dentro del sistema
* **Comando**: es la acción que quiero hacer
* **Argumento**: es el dato que necesita el comando para funcionar

### Ejemplo simple

```text
Router# ping 10.0.0.1
```

Acá:

* `Router#` = prompt
* `ping` = comando
* `10.0.0.1` = argumento

### Idea clave

No se escribe “porque sí”.
Primero miro el prompt, después elijo el comando y por último agrego el argumento que hace falta.

---

## Explicación técnica

### 1. Prompt

El **prompt** es el indicador que aparece en la línea de comandos y muestra el modo en el que me encuentro dentro de Cisco IOS.

Ejemplos:

```text
Router>
Router#
Router(config)#
Router(config-if)#
Router(config-line)#
```

Cada uno representa un nivel distinto y define qué comandos tienen sentido ahí.

### 2. Comando

El **comando** es la palabra clave que le indica al dispositivo qué acción realizar.

Ejemplos:

```text
ping
show
enable
configure terminal
```

### 3. Argumento

El **argumento** es el valor específico que completa el comando.

Ejemplo:

```text
ping 192.168.1.1
```

* comando = `ping`
* argumento = `192.168.1.1`

### Conclusión técnica

La estructura de un comando en IOS depende de tres elementos:

* el contexto en que estoy
* la acción que quiero ejecutar
* el dato que necesita esa acción

---

## Estructura jerárquica de Cisco IOS

Cisco IOS trabaja en forma jerárquica.
Eso significa que no todos los comandos se pueden usar en todos los niveles.

### Modos principales

#### 1. User EXEC

Prompt:

```text
Router>
```

Es el modo más básico.
Sirve para observación simple y algunos comandos limitados.

#### 2. Privileged EXEC

Prompt:

```text
Router#
```

Es el modo con más control operativo.
Desde acá se puede administrar mejor el dispositivo y entrar a configuración.

#### 3. Global Configuration

Prompt:

```text
Router(config)#
```

Se usa para configuraciones generales del dispositivo.

#### 4. Interface Configuration

Prompt:

```text
Router(config-if)#
```

Se usa para configurar una interfaz específica.

#### 5. Line Configuration

Prompt:

```text
Router(config-line)#
```

Se usa para configurar líneas de acceso como consola, Telnet o SSH.

#### 6. Router Configuration

Prompt:

```text
Router(config-router)#
```

Se usa para configurar protocolos de routing como RIP, OSPF, EIGRP, etc.

---

## Explicación pedagógica de la jerarquía

Pensalo como un edificio:

* `Router>` = hall de entrada
* `Router#` = sala de control
* `Router(config)#` = taller principal
* `Router(config-if)#` = puerta específica del edificio
* `Router(config-line)#` = acceso de entrada/salida
* `Router(config-router)#` = sala de protocolos

### Regla clave

No todo se puede hacer desde cualquier piso.
Cada piso tiene sus herramientas.

---

## Cómo leer la sintaxis de un comando

La documentación de Cisco usa símbolos y formatos especiales.
Si no los entiendo, me pierdo.

### 1. Texto en negrita

Significa: lo escribo exactamente así.

Ejemplo:

```text
ping
```

No lo invento ni lo cambio.

---

### 2. Texto en cursiva

Significa: acá tengo que reemplazar eso por un valor real.

Ejemplo:

```text
ping [ip_address]
```

No escribo literalmente `ip_address`, sino algo como:

```text
ping 192.168.1.1
```

---

### 3. Corchetes `[ ]`

Significan: opcional.

Ejemplo:

```text
show interface [interface_name]
```

Eso quiere decir que puedo:

* poner una interfaz específica
* o no poner nada y ver todas

---

### 4. Llaves `{ }`

Significan: obligatorio.

Ejemplo:

```text
interface {gigabitethernet | fastethernet} [interface_number]
```

Tengo que elegir sí o sí una opción entre las que están dentro de las llaves.

---

### 5. Barra vertical `|`

Significa: “o”.

Ejemplo:

```text
{permit | deny}
```

Debo elegir una de las opciones.

---

## Resumen de sintaxis

* `[ ]` = opcional
* `{ }` = obligatorio
* `|` = una opción entre varias
* cursiva = valor variable
* negrita = escribir exacto

---

## Ayuda contextual de IOS

Cisco IOS tiene ayuda incorporada.
No siempre hace falta memorizar todo.

### Signo `?`

Sirve para:

* ver comandos disponibles
* ver qué opciones hay
* ver qué argumento falta
* explorar la sintaxis correcta

### Ejemplo

```text
Router# show ?
```

Esto muestra qué se puede escribir después de `show`.

---

## Tipos de mensajes que puedo ver

### 1. Comando incompleto

```text
% Incomplete command.
```

Significa que el comando existe, pero todavía le falta algo.

### 2. Entrada inválida

```text
% Invalid input detected at '^' marker.
```

Significa que escribí algo incorrecto y el símbolo `^` me marca dónde detectó el problema.

---

## Ejemplo explicado de ayuda contextual

Secuencia tipo:

```text
Cisco# clock ?
Cisco# clock set
% Incomplete command.
Cisco# clock set ?
Cisco# clock set 19:50:00
% Incomplete command.
Cisco# clock set 19:50:00 ?
Cisco# clock set 19:50:00 25 6
                  ^
Invalid input detected at '^' marker.
```

### ¿Qué me enseña esto?

* que `?` me ayuda a completar
* que “incomplete command” significa que voy bien, pero falta algo
* que `^` marca el punto del error
* que IOS no solo ejecuta, también guía

---

## Atajos de teclado útiles en la CLI

### Tab

Autocompleta comandos parciales.

Ejemplo:

```text
sh + Tab = show
```

### Backspace

Borra el carácter a la izquierda del cursor.

### Ctrl + D

Borra el carácter debajo del cursor.

### Ctrl + K

Borra desde el cursor hasta el final de la línea.

### Ctrl + W

Borra la palabra a la izquierda del cursor.

### Flechas

Permiten mover el cursor y editar.

### Ctrl + A

Lleva al inicio de la línea.

### Ctrl + E

Lleva al final de la línea.

### Ctrl + Shift + 6

Interrumpe un proceso.

---

## Aplicación práctica real

### Ejemplo 1

```text
Router# ping 10.0.0.1
```

* prompt = `Router#`
* comando = `ping`
* argumento = `10.0.0.1`

### Ejemplo 2

```text
Router(config)# interface gigabitethernet 0/0/0
```

* prompt = `Router(config)#`
* comando = `interface`
* argumento = `gigabitethernet 0/0/0`

### Ejemplo 3

```text
Router(config-if)# ip address 192.168.1.1 255.255.255.0
```

* prompt = `Router(config-if)#`
* comando = `ip address`
* argumentos = `192.168.1.1 255.255.255.0`

---

## Cómo se conecta esto con Packet Tracer

Cuando configuré un router en Packet Tracer y escribí algo como:

```text
Router> enable
Router# configure terminal
Router(config)# interface gigabitethernet 0/0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown
```

ya estaba aplicando esta teoría.

Eso demuestra que esta sesión no es solo teoría:

* me ayuda a leer mejor la CLI
* me ayuda a no equivocarme de modo
* me ayuda a entender por qué un comando a veces falla

---

## Modelo mental

### Fórmula principal

```text
Prompt = dónde estoy
Comando = qué hago
Argumento = con qué lo hago
```

### Otra fórmula útil

```text
No escribo a ciegas.
Primero leo el prompt.
Después elijo el comando.
Después agrego el argumento.
```

---

## Mnemotecnia

### Para estructura de comando

```text
Contexto → Acción → Detalle
```

### Para símbolos

```text
[ ] = opcional
{ } = obligatorio
| = o
? = ayuda
^ = error
```

---

## Errores típicos

* escribir sin mirar el prompt
* confundir prompt con comando
* confundir comando con argumento
* creer que `[ ]` significa obligatorio
* no usar `?` cuando no sé cómo sigue
* ver `^` y no revisar dónde está el error
* intentar usar comandos correctos en el modo equivocado

---

## Troubleshooting de esta sesión

### Si un comando falla, me pregunto:

1. ¿Estoy en el prompt correcto?
2. ¿El comando está bien escrito?
3. ¿Le falta algún argumento?
4. ¿Estoy respetando la sintaxis?
5. ¿Puedo usar `?` para descubrir qué sigue?

### Traducción simple

Troubleshooting acá no es “romperme la cabeza”.
Es leer las pistas que IOS ya me da:

* prompt
* `?`
* `% Incomplete command`
* `^`

---

## Regla de oro

Antes de escribir un comando, miro el prompt.
Después veo si necesito argumento.
Y si no estoy seguro, uso `?`.

---

## Resumen final

La estructura de comandos en Cisco IOS se basa en tres partes:

* prompt
* comando
* argumento

Además, la CLI usa una sintaxis específica que hay que saber interpretar:

* `[ ]` = opcional
* `{ }` = obligatorio
* `|` = elegir una opción
* `?` = ayuda contextual
* `^` = punto donde se detectó el error

Comprender esto me permite:

* escribir mejor los comandos
* entender los errores
* usar la ayuda de IOS
* moverme con más seguridad en Packet Tracer y en CLI real

Prompt = dónde estoy
Comando = qué hago
Argumento = con qué lo hago
```

```
```
