### Configuraciones de Pantalla
En la pestaña Proyecto > Configuración del proyecto en el menú de la izquierda en el tab Visualización> Ventana, puedo hacer configuraciones importantes del proyecto.
![[Pasted image 20250416115318.png]]
* **Cambiar el Ancho y Largo del Proyecto:**
  En el Contenedor Tamaño > Ancho del Viewport y Tamaño > Altura del Viewport.
  ![[Pasted image 20250416115058.png]]

* **Hacer que sea Escalable con otros dispositivos:**
  `Ventana > Estirar > Modo` cambiar a canvas_items
  `Ventana > Estirar > Aspecto` cambiar a Keep 
  ![[Pasted image 20250416115224.png]]
### Configuración para Debuggear
Para debuggear desde VS community 2022

### Agrupar Nodos
Cuando tienes un nodo con sus respectivos hijos para que en el momento en el que se mueva el nodo padre se muevan sus hijos con el, se puede hacer lo siguiente:

Seleccionar el nodo que queremos agrupar y en el bar menú de la propia escena clicar en **`Agrupar nodo Seleccionado`**.
![[Pasted image 20250416121152.png]]

### Configurar entradas (teclado, mouse, etc)
Para configurar las acciones de las teclas o del mouse, se hace de la siguiente manera, en **`Proyecto > Configuración del proyecto`**
para abrir la ventana de configuración y ahí clicas en la **`Pestaña de Entrada`** . Escriba `el nombre de la acción` en la barra superior y haga clic en el botón "Añadir" para agregar la acción `move_right`.![[Pasted image 20250416134331.png]]
Necesitamos asignar una tecla a la acción. Haz clic en el icono "+" a la derecha para abrir la ventana de configuración de eventos.

`Importante:` Solo asignamos una tecla a cada acción de entrada, pero puede asignar varias teclas, botones del mando o botones del ratón a la misma acción de entrada.

---

**`Nota:`** También puedes seguir las recomendaciones que se detallan en [[Recomendaciones en Godot]]