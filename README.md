# LiterAlura

**LiterAlura** es un proyecto educativo desarrollado como parte del programa **Alura LATAM - ONE (Oracle Next Education)**, enfocado en poner en práctica habilidades adquiridas durante el curso. Este proyecto combina el consumo de APIs externas, la persistencia de datos con Hibernate, Spring Boot y PostgreSQL, junto con la implementación de buenas prácticas de desarrollo.

---

## **Descripción del Proyecto**

El objetivo principal es construir un sistema que obtenga información sobre libros desde la API **Gutendex**, los almacene en una base de datos y permita realizar operaciones avanzadas como:

- Consultas personalizadas utilizando **JPQL**.
- Consultas automáticas generadas por **Spring Data JPA**.
- Filtrado de datos mediante el uso de **Streams** y **Lambdas**.
- Análisis estadístico con herramientas como **DoubleSummaryStatistics**.

Además, el proyecto incluye:
- Buenas prácticas como el uso de variables de entorno para la configuración de la base de datos, mejorando la seguridad y flexibilidad.
- Un menú interactivo que guía al usuario de manera intuitiva a través de sus funcionalidades.

---

## **Características**

- **Consumo de API y persistencia de datos:** Obtiene información de libros desde la API Gutendex y la almacena en una base de datos relacional.
- **Gestión de datos registrados:**
  - Mostrar libros registrados.
  - Mostrar autores con sus datos y los libros asociados.
- **Búsquedas avanzadas:**
  - Buscar autores vivos en un año específico.
  - Filtrar libros por idioma (español, inglés, francés, portugués).
- **Estadísticas y rankings:**
  - Top 10 libros más descargados.
  - Estadísticas de descargas: mínimo, máximo, promedio y total.
- **Validación y manejo de errores:**
  - Excepciones personalizadas para entradas inválidas y errores de API.

---

## **Requisitos del Sistema**

- **Java JDK 17** o superior.
- **Spring Boot 3.0** o superior.
- **PostgreSQL** como base de datos relacional.
- **Maven** para la gestión de dependencias.
- Cliente HTTP para pruebas (Postman o similar).

---

## **Instalación y Configuración**

### **Pre-requisitos**

1. Instala Java JDK 17 o superior.
   - Descarga desde: [Java 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
2. Configura PostgreSQL en tu máquina y crea una base de datos llamada `literalura`.
3. Configura el usuario y la contraseña en el archivo `application.properties`.

### **Pasos de Instalación**

1. Clona este repositorio en tu máquina local:
   ```bash
   git clone https://github.com/JeanRodriguezdev/LiterAlura.git
   ```

2. Accede al directorio del proyecto:
   ```bash
   cd LiterAlura
   ```

3. Instala las dependencias necesarias con Maven:
   ```bash
   mvn clean install
   ```

4. Ejecuta la aplicación:
   ```bash
   mvn spring-boot:run
   ```

---

## **Estructura del Proyecto**

El proyecto está organizado en los siguientes paquetes:

- **excepcion:** Manejo de errores personalizados.
  - `EntradaInvalidaException`
  - `PeticionNullEspacioEnBlancoException`
  - `ResultadosNoEncontradosException`
- **modelo:** Representación de las entidades principales.
  - `Autor`
  - `Libro`
  - Records: `DatoAutor`, `DatoLibro`, `DatoResultado`
- **principal:** Contiene la clase principal del programa.
  - `Principal`
- **repositorio:** Interfaces para la comunicación con la base de datos.
  - `IAutorRepositorio`
  - `ILibroRepositorio`
- **servicio:** Lógica de negocio y consumo de la API externa.
  - `ConsumoApi`
  - `Deserializacion`
  - Interfaz: `IDeserializacion`

---

## **Tecnologías Utilizadas**

- **Lenguaje de programación:** Java ☕
- **Framework:** Spring Boot
- **Base de Datos:** PostgreSQL 🐘
- **IDE recomendado:** IntelliJ IDEA (pero puedes usar cualquier otro).
- **API Consumida:** Gutendex
- **Herramientas de Construcción:** Maven
- **Dependencias:** Jackson, Spring Data JPA, Spring Web, Spring Boot DevTools y PostgreSQL Driver

---
