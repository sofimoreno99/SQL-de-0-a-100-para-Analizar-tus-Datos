### SQL-de-0-a-100-para-Analizar-tus-Datos

# ¿Qué es SQL?
SQL es un acrónimo en inglés para Structured Query Language.  Un Lenguaje de Consulta Estructurado. Un tipo de lenguaje de programación que te permite manipular y descargar datos de una base de datos y es el lenguaje utilizado por la mayoría de los Sistemas Gestores de Bases de Datos Relacionales  (SGBDR) .Este tipo de lenguaje de programación permite comunicarse con la base de datos y realizar operaciones de acceso y manipulación de la información almacenada.

El lenguaje de programación SQL no solo permite realizar operaciones de selección, inserción, actualización y eliminación de datos sino también operaciones administrativas sobre las bases de datos. Por tanto, se trata de un lenguaje completo de bases de datos que va más allá de la recuperación de la información.

El SQL se usa para controlar todas las funciones que un sistema gestor de base de datos brinda a sus usuarios, proporcionando además un marco para crear la propia base de datos, gestionar su seguridad, actualizar sus contenidos, recuperar los datos y compartirlos entre diferentes usuarios.

De hecho, la mayoría de los sistemas de gestión de base de datos relacionales usan el lenguaje de programación SQL para interactuar con la base de datos. Hyay vatios Sistemas Gestores de Bases de Datos, entre las mas conocidas se encuentran: Oracle, Microsoft SQL, MySQL y Access.

El lenguaje SQL se divide en tres subconjuntos de instrucciones, según la funcionalidad de éstas:

- DML (Data Manipulation Language – Lenguaje de Manipulación de Datos): se encarga de la manipulación de los datos. Es lo que usamos de manera más habitual para consultar, generar o actualizar información.
- DDL (Data Definition Language – Lenguaje de Definición de Datos): se encarga de la manipulación de los objetos de la base de datos, por ejemplo, crear tablas u otros objetos.
- DCL (Data Control Language – Lenguaje de Control de Datos): se encarga de controlar el acceso a los objetos y a los datos, para que los datos sean consistentes y sólo puedan ser accedidos por quien esté autorizado a ello.
- TCL (Transactional Control Language- Lenguaje de Control Transaccional): Permite administrar diferentes transacciones que ocurren dentro de una base de datos.


# DML Manipulación de datos

- SELECT: Recupera datos de la base de datos.
La sintaxis básica de SELECT es:
SELECT lista de campos FROM nombre de la tabla
Si escribimos SELECT * FROM nombre de la tabla, se devuelven todos los registros de la tabla. 

- INSERT: Añade nuevas filas de datos a la base de datos.
La sintaxis básica de INSERT ES:
INSERT INTO nombre de la tabla (lista de campos) values(lista de valores)

- DELETE: Suprime filas de datos de la base de datos.
La sintaxis básica de DELETE es:
DELETE FROM nombre de la tabla WHERE condición que deben cumplir los registros que queremos borrar.

- UPDATE: Modifica datos existentes en la base de datos.
La sintaxis básica de UPDATE es:
UPDATE nombre de la tabla SET nombre del campo = valor nuevo WHERE condición que deben cumplir todos los registros que se modificarán.

# DDL Definición de datos

CREATE: Utilizado para crear nuevas tablas, campos e índices.
ALTER: Utilizado para modificar las tablas agregando campos o cambiando la definición de los campos.
DROP: Empleado para eliminar tablas e índices.
TRUNCATE: Empleado para eliminar todos los registros de una tabla.
COMMENT: Utilizado para agregar comentarios al diccionario de datos.
RENAME: Tal como su nombre lo indica es utilizado para renombrar objetos.

# DCL Control de datos

GRANT: permite otorgar permisos.
REVOKE: elimina los permisos que previamente se han concedido.

# TCL Control transaccional de datos

COMMIT: Empleado para guardar el trabajo hecho.
ROLLBACK: Utilizado para deshacer la modificación que hice desde el último COMMIT.

# Tipos de datos en SQL

Tipos de datos de texto
- CHAR (tamaño)	Tiene una cadena de longitud fija (puede contener letras, números y caracteres especiales). El tamaño fijo se especifica entre paréntesis. Puede almacenar hasta 255 caracteres
- VARCHAR (tamaño)	Tiene una cadena de longitud variable (puede contener letras, números y caracteres especiales). El tamaño máximo se especifica entre paréntesis. Puede almacenar hasta 255 caracteres. Nota: si agrega un valor mayor que 255, se convertirá en un tipo de texto
- TINYTEXT	Tiene una cadena con una longitud máxima de 255 caracteres
- TEXTO	Tiene una cadena con una longitud máxima de 65.535 caracteres
- BLOB	Para BLOB (Objetos grandes binarios). Almacena hasta 65.535 bytes de datos
- MEDIUMTEXT	Tiene una cadena con una longitud máxima de 16,777,215 caracteres
- MEDIUMBLOB	Para BLOB (Objetos grandes binarios). Tiene capacidad para 16.777.215 bytes de datos
- LONGTEXT	Tiene una cadena con una longitud máxima de 4.294.967.295 caracteres
- LONGBLOB	Para BLOB (Objetos grandes binarios). Tiene capacidad para 4.294.967.295 bytes de datos
- ENUM (x, y, z, etc.)	Permite ingresar una lista de valores posibles. Puede enumerar hasta 65535 valores en una lista ENUM. Si se inserta un valor que no está en la lista, se insertará un valor en blanco.


Tipos de datos numéricos

- TINYINT (tamaño)	-128 a 127 normal. 0 a 255 SIN FIRMAR *. La cantidad máxima de dígitos se puede especificar entre paréntesis
- SMALLINT (tamaño)	-32768 a 32767 normal. 0 a 65535 SIN FIRMAR *. La cantidad máxima de dígitos se puede especificar entre paréntesis
- MEDIUMINT (tamaño)	-8388608 a 8388607 normal. 0 a 16777215 SIN FIRMAR *. La cantidad máxima de dígitos se puede especificar entre paréntesis
- INT (tamaño)	-2147483648 a 2147483647 normal. 0 a 4294967295 SIN FIRMAR *. La cantidad máxima de dígitos se puede especificar entre paréntesis
- BIGINT (tamaño)	-9223372036854775808 a 9223372036854775807 normal. 0 a 18446744073709551615 SIN FIRMAR *. La cantidad máxima de dígitos se puede especificar entre paréntesis
- FLOAT (tamaño, d)	Un pequeño número con un punto decimal flotante. La cantidad máxima de dígitos se puede especificar en el parámetro de tamaño. El número máximo de dígitos a la derecha del punto decimal se especifica en el parámetro d
- DOBLE (tamaño, d)	Un número grande con un punto decimal flotante. La cantidad máxima de dígitos se puede especificar en el parámetro de tamaño. El número máximo de dígitos a la derecha del punto decimal se especifica en el parámetro d
- DECIMAL (tamaño, d)	Un DOBLE almacenado como una cadena, lo que permite un punto decimal fijo. La cantidad máxima de dígitos se puede especificar en el parámetro de tamaño. El número máximo de dígitos a la derecha del punto decimal se especifica en el parámetro d

Tipos de datos para fechas

- DATE ()	Una fecha. Formato: AAAA-MM-DD
Nota: el rango admitido es de '1000-01-01' a '9999-12-31'

- DATETIME ()	* Una combinación de fecha y hora. Formato: AAAA-MM-DD HH: MI: SS
Nota: el rango admitido es de '1000-01-01 00:00:00' a '9999-12-31 23:59:59'

- TIMESTAMP ()	* Una marca de tiempo. Los valores de TIMESTAMP se almacenan como el número de segundos desde la época de Unix ('1970-01-01 00:00:00' UTC). Formato: AAAA-MM-DD HH: MI: SS
Nota: el rango admitido es de '1970-01-01 00:00:01' UTC a '2038-01-09 03:14:07' UTC

- TIME ()	Un tiempo. Formato: HH: MI: SS
Nota: el rango admitido es de '-838: 59: 59' a '838: 59: 59'

- YEAR ()	Un año en formato de dos o cuatro dígitos.
Nota: Valores permitidos en formato de cuatro dígitos: de 1901 a 2155. Valores permitidos en formato de dos dígitos: 70 a 69, que representan los años de 1970 a 2069

# Datos de SQL

SQL no es sensible a mayúsculas: SELECT y select funcionan lo mismo.


## Objetos de las bases de datos

# Crear una base de datos
CREATE DATABASE nombre de base de datos
SHOW DATABASES: para ver todas las bases de datos que tenemos
USE: para usar una base de dato:
Sintaxis: USE nombre de base de dato

# Tablas

Sentencias para su creación, modificación y destrucción

- CREATE TABLE
Sintaxis: CREATE TABLE [dueño de la tabla].[nombre de la tabla]
(
[nombre del campo] [tipo del campo](longitud) NULL,
 ...
) 

Repasemos los elementos:
- Dueño de la tabla: Es el usuario que tendrá primariamente todos los derechos sobre la 
tabla que vamos a crear.
- Nombre de la tabla: Es el nombre por el que vamos a identificar a la tabla más adelante. 
Deberá ser único. (otra tabla deberá llamarse distinto)
- Nombre del campo: Es el nombre que vamos a dar a un campo. Debe ser único dentro de 
la tabla pero puede repetirse en otras tablas. Mi sugerencia es que al mismo atributo lo 
llamen siempre igual en todas las tablas en las que aparezca.
- Tipo del campo: Es el tipo de dato que vamos a guardar en ese campo. Distintos motores 
de bases de datos los organizan de diferentes maneras.

Parámetros opcionales:
 IF NOT EXISTS: Evita que se produzca un error si la tabla existe. Sin embargo, no
se verifica que la tabla existente tenga una estructura idéntica a la indicada por
el CREATE TABLE.
 LIKE: CREATE TABLE ... LIKE crea una tabla vacía basada en la definición de
otra tabla, incluidos los atributos e índices de columna definidos en la tabla original:
CREATE TABLE destino_tbl LIKE origen_tbl;
 NOT NULL | NULL: especifica si se acepta o no que el dato quede vacío. Si no se
especifica NULL ni NOT NULL, la columna se trata como si se hubiera especificado
NULL.
 DEFAULT: Especifica un valor predeterminado para una columna.
 AUTO_INCREMENT: El valor de la columna se imcrementa automáticamente a
medida que se suman registros.
 PRIMARY KEY: se declara implícitamente como NOT NULL.
 UNIQUE: Un índice UNIQUE crea una restricción tal que todos los valores del
índice deben ser distintos. Se produce un error si intenta agregar una nueva fila
con un valor clave que coincide con una fila existente. Un índice UNIQUE sólo
permite múltiples valores NULL para las columnas que pueden contener NULL.
 FOREIGN KEY: Permiten realizar referencias cruzadas de datos relacionados
entre tablas, que ayudan a mantener la coherencia de estos datos dispersos.


- ALTER TABLE
Sintaxis: ALTER TABLE [dueño de la tabla].[nombre de la tabla]
(
[nombre del campo] [tipo del campo](longitud) NULL,
 ..)
 
 Podemos realizar distintas acciones como
●	ALTER TABLE … RENAME… 
●	ALTER TABLE … DROP COLUMN… 
●	ALTER TABLE … DROP PRIMARY KEY…
●	ALTER TABLE … ADD… 
●	ALTER TABLE … ADD…AFTER… 
●	ALTER TABLE … ADD…FIRST; 
●	ALTER TABLE … ADD…PRIMARY KEY… 
●	ALTER TABLE … MODIFY COLUMN…
●	ALTER TABLE … ADD column_name datatype;
●	ALTER TABLE … DROP column_name;
●	ALTER TABLE … ADD INDEX [name](column, …);
●	ALTER TABLE … ADD PRIMARY KEY (column_name,…);
●	ALTER TABLE … DROP PRIMARY KEY (column_name,…);
●	ALTER TABLE...MODIFY COLUMN ... INT auto_increment;

  - DROP TABLE
Sintaxis: DROP TABLE dueño de la tabla.nombre de la tabla

Al borrarla desaparecen tanto los datos como la estructura

- TRUNCATE TABLE
Sintaxis:TRUNCATE TABLE dueño de la tabla.nombre de la tabla

Se utiliza para borrar todo el contenido de una tabla pero sin tocar la estructura.

# Insertar filas en una tabla
INSERT INTO… VALUES(…)

INSERT INTO… SET…


# Consultando datos de una tabla

Utilizamos la funcion SELECT, junto con diferentes comandos como: 

- SELECT DISTINCT: se utiliza cuando deseamos obtener simplemente una lista de los valores diferentes (distintos), en una base de datos con duplicados.
Sintaxis: SELECT DISTINCT lista de campos FROM nombre de tabla; 

- SELECT ...FROM... WHERE: el comando WHERE se utiliza cuando deseamos realizar una consulta que cumpla con uno o mas criterios determinados. 
Para especificar dos condiciones que deseamos que se cumplan utilizamos el comando AND, la sintaxis es la siguiente: 
SELECT ... FROM... WHERE.... AND.....
Para especificar dos condiciones en la que deseamos que por lo menos una se cumpla utilizamos el comando OR, la sintaxis es la siguiente: 
SELECT ... FROM... WHERE.... OR.....

- SELECT... FROM... WHERE...ORDER BY... ASC/DESC : ORDER BY nos indica como ordenar la consulta. Puede ser ASC- DESC.
- SELECT... COUNT... WHERE


LENGTH(): nos devuelve la longitud de los valores de los campos de texto.
Sintaxis: SELECT ..., LENGTH(expresion) FROM .... 

SUBSTR(): nos devuelve una subserie de una serie.
Sintaxis: SUBSTR(expresion,posicion_de_inicio,longitud) 

TRIM(): se utiliza para eliminar un prefijo o sufijo determinado de una cadena. El patrón más común a eliminarse son los espacios en blanco.
Sintaxis: SELECT TRIM(expresion) AS ... FROM...

CAST(): nos sirve para transformar uno o más valores de un tipo de datos a otro.
Sintaxis: CAST ( Expresion_de_origen AS tipo_de_dato (lenght) ) 

CONCAT(): permite concatenar cadenas, columnas o valores sin límite, de forma que el resultado siempre será una cadena de textos con todos los valos introducidos.
Sintaxis: CONCAT ( cadena1, cadena2 );
Si queremos que entre medio de ambas cadenas vaya un espacio podemos colocar la siguiente sintaxis:
Sintaxis: CONCAT ( cadena1," ", cadena2 );

COALESCE(): ayuda a estimar y devolver el primer valor NO NULO del conjunto de datos o base de datos.
Sintaxis: COALESCE (expresiones) 

CASE(): compara 2 o más valores y devuelve un resultado.
Sintaxis: case VALORACOMPARAR
  when VALOR1 then RESULTADO1
  when VALOR2 then RESULTADO2
  ...
  else RESULTADO3
 end
 Puedo usar tambien END AS .... especificando la columna donde quiero ver los resultados. 



