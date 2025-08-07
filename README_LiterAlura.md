
# LiterAlura 

LiterAlura es un catálogo de libros interactivo desarrollado en Java con Spring Boot. Permite consultar títulos de la biblioteca digital gratuita Project Gutenberg mediante la API Gutendex, almacenar los datos en una base de datos PostgreSQL y realizar consultas desde la consola. 

Este proyecto fue desarrollado como parte del programa ONE (Oracle Next Education) de Alura Latam.

---

## 🚀 Funcionalidades

- 🔍 Buscar libros por título (desde la API Gutendex)
- 📚 Listar todos los libros almacenados
- 👤 Listar autores registrados
- 🧓 Consultar autores vivos en un año específico
- 🌐 Consultar la cantidad de libros por idioma

---

## 🛠️ Tecnologías utilizadas

- Java 17
- Spring Boot 3.2.3
- Maven 4
- PostgreSQL 16+
- Jackson (para manipulación de JSON)
- Spring Data JPA

---

## 📦 Estructura del Proyecto

```bash
com.literalura
│
├── model            # Entidades JPA: Libro, Autor
├── repository       # Repositorios JPA
├── service          # Lógica de negocio y consumo de API
├── dto              # Clases para mapear la respuesta JSON
├── principal        # Clase principal que ejecuta el menú
└── LiterAluraApplication.java
```

---

## 📄 Requisitos previos

- Java JDK 17+
- Maven 4+
- PostgreSQL 16+
- IDE recomendado: IntelliJ IDEA

---

## ⚙️ Configuración del entorno

1. Clonar el repositorio
```bash
git clone https://github.com/tu-usuario/literalura.git
cd literalura
```

2. Crear la base de datos en PostgreSQL
```sql
CREATE DATABASE literalura;
```

3. Configurar `application.properties`
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/literalura
spring.datasource.username=TU_USUARIO
spring.datasource.password=TU_CONTRASENA
spring.jpa.hibernate.ddl-auto=update
```

4. Ejecutar el proyecto
```bash
mvn spring-boot:run
```

---

## 🖥️ Uso

El sistema ofrece un menú por consola con opciones numeradas. El usuario puede:

- Ingresar un título de libro para buscarlo en Gutendex
- Ver todos los libros almacenados en la base
- Consultar todos los autores
- Ingresar un año para ver autores vivos en ese período
- Ingresar un idioma (`en`, `es`, etc.) para ver cuántos libros hay en ese idioma

---

## 📌 Observaciones

- El sistema solo guarda el primer autor e idioma de cada libro, para simplificar el modelo.
- Se recomienda verificar los datos ingresados por el usuario para evitar errores.

---

## 🤝 Contribuciones

Este proyecto fue desarrollado con fines educativos, pero cualquier contribución o sugerencia es bienvenida.

---

## 📚 Créditos

Desarrollado por Alan Gurrieri como parte del programa ONE (Oracle Next Education) en colaboración con Alura Latam.

API utilizada: [Gutendex](https://gutendex.com/)

---

## 📝 Licencia

Este proyecto se distribuye bajo licencia MIT. Ver [LICENSE](LICENSE) para más información.
