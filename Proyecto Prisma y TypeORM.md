# Creación de proyectos con Prisma y TypeORM

### Proyecto con Prisma
Prisma es un toolkit de base de datos de código abierto que permite acelerar el desarrollo y tener un mejor control y acceso a los datos en proyectos de Node.js con MySQL, PostgreSQL o SQLite 

**Podemos crear un proyecto con Prisma siguiendo estos pasos:**
* Utilizar el comando de instalación de Prisma: npm install -g prisma

* Crear un archivo de configuración para especificar la conexión a la base de datos y otras configuraciones necesarias. Ya sea en formato: XML, YAML o JSON

* Crear un archivo donde se defina el modelo de datos utilizando el lenguaje de definición de Prisma. Para deifinir el modelo de datos se tiene que ubicar en el archivo de esquema de Prisma. Este archivo se encuentra en la carpeta prisma y tiene la extensión ".prisma". Aquí se especifica las tablas y relaciones de la base de datos.

* Utilizar el comando de generación de cliente de Prisma para generar el código necesario para interactuar con la base de datos: "npx prisma generate"
Este comando generará el cliente de Prisma en la carpeta node_modules/@prisma/client. El cliente de Prisma es un generador de consultas de tipo seguro y autogenerado que puedes utilizar para interactuar con la base de datos desde la aplicación Node.js o TypeScript.

* Utilizar el cliente de Prisma en el código del proyecto para realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar): Crear una nueva tarea, leer todas las tareas existentes, actualizar una tarea existente y eliminar una tarea.

### Proyecto con TypeORM 
TypeORM es un Object-Relational Mapper (ORM) que permite crear bases de datos y manipular los datos sin la necesidad de conocer o usar SQL,

**Podemos crear un proyecto con TypeORM siguiendo estos pasos:**

* Utilizar el comando de instalación de TypeORM: npm install typeorm

* Crear un archivo de configuración para especificar la conexión a la base de datos y otras configuraciones necesarias: ormconfig.json 

* Crear clases que representen las tablas de la base de datos y definir las relaciones entre ellas utilizando los decoradores proporcionados por TypeORM.

* Utilizar las clases y métodos proporcionados por TypeORM para realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar): Crear una nueva tarea, leer todas las tareas existentes, actualizar una tarea existente y eliminar una tarea.

## Conclusiones
Tanto Prisma como TypeORM son herramientas poderosas para interactuar con bases de datos en proyectos de Node.js. Ambos proporcionan funcionalidades esenciales como el modelado de datos, las migraciones y las operaciones CRUD.




