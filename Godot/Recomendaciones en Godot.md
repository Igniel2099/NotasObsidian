* Como regla general, el nodo raíz de una escena debe reflejar la funcionalidad deseada del objeto (no de programación ).
* Si quiero programar en C# necesitas (re)construir los archivos assembly del proyecto cada vez que quieras tener visibles las variables **`exportadas`** o las **`señales`**. 
  ```c#
	[Export]
	public int Speed { get; set; } = 400;
	[Signal]
	public delegate void HitEventHandler();
	```
  `nota`: Para saber mas sobre **Signal** que puede ser un decorador particular ira a [[Signal Como funciona en CSharp]]
  Esta construcción puede ser lanzada manualmente pulsando el botón "Build" en la parte superior derecha del editor.![[Pasted image 20250416132213.png]]