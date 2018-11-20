# RESTfulWS

## a) Instalación

    Para clonar el repositorio:
    ```
    git clone https://github.com/MikePineda/RESTfulWS.git
    ```

    ** Abrir en NetBeans **

    1. Dar clic en `File -> Open project.
    2. Seleccionar la carpeta raíz donde se clonó el proyecto.
    3. Correr Clean and Build dando clic derecho en el proyecto.
    4. Darle en `run.


## b) Uso

    ** Administrador web de archivos **

        Acceder al siguiente path:

        ```
        RESTfulWS/login

        ```

    ** RESTful API **

    **Recurso api/v1/**  
        1. **GET**: Lista los recursos disponibles.
        2. **OPTIONS**: Documentación del recurso.

        **Recurso api/v1/file**  
            1. **GET**: Descarga un archivo mediante el parámetro path. 
            ```
            api/v1/file/?path=
            ```
            2. **POST**: Sube un archivo mediante los parámetros name, dir y file.
            ```
            api/v1/file/ name="imagen.jpg" dir="/Files" file@/Users/User/Downloads/imagen.jpg --form
            ```
            3. **DELETE**: Elimina un archivo mediante el parámetro path.
            ```
            api/v1/file/?path=
            ```
            4. **OPTIONS**: Documentación del recurso.

        **Recurso api/v1/directory**  
            1. **GET**: Lista los archivos de un directorio mediante el parámetro dir. 
            ```
            api/v1/directory/?dir=
            ```
            2. **OPTIONS**: Documentación del recurso.

        **Recurso api/v1/notify**  
            1. **GET**: Lista las notificaciones enviadas.
            2. **POST**: Envía una notificación mediante los parámetros subject, message, toAddress y ccAddress.
            ```
            api/v1/notify subject="hello" message="Que onda raza" toAddress="example@email.com" ccAddress="example2@email.com"
            ```
            3. **OPTIONS**: Documentación del recurso.

        **Recurso api/v1/user**  
            1. **GET**: Lista los usuarios.
            2. **POST**: Crea un usuario mediante los parámetros username, password y fullName.
            ```
            api/v1/user username="user" password="pass" fullName="John Doe"
            ```
            3. **OPTIONS**: Documentación del recurso.

        **Recurso api/v1/user/{username}**  
            1. **GET**: Muestra la información del usuario.
            2. **PUT**: Actualiza la información del usuario mediante los parámetros username, password y fullName.
            ```
            api/v1/user/user username="user" password="pass" fullName="John Doe"
            ```
            3. **DELETE**: Elimina al usuario.
            4. **OPTIONS**: Documentación del recurso.


## c) Créditos

    Miguel Eduardo Pineda López
    2780483
    Computación Avanzada en Java.

## d) Licencia 

    El proyecto no cuenta con ninguna licencia.
