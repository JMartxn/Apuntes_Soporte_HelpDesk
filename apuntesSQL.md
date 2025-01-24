# **Apuntes de SQL**

## **Inicio a este lenguaje y entorno.**

SQL (Structured Query Language) tiene diferentes dialectos y extensiones desarrollados por proveedores de bases de datos para adaptarse a sus plataformas. Aunque todos comparten una base común de funcionalidades, cada uno introduce características específicas para optimizar y extender sus capacidades. A continuación, se presentan algunos de los lenguajes y dialectos más destacados de SQL:

---

### **1\. Lenguajes principales en SQL**

SQL se divide en varios sublenguajes según el propósito de las operaciones que realizan:

* **DDL (Data Definition Language)**:  
  Define la estructura de la base de datos y los objetos asociados (tablas, índices, vistas, etc.).  
  * Comandos principales: `CREATE`, `ALTER`, `DROP`, `TRUNCATE`.  
* **DML (Data Manipulation Language)**:  
  Maneja los datos dentro de las tablas.  
  * Comandos principales: `SELECT`, `INSERT`, `UPDATE`, `DELETE`.  
* **DQL (Data Query Language)**:  
  Es un subconjunto de DML que se centra en la consulta de datos.  
  * Comando principal: `SELECT`.  
* **DCL (Data Control Language)**:  
  Administra permisos y el control de acceso a la base de datos.  
  * Comandos principales: `GRANT`, `REVOKE`.  
* **TCL (Transaction Control Language)**:  
  Gestiona las transacciones para garantizar la integridad de los datos.  
  * Comandos principales: `COMMIT`, `ROLLBACK`, `SAVEPOINT`.

---

### **2\. Dialectos de SQL por proveedores**

* **MySQL/MariaDB**:  
  Orientado a rendimiento, con soporte para extensiones como `LIMIT` en consultas.  
  * Ejemplo: `SELECT * FROM tabla LIMIT 10;`  
* **PostgreSQL**:  
  Altamente compatible con el estándar SQL y con extensiones avanzadas para manejo de JSON, índices GIN/GiST, y procedimientos almacenados.  
  * Ejemplo: `SELECT to_json(tabla) FROM tabla;`  
* **Microsoft SQL Server (T-SQL)**:  
  Añade características como procedimientos almacenados avanzados, manejo de variables, y `WITH` para CTE (Common Table Expressions).  
  * Ejemplo: `SELECT TOP 10 * FROM tabla;`  
* **Oracle SQL (PL/SQL)**:  
  Proporciona potentes herramientas para el manejo de procedimientos almacenados y triggers.  
  * Ejemplo: `SELECT * FROM tabla WHERE ROWNUM <= 10;`  
* **SQLite**:  
  Diseñado para ser ligero y sin configuración, utilizado en aplicaciones móviles y de escritorio.  
  * Ejemplo: `SELECT * FROM tabla LIMIT 10;`  
* **IBM Db2 SQL**:  
  Orientado a grandes entornos empresariales, con características para manejo de datos distribuidos.  
* **Snowflake SQL**:  
  Diseñado para análisis de datos en la nube, con escalabilidad y soporte para SQL analítico.

---

### **3\. Otros Dialectos Especializados**

* **Amazon Redshift SQL**: Para análisis de datos en el entorno de Amazon Web Services.  
* **Google BigQuery SQL**: Optimizado para análisis de grandes volúmenes de datos en la nube.  
* **ClickHouse SQL**: Enfocado en consultas analíticas de alta velocidad.

Cada dialecto se adapta a diferentes escenarios, por lo que la elección depende de las necesidades de la aplicación o entorno empresarial.

## **Principales RDBMS \- ORACLE vs MySQL**

Oracle SQL y MySQL son sistemas de gestión de bases de datos relacionales (RDBMS), pero tienen diferencias importantes en diseño, características y casos de uso. Aquí está un desglose de las diferencias clave entre ellos:  
---

### **1\. Propósito y Escenarios de Uso**

* **Oracle SQL**:  
  * Orientado a grandes empresas y entornos complejos que requieren alta disponibilidad, escalabilidad y características avanzadas.  
  * Ideal para sistemas críticos, aplicaciones financieras, y manejo de transacciones a gran escala.  
  * Requiere una licencia paga (aunque tiene una versión gratuita limitada llamada Oracle XE).  
* **MySQL**:  
  * Popular en aplicaciones web y sistemas pequeños o medianos.  
  * Muy utilizado en soluciones de código abierto y startups debido a su simplicidad y menor costo.  
  * Gratuito bajo la licencia GPL, aunque también tiene una versión comercial.

---

### **2\. Lenguaje y Funcionalidades**

* **Soporte de Procedimientos Almacenados y PL/SQL (Oracle)**:  
  * Oracle utiliza **PL/SQL** (Procedural Language SQL), un lenguaje completo para crear procedimientos almacenados, funciones, y triggers con lógica avanzada.  
  * MySQL soporta procedimientos almacenados, pero su funcionalidad es limitada en comparación con PL/SQL.  
* **Manipulación de Datos**:  
  * Oracle tiene soporte avanzado para **particionamiento de tablas**, **índices bitmap**, y **clustering** para optimización del rendimiento.  
  * MySQL utiliza principalmente índices B-tree y es menos avanzado en el manejo de datos a gran escala.  
* **Jerarquías y Consultas Recursivas**:  
  * Oracle soporta **connect by** y consultas recursivas avanzadas para manejar jerarquías.  
  * MySQL agregó soporte para **WITH RECURSIVE** en versiones más recientes, pero su implementación es básica.

---

### **3\. Tipos de Datos**

* Oracle tiene una variedad más amplia de tipos de datos, como:  
  * **RAW, CLOB, BLOB, NCLOB** para datos multimedia o binarios.  
  * Manejo nativo de **XML** y **JSON**.  
* MySQL ofrece tipos de datos básicos, pero ha mejorado con soporte nativo para JSON desde la versión 5.7.

---

### **4\. Transacciones y Concurrencia**

* **Oracle**:  
  * Tiene un modelo de **control multiversión (MVCC)** más avanzado, que garantiza consistencia incluso en transacciones de larga duración.  
  * Incluye soporte para **bloqueos de nivel fila** más granular.  
* **MySQL**:  
  * Utiliza el motor de almacenamiento **InnoDB** para MVCC, pero su implementación es menos robusta.  
  * El manejo de transacciones y concurrencia es suficiente para aplicaciones comunes, pero no tan avanzado como Oracle.

---

### **5\. Seguridad**

* **Oracle**:  
  * Ofrece características avanzadas como **Virtual Private Database (VPD)**, **Data Masking**, y **Transparent Data Encryption (TDE)**.  
  * Ideal para cumplir con regulaciones estrictas de seguridad (como GDPR o PCI DSS).  
* **MySQL**:  
  * Proporciona seguridad básica con permisos de usuario y SSL para conexiones cifradas.  
  * Las funciones avanzadas de seguridad suelen requerir configuraciones adicionales.

---

### **6\. Rendimiento**

* **Oracle**:  
  * Diseñado para optimizar cargas de trabajo mixtas (OLTP y OLAP).  
  * Funciones avanzadas como paralelismo, optimización basada en costos (CBO), y particionamiento dinámico.  
* **MySQL**:  
  * Más ligero y rápido para cargas de trabajo simples o aplicaciones pequeñas.  
  * Depende de configuraciones manuales para manejar cargas pesadas de manera eficiente.

---

### **7\. Ecosistema y Herramientas**

* **Oracle**:  
  * Herramientas avanzadas como Oracle Enterprise Manager, Data Pump, y soporte para replicación en tiempo real.  
  * Integración nativa con otras herramientas empresariales de Oracle (ERP, CRM).  
* **MySQL**:  
  * Ecosistema más sencillo, con herramientas populares como **phpMyAdmin**, **Workbench**, y compatibilidad con sistemas de código abierto.

---

### **8\. Costo**

* **Oracle**:  
  * Altamente costoso en licencias y mantenimiento, pero con un sólido retorno de inversión para grandes empresas.  
* **MySQL**:  
  * Gratuito para la mayoría de los casos (edición Community). La edición comercial tiene costos, pero sigue siendo más económica que Oracle.

---

### **9\. Comunidad y Soporte**

* **MySQL**:  
  * Amplia comunidad de código abierto con una gran cantidad de recursos gratuitos.  
* **Oracle**:  
  * Soporte empresarial formal y comunidad técnica activa, pero menos accesible para desarrolladores individuales.

---

### **Resumen**

| Característica | Oracle SQL | MySQL |
| ----- | ----- | ----- |
| **Complejidad** | Avanzado y robusto | Sencillo y ligero |
| **Coste** | Licencia paga | Gratuito (GPL) |
| **Rendimiento** | Ideal para grandes volúmenes | Mejor para sistemas pequeños |
| **Seguridad** | Avanzada (TDE, VPD, etc.) | Básica |
| **Transacciones** | Más sólido y avanzado | Suficiente para aplicaciones |
| **Casos de uso** | Empresas, finanzas, gobierno | Aplicaciones web y startups |

La elección entre Oracle SQL y MySQL depende del tamaño del proyecto, el presupuesto y los requerimientos específicos del sistema.

## **Ejemplo de código sql para mySQL.**

```sql
-- Crear la base de datos
CREATE DATABASE holamundo;

-- Mostrar bases de datos
SHOW DATABASES;

-- Usar la base de datos recién creada
USE holamundo;

-- Crear la tabla animales
CREATE TABLE animales (
  id INT,
  tipo VARCHAR(255),
  estado VARCHAR(255),
  PRIMARY KEY (id)
);

-- Insertar datos en la tabla
INSERT INTO animales (tipo, estado) VALUES ('Chanchito','feliz');

-- Modificar la columna id para que sea autoincrementable
ALTER TABLE animales MODIFY COLUMN id INT AUTO_INCREMENT;

-- Ver la estructura de la tabla
SHOW CREATE TABLE animales;

-- Crear la tabla animales con autoincremento para id
CREATE TABLE `animales` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `tipo` VARCHAR(255) DEFAULT NULL,
  `estado` VARCHAR(255) DEFAULT NULL,
  PRIMARY KEY (`id`)
);

-- Insertar más datos en la tabla
INSERT INTO animales (tipo, estado) VALUES ('Chanchito','feliz');
INSERT INTO animales (tipo, estado) VALUES ('dragon','feliz');
INSERT INTO animales (tipo, estado) VALUES ('felipe','feliz');

-- Consultas SELECT
SELECT * FROM animales;

-- Consultas con condiciones WHERE
SELECT * FROM animales WHERE id=1;
SELECT * FROM animales WHERE estado = 'feliz';
SELECT * FROM animales WHERE estado = 'feliz' AND tipo = 'chanchito';

-- Actualizar el estado de un animal
UPDATE animales SET estado = 'superfeliz' WHERE id = 3;

-- Eliminar un animal
DELETE FROM animales WHERE id=2;

-- Nota: Para el comando DELETE y UPDATE es necesario especificar un id para evitar errores masivos.



He ampliado la tabla con más ejemplos de tipos de combinaciones (joins) y similares. Aquí está la versión actualizada:

| Funcionalidad | Consulta | Descripción |
| ----- | ----- | ----- |
| **Seleccionar todos los datos** | `SELECT * FROM nombre_tabla;` | Devuelve todos los registros de la tabla. |
| **Seleccionar columnas específicas** | `SELECT columna1, columna2 FROM nombre_tabla;` | Devuelve solo las columnas indicadas. |
| **Filtrar datos con `WHERE`** | `SELECT * FROM nombre_tabla WHERE columna = 'valor';` | Filtra los resultados según la condición especificada. |
| **Ordenar resultados** | `SELECT * FROM nombre_tabla ORDER BY columna ASC; SELECT * FROM nombre_tabla ORDER BY columna DESC;` | Ordena los resultados de manera ascendente o descendente. |
| **Limitar resultados** | `SELECT * FROM nombre_tabla LIMIT 10;` | Muestra solo el número indicado de registros. |
| **Insertar un registro** | `INSERT INTO nombre_tabla (columna1, columna2) VALUES ('valor1', 'valor2');` | Agrega un nuevo registro a la tabla. |
| **Insertar múltiples registros** | `INSERT INTO nombre_tabla (columna1, columna2) VALUES ('valor1', 'valor2'), ('valor3', 'valor4');` | Agrega varios registros a la tabla en una sola consulta. |
| **Actualizar registros** | `UPDATE nombre_tabla SET columna1 = 'nuevo_valor' WHERE columna2 = 'valor';` | Modifica los valores de una o más columnas en registros específicos. |
| **Eliminar registros** | `DELETE FROM nombre_tabla WHERE columna = 'valor';` | Elimina los registros que cumplan con la condición especificada. |
| **Contar registros** | `SELECT COUNT(*) FROM nombre_tabla;` | Devuelve el número total de registros en la tabla. |
| **Agrupar datos** | `SELECT columna, COUNT(*) FROM nombre_tabla GROUP BY columna;` | Agrupa los registros según una columna y aplica una función de agregación. |
| **Unir tablas (INNER JOIN)** | `SELECT a.columna1, b.columna2 FROM tabla1 a INNER JOIN tabla2 b ON a.id = b.id;` | Une dos tablas mostrando solo las coincidencias. |
| **Unión externa izquierda (LEFT JOIN)** | `SELECT a.columna1, b.columna2 FROM tabla1 a LEFT JOIN tabla2 b ON a.id = b.id;` | Devuelve todos los registros de la tabla izquierda y las coincidencias de la derecha. |
| **Unión externa derecha (RIGHT JOIN)** | `SELECT a.columna1, b.columna2 FROM tabla1 a RIGHT JOIN tabla2 b ON a.id = b.id;` | Devuelve todos los registros de la tabla derecha y las coincidencias de la izquierda. |
| **Unión completa (FULL OUTER JOIN)** | `SELECT a.columna1, b.columna2 FROM tabla1 a FULL OUTER JOIN tabla2 b ON a.id = b.id;` | Devuelve todos los registros de ambas tablas, incluso si no hay coincidencias. |
| **Unión cruzada (CROSS JOIN)** | `SELECT a.columna1, b.columna2 FROM tabla1 a CROSS JOIN tabla2 b;` | Devuelve el producto cartesiano de ambas tablas. |
| **Unión automática (USING)** | `SELECT * FROM tabla1 JOIN tabla2 USING (columna_común);` | Une dos tablas automáticamente en función de una columna común. |
| **Subconsultas** | `SELECT columna1 FROM tabla1 WHERE columna2 IN (SELECT columna3 FROM tabla2);` | Usa los resultados de una consulta dentro de otra. |
| **Consultas con `EXISTS`** | `SELECT * FROM tabla1 WHERE EXISTS (SELECT * FROM tabla2 WHERE tabla1.id = tabla2.id);` | Verifica si existe al menos un registro en una subconsulta. |
| **Eliminar duplicados** | `SELECT DISTINCT columna FROM nombre_tabla;` | Devuelve resultados únicos, eliminando duplicados. |
| **Combinar resultados (`UNION`)** | `SELECT columna1 FROM tabla1 UNION SELECT columna2 FROM tabla2;` | Combina los resultados de dos consultas y elimina duplicados. |
| **Combinar resultados con duplicados (`UNION ALL`)** | `SELECT columna1 FROM tabla1 UNION ALL SELECT columna2 FROM tabla2;` | Combina los resultados de dos consultas, incluyendo duplicados. |
| **Crear tabla** | `CREATE TABLE nombre_tabla (id INT PRIMARY KEY, columna1 VARCHAR(50), columna2 INT);` | Crea una nueva tabla con las columnas especificadas. |
| **Eliminar tabla** | `DROP TABLE nombre_tabla;` | Elimina completamente la tabla y sus datos. |

La **normalización** en bases de datos es un proceso para organizar la información en tablas, evitando redundancias y asegurando que los datos estén correctamente relacionados. Esto ayuda a que la base de datos sea eficiente, fácil de mantener y menos propensa a errores.

### **Reglas básicas de normalización:**

1. **Primera forma normal (1FN):**  
   * Cada columna debe contener un único valor (no listas ni conjuntos).  
   * Todas las filas deben ser únicas y tener un identificador (clave primaria).  
     **Ejemplo malo:**  
     | ID | Nombre | Teléfonos |  
     |-----|------------|------------------|  
     | 1 | Juan | 123, 456 |  
     **Ejemplo bueno:**  
     | ID | Nombre | Teléfono |  
     |-----|------------|------------------|  
     | 1 | Juan | 123 |  
     | 1 | Juan | 456 |

---

2. **Segunda forma normal (2FN):**  
   * Cumple 1FN.  
   * Los datos que no dependen de la clave primaria se separan en otra tabla.  
     **Ejemplo malo:**  
     | Pedido\_ID | Cliente | Dirección | Producto |  
     |-----------|------------|---------------|-----------|  
     | 1 | Ana | Calle 1 | Laptop |  
     | 2 | Ana | Calle 1 | Teclado |  
     **Ejemplo bueno:**  
     **Clientes:**  
     | Cliente\_ID | Nombre | Dirección |  
     |------------|---------|------------|  
     | 1 | Ana | Calle 1 |  
     **Pedidos:**  
     | Pedido\_ID | Cliente\_ID | Producto |  
     |-----------|------------|-----------|  
     | 1 | 1 | Laptop |  
     | 2 | 1 | Teclado |

---

3. **Tercera forma normal (3FN):**  
   * Cumple 2FN.  
   * Ningún dato debe depender de algo que no sea la clave primaria.  
     **Ejemplo malo:**  
     | ID | Producto | Categoría | Categoría\_Descripción |  
     |------|-----------|-----------|-----------------------|  
     | 1 | Laptop | 101 | Electrónica |  
     | 2 | Teclado | 101 | Electrónica |  
     **Ejemplo bueno:**  
     **Productos:**  
     | Producto\_ID | Producto | Categoría\_ID |  
     |-------------|-----------|--------------|  
     | 1 | Laptop | 101 |  
     | 2 | Teclado | 101 |  
     **Categorías:**  
     | Categoría\_ID | Categoría\_Descripción |  
     |--------------|-----------------------|  
     | 101 | Electrónica |

---

### **Resumen rápido:**

* **1FN:** Cada celda debe tener un solo valor.  
* **2FN:** Elimina datos repetidos y separa tablas relacionadas.  
* **3FN:** Asegúrate de que cada dato dependa directamente de la clave primaria, no de otros datos.

