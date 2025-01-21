![banner color negro books](https://github.com/user-attachments/assets/d73b4244-36e2-4043-be07-4872d7001856)
<p align="center"> 
  <img src="http://img.shields.io/static/v1?label=STATUS&message=EN%20DESARROLLO&color=ORANGE&style=for-the-badge" /> 
  <img src="https://img.shields.io/badge/language-Java-007396?style=for-the-badge"/> 
  <img src="https://img.shields.io/badge/database-PostgreSQL-336791?style=for-the-badge"/> 
</p>

## Descripción del Proyecto
Literatura es un proyecto educativo desarrollado como parte del programa Alura LATAM - ONE (Oracle Next Education), 
enfocado en poner en práctica habilidades adquiridas durante el curso. Este proyecto combina el consumo de APIs externas, 
la persistencia de datos con Hibernate, Spring Boot y PostgreSQL, junto con la implementación de buenas prácticas de desarrollo.

El objetivo principal es construir un sistema que obtenga información sobre libros desde la API Gutendex, 
los almacene en una base de datos y permita realizar operaciones avanzadas como:

- Consultas personalizadas utilizando JPQL.
- Consultas automáticas generadas por Spring Data JPA.
- Filtrado de datos mediante el uso de Streams y Lambdas.
- Análisis estadístico con herramientas como DoubleSummaryStatistics.

El proyecto incluye buenas prácticas como el uso de variables de entorno para la configuración de la base de datos,
mejorando la seguridad y flexibilidad. Además, incorpora un menú interactivo que guía al usuario de manera intuitiva a través de sus funcionalidades.

## 🔧 Tecnologías Utilizadas
- **Lenguaje de programación:** Java ☕
- **Framework:** Spring Boot 
- **Base de Datos:** PostgreSQL 🐘
- **IDE:** IntelliJ IDEA (recomendado, pero puedes usar cualquier otro).
- **API Consumida:** Gutendex
- **Herramientas de Construcción y Gestión de Dependencias:** Maven
- **Dependencias:** Jackson, Spring Data JPA, Spring Web, Spring Boot DevTools y PostgreSQL Driver

## 🚀 Instalación
### 📋 Pre-requisitos

1. Instala en tu ordenador Java JDK 17 o superior.

- Descarga desde: [Java 17](https://www.oracle.com/ar/java/technologies/downloads/#java17)
2. Configura PostgreSQL en tu máquina.

- Crea una base de datos llamada literatura.
- Configura usuario y contraseña en el archivo application.properties.
3. Clona este repositorio en tu ordenador:
````
https://github.com/Erika-Gimenez/Literalura.git

````
- Navega hasta la carpeta del proyecto.
````
cd literalura

````
4. Ejecuta el proyecto en tu IDE favorito (IntelliJ IDEA, Eclipse, etc.).

- IDE recomendado: [IntelliJ IDEA](https://www.jetbrains.com/idea/)

> [!NOTE]
> Las dependencias principales ya están incluidas en el archivo pom.xml. Asegúrate de actualizar Maven para descargarlas:
````
mvn clean install

````

## 🏗️ Estructura del Proyecto
### Subpaquetes y sus responsabilidades:
- **excepcion:** Manejo de errores personalizados.
  - Clases: EntradaInvalidaException, PeticionNullEspacioEnBlancoException, ResultadosNoEncontradosException.
- **modelo:** Representación de las entidades principales.
   - Clases: Autor, Libro. 
   - Records: DatoAutor, DatoLibro, DatoResultado.
- **principal:** Contiene la clase principal del programa.
   - Clase: Principal.
- **repositorio:** Interfaces para la comunicación con la base de datos.
   - Interfaces: IAutorRepositorio, ILibroRepositorio.
- **servicio:** Lógica de negocio y consumo de la API externa.
   - Clases: ConsumoApi, Deserializacion
   - Interfaz: IDeserializacion.

## 📂 Funcionalidades
1. Consumo de API y persistencia:

- Obtiene datos de libros desde una API y los guarda en la base de datos.
2. Gestión de datos registrados:

- Mostrar libros registrados.
- Mostrar autores con sus datos y los libros asociados.
3. Búsquedas avanzadas:

- Buscar autores vivos en un año específico.
- Filtrar libros por idioma (español, inglés, francés, portugués).
4. Estadísticas y rankings:

- Top 10 libros más descargados.
- Estadísticas de descargas: mínimo, máximo, promedio, total.
5. Validación y manejo de errores:

- Excepciones personalizadas para entradas inválidas y errores de API.
  
## 🙌 Contribuciones
¡Me encantaría tu ayuda para mejorar este proyecto! Puedes contribuir de varias maneras:
* Si encuentras algún error o problema.
* Si tienes ideas para nuevas funcionalidades o mejoras.

## ✒️ Autores 

[<img src="https://github.com/user-attachments/assets/1e99f8e5-f229-4128-837a-554d2844c64c" width=115><br><sub>Gimenez Erika</sub>](https://github.com/Erika-Gimenez)

## 😊 Contacto 

* [Linkedin](https://www.linkedin.com/in/erika-gimenez/).
* [GitHub](https://github.com/Erika-Gimenez).

> [!NOTE]
>  Nuevas opciones en el menú.
>  Experimentar con una interfaz gráfica en el futuro para mejorar la experiencia del usuario.
