<<<<<<< HEAD
# 🧠 Proyecto Optimización del talento

Cliente: ABC Corporation

Equipo de análisis: Consultoras de Data Analytics

Objetivo: Identificar los factores clave que influyen en la satisfacción laboral y la retención del talento en la empresa.

## 🛠️ Tecnologías Utilizadas:

💻 Lenguajes: Python y MySQL.

🔗 Uso de funciones y bucles para reutilización e imputación de datos nulos o duplicados.


## 🧩 Fase 1. Exploración inicial del conjunto de datos (EDA)
Iniciamos el proyecto realizando una revisión detallada de la base de datos interna de recursos humanos de ABC Corporation. Esta contenía información sobre:

- Género, edad, estado civil y nivel educativo

- Cargo (Job Role), departamento, tipo de jornada

- Indicadores de satisfacción: ambiente laboral, trabajo remoto, oportunidades de formación, etc.

- Datos sobre rotación de empleados (quién ha dejado la empresa y quién permanece)

Luego de revisar cada columna, buscamos filas duplicadas, eliminamos columnas que no aportaban valor, identificamos valores únicos y erratas. Analizamos la estructura y longitud de los datos y finalmente exploramos los datos nulos.


## 🧹 Fase 2. Limpieza y transformación de los datos
Una vez exploradas las columnas en el EDA realizamos las siguientes transformaciones:

- Identificamos posibles patrones para realizar la imputación de los nulos que consideramos necesarios.

- Eliminamos columnas que no aportaban valor.

- Tratamos valores inconsistentes y corregimos errores de sintaxis.

- Estandarizamos los nombres de columnas para facilitar su análisis.

- Agrupamos valores para facilitar las visualizaciones.

Este paso nos permitió tener una BBDD limpia y así entender la estructura del conjunto de datos y comenzar a generar hipótesis sobre los factores que podrían estar afectando la satisfacción y cómo lograr la retención del empleado.

## 📊 Fase 3. Análisis exploratorio con visualizaciones estratégicas
Realizamos múltiples visualizaciones para detectar patrones y correlaciones significativas:

🧩 Grafica de correlación con variables numéricas:

Esta gráfica nos permitió identificar las variables que tenían una relación fuerte y valorar si eran relevantes. 

👩‍💼 Puestos vs Rotación:

 Analizamos los puestos que tienen alta rotación como Sales Executive y baja rotación como Human Resources.

⚠️ Género y puesto de trabajo:

Esta gráfica nos permitió observar que existe una brecha de género bastante marcada (mayor % de hombres vs % de mujeres) sobre todo en puestos técnicos, científicos y de ventas. 

🏡 Trabajo remoto y satisfacción:

En esta ocasión con esta gráfica concluimos que el teletrabajo no es una causa de renuncia, sin embargo hay que destacar que los empleados que realizan trabajo en remoto están más satisfechos que los empleados que trabajan de forma presencial.

🏢 Porcentaje de empleados por departamento vs rotación:

Esta gráfica nos permitió analizar dónde se concentra el mayor % de empleados por departamento, y la rotación de los mismos, siendo el grueso en puestos técnicos, científicos y de ventas. 

## 📃 Fase 4. Diseño de BBDD e Insercción de los Datos 

Conectamos las base de datos que creamos en SQL con los datos que teníamos limpios desde Python. 

Dividiendo los datos en tres tablas:
- Detalles del empleado
- Detalles del puesto de trabajo
- Detalles de la encuesta de satisfacción laboral.

Considerando la columna ID_empleado como la que conecta a las tres tablas (Primary Key). 
Esta fase nos permitió continuar analizando las relaciones entre las columnas para ayudar a la empresa a conseguir sus objetivos.

## 🔮 Recomendaciones para ABC Corporation

- Crear un plan para la reducción de la brecha de género, sobre todo algunos puestos podrían requerir políticas personalizadas.

- Implementar programas de retención específicos para empleados jóvenes y aquellos con menos tiempo en la compañía.

- Encuesta de satisfacción más detallada, incluyendo aspectos como liderazgo, carga emocional y para los empleados que renuncian el motivo (categorizado) de la misma.

- Hemos identificado que algunos departamentos y roles tienen mayor concentración de insatisfacción lo que podría indicar un riesgo de rotación.

- Realizar un análisis trimestral de indicadores de clima laboral para detectar señales tempranas de riesgo.

- Crear planes de desarrollo y mentoría personalizados, especialmente para perfiles críticos o imprescindibles para la empresa.

- Incorporar este análisis en la plataforma de selección inteligente, mejorando la retención de personal desde el proceso de reclutamiento.

## 🚀 Retos y aprendizajes

- Aprendizaje y conocimiento en paralelo.

- Interpretación diversa y consenso a posteriori de cada miembro del equipo.

- Importancia del conocimiento de los datos y  las preguntas clave.

- La calidad de una base de datos explorada y limpiada de una forma correcta contribuyen a un análisis eficiente, y conclusiones acertadas. 


## 📩 Contacto
Si tienes preguntas o sugerencias, no dudes en contactarnos a hello@3DataHers.com estaremos encantadas de absolver tus dudas!

✨ ¡Gracias por tu interés en nuestro proyecto y seguimos en contacto! 🎉
=======
# project-da-promo-49-modulo-3-team-5
>>>>>>> 40fa05d12b6b6981032645672a63f7ae6bfe940b
