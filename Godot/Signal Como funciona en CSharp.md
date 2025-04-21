
---
## ✅ ¿Por qué aparece la señal en la pestaña de señales del editor?

En **Godot (C#)**, cuando tú escribes esto:

```csharp
[Signal]
public delegate void ChoqueEventHandler();
```

Estás haciendo lo siguiente:

1. **Estás creando una señal personalizada** que se llama `Choque`.
    
2. El atributo `[Signal]` le dice a Godot que **registre esa señal en el sistema de señales del editor**, al igual que `signal choque` en GDScript.
    
3. Cuando el motor Godot carga el script, **detecta automáticamente esa señal** y la **muestra en la pestaña de señales** del editor para que la puedas conectar visualmente (igual que en GDScript).
    

---

### 🧪 ¿Y por qué el nombre `Choque` y no `ChoqueEventHandler`?

Porque Godot toma el **nombre del delegado (`ChoqueEventHandler`)** y le **quita el "EventHandler" al final** para obtener el **nombre real de la señal**: `Choque`.

📌 Esto es una convención del motor para que sea más legible.  
Por eso, cuando haces esto:

```csharp
EmitSignal(nameof(Choque));
```

Estás emitiendo la señal `"Choque"` que se ve en el editor.

---

### 🧠 En resumen:

|Código en C#|Lo que Godot interpreta|
|---|---|
|`[Signal] public delegate void ChoqueEventHandler();`|Se crea una señal llamada **"Choque"** en el editor|
|`EmitSignal(nameof(Choque));`|Lanza esa señal cuando se cumpla una condición|
|Pestaña **Señales** del editor|Te permite **conectarla visualmente** desde otros nodos|
