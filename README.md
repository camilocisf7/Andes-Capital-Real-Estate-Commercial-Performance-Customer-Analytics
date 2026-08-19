# Andes-Capital-Real-Estate-Commercial-Performance-Customer-Analytics

##  Tabla de contenidos

- [Resumen ejecutivo](#-resumen-ejecutivo)

- [Objetivo del proyecto](#-objetivo-del-proyecto)

- [Preguntas de negocio](#-preguntas-de-negocio)

- [Datos](#-datos)

  - [Tabla de hechos: Ventas](#tabla-de-hechos-ventas)

  - [Dimensión de clientes](#dimensión-de-clientes)

  - [Dimensión de propiedades](#dimensión-de-propiedades)

  - [Dimensión de fechas](#dimensión-de-fechas)

- [Preparación y validación de datos](#-preparación-y-validación-de-datos)

- [Modelo de datos](#-modelo-de-datos)

- [Análisis y métricas](#-análisis-y-métricas)

  - [Indicadores comerciales](#indicadores-comerciales)

  - [Análisis temporal](#análisis-temporal)

  - [Análisis de clientes](#análisis-de-clientes)

  - [Análisis de propiedades](#análisis-de-propiedades)

- [Dashboard](#-dashboard)

  - [Resumen ejecutivo](#resumen-ejecutivo)

  - [Desempeño comercial](#desempeño-comercial)

  - [Clientes y recurrencia](#clientes-y-recurrencia)

- [Principales insights](#-principales-insights)

- [Recomendaciones](#-recomendaciones)

- [Estructura del proyecto](#-estructura-del-proyecto)

- [Cómo visualizar el proyecto](#-cómo-visualizar-el-proyecto)

- [Herramientas utilizadas](#-herramientas-utilizadas)

- [Sobre mí](#-sobre-mí)


**Objetivo**
Andes Capital Real Estate necesitaba una visión más clara de su desempeño comercial para identificar los principales generadores de ingresos, entender el comportamiento de sus clientes y detectar oportunidades de crecimiento y recurrencia.

**DataSet**
| Tabla | Contenido | Uso en el análisis|
| -------- | -------- | -------- |
| hecho_ventas_propiedades| Transacciones de venta | Ingresos, ventas y comisiones |
| dim_clientes| Información de clientes | Segmentación y recurrencia |
| dim_propiedades | Características de propiedades | Marketing analysis |
| User activity| User events and timestamps | Análisis de propiedades |
| dim_fecha| Calendario | Tendencias e inteligencia temporal |

**Granularidad**

Cada fila de hecho_ventas_propiedades representa una transacción individual de venta de una propiedad.

**Preparación de datos**
* Validación de tipos de datos.
* Identificación de valores nulos.
* Detección de registros duplicados.
* Validación de identificadores únicos.
* Comprobación de relaciones entre la tabla de hechos y las dimensiones.
* Validación de fechas de venta.
* Revisión de valores numéricos como precios y comisiones.
* Creación de una tabla calendario.
* Validación de los cálculos de comisión.
* Estandarización de categorías cuando fue necesario.

* Se verificó que el monto_comision fuera consistente con el precio_venta y el porcentaje_comision, evitando utilizar métricas de comisión potencialmente inconsistentes en el análisis.

**Modelo de datos**

Se construyó un modelo de datos en esquema estrella, utilizando hecho_ventas_propiedades como tabla de hechos y dim_clientes, dim_propiedades y dim_fecha como dimensiones.

****Métricas****

**Indicadores comerciales**

* Ingresos totales
* Número de ventas
* Precio promedio de venta
* Comisión total
* Comisión promedio
* Clientes únicos

**Inteligencia temporal**

* Ingresos YTD
* Ingresos MTD
* Crecimiento YoY
* Variación YoY
* Evolución mensual

**Clientes**

* Clientes nuevos
* Clientes recurrentes
* Tasa de recompra
* Número de compras por cliente

**Visualization**
* Built an executive dashboard in Tableau.
* Created KPI cards and business-focused visualizations.
* Highlighted conversion, profitability and customer behavior.

**Insights**

Por canal: Corredor concentra 72,7% de ventas e ingresos (proporcional), pero su comisión promedio es 4,0% contra 1,5% de Directo — $176M en comisiones vs $24,5M, pese a que Corredor solo genera 2,7x más ingresos que Directo. Ahí hay una historia de rentabilidad neta, no solo de ingresos brutos.

Por segmento de comprador: Primera vez lidera con 62,4% de ventas y 62,9% de ingresos; Inversionista 24,6%/24,5%; Alto patrimonio 13%/12,6% — participación bastante proporcional entre segmentos, sin distorsiones grandes.

Por ciudad: Bogotá tiene más ventas (4.377 vs 4.123) pero Ciudad de México genera más ingresos ($3.242M vs $2.770M) — ticket promedio más alto en CDMX ($786K vs $633K).

Estacionalidad y crecimiento: el patrón se repite en ambos años — picos en marzo-abril y septiembre-noviembre, valles en enero-febrero y mitad de año. 2024 cerró en ~$3.165M vs ~$2.848M en 2023, +11,1% interanual

**Recomendaciones**
El canal Corredor genera 72,7% de los ingresos pero se lleva $176M en comisiones (4,0% promedio) contra solo $24,5M de Directo (1,5%). Eso es 7,2x más costo por apenas 2,7x más ingreso.

Recomendación: evaluar reducir el % de comisión en tramos altos de precio, o incentivar más el canal Directo con herramientas digitales — cada punto porcentual que se mueva de Corredor a Directo libera margen directo.

Departamento es 60% de las ventas pero solo 30,7% de los ingresos (ticket promedio $362K vs $1,8M en Comercial).

Recomendación: si el objetivo es crecer ingresos, priorizar esfuerzo comercial en Casa y Comercial, que tienen mejor ingreso por operación. Si el objetivo es volumen/liquidez de inventario, Departamento sigue siendo el motor.

**Sobre mí**
Camilo Q. Franco — Economista & Data Analyst

Economista con formación en análisis de datos, inteligencia de negocios y análisis cuantitativo. Experiencia utilizando SQL, Python, R, Tableau, Power BI y Excel para transformar datos en insights que apoyan la toma de decisiones empresariales.
