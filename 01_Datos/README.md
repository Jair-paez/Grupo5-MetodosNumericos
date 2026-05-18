# Carpeta de Datos (01_Datos)

Esta carpeta contiene las bases de datos unificadas para el proyecto de Métodos Numéricos.

## Archivos en esta carpeta

1. steam_raw_unified_all_columns.csv
   * Descripcion: Este es el dataset unificado completo, crudo y con todas las columnas cruzadas de games.csv, reviews.csv y steamspy_insights.csv (140,132 registros y 35 columnas).
   * Proposito: Es la fuente de verdad del proyecto. Desde aqui se cargara y limpiara la informacion en tu codigo secuencial.

---

## Diccionario de Variables (Caracteristicas del Dataset)

Para el modelamiento matematico, cuentas con las siguientes columnas agrupadas por su naturaleza:

### 1. Variables de Identificacion e Informacion Basica
* app_id: Identificador unico del juego en la tienda Steam (clave de cruce).
* name: Nombre oficial del juego.
* release_date: Fecha de lanzamiento original.
* is_free: Variable binaria (1 si el juego es gratuito, 0 si es de pago).
* type: Tipo de producto en la plataforma (game, demo, dlc).
* developer: Nombre del desarrollador o estudio creador.
* publisher: Distribuidor comercial del juego.
* genres: Generos del juego (ej: "Action, Strategy, Indie").

### 2. Variables de Percepcion de Calidad y Puntuacion
* review_score: Puntuacion discreta de Steam (0 a 9).
* review_score_description: Categoria cualitativa de las reviews (ej: "Overwhelmingly Positive", "Mixed").
* reviews_positive: Cantidad de resenas positivas escritas por usuarios.
* reviews_negative: Cantidad de resenas negativas escritas por usuarios.
* reviews_total: Total de resenas acumuladas (reviews_positive + reviews_negative).
* approval_ratio (Calculada Continuo): Relacion continua de aprobacion entre 0.0 y 1.0.
    $$\text{approval\_ratio} = \frac{\text{reviews\_positive}}{\text{reviews\_total}}$$
* metacritic_score: Puntuacion oficial de Metacritic (escala de 0 a 100).

### 3. Variables de Consumo y Popularidad (Ventas Estimadas)
* owners_range: Rango estimado de compradores segun SteamSpy (ej: "10,000,000 .. 20,000,000").
* estimated_owners (Calculada Continuo): Punto medio del rango de compradores, util para regresion.
* concurrent_users_yesterday: Cantidad de jugadores activos simultaneamente en las ultimas 24 horas.
* playtime_average_forever: Tiempo promedio de juego de los usuarios en minutos.
* playtime_median_forever: Mediana de tiempo de juego de los usuarios en minutos.

### 4. Variables de Precio y Descuento
* steamspy_price: Precio del juego en centavos de dolar (ej: 999 centavos = $9.99 USD).
* price_usd (Calculada Continuo): Precio del juego normalizado en dolares USD continuos.
* steamspy_initial_price: Precio de lanzamiento del juego en centavos.
* steamspy_discount: Porcentaje de descuento activo al momento del raspado de datos.
