# Configuración de Prisma y Seeds


### Primero crear un proyecto nestjs:
* nest new hunting (npm): Este comando se utiliza para crear un nuevo proyecto de NestJS con el nombre "hunting" y utilizando npm como gestor de dependencias. Al ejecutar este comando, se generará la estructura básica del proyecto y se instalarán todas las dependencias necesarias para que funcione correctamente


### Configurar prisma (npm) carpeta hunting
* npm install prisma --dev: Este comando instala la biblioteca de Prisma como una dependencia de desarrollo en un proyecto de TypeScript. Prisma es una herramienta que proporciona acceso a la base de datos y facilita la gestión de datos.

* npm install @prisma/client: Este comando instala el cliente de Prisma, que es un generador de consultas autogenerado que permite el acceso a la base de datos de forma segura y reduce la cantidad de código repetitivo. 

* npx prisma init: Este comando inicializa un proyecto de Prisma en el directorio actual. Crea un directorio llamado "prisma" que contiene un archivo de esquema básico llamado "schema.prisma". El archivo de esquema define el modelo de datos y la configuración de la base de datos..


### Carpeta prisma
* Crear un seed.ts en la carpeta Prisma y copiar el código:

import { PrismaClient } from '@prisma/client';


// initialize Prisma Client
const prisma = new PrismaClient();


async function main() {
  // create two dummy articles
  const post1 = await prisma.article.upsert({
    where: { name: 'Aliens' },
    update: {},
    create: {
      name: 'Aliens',
      description: 'fictional being from another world.',
      lastSee:
        "Simón Bolívar 1-62 y Manuel Vega",
      countLastSee:12,  
      extinct: false,
    },
  });


    const post2 = await prisma.article.upsert({
    where: { name: 'Vampires' },
    update: {},
    create: {
      name: 'Vampires',
      description: 'leave its grave at night to drink the blood of the living by biting their necks with long pointed canine teeth.',
      lastSee:
        "Calderon Park",
      countLastSee:5,  
      extinct: false,
    },
  });






  console.log({ post1, post2 });
}


// execute the main function
main()
  .catch((e) => {
    console.error(e);
    process.exit(1);
  })
  .finally(async () => {
    // close Prisma Client at the end
    await prisma.$disconnect();
  });




### Ejecutar el comando 
* npx prisma db seed: Se utiliza para llenar una base de datos con datos de prueba y se ejecuta a través de un script de siembra personalizado





