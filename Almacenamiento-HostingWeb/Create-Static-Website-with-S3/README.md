# Lab- Creacion de una pagina web estatica con S3
Crearemos un bucket de S3 el cual se configurara como un hosting de una pagina web estatica, adicional modificaremos la politica del bucket para permitir el accesos publico.
## 1.- Creacion del bucket
En la consola de administracion de AWS, en la barra de busqueda escribimos S3, luego seleccionamos **Create bucket**

  - Ingresamos el nombre del bucket *mcm-website-15828*
  - Para crear el bucket aceptamos las demas configuraciones comom predeterminadas, y seleccionamos **Create bucket**
## 2.- Configuracion del bucket como una pagina web statica

Actualizamos la propiedad del bucket  *Static website hosting*

   - En la pestaña **Properties**, seleccionar *Edit* **Static website hosting**
   - 
