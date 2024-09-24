
# Cheatsheet de SQL

## 1. Consultas Básicas

- **Seleccionar datos:**
  ```sql
  SELECT columna1, columna2 FROM tabla;
  ```

- **Seleccionar todos los datos:**
  ```sql
  SELECT * FROM tabla;
  ```

- **Condiciones (WHERE):**
  ```sql
  SELECT * FROM tabla WHERE condicion;
  ```

## 2. Ordenar Resultados

- **Ordenar por una columna:**
  ```sql
  SELECT * FROM tabla ORDER BY columna ASC;  -- ASC para ascendente, DESC para descendente
  ```

## 3. Filtrado Avanzado

- **Operadores lógicos:**
  ```sql
  SELECT * FROM tabla WHERE condicion1 AND condicion2;
  SELECT * FROM tabla WHERE condicion1 OR condicion2;
  SELECT * FROM tabla WHERE NOT condicion;
  ```

- **Comparaciones:**
  ```sql
  SELECT * FROM tabla WHERE columna = valor;
  SELECT * FROM tabla WHERE columna BETWEEN valor1 AND valor2;
  SELECT * FROM tabla WHERE columna IN (valor1, valor2, ...);
  ```

## 4. Funciones de Agregación

- **Contar, sumar, promedio, máximo, mínimo:**
  ```sql
  SELECT COUNT(columna) FROM tabla;
  SELECT SUM(columna) FROM tabla;
  SELECT AVG(columna) FROM tabla;
  SELECT MAX(columna) FROM tabla;
  SELECT MIN(columna) FROM tabla;
  ```

## 5. Agrupación de Datos

- **Agrupar resultados:**
  ```sql
  SELECT columna, COUNT(*) FROM tabla GROUP BY columna;
  ```

- **Filtrar grupos:**
  ```sql
  SELECT columna, COUNT(*) FROM tabla GROUP BY columna HAVING COUNT(*) > 1;
  ```

## 6. Uniones

- **Unir tablas:**
  ```sql
  SELECT * FROM tabla1 JOIN tabla2 ON tabla1.columna = tabla2.columna;
  ```

- **Uniones externas:**
  ```sql
  SELECT * FROM tabla1 LEFT JOIN tabla2 ON tabla1.columna = tabla2.columna;  -- LEFT
  SELECT * FROM tabla1 RIGHT JOIN tabla2 ON tabla1.columna = tabla2.columna; -- RIGHT
  SELECT * FROM tabla1 FULL JOIN tabla2 ON tabla1.columna = tabla2.columna;  -- FULL
  ```

## 7. Insertar Datos

- **Insertar una fila:**
  ```sql
  INSERT INTO tabla (columna1, columna2) VALUES (valor1, valor2);
  ```

- **Insertar múltiples filas:**
  ```sql
  INSERT INTO tabla (columna1, columna2) VALUES (valor1, valor2), (valor3, valor4);
  ```

## 8. Actualizar Datos

- **Actualizar filas existentes:**
  ```sql
  UPDATE tabla SET columna1 = nuevo_valor WHERE condicion;
  ```

## 9. Eliminar Datos

- **Eliminar filas:**
  ```sql
  DELETE FROM tabla WHERE condicion;
  ```

## 10. Crear y Modificar Tablas

- **Crear tabla:**
  ```sql
  CREATE TABLE tabla (
      columna1 tipo,
      columna2 tipo,
      ...
  );
  ```

- **Agregar columna:**
  ```sql
  ALTER TABLE tabla ADD columna tipo;
  ```

- **Eliminar columna:**
  ```sql
  ALTER TABLE tabla DROP COLUMN columna;
  ```

## 11. Índices

- **Crear índice:**
  ```sql
  CREATE INDEX nombre_indice ON tabla (columna);
  ```

## 12. Comandos de Transacciones

- **Iniciar transacción:**
  ```sql
  BEGIN;
  ```

- **Confirmar cambios:**
  ```sql
  COMMIT;
  ```

- **Deshacer cambios:**
  ```sql
  ROLLBACK;
  ```

