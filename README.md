# RetailPro --- Análisis de ventas y rendimiento comercial

## Descripción del proyecto

RetailPro es una cadena de tiendas de retail que comercializa productos
de distintas categorías ---como tecnología, indumentaria y hogar--- a
través de canales físicos y online.

Este proyecto tiene como propósito centralizar y analizar la información
histórica de ventas para ofrecer a la dirección comercial una visión
clara del rendimiento del negocio. A través de consultas SQL, un proceso
de ETL y un dashboard interactivo en Power BI, se busca transformar los
datos operativos en información útil para la toma de decisiones.

El análisis contempla el comportamiento mensual de las ventas, el
desempeño de productos y categorías, y los patrones de compra de los
clientes.

## Objetivos del negocio

-   **Monitorear el rendimiento comercial:** analizar la evolución
    mensual de la facturación y el volumen de pedidos.
-   **Identificar productos destacados:** reconocer los productos con
    mayor facturación y cantidad de unidades vendidas.
-   **Analizar categorías:** comparar el desempeño comercial de las
    distintas categorías de productos.
-   **Conocer a los clientes:** explorar el comportamiento de compra y
    la distribución de las ventas según características de los clientes.
-   **Mejorar la toma de decisiones:** brindar información que permita
    orientar acciones comerciales, promociones y decisiones de stock.

## Alcance del proyecto

El trabajo se organiza en tres etapas principales:

1.  **Base de datos y análisis con SQL.** Se utilizan consultas para
    filtrar registros, agrupar información, aplicar condiciones sobre
    agregaciones y relacionar las tablas de ventas, clientes y
    productos.
2.  **Proceso ETL y modelado en Power BI.** Se prepara la información
    mediante Power Query: revisión de tipos de datos, limpieza,
    eliminación de duplicados y tratamiento de los valores nulos.
3.  **Dashboard interactivo.** Se construye un reporte en Power BI con
    indicadores comerciales y visualizaciones que facilitan el análisis
    de los resultados.

## Tecnologías utilizadas

  -----------------------------------------------------------------------
  Tecnología   Y                        Uso en el proyecto
  ----------------------------------------------------------------------
  SQL Server:                          Consulta, filtrado, agregación y
                                      combinación de datos relacionales.

  Power BI Desktop:                    Modelado, análisis y visualización
                                      de los datos.

  Power Query:                         Limpieza y transformación de datos
                                      durante el proceso ETL.

  GitHub:                               Control de versiones y
                                      documentación del proyecto.


## Estructura del repositorio

La siguiente estructura es una propuesta de organización. Ajustá los
nombres de carpetas y archivos para que coincidan con los que
efectivamente subas a GitHub.

``` text
RetailPro/
├── data/
│   └── README.md                 # Descripción de los datos y su origen
├── sql/
│   ├── 01_creacion_tablas.sql    # Creación o preparación de tablas
│   ├── 02_consultas_analisis.sql # Consultas analíticas
│   └── README.md                 # Orden de ejecución y descripción
├── powerbi/
│   └── RetailPro_Dashboard.pbix  # Reporte de Power BI
├── docs/
│   └── capturas_dashboard/       # Imágenes del dashboard
└── README.md
```

## Cómo ejecutar el proyecto

### 1. Requisitos previos

-   SQL Server y una herramienta para ejecutar consultas, como SQL
    Server Management Studio (SSMS).
-   Power BI Desktop.
-   Los archivos de datos y scripts incluidos en el repositorio, o las
    fuentes de datos configuradas para el proyecto.

### 2. Preparar la base de datos

1.  Cloná o descargá este repositorio.
2.  Abrí SQL Server Management Studio y conectate a la instancia
    correspondiente.
3.  Creá o seleccioná la base de datos de trabajo.
4.  Revisá los scripts de la carpeta `sql/`.
5.  Ejecutá primero el script de creación o preparación de tablas, si
    está incluido.
6.  Cargá los datos de origen siguiendo las instrucciones disponibles.
7.  Ejecutá las consultas analíticas en el orden indicado en los
    archivos.

Las consultas utilizan operaciones como `WHERE`, `GROUP BY`, `HAVING` e
`INNER JOIN` para filtrar, resumir y relacionar la información.

### 3. Abrir el dashboard en Power BI

1.  Abrí Power BI Desktop.
2.  Desde **Archivo \> Abrir**, seleccioná
    `powerbi/RetailPro_Dashboard.pbix`.
3.  Si Power BI solicita credenciales o rutas de origen, actualizá la
    conexión para que apunte a la ubicación de los datos disponible en
    tu entorno.
4.  Seleccioná **Actualizar** para cargar los datos transformados.
5.  Explorá las páginas, filtros e indicadores del reporte.

> Los nombres de archivos y rutas de esta guía son referenciales. Deben
> coincidir con la estructura real del repositorio antes de publicar el
> proyecto.

## Métricas e indicadores

El proyecto contempla indicadores para analizar distintas dimensiones
del rendimiento comercial. Entre las métricas consideradas se
encuentran:

-   **Facturación total:** importe total generado por las ventas en el
    período analizado.
-   **Cantidad de pedidos:** número de pedidos registrados.
-   **Ticket promedio:** facturación dividida por la cantidad de
    pedidos.
-   **Unidades vendidas:** cantidad total de productos vendidos.
-   **Facturación por producto:** importe generado por cada producto.
-   **Unidades vendidas por producto:** volumen de unidades
    comercializadas por producto.
-   **Facturación por categoría:** contribución de cada categoría a la
    facturación.
-   **Evolución mensual:** variación de la facturación y los pedidos a
    lo largo del tiempo.
-   **Análisis de clientes:** distribución de las ventas según los
    atributos disponibles de los clientes.

La disponibilidad de cada indicador depende de las columnas presentes en
las tablas y de las transformaciones realizadas.

## Hallazgos preliminares

A partir de los resultados de consultas compartidos durante el
desarrollo, se identificaron los siguientes puntos para el mes 3:

1.  **Resumen mensual:** se registró una facturación de **\$6.444**, con
    **10 pedidos** y un ticket promedio de **\$644,40**.
2.  **Productos con mayor facturación entre los registros mostrados:**
    el producto con ID 1 alcanzó **\$3.600**, seguido por el producto
    con ID 3, con **\$1.350**.
3.  **Mayor volumen de unidades:** el producto con ID 2 registró **13
    unidades vendidas**, aunque su facturación fue de **\$364**.

### Observación sobre la conciliación de importes

La suma de la facturación de los cinco productos incluidos en el
resultado compartido del ranking es **\$6.444**.

Los hallazgos son preliminares y corresponden únicamente a los
resultados disponibles. No permiten concluir qué productos o categorías
son más rentables en términos de ganancia, ya que para calcular
rentabilidad se necesitarían datos de costos y márgenes. La facturación
no equivale a la ganancia.

## Próximas mejoras

-   Incorporar comparaciones entre períodos para medir variaciones de
    facturación y pedidos.
-   Analizar el desempeño por canal de venta, si la fuente contiene esa
    dimensión.
-   Profundizar el análisis de clientes para identificar segmentos de
    mayor contribución.
-   Incorporar costos y márgenes para evaluar rentabilidad, además de
    facturación.
-   Documentar las reglas de transformación y las definiciones de cada
    KPI.

## Autor y estado del proyecto

**Proyecto:** RetailPro --- Análisis de ventas y rendimiento comercial\
**Estado:** Proyecto de análisis de datos en desarrollo.
