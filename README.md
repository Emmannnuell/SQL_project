# Análisis de Datos para Plataforma de Libros en Línea (SQL & Pandas)

## 📝 Descripción del Proyecto
Este proyecto simula un caso de estudio real donde se analiza la base de datos de una plataforma de libros electrónicos (vía una base de datos relacional). El objetivo estratégico es extraer insights sobre el catálogo de libros, el volumen de páginas por editorial, la satisfacción de los usuarios con los autores y el comportamiento de los clientes más activos ("Power Users") para guiar las decisiones del equipo de Producto y Contenido.

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python 3.12
* **Análisis de Datos:** Pandas
* **Base de Datos y Conexión:** SQL, SQLAlchemy
* **Motor de BD Local:** SQLite (para garantizar reproducibilidad autónoma)
* **Entorno:** Jupyter Notebook / VS Code

## 🗺️ Modelo de Datos (Estructura)
El ecosistema de datos está compuesto por 5 tablas interconectadas:
1. `books`: Catálogo central (IDs, títulos, páginas, fechas, autores y editoriales).
2. `authors`: Registro de escritores y escritoras.
3. `publishers`: Casas editoriales de los libros.
4. `ratings`: Calificaciones numéricas (1 a 5 estrellas) otorgadas por los usuarios.
5. `reviews`: Reseñas cualitativas en formato de texto escritas por los usuarios.

## 🔍 Consultas Estratégicas Resueltas
El cuaderno contiene la lógica optimizada para resolver las siguientes necesidades de negocio:
* **Métrica 1:** Conteo de libros publicados después del 1 de enero de 2000.
* **Métrica 2:** Cálculo del número de reseñas y la calificación promedio para cada libro del catálogo.
* **Métrica 3:** Identificación de la editorial líder en contenido relevante (libros con más de 50 páginas).
* **Métrica 4:** Encontrar al autor con la calificación promedio más alta (filtrando por volumen mínimo mediante `HAVING`).
* **Métrica 5:** Determinar el número promedio de reseñas de texto entre los usuarios más activos (*Power Users*) usando Expresiones de Tabla Comunes (CTEs con `WITH`) y `LEFT JOIN`.

## 🖥️ Nota de Ingeniería y Reproduducibilidad
Para asegurar que este repositorio sea **Ejecutable y autónomo**, la arquitectura se migró a un entorno local basado en **SQLite**. El cuaderno incluye un pipeline que inicializa las tablas con datos de muestra idénticos en estructura a la base de producción, permitiendo ejecutar todas las consultas avanzadas en tiempo real.