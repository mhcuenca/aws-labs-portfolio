# Lab- Creacion de una pagina web estatica con S3
Crearemos un bucket de S3 el cual se configurara como un hosting de una pagina web estatica, adicional modificaremos la politica del bucket para permitir el accesos publico.
## 1.- Creacion del bucket
En la consola de administracion de AWS, en la barra de busqueda escribimos S3, luego seleccionamos **Create bucket**

  - Ingresamos el nombre del bucket *mcm-website-15828*
  - Para crear el bucket aceptamos las demas configuraciones comom predeterminadas, y seleccionamos **Create bucket**
## 2.- Configuracion del bucket como una pagina web statica

Actualizamos la propiedad del bucket   **Static website hosting**

   - En la pestaña **Properties**, seleccionar *Edit* **Static website hosting**
     - Para la opcion **Static website hosting**, seleccionar **Enable**
     - Para **Hosting type**, select **Host a static website**
     - Para **Index document**, enter *index.html*
     - Para **Error document**, enter *error.html*
  Y seleccionamos **save changes** para guardar cambios. Regresamos a la seccion de  **Static website hosting** y copiamos
el valor para **Bucket website endpoint** y lo guardamos, con el link anterior podemos ingresar a nuestra pagina web  luego.

## 3.- Permitir acceso publico al bucket
Por defecto, Amazon S3 bloquea el acceso publico a tu cuenta y buckets. Para usar el bucket para hospedar un sitio web estatico, debemos permitir acceso publico al bucket. Usa los siguientes pasos para editar los permisos para el bloque de acceso publico.

- En la pagina del bucket creado, seleccionar la pestaña **Permissions**
- En la seccion **Block public access(bucket settings)**, seleccionar *Edit*
- Borrar **Block** todo **public access** y seleccionar **Save changes**
- En la ventana emergente **Edit Block public access(bucket settings)** ingrese *Confirm* y seleccionar **confirm**
  
## 4.- Adjuntar una politica de bucket para permitir el acceso publico al contenido del bucket

Añadiremos unas politica de bucket para permitir **acceso de lectura publica** al contenido del bucket.
Con el permiso adjuntado cualquiera de internet puede acceder a tu bucket. 

  - Seleccionar la pestaña **Permissions**
  - Debajo de **Bucket Policy** seleccionar *Edit*
  - Para permitir **acceso de lectura publica** para tu sitio web, copia la siguiente politica de bucket en el editor de politicas de bucket.
  - Luego de actualizar la politica, seleccionar **Save Changes**
## 5.- Cargar los archivos del sitio web, prueba del sitio web

Cargaremos al bucket los archivos *index.html* y *error.html*
  - En la pestaña **Objects**, seleccionamos **Upload**
  - Seleccionar **Add files** y cargamos nuestros archivos que tenemos en nuestro directorio local seleccionando **Upload**
  - Ahora para acceder el sitio web copiamos el URL que guardamos anteriormente en nuestro navegador.
  - Finalmente se logra ver la pagina web.
  - si adicionamos al URL un path que no existe como por ejemplo /aboutus.html nos dara la pagina error.html
# Fin del Laboratorio

    
