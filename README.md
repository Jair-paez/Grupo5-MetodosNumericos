# Modelo para el Analisis de factores que influyen en la popularidad de los videojuegos

## Informacion Academica
* Institucion: Escuela Politecnica Nacional EPN
* Materia: Metodos Numericos
* Semestre: 2026-A
* Fecha de entrega: 27 de mayo de 2026
* Estudiantes:
  * Ricardo Cisneros
  * Hugo Coyago
  * Jair Paez

---

## Descripcion del Proyecto
Este proyecto de investigacion academica tiene como objetivo aplicar herramientas de analisis numerico y modelamiento matematico para comprender la dinamica de exito de los videojuegos distribuidos en la plataforma Steam.

Para que el modelo matematico sea riguroso y tenga coherencia real, nos enfocaremos en un esquema multivariable libre de dependencias lineales y multicolinealidad, garantizando la inversion optima de matrices en el ajuste de curvas por minimos cuadrados. El modelo consta de exactamente una variable objetivo y diez variables independientes totalmente pobladas en nuestra base de datos.

### Variable Objetivo Eje Y
* estimated_owners: Ventas estimadas continuas obtenidas mediante el punto medio aritmetico del rango de compradores.

### Las Diez Variables Predictoras Independientes Eje X
1. price_usd: Precio de venta actual normalizado en dolares continuos.
2. steamspy_initial_price: Precio de venta inicial del videojuego antes de aplicar descuentos.
3. steamspy_discount: Porcentaje de descuento o rebaja activa en la tienda.
4. approval_ratio: Proporcionalidad de aprobacion continua de los usuarios en una escala de cero a uno.
5. reviews_total: Volumen total de opiniones y calificaciones registradas por la comunidad de Steam.
6. concurrent_users_yesterday: Usuarios activos simultaneos registrados el dia anterior.
7. is_free: Indicador binario discreto de gratuidad del producto donde uno es gratis y cero es de pago.
8. language_count: Cantidad total de idiomas de localizacion en los que esta disponible el software.
9. category_count: Cantidad total de caracteristicas tecnicas y modos de juego que ofrece el videojuego.
10. release_year: Ano de lanzamiento numerico extraido de la fecha de publicacion oficial.

---

## Distribucion y Estructura Organizativa
Para asegurar el orden, el rigor academico y la facilidad de revision, el proyecto esta estructurado bajo un esquema de carpetas numeradas. A continuacion se presenta el mapa visual de directorios:

```text
Proyecto/ - Raiz del repositorio
├── 01_Datos/
│   ├── Datos crudos/
│   │   └── steam-insights-main/
│   │       ├── games/
│   │       ├── reviews/
│   │       └── steamspy_insights/
│   ├── README.md - Diccionario de variables y especificaciones
│   └── steam_raw_unified_all_columns.csv - Dataset unificado final
├── 02_Codigo/
│   └── Codigo_Proyecto.ipynb - Jupyter Notebook principal secuencial
├── 03_Informe/
│   ├── Proyecto1_Grupo5.docx - Documento de Word con el avance del informe
│   └── Proyecto1_Grupo5_Respaldo.docx - Respaldo del documento original
├── 04_Presentacion/
│   └── .gitkeep - Archivo de soporte para la carpeta de diapositivas
├── 05_Referencias/
│   ├── material_curso/ - Diapositivas de clase, silabo y examenes previos
│   └── bibliografia.md - Referencias bibliograficas en formato APA
├── .gitignore - Control de exclusion de archivos grandes para GitHub
├── README.md - Este manual general del proyecto
└── Requisitos.txt - Lista de librerias y dependencias necesarias
```

### Descripcion de las Carpetas

1. 01_Datos/
   * Datos crudos/: Almacena los archivos originales sin procesar descargados de GitHub.
   * steam_raw_unified_all_columns.csv: Es el producto de la Parte 1 del codigo; un archivo plano consolidado con los datos unificados.
   * README.md: Explica columna por columna que significa cada variable en el dataset unificado.

2. 02_Codigo/
   * Contiene Codigo_Proyecto.ipynb, el notebook de Jupyter estructurado secuencialmente que realiza la unificacion, limpieza y los calculos numericos del modelo.

3. 03_Informe/
   * Almacena el reporte formal escrito bajo formato cientifico academico. Contiene el archivo Proyecto1_Grupo5.docx con la tabla de variables y la descripcion alineada.

4. 04_Presentacion/
   * Guardara las diapositivas disenadas para la defensa oral del proyecto.

5. 05_Referencias/
   * Contiene el archivo bibliografia.md con fuentes bibliograficas configuradas en formato APA y la carpeta material_curso para archivar los PDFs de teoria y examenes de Metodos Numericos.

---

## Guia Rapida para Replicacion

Este proyecto esta disenado para ser cien por ciento reproducible. Para ejecutar el codigo en cualquier computador, siga este procedimiento:

### 1. Instalar Dependencias
Asegurese de instalar las librerias necesarias especificadas en el archivo de requisitos:
```bash
pip install -r Requisitos.txt
```

### 2. Abrir Jupyter y Ejecutar el Notebook
Inicie el servidor de Jupyter en la terminal y navegue hasta el codigo:
```bash
jupyter notebook
```
Abra el archivo 02_Codigo/Codigo_Proyecto.ipynb y ejecute el bloque secuencial de codigo para reconstruir la base de datos unificada en tiempo real.
