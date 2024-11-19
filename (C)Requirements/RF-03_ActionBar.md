# Action Bar

- Barra que conteiene un conjunto de botones que permiten la rápida navegación por la plataforma.

## Descripción
- La barra de accion debe de contar con tres botones principales que se comportan como posiciones o estados en la aplicación.
- No puede haber mas de un botón presionado y estos se resaltan durante todo el momento en el que el usuario este dentro de esa `accion`.
- Las acciones se definen como las posiciones en las que puede estar la aplicación. En total son tres y son:
  - Notificaciones
  - Pagina de inicio
  - Añadir Plataforma
### Notificaciones
- El usuario podrá acceder a esta sección a traves del boton izquierdo en la barra de acción.
- En la seccion de `notificaciones`, el usuario podrá ver diferents `items` que contienen información relevante. Estos `items` se dividen en tres tipos:
  - `Tarea`
  - `Examen`
  - `Noticia/Novedad`  
Cada `item` de notificación incluye:
    - Nombre de la plataforma
    - Fecha de inicio
    - Fecha de expiración(excepto para las noticias, que no tienen fecha de expiración).
    - Nombre del curso
    - Descripción
    - Una etiqueta que indique el tipo de notificación.
- Al apretar la opción de `ver` en el item de notificación se redirigirá al usuario a la `plataforma`, `curso` y `actividad/noticia` especificado en la notificación.
- Estas notificaciones podran ser buscadas facilmente a traves del [`RF-03`], el sistema de busqueda y filtrado de la aplicación.

### Pagina de inicio
- El usuario puede acceder a esta sección mediante el boton central.
- En esta seccion se muestran items que pueden contener las plataformas(`item.plataforma`) o los cursos de estas plataformas(`item.curso`).  
Para los items de tipo plataforma:
  - :one: Podrás acceder a las plataformas que tengas registradas previamente mediante un click o presionarlas.
  - :two: Se indicará la cantidad de notificaciones que contengan las plataformas y se colorearan dependiendo de la cantidad:
    - <span style="background-color:#62c51e;color:#262628;"><strong>Verde</strong></span>: Este color indica que no hay notificaciones pendientes en la plataforma, alerta baja.
    - <span style="background-color:#0c2e93;color:#ffffff;"><strong>Azúl</strong></span>: Este color indica la cantidad media de notificaciones 1-3, alerta media.
    - <span style="background-color:#ff2323;color:#ffffff;"><strong>Rojo</strong></span>: Este color indica la cantidad más alta de notificaciones, alerta alta.
    >*Los colores son extraidos de la guia de diseño en la documentación*
  - :three: En la esquina superior izquierda se mostrará información del estado de la plataforma:
    - <span style="background-color:#3bac31;color:#262628;"><strong>Verde</strong></span>: Online, la plataforma esta funcionando correctamente y se puede acceder sin problemas.
    - <span style="background-color:#ffde66;color:#262628;"><strong>Amarillo</strong></span>: La plataforma esta en mantenimiento, no se puede acceder a la plataforma debido a que se esta trabajando en ella. Normalmente los estudiantes son avisados antes de que esto suceda.
    - <span style="background-color:#e66e34;color:#262628"><strong>Naranja</strong></span>: La plataforma esta fuera de servicio por algun problema no especificado. El usuario no puede acceder a la plataforma debido a que esta fuera de servicio.
     >*Los colores son extraidos de la guia de diseño en la documentación*
  - :four: Se muestra el logo de la plataforma.
  - :five: Se muestra el nombre de la plataforma.
  - :six: Se muestra una breve descripcion de la plataforma.
  
 - Para los items tipo curso:
   - :one: Se heredan las carateristicas: :two:,:three: y :five: de los `items.plataforma`.
   - :two: Se muestra el nombre del curso.
   - :three: Se muestra el numero de semestre en el que se encuentra el curso.
   - Se muestra el nombre del profesor a cargo del curso.
- Los items pueden ser buscados y filtrados como se especifica en [`RF-03`].
### Agregar plataforma
- El usuario puede acceder a esta seccion mediante el boton derecho de la barra de acción.
- En esta sección se podrá agregar plataformas ingresando el URl en un campo de texto indicado en la plataforma. La aplicación detectará la plataforma y creará el item que sera mostrado en a seccion de pagina de inicio.
- La plataforma utilizará las credenciales introducidas previamente cuando se inició sesión por primera vez(`correo institucional`). En caso de que la plataforma ingresada necesite usuario y contraseña que no sean el correo institucional la aplicación te pedirá el correo o usuario y la contraseña para poder ingresar y en caso de necesitarlo un captcha.
- La primera vez que el usuario inicie sesion en la aplicación se mostrará la seccion de agregar plataforma y las otras estarán bloqueadas hasta que se termine el porceso de agregar una plataforma.
``` mermaid
graph TD
    A[Usuario ingresa correo y contraseña] --> B[Iniciar sesión]
    B --> C[Correo Institucional]--> G
    B --> C2[Contraseña]--> G
    B --> D[Crear item de plataforma]
    D --> E[Pedir URL de la plataforma escolar]
    E --> F[Usuario ingresa URL]
    F --> G[Utilizar correo y contraseña en la plataforma]
    G --> H[Captcha, si es necesario]
    H --> I[URL]
    I --> J[Buscar datos de la plataforma]
    J --> K[Estado: <br/>- Online<br/>- Maintenance<br/>- Offline]
    J --> K2[Nombre de plataforma] --> L
    J --> K3[Cursos inscritos] --> L
    J --> K4[Numero de notificaciones] --> L
    
    K --> L[Mostrar en items.plataforma]
    J --> 
    L --> M[Mostrar en items. cursos]

    subgraph Base de Datos
        C
        C2
        I
        
        K
        K2
        K3
        K4
    end
```

``` mermaid
erDiagram
    USER {
        string email
        string password
    }
    PLATFORM_ITEM {
        string url
        string platform_name
        string status
        int total_notifications
        int total_courses
    }
    COURSE {
        string course_name
        string platform_name
        string professor_name
        int notifications
        string semester
    }
    TASK {
        string description
        date due_date
    }
    EXAM {
        string description
        date exam_date
    }
    NEWS {
        string title
        string content
        date date
    }

    USER ||--o{ PLATFORM_ITEM : creates
    PLATFORM_ITEM ||--o{ COURSE : contains
    PLATFORM_ITEM ||--o{ TASK : contains
    PLATFORM_ITEM ||--o{ EXAM : contains
    PLATFORM_ITEM ||--o{ NEWS : contains
```

## 




[`RF-03`]: https://github.com/Ozia112/Team-2-FSE-repo/blob/FIS-Project-Stage-3/PD/PD2/OrtizIsaac.md