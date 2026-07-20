# Análisis de Accidentalidad Vial y Simulación Predictiva (Calarcá)

Este proyecto presenta un análisis de datos exhaustivo sobre la siniestralidad vial en el municipio de Calarcá utilizando **Power BI** y **DAX**. El objetivo principal es evaluar el comportamiento histórico de los accidentes, identificar patrones de severidad y proyectar escenarios futuros basados en el **Plan Nacional de Seguridad Vial (PNSV)** bajo el marco del Decreto 1430.

## Estructura del Informe

El reporte está desarrollado bajo un enfoque narrativo y técnico dividido en tres secciones clave:

1. **Distribución de Fatalidad:** Análisis de la gravedad de los siniestros (Con Heridos, Con Muertos, Solo Daños) y su evolución proporcional.
2. **Comportamiento en el Tiempo:** Análisis cronológico de la frecuencia de accidentes y cálculo de tendencias históricas.
3. **Simulación PNSV 2030:** Un simulador interactivo utilizando parámetros DAX que permite evaluar el impacto de las políticas públicas y los accidentes evitados según las metas de decremento establecidas.



## Hallazgos Clave

### La Paradoja de Severidad Vial
A través del cruce de variables cronológicas y de gravedad, se identificó un comportamiento crítico en el municipio: **a pesar de registrarse una disminución paulatina en el volumen total de accidentes año tras año, la severidad de estos ha aumentado considerablemente.**

* **Incremento Sostenido:** Entre 2017 y 2022, la tasa de siniestros graves (aquellos que involucran heridos o víctimas fatales) creció a un ritmo promedio del **5% anual**.
* **Impacto Post-Pandemia:** Este fenómeno se tornó crítico en la etapa de reactivación económica (2022), donde los accidentes con heridos y muertes desplazaron drásticamente a los choques simples de "Solo Daños", representando más del **74%** del total de casos. 
* **Conclusión Analítica:** Aunque hay menos colisiones físicas en las vías, los incidentes actuales ocurren bajo condiciones de mayor riesgo (como excesos de velocidad o mayor flujo de carga pesada), transformando choques comunes en tragedias humanas.

### Proyección Inercial vs. Escenario Intervenido (2030)
* **Escenario Base (Inercial):** Al aplicar modelos de extrapolación estadística hacia el año 2030, se evidencia que, de mantenerse la inercia actual sin intervenciones, el municipio experimentará picos cíclicos agresivos de accidentalidad que replicarán los peores años históricos.
* **Escenario Intervenido:** El simulador interactivo demuestra matemáticamente cómo la adopción de las metas del PNSV (ej. una reducción del 50%) altera la curva de proyección en tiempo real, permitiendo cuantificar los accidentes directamente evitados en el mediano plazo.


## Tecnologías y Conceptos Aplicados

* **Power BI Desktop:** Modelado de datos, diseño de interfaz de usuario (UI/UX) y visualización interactiva.
* **Modelado de Datos:** Implementación de tablas de hechos y dimensiones (Tablas de fechas expandidas para análisis predictivo).
* **Expresiones DAX:** 
  * Uso de funciones de cálculo avanzado (`CALCULATE`, `DIVIDE`, `COUNT`).
  * Creación de parámetros dinámicos para la simulación de hipótesis (*What-If analysis*).
  * Programación de medidas híbridas de series temporales para el cálculo de tasas de variación anual acumulada.
 
## Fuente de los Datos

Los datos utilizados en este desarrollo son oficiales, públicos y provienen del **Portal de Datos Abiertos del Estado Colombiano (datos.gov.co)**. 

* **Dataset:** Histórico de Accidentes de Tránsito / Siniestralidad Vial.
* **Entidad emisora:** Ministerio de Tecnologías de la Información y las Comunicaciones de Colombia (MinTIC)
* **Filtro temporal:** Registros consolidados entre los años 2017 y 2022.
* * **Enlace oficial:** [Accidentes de Tránsito (2017 - 2022) - Datos Abiertos](https://www.datos.gov.co/Transporte/ACCIDENTES-DE-TRANSITO-DESDE-MARZO-2017-A-DICIEMBR/wacd-xkg8)
