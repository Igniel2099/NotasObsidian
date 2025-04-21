## Terminología

- **Interfaz:** Es una capa de abstracción que permite la comunicación entre dos sistemas. Proporciona la información necesaria sin exponer cómo funciona internamente (como un intermediario).
    
- **API (Application Programming Interface):** Es una interfaz que permite que aplicaciones se comuniquen y compartan datos entre sí.
    ![[Pasted image 20250414191508.png]]
- **Arquitectura de software:** Es la forma en que está estructurado y diseñado un software, definiendo sus componentes y cómo interactúan.
    
- **Servicio Web:** Sistema que permite la comunicación entre dispositivos a través de una red (por ejemplo, internet o una red local), generalmente utilizando el protocolo HTTP.
    
- **REST (Representational State Transfer):** Estilo de arquitectura para diseñar APIs que utilizan métodos HTTP y recursos bien definidos.
    
- **RESTful:** Se dice que una API es RESTful cuando respeta correctamente los principios de la arquitectura REST.
    
- **JSON (JavaScript Object Notation):** Formato de texto ligero usado para intercambiar datos. Está estructurado en pares clave-valor.
    
- **Token:** Es un identificador único que contiene datos de autenticación, y permite consumir APIs privadas o protegidas.
    
- **Las APIs pueden ser locales o remotas:**
    
    - **Locales:** Si se ejecutan en tu propia máquina o red local.
        
    - **Remotas:** Si están alojadas en un servidor externo (por ejemplo, en internet).
        
- **Consultar Recursos (URI):** Un URI (Identificador Uniforme de Recursos) identifica de manera única un recurso. Para acceder a él se usa un _endpoint_, que es la URL completa.
    
- **Códigos de estado HTTP:**
    
    - **200:** Éxito
        
    - **300:** Redirecciones
        
    - **400:** Error del cliente (solicitud inválida)
        
    - **500:** Error del servidor
        
- **Métodos HTTP:**
    
    - `GET`: Obtener recursos
        
    - `POST`: Crear un nuevo recurso
        
    - `PUT`: Actualizar un recurso existente
        
    - `DELETE`: Eliminar un recurso
        
- **Formato de respuesta común:** JSON suele ser el formato más usado para las respuestas de una API.
    

---

### Buenas prácticas en APIs:

- **HATEOAS (Hypermedia As The Engine Of Application State):** Las respuestas de la API incluyen enlaces a otras acciones relacionadas (por ejemplo, enlaces para editar, borrar, etc.).
    
- **Seguridad:** Autenticación con tokens, uso de HTTPS, validación de entradas.
    
- **Testeo:** Verificar el correcto funcionamiento de cada endpoint con pruebas unitarias o herramientas como Postman.
    
- **Documentar:** Explicar claramente cómo usar la API (endpoints, parámetros, respuestas, errores). Ejemplo: Swagger.

## API's que voy a usar:
* Una API para gestionar los Mails [[API Mail]]
* Una API para gestionar información de Super Héroes [[API Superheroes]]
* Una API para gestionar mi BBDD [[API Gestión BBDD]]
