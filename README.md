# Proyecto-React-Node-Mongo

## Planteamiento del proyecto

Desde el equipo de full-stack, nos han enviado una aplicación web desarrollada con React, Node.js y MongoDB. La arquitectura consta de un front-end (cliente) y un back-end (servidor).

Nuestra tarea consiste en implementar el despliegue de la aplicación en dos instancias de Cloud Run y asegurar la conexión entre el servidor y el cliente por un lado, y con MongoDB por el otro.

## Resolución:

### **Conectar Servidor con Base de Datos**

Una vez que hayamos creado la base de datos en MongoDB, utilizaremos Compass para establecer la conexión con nuestra instancia. Para lograr esto, es necesario que nuestro proveedor en la nube proporcione la cadena de conexión adecuada, siguiendo este formato: `mongodb+srv://<username>:<password>@cluster0.2lnyz2p.mongodb.net/`. Esta cadena contiene las credenciales de la base de datos, por lo tanto, la guardaremos como un secreto en el Secret Manager:

1. **Cadena de Conexión MongoDB:**
   - `mongodb+srv://<username>:<password>@cluster0.2lnyz2p.mongodb.net/`

2. **Almacenamiento Seguro:**
   - Guardaremos la cadena de conexión como un secreto en el Secret Manager de nuestro proveedor de servicios en la nube.

