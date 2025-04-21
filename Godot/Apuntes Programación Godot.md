* El método `_ready()` se llama cuando un nodo entra en la escena.
* El método `_process()` se llama en cada frame, así que la usaremos para actualizar elementos del juego que esperamos que cambien a menudo.
* Puedes detectar si una tecla se está presionando usando `Input.is_action_pressed()`, lo que devuelve `true` si está presionada o `false` en caso contrario.
* El siguiente Bloque de codigo utiliza Clamp() en C#
``` CSharp
Position += velocity * (float)delta;
Position = new Vector2(
    x: Mathf.Clamp(Position.X, 0, ScreenSize.X),
    y: Mathf.Clamp(Position.Y, 0, ScreenSize.Y)
);
```
  La función `Mathf.Clamp` se asegura de que un valor se mantenga dentro de un rango. Es decir, si el valor está fuera de los límites que le indicas (en este caso, entre 0 y `ScreenSize.X`), la función lo "ajustará" a ese límite.

- **Si el valor es menor que 0:**  
    `Mathf.Clamp(valor, 0, ScreenSize.X)` devolverá 0.
    
- **Si el valor es mayor que `ScreenSize.X`:**  
    La función devolverá `ScreenSize.X`.
    
- **Si el valor ya está entre 0 y `ScreenSize.X`:**  
    Se devolverá el mismo valor.
    

Por ejemplo, si `ScreenSize.X` es 800 y el valor que se intenta clamar es -50, el resultado será 0. Si el valor es 850, el resultado será 800. Esto evita que la posición quede fuera de los límites de la pantalla.

### Clase del Nodo AnimatedSprite2D
* Atributo FlipH y FLipV:
  En el contexto de Godot, estos atributos son  una bandera booleana que, cuando está activada (`true`), invierte o "voltea" horizontalmente la imagen de un sprite. Es decir, cambia la orientación del sprite de modo que lo que estaba a la derecha pasa a la izquierda y viceversa. Esto es especialmente útil para representar la dirección en la que un personaje o elemento se está moviendo sin tener que crear dos versiones diferentes de la imagen.
* El atributo **Animation** del objeto **AnimatedSprite2D** es una propiedad de tipo _string_ que determina cuál de las animaciones definidas en el recurso de SpriteFrames asociado se mostrará y reproducirá. Aquí te dejo una descripción detallada:
	 -  **Selección de animación:**  
		Cada **AnimatedSprite2D** está vinculado a un recurso _SpriteFrames_, que contiene una o varias animaciones (listas de imágenes o "frames"). El atributo **Animation** indica el nombre de la animación que se debe utilizar en ese momento.  
		Por ejemplo, si tienes animaciones llamadas "Idle", "Run" y "Jump", asignar **Animation = "Run"** le indica al nodo que muestre y reproduzca la animación correspondiente a correr.