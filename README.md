# Modelación y pronóstico del turismo en Costa Rica

## Información del proyecto

**Autor:** David Eduardo Brenes Hernández  
**Universidad:** Universidad de Costa Rica  
**Escuela:** Escuela de Estadística  
**Curso:** XS-0127 Análisis de Series Temporales  
**Profesor:** Christopher Torres Rojas  
**Año:** 2026

## Descripción

El presente proyecto tiene como objetivo comparar la capacidad predictiva de diferentes modelos de series temporales para las llegadas internacionales de turistas por vía aérea a Costa Rica durante el periodo 2009–2025.

Se evaluaron cuatro familias de modelos:

- Suavizamiento exponencial.
- ARIMA/SARIMA.
- Regresión.
- Regresión dinámica.

## Fuente de los datos

Los datos fueron obtenidos del tablero interactivo del Departamento de Estadística Turística del Instituto Costarricense de Turismo (ICT).

[Consultar fuente original de los datos](https://app.powerbi.com/view?r=eyJrIjoiZGFjYTI5NTAtYmRiNy00ZjQ2LTk5ZDYtZGY2N2Q0YWNjNzcyIiwidCI6ImQwN2I2NTM1LTFkZGMtNDA2YS04MzQxLTBiMGEzMDlkNDExNSIsImMiOjR9)

**Filtros utilizados:**

- Periodo: enero de 2009 a diciembre de 2025.
- Región: todas.
- País: todos.
- Vía de ingreso: aérea.
- Frecuencia: mensual.
- Número de observaciones: 204.

Los datos fueron transcritos directamente en R y se adjuntan adicionalmente en formato CSV.

## Principales resultados

El modelo seleccionado fue la regresión dinámica con tendencia lineal, estacionalidad mensual y errores ARIMA(4,0,0).

| Indicador | Resultado |
|---|---:|
| RMSE fuera de muestra | 26.617,18 |
| MAE fuera de muestra | 19.898,07 |
| MAPE fuera de muestra | 10,55 % |
| MASE fuera de muestra | 0,6270 |
| Total de llegadas pronosticadas para 2026 | 2.979.040 |

## Archivos del repositorio

- `Proyecto_Series_Temporales.Rmd`: código reproducible de la investigación.
- `Datos_turismo_2009_2025.csv`: datos utilizados en el estudio.

## Reproducibilidad

El análisis se desarrolló utilizando R versión 4.5.1 y los siguientes paquetes:

- forecast
- ggplot2
- fpp2
- astsa
- tseries

Para reproducir el análisis, se debe descargar el archivo R Markdown, abrirlo en RStudio, instalar los paquetes requeridos y ejecutar la opción **Knit**.

Los datos se encuentran incorporados directamente en el código, por lo que no se requiere importar archivos externos para ejecutar el análisis.
