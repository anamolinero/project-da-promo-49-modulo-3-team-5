## Informe Técnico: Análisis Exploratorio de Datos para la Optimización de Talento en ABC Corporation

### Resumen

El presente informe técnico resume las fases iniciales de este proyecto, detallando los resultados obtenidos a través de nuestro análisis exploratorio de datos (EDA), los procesos de limpieza de datos implementados y la estrategia de gestión de valores nulos. El objetivo principal es identificar patrones, tendencias y relaciones significativas dentro de los datos disponibles, con el fin de proporcionar a ABC Corporation información valiosa y basada en evidencia para fundamentar sus decisiones estratégicas en la gestión de talento.

### Objetivo

- Análisis Exploratorio de Datos (EDA): Obtener una comprensión profunda de la estructura, las características y las posibles relaciones dentro de los datos proporcionados. Esto incluyó la identificación de variables clave, la detección de patrones y tendencias, y la formulación de hipótesis iniciales.

- Limpieza de Datos: Identificar y corregir errores, inconsistencias y formatos inadecuados presentes en los datos para asegurar su calidad y fiabilidad para análisis posteriores.

- Gestión de Valores Nulos: Evaluar la presencia, distribución y posibles causas de los valores faltantes en los datos, e implementar una estrategia adecuada para su tratamiento con el fin de minimizar el sesgo y maximizar la utilidad de la información.

### Metodología

Para alcanzar los objetivos definidos, se aplicó la siguiente metodología en cada una de las fases iniciales:

***1. Análisis Exploratorio de Datos (EDA)***

- Carga e Inspección Inicial: Los conjuntos de datos proporcionados por ABC Corporation fueron cargados utilizando la librería Pandas de Python, pd.read_csv("hr_raw_data.csv", index_col = 0). Se realizó una inspección inicial mediante la visualización de las primeras y últimas filas (.head(), .tail()), para contar el número de filas y columnas (.shape), la obtención de información general (.info()), el resumen estadístico descriptivo de las columnas numéricas (.describe().T), el resumen estadístico descriptivo de las columnas no numéricas (.describe(include="O").T), con (.isnull().sum()) se contabilizan los nulos y para identificar los duplicados usamos (.duplicated()).

- Análisis de Variables Individuales: Se examinó la distribución de cada variable mediante (.value_counts()) que indica cuántas veces aparece en la columna y (.unique()) para visualizar todos los valores únicos.

***2. Limpieza de Datos***

- Identificación de Inconsistencias: Se buscaron inconsistencias en el formato de los datos (números, texto, etc.), errores tipográficos en variables categóricas y posibles duplicados.

- Corrección de Errores: Se aplicaron técnicas para corregir los errores identificados, como la estandarización de formatos, la corrección de erratas (cuando fue posible con un alto grado de certeza) y la eliminación de duplicados (basándose en criterios definidos).

- Tratamiento de Formatos Inadecuados: Se realizaron conversiones de tipo de datos cuando fue necesario para facilitar el análisis (conversión de columnas de texto que representan números a tipo numérico).

***3. Gestión de Valores Nulos***

- Detección y Evaluación: Se identificaron las columnas con valores nulos y se calculó el porcentaje de datos faltantes en cada una. Se analizó la distribución de los valores nulos para identificar posibles patrones o sesgos en su ausencia.

- Estrategia de Tratamiento: Se implementó una estrategia de gestión de valores nulos basada en la naturaleza de los datos y el potencial impacto de los valores faltantes en el análisis. Las estrategias consideradas y aplicadas incluyeron:

    * Eliminación: Eliminación de filas o columnas con un porcentaje significativo de valores nulos (solo cuando se consideró apropiado y con justificación).

    * Imputación: Reemplazo de los valores nulos por un valor estimado (media, mediana, moda) o mediante técnicas de imputación más avanzadas (si la naturaleza de los datos lo requería).

    * Mantenimiento: En algunos casos, se decidió mantener los valores nulos, especialmente si su ausencia en sí misma podía ser informativa.

### Resultados Obtenidos

A continuación, se presentan los hallazgos más relevantes de cada una de las fases iniciales:

***1. Resultados del Análisis Exploratorio de Datos (EDA)***

- N° Columnas: 41

- N° Filas: 1678

- Columnas 'employeecount', "over18", "numberchildren", "sameasmonthlyincome","roledepartament" duplicadas y no necesarias.

- Filas duplicadas: 64

- Valores nulos: 13681

- Columnas que tienen valores con mayusculas y minusculas 'department', 'educationfield', 'jobrole', 'maritalstatus', "standardhours", "remotework", "overtime"

- Columna "maritalstatus" con valores que tienen errores ortotipográficos.

- Dataframe sin indice establecido.

- En columna "gender", 'remotework' y "businesstravel" diversidad de valores para significados similares.

- En la columna "age" se cuenta con valores en texto y numericos.

- En la columna 'distancefromhome' existen valores negativos y positivos.

- Las columnas "monthlyincome", "monthlyrate", "salary" tienen valores con el simbolo "$", "," y son de tipo obj.

- Las columnas "performancerating", "totalworkingyears", "worklifebalance", "yearsincurrentrole" tienen valores con "," y son de tipo obj.

- Los valores decimales en las columnas "dailyrate", "$_hourlyrate" son extensos.


***2. Resultados de la Limpieza de Datos***

- Columnas: Se eliminaron columnas no necesarias y duplicadas; "employeecount", "over18", "numberchildren", "sameasmonthlyincome","roledepartament".

- Filas: Se eliminaron 64 filas duplicados.

- Renombrar etiqueta de columnas: Columnas con simbolo "%", "$" y columna "employeenumber"; "hourlyrate" por "$_hourlyrate", "dailyrate" por "$_dailyrate", "monthlyincome" por "$_monthlyincome", "monthlyrate" por "$_monthlyrate", "salary"por "$_salary", "employeenumber" por "employee_id", "percentsalaryhike" por "%_percentsalaryhike".

- Indice: Se establecio la columna "employeenumber" como índice.

- Cambiar "mayusculas" a "minusculas".

- Corregir erratas de los valores únicos de "marital status"; "marreid" por "married".

- Unificar a dos variables; en columna "gender": 'male' y 'femele y en columna "remotework": "true" y "false .

- Unificar valores números enteros en la columna "age".

- Corregir valores negativos en la columna 'distancefromhome'.

- Cambiar valores NaN por non_travel en la columna "businesstravel".

- Unificar los valores de las columnas "$_monthlyincome", "$_monthlyrate", "$_salary","performancerating", "totalworkingyears", "worklifebalance", "yearsincurrentrole"; quitando simbolo del "$", reemplazando "," por "." y convertiendo a numeros decimales según corresponda.

- Redondear a 2 decimales los valores de las columnas "$_dailyrate", "$_hourlyrate".

***3. Resultados de la Gestión de Valores Nulos***

- Se identificaron y contabilizaron los valores nulos en las columnas; "department" presenta 1312, "educationfield" presenta 745, "$_hourlyrate" presenta 1210, "maritalstatus" presenta 651, "$_monthlyincome" presenta 468, "overtime" presenta 676,"performancerating" presenta	195,  "standardhours"	presenta 338,  "totalworkingyears" presenta	526, "worklifebalance" presenta 108,"yearsincurrentrole" presenta 1580 y "$_salary" presenta 274.

- Se opto por realizar tratamiento a las columnas, clasificando:

     * Columnas categorigas, reemplazar por la "moda" en "overtime", "standardhours" y "None" en 'department', 'educationfield', 'maritalstatus.

     * Columnas numericas; para la columna "yearsincurrentrole", debido al alto porcentaje de valores nulos se opta por reemplazar con "None". En el caso de las columnas '$_hourlyrate', '$_monthlyincome', 'performancerating', 'totalworkingyears' y '$_salary' tenemos valores atípicos y la columna "worklifebalance" posee un porcentage considerable de nulos por lo que optaremos por reemplazar los nulos con métodos más avanzados como IterativeImputer. 

### Análisis de los Resultados de las Fases Iniciales

El análisis inicial revela que la base de datos requería una intervención significativa para garantizar su calidad. Tras la limpieza y la gestión de nulos, nos encontramos en una posición mucho mejor para explorar las relaciones subyacentes en los datos y obtener información valiosa para la optimización del talento en ABC Corporation. La alta cantidad de nulos en ciertas columnas y las inconsistencias iniciales sugieren áreas donde se podría mejorar la gestión y la recopilación de datos en el futuro.