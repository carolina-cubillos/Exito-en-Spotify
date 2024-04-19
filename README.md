# Exito-en-Spotify
En este proyecto busco averiguar si es posible encontrar las características claves para lanzar una canción exitosa en Spotify

![_317bb9e3-357f-462f-9462-e649dcdfdb05](https://github.com/carolina-cubillos/Exito-en-Spotify/assets/152019603/02814c78-8536-4277-b4ab-97459cb522cc)


## Temas
- [Introducción](#introducción)
- [Herramientas](#herramientas)
- [Procesamiento](#procesamiento)
- [Validación de hipótesis](#validación-de-hipótesis)
- [Resultados](#resultados)
- [Conclusiones y recomendaciones](#conclusiones-y-recomendaciones)

## Introducción
En un mundo en el que la industria musical es extremadamente competitiva y está en permanente evolución, la capacidad de tomar decisiones basadas en datos se ha convertido en un activo invaluable. En este contexto, una discográfica se enfrenta al emocionante desafío de lanzar un nuevo artista en el escenario musical global. Afortunadamente, cuenta con una herramienta poderosa en su arsenal: un extenso dataset de Spotify con información sobre las canciones más escuchadas en 2023. La discográfica planteó una serie de hipótesis sobre qué hace que una canción sea más escuchada, las que deberán ser analizadas para asegurar un lanzamiento exitoso.

## Herramientas
- SQL (Google BigQuery)
- Python 
- Power BI

## Procesamiento
- Se identifican valores nulos a través de comandos SQL COUNT, WHERE y IS NULL.
- Se identifican duplicados a través de comandos SQL COUNT, GROUP BY, HAVING.
- Se manejan variables que no son útiles para el análisis a través de comandos SQL SELECT EXCEPT.
- Se identifican datos discrepantes en variables categóricas utilizando el comandos de manejo de string, como REGEXP.
- Se identifican datos discrepantes en variables niméricas utilizando comandos como MAX, MIN y AVG.
- Se comprueba y modifican tipos de datos, cuando es necesario, utilizando CAST.
- Se crean nuevas variables utilizando CONCAT  y SUM.
- Se construyen tablas auxiliares utilizando WITH.
- Se unen las tablas utilizando LEFT JOIN.


  
## Validación de hipótesis
Las hipótesis a verificar son:

1. Las canciones con un mayor BPM (Beats Por Minuto) tienen más éxito en términos de cantidad de streams en Spotify. 
2. Las canciones más populares en el ranking de Spotify también tienen un comportamiento similar en otras plataformas como Deezer.
3. La presencia de una canción en un mayor número de playlists se relaciona con un mayor número de streams.
4. Los artistas con un mayor número de canciones en Spotify tienen más streams totales.
5. Las características de la música influyen en el éxito en términos de cantidad de streams en Spotify.


## Resultados

H1. No hay evidencia fuerte para respaldar la hipótesis. La correlación es cercana a cero y los valores de la prueba Mann-Whitney no indican una diferencia significativa. La hipótesis se rechaza

![image](https://github.com/carolina-cubillos/Exito-en-Spotify/assets/152019603/2e8ed2bf-7c0c-4d89-ab36-453bb1794ef1)

H2. Correlación positiva moderada, respaldando la idea de que las canciones populares en Spotify también son populares en Apple Music y Deezer. La hipótesis se confirma.

![image](https://github.com/carolina-cubillos/Exito-en-Spotify/assets/152019603/60f93e20-2cc8-4041-a618-fcb8731429f2)

H3.Existe una correlación fuerte y positiva, respaldando la hipótesis. La Hipótesis se confirma.

![image](https://github.com/carolina-cubillos/Exito-en-Spotify/assets/152019603/2b7a1dc0-f7b5-40ea-adbf-7030400b7015)

H4.Existe una correlación fuerte y positiva.  La Hipótesis se confirma.

![image](https://github.com/carolina-cubillos/Exito-en-Spotify/assets/152019603/4b5f5d0e-fbe4-49f8-a355-faf3ec1117ec)

H5.Existe una correlación debil y negativa respecto a danceabillity y una correlación media positiva en cuanto a speechiness. Pero en términos generales no se detecta ninguna correlación muy fuerte.

![image](https://github.com/carolina-cubillos/Exito-en-Spotify/assets/152019603/fc8ccdc1-b07d-4bfa-a209-85b14b77c7e7)

![image](https://github.com/carolina-cubillos/Exito-en-Spotify/assets/152019603/4e2f01a5-9344-4bba-9237-84fdddf07c41)

![image](https://github.com/carolina-cubillos/Exito-en-Spotify/assets/152019603/f9d04446-d6c0-462a-9c18-f3a6dc9ae350)





## Adicional
En el análisis exploratorio se detectaron hallazgos adicionales que pueden ser de interés.
La gran mayoría de canciones reproducidas en el periodo entre la decada de los 30 al 70 corresponden a canciones Navideñas. 

![image](https://github.com/carolina-cubillos/Exito-en-Spotify/assets/152019603/672ca5e1-5ee3-49a9-b0a4-6b751af32e77)




## Conclusiones y recomendaciones
- Se podrían considerar como variables relevantes a la hora de la composición danceability y speechiness, sin embargo no garantizarán éxito asegurado.
- Resulta relevante estar presente en un gran número de playlists.
- Es recomendable estar presentes en todas las plataformas de streaming
- Es posible pensar que la temática Navideña permite trascender al paso de los años y volverse un clásico
- No es posible garantizar el éxito con las variables estudiadas, por lo que se recomienda poner esfuerzo también en otras áreas como marketing y redes sociales. Se recomienda analizar resultados en plataformas como TikTok y Youtube.
