# Análisis de Ventas Históricas: RetroData Games

Este es el segundo proyecto de mi portafolio profesional, enfocado en el sector de los videojuegos. 

## Objetivo del Proyecto
El objetivo fue analizar las ventas de videojuegos icónicos cruzando la información de los títulos con sus respectivas consolas. El reto principal fue conectar bases de datos separadas para extraer insights limpios y listos para la toma de decisiones.

## Herramientas Utilizadas
* **Python (Pandas):** Para estructurar los dataframes iniciales y simular el entorno del negocio.
* **SQL (SQLite):** Para realizar un cruce de tablas avanzado (`INNER JOIN`) utilizando llaves relacionales.
* **Seaborn:** Para el diseño de una gráfica de barras de alto impacto con la paleta de colores "magma".

## Descubrimientos Clave (Insights)

Gracias a la consulta SQL que construí, logramos consolidar la siguiente información:

* **El Juego más Vendido:** Wii Sports con 82.9 millones de copias vendidas.
* **Dominio de Mercado:** Al analizar las consolas, el gráfico muestra un claro dominio de la compañía Nintendo en el Top de ventas históricas de este reporte.

## 🚀 Código SQL Destacado
Este es el bloque de lógica relacional que diseñé para unir las tablas de juegos y consolas sin duplicar información:

```sql
SELECT tabla_juegos.Nombre_Juego, tabla_juegos.Ventas_Millones, tabla_consolas.Nombre_Consola
FROM tabla_juegos
INNER JOIN tabla_consolas ON tabla_juegos.ID_Consola = tabla_consolas.ID_Consola
