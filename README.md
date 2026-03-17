# Análisis de Violencia Intrafamiliar en Colombia

Este repositorio contiene el análisis exploratorio de datos (EDA) sobre incidentes de violencia intrafamiliar en Colombia. El objetivo principal fue identificar patrones, tendencias y características demográficas de la violencia intrafamiliar para informar sobre posibles intervenciones y estrategias de prevención.

## Estructura del Repositorio

*   `Reporte_Delito_Violencia_Intrafamiliar_Polic_a_Nacional.csv`: El conjunto de datos original utilizado para el análisis.

## Periodo de Análisis

Los datos analizados en este estudio abarcan el periodo desde **2010 hasta 2021**.

## Análisis Realizado

El análisis se llevó a cabo en varias etapas:

### 1. Extracción y Carga de Datos

Los datos fueron cargados desde el archivo CSV en un DataFrame de Pandas para su manipulación y análisis.

### 2. Transformación y Limpieza de Datos

*   Se creó una copia del DataFrame original (`df_clean`) para realizar las transformaciones.
*   La columna `FECHA HECHO` se convirtió a formato `datetime` y se extrajeron el `AÑO` y el `MES`.
*   Los valores nulos en `GRUPO ETARIO` fueron imputados con la etiqueta 'Desconocido'.
*   Las filas con valores nulos restantes en `FECHA HECHO`, `GENERO` y `ARMAS MEDIOS` fueron eliminadas para asegurar la integridad del análisis.

### 3. Análisis Exploratorio de Datos (EDA)

Se exploraron las distribuciones de las siguientes variables:

*   `GENERO`: Distribución de incidentes por género.
*   `GRUPO ETARIO`: Distribución de incidentes por grupo etario.
*   `ARMAS MEDIOS`: Distribución de incidentes según el tipo de arma o medio utilizado.
*   `DEPARTAMENTO` y `MUNICIPIO`: Identificación de las regiones con mayor incidencia.
*   `FECHA HECHO` (`YEAR` y `MONTH`): Análisis de tendencias temporales (anuales y mensuales).

### 4. Análisis de la Columna `CANTIDAD`

Se investigó la columna `CANTIDAD` (número de personas afectadas por incidente) para entender:

*   Su distribución general (cuántos incidentes afectan a 1, 2 o más personas).
*   El promedio de personas afectadas por `GENERO`, `GRUPO ETARIO` y `ARMAS MEDIOS`.
*   El total acumulado de personas afectadas para estas mismas categorías, proporcionando una medida del impacto global.

## Hallazgos Clave

*   **Impacto Desproporcionado en Mujeres Adultas**: La violencia intrafamiliar afecta predominantemente a mujeres adultas en Colombia. El número de incidentes reportados es significativamente mayor para el género femenino en casi todos los grupos etarios y departamentos.
*   **Patrón en Menores**: En el grupo de `MENORES`, los hombres presentan un número ligeramente mayor de incidentes que las mujeres, lo que sugiere dinámicas específicas en la violencia infantil que merecen mayor investigación.
*   **Regiones con Mayor Incidencia**: Cundinamarca, Antioquia y Valle son los departamentos que registran el mayor número total de incidentes. La predominancia de víctimas femeninas se mantiene constante en estas regiones.
*   **Tipos de Medios**: Las agresiones más comunes se dan con 'CONTUNDENTES' y 'ARMA BLANCA / CORTOPUNZANTE'.
*   **Tendencia Temporal**: Se observó un pico notable de incidentes en el año 2020, lo que podría estar relacionado con factores coyunturales como la pandemia de COVID-19.
*   **Incidente Unipersonal Común**: La mayoría de los incidentes reportados involucran a una sola persona, aunque la suma de `CANTIDAD` resalta el impacto masivo en mujeres y adultos.

## Conclusiones

La violencia intrafamiliar es un problema sistémico y persistente en Colombia, con un impacto devastador y desproporcionado en las mujeres adultas. Aunque los hombres también son víctimas, el patrón de victimización femenina es alarmante y consistente a nivel nacional. La `CANTIDAD` de personas afectadas por incidente subraya que, aunque a menudo se reporta un solo afectado, el número acumulado de víctimas es inmenso.

## Recomendaciones

1.  **Intervenciones Dirigidas**: Desarrollar programas de prevención y apoyo específicos para mujeres adultas.
2.  **Investigación en Menores**: Realizar estudios más profundos sobre las dinámicas de la violencia intrafamiliar en menores, particularmente el patrón en varones.
3.  **Concientización y Educación**: Implementar campañas públicas para fomentar la denuncia y abordar las diversas manifestaciones de la violencia.
4.  **Análisis de Factores Contextuales**: Integrar datos socioeconómicos y coyunturales para una comprensión más holística.
5.  **Desglose de Tipos de Violencia**: Analizar los incidentes por tipo de violencia (física, psicológica, etc.) si los datos lo permiten.
6.  **Monitoreo Continuo**: Mantener un seguimiento constante de las tendencias para evaluar la efectividad de las políticas.

