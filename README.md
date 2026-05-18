# Modelado Numérico del Éxito Comercial y de Aprobación de Videojuegos en Steam

## Información Académica

Institución: Escuela Politécnica Nacional 

Materia: Métodos Numéricos

Semestre: 2026-A

Estudiante: 

* Ricardo Cisneros
* Hugo Coyago
* Jair Paez

## Descripción del Proyecto (Tentativo)

Este proyecto de investigación académica tiene como objetivo aplicar herramientas de análisis numérico y modelamiento matemático para comprender la dinámica de éxito de los videojuegos distribuidos en la plataforma Steam.

De manera tentativa, nos enfocaremos en modelar la relación matemática entre variables comerciales y cualitativas de los videojuegos. A través de métodos como Ajuste de Curvas (Mínimos Cuadrados) y algoritmos de Resolución de Ecuaciones No Lineales , buscaremos encontrar funciones óptimas que aproximen el comportamiento de estos datos y nos permitan predecir o encontrar puntos de equilibrio en el mercado de videojuegos.

## Distribución y Estructura Organizativa

Para asegurar el orden, el rigor académico y la facilidad de revisión, el proyecto está estructurado bajo un esquema de carpetas numeradas. A continuación se presenta el mapa visual de directorios:

```text
📂 Proyecto/ (Raíz)
├── 📁 01_Datos/
│   ├── 📁 Datos crudos/
│   │   └── 📁 steam-insights-main/
│   │       ├── 📁 games/
│   │       ├── 📁 reviews/
│   │       └── 📁 steamspy_insights/
│   ├── 📄 README.md (Diccionario de variables y especificaciones)
│   └── 📄 steam_raw_unified_all_columns.csv (Dataset unificado final)
├── 📁 02_Codigo/
│   └── 📄 Codigo_Proyecto.ipynb (Jupyter Notebook principal secuencial)
├── 📁 03_Informe/
│   └── 📄 (Espacio reservado para el informe académico final en PDF)
├── 📁 04_Presentacion/
│   └── 📄 (Espacio reservado para las diapositivas de la defensa oral)
├── 📁 05_Referencias/
│   ├── 📁 material_curso/ (Diapositivas de clase y sílabo )
│   └── 📄 bibliografia.md (Referencias bibliográficas)
├── 📄 .gitignore (Control de exclusión de archivos grandes para GitHub)
├── 📄 README.md (Este manual general del proyecto)
└── 📄 Requisitos.txt (Lista de librerías y dependencias necesarias)
```

### Descripción de las Carpetas

1. 01_Datos/

   * Datos crudos/: Almacena los archivos originales sin procesar descargados de GitHub.
   * steam_raw_unified_all_columns.csv: Es el producto de la Parte 1 del código; un archivo plano consolidado donde se cruzaron los tres archivos crudos.
   * README.md: Explica columna por columna qué significa cada variable en el dataset unificado.
2. 02_Codigo/

   * Contiene Codigo_Proyecto.ipynb, el notebook de Jupyter estructurado secuencialmente que realiza desde la fusión de archivos y limpieza, hasta los cálculos numéricos del modelo.
3. 03_Informe/

   * Almacenará el reporte formal escrito bajo formato científico-académico que se entregará al docente.
4. 04_Presentacion/

   * Guardará las diapositivas de PowerPoint o PDF diseñadas para la defensa oral frente al tribunal de la materia.
5. 05_Referencias/

   * Contiene el archivo bibliografia.md con fuentes bibliográficas.

## Guía Rápida para Replicación

Este proyecto está diseñado para ser 100% reproducible. Para ejecutar el código en cualquier computador, siga este procedimiento:

### 1. Preparar el Entorno Virtual e Instalar Dependencias

Asegúrese de instalar las librerías necesarias especificadas en el archivo de requisitos:

```bash
pip install -r Requisitos.txt
```

### 2. Abrir Jupyter y Ejecutar el Notebook

Inicie el servidor de Jupyter en la terminal y navegue hasta el código:

```bash
jupyter notebook
```

Abra el archivo 02_Codigo/Codigo_Proyecto.ipynb y ejecute el bloque secuencial de código para reconstruir la base de datos unificada en tiempo real.
