
---
## 🔷 `Area2D`

> Nodo ideal para detectar colisiones o zonas de interacción sin aplicar física real.

- Usos comunes:
  - Detectar entrada/salida de objetos
  - Ítems que se pueden recoger (como monedas)
  - Zonas de daño o activación

- Suele ir acompañado de:
  - `Sprite2D`: imagen del objeto
  - `CollisionShape2D`: define el área de detección

### 📦 Estructura de ejemplo:

![[Pasted image 20250415193524.png]]


💡 **Tip**: Puedes moverlo libremente por código, ya que no está afectado por la física.

---

## 🔶 `RigidBody2D`

> Nodo con simulación física real (gravedad, rebotes, masa, etc.)

- Usos comunes:
  - Enemigos que caen, ruedan o rebotan
  - Objetos pesados o interactivos
  - Balas o proyectiles con trayectorias físicas

- Suele ir acompañado de:
  - `Sprite2D`: imagen del objeto
  - `CollisionShape2D`: colisión física
  - `VisibleOnScreenNotifier2D`: detecta si sale de la pantalla

### 📦 Estructura de ejemplo:

![[Pasted image 20250415195202.png]]

💡 **Tip**: Usa `.ApplyImpulse()` o `.LinearVelocity` para moverlo con física.

---

## ⚔️ ¿Cuándo usar `Area2D` o `RigidBody2D`?

| Escenario                               | Nodo recomendado                        |
| --------------------------------------- | --------------------------------------- |
| Recoger objetos como monedas            | `Area2D`                                |
| Detectar si el jugador entra a una zona | `Area2D`                                |
| Enemigos con comportamiento físico      | `RigidBody2D`                           |
| Proyectiles que caen o rebotan          | `RigidBody2D`                           |
| Movimiento controlado sin física        | `CharacterBody2D` o `Node2D` con código |

---
## 🔷 `Node`

> Nodo base más simple en Godot.  
   Se utiliza principalmente como **contenedor lógico** para agrupar otros nodos sin aportar funcionalidades visuales ni físicas.

💡 Muy útil para organizar la jerarquía de una escena.

---
## 🔷 `TextureRect`
> Nodo usado para **mostrar imágenes** dentro de un área rectangular.

- Común en interfaces (`CanvasLayer`)
- Puedes controlar su tamaño, estirado y alineación
- Ideal para mostrar **UI**, fondos, iconos o retratos de personajes

---
## 🔷 `Timer`
> Nodo que actúa como **temporizador**. Muy útil para controlar el tiempo en eventos del juego.

- Puede contar hacia adelante o repetirse automáticamente
- Emite la señal `timeout()` cuando termina
- Útil para:
  - disparos repetidos
  - enemigos que atacan cada cierto tiempo
  - retrasos y animaciones
### Atributos clave

#####  `Wait Time`
Define el **tiempo en segundos** que el temporizador esperará antes de emitir la señal `timeout()`.

- Tipo: `float`
- Es el intervalo entre ejecuciones si el timer se repite.

📌 Ejemplo: Si `Wait Time = 2.0`, el `Timer` se activa cada 2 segundos.

---

##### `One Shot`
Determina si el `Timer` **se ejecuta una sola vez** o **se repite automáticamente**.

- `true`: solo se ejecuta una vez.
- `false`: se reinicia automáticamente al terminar.

💡 Útil para distinguir entre acciones únicas (como una animación retrasada) y repetitivas (como disparos cada pocos segundos).

---
##### `Autostart`
Si está activado, el `Timer` **comienza automáticamente al iniciar la escena**, sin necesidad de llamarlo desde el código.

- `true`: comienza solo.
- `false`: debes iniciar el temporizador manualmente con `Start()`.

💡 Ideal para eventos que deben comenzar apenas se entra a la escena.

---
### 🧠 Extras útiles (por código)

```csharp
var timer = GetNode<Timer>("Timer");
timer.Start();    // Inicia el timer (espera el tiempo de Wait Time)
timer.Stop();     // Detiene el timer manualmente
timer.WaitTime = 3.5f; // Cambia el tiempo de espera desde código
```

---

## 🔷 `AudioStreamPlayer2D`
> Nodo para reproducir **sonido 2D** posicionado en el mundo.

- El sonido se escucha en función de su posición relativa al jugador
- Admite efectos como volumen, pitch, y atenuación espacial
- Soporta archivos `.wav`, `.ogg`, `.mp3`, etc.

📌 Ideal para:
  - pasos del personaje
  - explosiones cercanas
  - música ambiente local

---

## 🔷 `Marker2D`
> Nodo invisible usado para **marcar posiciones** en el espacio 2D.

- No tiene colisión ni imagen
- Solo guarda posición y rotación
- Muy útil como:
  - punto de aparición de enemigos o proyectiles
  - waypoint para movimiento
  - referencia de anclaje

💡 Consejo: puedes moverlo en el editor y usar su posición en tiempo de ejecución con `marker.GlobalPosition`

---

Puedes ver algunas configuraciones en: [[Configuraciones de Godot]]
Para Aprender a programar con estos nodos mirar: [[Apuntes Programación Godot]]