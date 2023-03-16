# Curso UDEMY: APIs con TypeScript como si estuvieras en Angular. 
The Good Code Academy

Crea Servicios Web API como un PRO. Aprende desde cero.

## indice del curso

### Seccion 1, introduccion
1. S01-CL01: Presentación del curso
2. S01-CL02: Plataforma Udemy y cómo formular preguntas
3. S01-CL03: Valoración del curso

### Seccion 2, Introduccion y preparacion del entorno de desarrollo
4. S02-CL01: Qué es NestJS
5. S02-CL02: Primeros pasos: instalación NestJS
6. S02-CL03: Instalando XAMPP para base de datos local MySQL
7. S02-CL04: Entorno de desarrollo: Visual Studio Code

### Seccion 4, Desarrollo API con NestJS
8. S03-CL01: Configurando el proyecto
9. S03-CL02: Controladores
10. S03-CL03: Configuración conexión a base de datos (MySQL)
11. S03-CL04: Declaración de entidades
12. S03-CL05: Repositorios y Proveedores
13. S03-CL06: Inyección de dependencias

### Seccion 4, Consumo de API
14. S04-CL01: Instalación de Postman
15. S04-CL02: Petición POST en Postman
16. S04-CL03: Petición GET en Postman
17. S04-CL04: Petición PUT en Postman
18. S04-CL05: Petición DELETE en Postman
19. S04-CL06: Consumiendo la API desde aplicación Androi


# Seccion 1, introduccion
## 1. S01-CL01: Presentación del curso
### ¿QUE ES NESTJS?

Es un framework para crear aplicaciones del lado del servidor (Backend) a través de NodeJS.

Programar en TS sencillo con diferentes paradigmas

Es modular y resuelve problemas de escalabilidad y estructuración de proyectos.

Soporta Arquitectura monolítica y de microservicios, MVC, Websockets y GraphQL.



### ¿POR QUÉ NESTJS?

Soporta Typescript y Javascript + Babel.

Es Multiparadigma: Programación Orientada a Objetos (OOP), Programación Funcional (FP) y Programación Reactiva Funcional (FRP).

Integra con diferentes bases de datos: MySQL, PostgreSQL, SQLite, MongoDB…

Extremadamente sencillo de usar.

Arquitectura, convenciones y estructura de proyecto igual que Angular.



### BENEFICIOS DE USAR NESTJS

Si aprendes a usar NestJS, aprenderás Angular de forma natural e inconsciente.

Si sabes Angular pero crees que no sabes backend, con NestJS te darás cuenta que si sabes.

Framework moderno que usa las últimas y mejores librerías y herramientas.

Experiencia de desarrollo divertida y altamente productiva.



### COMUNIDAD, CRECIMIENTO Y DOCUMENTACIÓN

- Proyecto Open Source, de libre uso y gratuito.

- Apoyado por más de 13.000 desarrolladores en GitHub.

- Activo y en constante crecimiento.

- Extensa documentación, clara y llena de ejemplos.

## 2. S01-CL02: Plataforma Udemy y cómo formular preguntas
Instrucciones generales para hacer preguntas y navegar en l aplataforma UDEMY

## 3. S01-CL03: Valoración del curso
Instrucciones generales para valorar el curso, se indica que debe valorarse el curso de manera positiva o posponer hasta el final.

# Seccion 2, Introduccion y preparacion del entorno de desarrollo
## 4. S02-CL01: Qué es NestJS
Framework de programacion vbasado en nodejs, aplicaciones backend o API para clientes app consumir datos de una BD en un servidor.

Desarrollo en el servidor los componentes para que otras app consuman datos,

Proyecto con alto crecimiento, permite a desarrolladores angular pasar al backend

Lo lidera Kamil Mysliwiec cuenta con patrocinadores diversos

Crecimiento significativo por facilidad de pasar al backend desarrolladores angular, basado en arquitectura angular.

Framework permite mejorar las aplicaciones backend como express y fastify, se basa en ellas y mejora la arquitectura.

Permie usar JS en front y back y su documentacion tecnica es muy elaborada y detallada.

## 5. S02-CL02: Primeros pasos: instalación NestJS
Para instalar nestjs y crear aplicaciones de backend hay que tener en cuenta que usa typescript, los requisitos de version oficial es mayor oi igual a la version 12 pero no la 13.

    https://docs.nestjs.com/first-steps

Para verificar instalacion de nodejs

    $ node -v

En caso que no cumpla los requisitos debe instalarse nodejs que es la maquina virtual de navegadores como chrome para ejecutar js, en lugar de hacerlo en navegador dse hace en maquina local con nodejs que es un interprete y runtime.

Segun la documentacion de nodejs es necesario instalar nestjs y su cli de manera global

    $ npm i -g @nestjs/cli

### Creacion primer proyecto nest
Es necesario ir hasta el directorio donde se quiere alojar el proyecto y se ejecuta la siguiente linea de codigo

    $ nest new project-name

Se indica el nombre del proyecto y se selecciona el manejador de paquetes que se quiere usar, en este casos e va a usar npm. Una vez finaliza la creacion de la aplicacion indica que se puede acceder a la app asi:

    $ cd messages-app
    $ npm run start

De esta manera ya esta lanada la aplicacion backend en un puerto local que se peude consumir desde u cliente.

En este momento la aplicacion nop tiene controladores definidos.

## 6. S02-CL03: Instalando XAMPP para base de datos local MySQL
Se recomuenda la instalacion de XAMPP para el manejo de la base de datos.
Una vez instalada se debe arrancar los servicios, MySQL para arrancar la base de datos y apache para tener el manejador grafico de la base de datos.

Php my admin permite gestionar graficamente la base de datos.

### Creacion de base de datos proyecto con usuario de acceso
Se crea la base de datos para el proyecto en XAMPP con nombre sendmeapp_db y se indica utf8-unicode. Una vez creada la BD solo resta gestionar un usuario para acceder a la BD.

### Creacion de usuario para acceso a BD
Dentro de Phpmyademin, estando en la pestaña privilegios se accede a crear un usuario en la parte inferior, se le da como nombre nest, el host es en local y la contraseña sera app. Se seleccionan todos los permisos y se ha creado el usuario .

User account 'nest'@'localhost' - Database sendmeapp\_db

## 7. S02-CL04: Entorno de desarrollo: Visual Studio Code
Es una aplicacion potente y sencilla para desarrollo de aplicaciones, en este caso con nest js framework. Se instala VSC en el sistema operativo.
Dentro se abre el proyecto creado previamente con el comando de node cli. La gran cantidad de librerias permiten mejorar la interaccin con comandos o abreviaturas.

Dentro de las extensinoes de VSC se busca con nestjs, se recomienda siempre descargar las extensiones que han sido descargadas por una gran cantidad de personas

Vscode NestJs Snippets

En la documentacion del plugin se puede apreciar que una de las instrucciones es recargar VSC, se procede a reiniciar.

El entorno de desarrollo de nestjs está listo.

# Seccion 3, Desarrollo API con NestJS
## 8 . S03-CL01: Configurando el proyecto
La descripcion de los ficheros del proyecto es:

### Archivos de configuracion

/nest-cli
COnfguraciones basicas del framework como lenguaje y directorio raiz

/package.json
COnfiguracion de las dependencias y librerias de las que hace uso js.
Al escribir npm install en la terminal recorre el archivo y genera el directorio dentro de node_modules


/tsconfig.json
Configuracion del compilador de typescript. Se configura la version de js y el directorio outDir donde se entrega la ruta de los archivos js

/tslint.json
Contiene normlas de codificacion para ts y que el proyecto aisa en caso de saltar alguna.

### Archivos de proyecto en /src
Dentro del directorio /src estan los archivos a desarrollar.

/main.ts
Fichero principal de la aplicacion en donde se define la instancia de nestfactory que es una instancia del framework para crear la API. Esta conectado al modulo app que es una importacion del modulo principal de la aplciacino que carga los controladores principales, por la similitud con angular, AppModule seria el modulo principal que se carga como bootstrap o arranque de la aplicacion ademas se tiene la resolucion del puerto donde la aplicacion estara escuchando el servicio de api, que peude ser modificado a cualquier otro puerto que se encuentr libre.

    import { NestFactory } from '@nestjs/core';
    import { AppModule } from './app.module';

    async function bootstrap() {
      const app = await NestFactory.create(AppModule);
      await app.listen(3000);
    }
    bootstrap();


/app.module.ts
Viene indicado por el decorador @module para indicar que la clase que se va a definir es de tipo modulo y tiene varios bloques de configuracion:
imports: hace referencia a modulos, dependencias y cpmponentes necesarios par a usar el modulo
controllers: seccion de todos los controladores que hacen parte del modulo un modulo agrupa varios controladores.
providers: servicios donde se encuentran los metodos de acceso a los datos, se tiene declarado un servicio AppService.

    import { Module } from '@nestjs/common';
    import { AppController } from './app.controller';
    import { AppService } from './app.service';

    @Module({
      imports: [],
      controllers: [AppController],
      providers: [AppService],
    })
    export class AppModule {}


Esta es la declaracion del modulo que es el componente principal de una parte de la aplicacino y se va a encargar de cargar los servicios y controladores.

/app.controller.ts
COntiene la estructura basica de un controlador. El decorador es @COntroller con un metodo constructor donde se recibe por inyeccino de dependencia el servicio. Es como si se estuviera haciendo un new o creacion de objeto de tipo AppService al que se accede desde diferentes metodos para acudir a fuente de datos.

    import { Controller, Get } from '@nestjs/common';
    import { AppService } from './app.service';

    @Controller()
    export class AppController {
      constructor(private readonly appService: AppService) {}

      @Get()
      getHello(): string {
        return this.appService.getHello();
      }
    }

Inicialmente tiene una invocacion metodo getHello que le devuelve un mensaje o un conjunto de datos que se usa para devolverse al usauario en cada peticion. Se van a ver a fondo mas adelante cuando se aprenda a diseñar controladores y trabajar con ellos.

Hasta este punto los fucheros principales de configuracion con los que se va a trabajar mas adelante profundizando en el uso de los diferentes controladores, servicios y modulos.


## 9 . S03-CL02: Controladores

## 10. S03-CL03: Configuración conexión a base de datos (MySQL)

## 11. S03-CL04: Declaración de entidades

## 12. S03-CL05: Repositorios y Proveedores

## 13. S03-CL06: Inyección de dependencias



