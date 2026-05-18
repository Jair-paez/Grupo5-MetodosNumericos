# Modelado Numerico del Exito Comercial y de Aprobacion de Videojuegos en Steam

## Informacion Academica

* Institucion: Escuela Politecnica Nacional (EPN)
* Materia: Metodos Numericos
* Semestre: 2026-A
* Estudiante:
  * Ricardo Cisneros
  * Hugo Coyago
  * Jair Paez

---

## Descripcion del Proyecto (Tentativo)

Este proyecto de investigacion academica tiene como objetivo aplicar herramientas de analisis numerico y modelamiento matematico para comprender la dinamica de exito de los videojuegos distribuidos en la plataforma Steam.

De manera tentativa, nos enfocaremos en modelar la relacion matematica entre variables comerciales y cualitativas de los videojuegos, tales como:

* El Precio en Dolares de los juegos (price_usd)
* El Puntaje o Proporcion de Aprobacion de la comunidad (approval_ratio)
* La Cantidad de Ventas Estimadas o descargas en base a los rangos de SteamSpy (estimated_owners)

Aves de metodos como Ajuste de Curvas (Minimos Cuadrados) y algoritmos de Resolucion de Ecuaciones No Lineales (Busqueda de Raices), buscaremos encontrar funciones optimas que aproximen el comportamiento de estos datos y nos permitan predecir o encontrar puntos de equilibrio en el mercado de videojuegos.

---

## Distribucion y Estructura Organizativa

Para asegurar el orden, el rigor academico y la facilidad de revision, el proyecto esta estructurado bajo un esquema de carpetas numeradas. A continuacion se presenta el mapa visual de directorios:

```text
Proyecto/ (Raiz)
├── 01_Datos/
│   ├── Datos crudos/
│   │   └── steam-insights-main/
│   │       ├── games/
│   │       ├── reviews/
│   │       └── steamspy_insights/
│   ├── README.md (Diccionario de variables y especificaciones)
│   └── steam_raw_unified_all_columns.csv (Dataset unificado final)
├── 02_Codigo/
│   └── Codigo_Proyecto.ipynb (Jupyter Notebook principal secuencial)
├── 03_Informe/
│   └── (Espacio reservado para el informe academico final en PDF)
├── 04_Presentacion/
│   └── (Espacio reservado para las diapositivas de la defensa oral)
├── 05_Referencias/
│   ├── material_curso/ (Diapositivas de clase, silabo y examenes previos)
│   └── bibliografia.md (Referencias bibliograficas en formato APA)
├── .gitignore (Control de exclusion de archivos grandes para GitHub)
├── README.md (Este manual general del proyecto)
└── Requisitos.txt (Lista de librerias y dependencias necesarias)
```

### Descripcion de las Carpetas

1. 01_Datos/

   * Datos crudos/: Almacena los archivos originales sin procesar descargados de GitHub.
   * steam_raw_unified_all_columns.csv: Es el producto de la Parte 1 del codigo; un archivo plano consolidado donde se cruzaron los tres archivos crudos.
   * README.md: Explica columna por columna que significa cada variable en el dataset unificado.
2. 02_Codigo/

   * Contiene Codigo_Proyecto.ipynb, el notebook de Jupyter estructurado secuencialmente que realiza desde la fusion de archivos y limpieza, hasta los calculos numericos del modelo.
3. 03_Informe/

   * Almacenara el reporte formal escrito bajo formato cientifico-academico que se entregara al docente.
4. 04_Presentacion/

   * Guardara las diapositivas de PowerPoint o PDF disenadas para la defensa oral frente al tribunal de la materia.
5. 05_Referencias/

   * Contiene el archivo bibliografia.md con fuentes bibliograficas configuradas en formato APA y la carpeta material_curso/ para archivar los PDFs de teoria y examenes de Metodos Numericos del semestre actual.

---

## Guia Rapida para Replicacion

Este proyecto esta disenado para ser 100% reproducible. Para ejecutar el codigo en cualquier computador, siga este procedimiento:

### 1. Preparar el Entorno Virtual e Instalar Dependencias

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
