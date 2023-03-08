---
tags: [Empezando, Postman, Tutorial]
---

# Tutorial para Pruebas de Postman

Esta sección tiene como objetivo demostrar la configuración inicial que se debe aplicar a la colección de Postman, antes de realizar solicitudes a las API de Fiserv disponibles.

Si no ha utilizado la herramienta Postman como cliente HTTP para probar solicitudes, acceda al enlace oficial de la herramienta para obtener más información: 
 [Postman Official](https://www.postman.com/)

## Importar Colección

### 1. Abra Postman y haga clic en el botón de importación para abrir la colección provista

![Postman!](/assets/images/postman/postman-tutorial_1.png "Postman")

### 2. Después de importar la colección, verá que la siguiente contiene las solicitudes divididas por carpetas según cada entidad y también las solicitudes iniciales, por ejemplo, "Get Access Token"

![Postman!](/assets/images/postman/postman-tutorial_2.png "Postman")

## Crear el ambiente

### 3. En este paso configuraremos el ambiente necesario para ejecutar solicitudes en Postman de forma dinámica, ya que las solicitudes ya vienen configuradas con variables de ambiente las cuales configuraremos a continuación. Haga clic en el botón de ambientes y siga los siguientes pasos

![Postman!](/assets/images/postman/postman-tutorial_3.png "Postman")

### 4. Haga clic en el botón nuevamente en la sección de Ambiente para crear un ambiente para ejecutar solicitudes

![Postman!](/assets/images/postman/postman-tutorial_4.png "Postman")

### 5. Haga clic en el ambiente y luego defina el nombre de este ambiente

![Postman!](/assets/images/postman/postman-tutorial_5.png "Postman")

## Configurar la Colección

### 6. Ahora deberá crear las variables como el siguiente ejemplo con las credenciales enviadas. En este paso puede definir cuáles variables se utilizarán durante el uso de la colección, como punto final, puerto y otros

![Postman!](/assets/images/postman/postman-tutorial_6.png "Postman")

### 7.  En la esquina superior derecha, seleccione el ambiente creado para aplicar la configuración de las variables de ambiente creadas en el paso anterior

![Postman!](/assets/images/postman/postman-tutorial_7.png "Postman")

### 8. Si ha seguido los pasos correctamente hasta el momento, el ambiente está listo para enviar solicitudes a las API. Haga clic en Obtener Token de Acceso a la API para iniciar las pruebas para la API

![Postman!](/assets/images/postman/postman-tutorial_8.png "Postman")                      

## Ejecutar Primera Solicitud

### 9. Haga clic en el botón de Enviar

![Postman!](/assets/images/postman/postman-tutorial_9.png "Postman")

### 10. You will notice that you have got an "access_token" which is automatically set in the "token" environment variable and has an expiration date. When the token expires, you'll need to repeat the step above
Notará que tiene un "access_token" que se configura automáticamente en la variable de ambiente "token" y tiene una fecha de expiración. Cuando el token expire, deberá repetir el paso anterior

![Postman!](/assets/images/postman/postman-tutorial_10.png "Postman")

¡Ya está listo para comenzar a probar nuestras APIs!

---

## Ver también

- [Empezando](?path=docs/spanish/empezando.md)
- [Estructura](?path=docs/spanish/empezando/estructura.md)
- [Lista Servicios](?path=docs/spanish/empezando/lista-servicios.md)
- [Terminología](?path=docs/spanish/empezando/terminologia.md)

---
