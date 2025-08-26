Este proyecto explora la relación entre variables de salud y demografía de distintos países y la cantidad de muertes por COVID-19 por millón de habitantes, utilizando datos globales de COVID-19.

1. Descripción del Dataset

Datos originales: columnas de casos y muertes acumuladas y diarias, además de variables demográficas y de salud (edad media, esperanza de vida, densidad poblacional, pobreza extrema, infraestructura hospitalaria, etc.).

Filtrado: se seleccionaron 8 variables de salud y demografía, descartando variables muy incompletas o altamente correlacionadas por construcción.

Corrección de datos: se identificaron y corrigieron valores extremos erróneos (por ejemplo, la esperanza de vida de Central African Republic se corrigió de 18.8 a 57 según World Bank).

2. Análisis Exploratorio de Datos (EDA)

Se exploraron distribuciones univariadas mediante histogramas y boxplots individuales, observando outliers pero sin eliminarlos, ya que representan datos reales.

Se realizaron análisis bivariados:

Scatterplots de cada variable de salud/demografía vs total_deaths_per_million.

Cálculo de correlaciones para identificar variables más asociadas con la mortalidad por COVID:

Más correlacionadas positivamente: median_age, life_expectancy, handwashing_facilities, gdp_per_capita, hospital_beds_per_thousand.

Negativamente correlacionadas: extreme_poverty, diabetes_prevalence.

3. Modelado Predictivo

Se entrenaron varios modelos de regresión para predecir total_deaths_per_million:

Random Forest Regressor

Linear Regression

Gradient Boosting Regressor

Se eliminaron filas con valores faltantes en la variable objetivo para entrenar los modelos.

Se evaluó el rendimiento con MSE, R² y gráficos de predicciones vs valores reales, mostrando qué tan cerca de la línea de ajuste perfecto predicen los modelos.

Se calculó la importancia de las variables en Random Forest para identificar qué factores influyen más en la mortalidad por COVID-19.

4. Conclusiones

La edad media de la población y la esperanza de vida son factores clave asociados con la mortalidad por COVID-19.

Países con mejor infraestructura de salud y mayor PIB tienden a reportar más muertes por millón, probablemente debido a mayor precisión en el registro de casos.

La pobreza extrema se correlaciona negativamente, reflejando diferencias demográficas y posibles subreportes de muertes.
