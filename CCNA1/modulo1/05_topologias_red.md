# CCNA1 – Módulo 1
## Sesión 5: Topologías de red

## Objetivo
Comprender cómo se organizan los dispositivos dentro de una red y cómo esta estructura afecta el flujo de datos, la eficiencia y la seguridad.

---

## Qué es una topología de red

La topología de red es la forma en que los dispositivos están conectados entre sí, tanto físicamente como de manera lógica.

---

## Diagramas de red

Los diagramas de red son representaciones visuales que muestran:

- Dispositivos
- Conexiones
- Estructura de la red

Permiten entender, diseñar y administrar redes de forma eficiente.  

---

## Tipos de topología

Existen dos tipos principales:

### Topología física
Representa cómo están conectados físicamente los dispositivos (cables, ubicación, hardware).

### Topología lógica
Representa cómo fluye la información dentro de la red (rutas, direccionamiento, comunicación).

---

## Topología física

Describe:

- Ubicación de dispositivos
- Conexiones físicas (cables o WiFi)
- Infraestructura real de la red

Incluye elementos como:
- Computadoras
- Switches
- Routers
- Servidores

---

## Topología lógica

Describe:

- Flujo de datos
- Direccionamiento IP
- Rutas de comunicación
- Protocolos utilizados

Permite entender cómo viaja la información dentro de la red.  [oai_citation:1‡Tpologias de redes S5.pdf](sediment://file_00000000991c71f5bbbe420c0cc54c79)

---

## Topologías físicas comunes

### 1. Estrella
Todos los dispositivos se conectan a un punto central.

Ventajas:
- Fácil de administrar
- Fallo de un dispositivo no afecta a los demás

Desventajas:
- Si falla el nodo central, cae toda la red

---

### 2. Bus
Todos los dispositivos comparten un solo cable.

Ventajas:
- Económica
- Simple

Desventajas:
- Fallo del cable afecta toda la red
- Baja escalabilidad

---

### 3. Anillo
Dispositivos conectados en forma circular.

Ventajas:
- Flujo ordenado de datos
- Evita colisiones

Desventajas:
- Fallo en un punto rompe la red

---

### 4. Doble anillo
Versión redundante del anillo.

Ventajas:
- Alta disponibilidad
- Tolerancia a fallos

Desventajas:
- Más compleja
- Mayor costo

---

### 5. Árbol
Estructura jerárquica basada en múltiples estrellas.

Ventajas:
- Escalable
- Buena organización

Desventajas:
- Dependencia de nodos centrales

---

### 6. Malla
Todos los dispositivos están conectados entre sí.

Ventajas:
- Alta redundancia
- Alta confiabilidad

Desventajas:
- Costosa
- Compleja

---

### 7. Jerárquica
Varias estrellas conectadas en niveles.

Ventajas:
- Escalable
- Fácil de administrar

Desventajas:
- Dependencia de nodos superiores

---

### 8. Punto a punto
Conexión directa entre dos dispositivos.

Ventajas:
- Simple
- Rápida

Desventajas:
- No escalable

---

## Importancia de la topología

La topología define:

- Rendimiento de la red
- Escalabilidad
- Tolerancia a fallos
- Facilidad de mantenimiento

---

## Ejemplo práctico

En una empresa:

- Los empleados se conectan a un switch (estrella)
- Los switches se conectan a un router
- El router conecta a Internet

Esto combina varias topologías en una sola red.

---

## Conclusión

Las topologías de red determinan cómo se conectan los dispositivos y cómo circula la información. Elegir la topología adecuada impacta directamente en la eficiencia, seguridad y estabilidad de la red.

---

## Habilidades desarrolladas

- Identificación de topologías
- Interpretación de diagramas de red
- Comprensión del flujo de datos
- Base para diseño de redes
