# Análisis de Accidentalidad Vial y Simulación Predictiva (Calarcá)

Este proyecto presenta un análisis de datos exhaustivo sobre la siniestralidad vial en el municipio de Calarcá utilizando **Power BI** y **DAX**. El objetivo principal es evaluar el comportamiento histórico de los accidentes, identificar patrones de severidad y proyectar escenarios futuros basados en el **Plan Nacional de Seguridad Vial (PNSV)** bajo el marco del Decreto 1430.

## Estructura del Informe

El reporte está desarrollado bajo un enfoque narrativo y técnico dividido en cuatro secciones clave:

1. **Distribución de Fatalidad:** Análisis de la gravedad de los siniestros (Con Heridos, Con Muertos, Solo Daños) y su evolución proporcional.
2. **Comportamiento en el Tiempo:** Análisis cronológico de la frecuencia de accidentes y cálculo de tendencias históricas.
3. **Simulación PNSV 2030:** Un simulador interactivo utilizando parámetros DAX que permite evaluar el impacto de las políticas públicas y los accidentes evitados según las metas de decremento establecidas.
4. **Conclusiones y Hallazgos:** Interpretación narrativa de los datos y objetos visuales presentados a lo largo del informe.

## Fuente Normativa: Plan Nacional de Seguridad Vial (PNSV)

El escenario de simulación e intervención (2030) presentado en este análisis se fundamenta en las metas oficiales establecidas por el Gobierno Nacional de Colombia.

* **Documento de Referencia:** Plan Nacional de Seguridad Vial 2022-2031
* **Entidad Responsable:** Agencia Nacional de Seguridad Vial (ANSV), adscrita al Ministerio de Transporte de la República de Colombia
* **Marco Normativo:** Decreto 1430 de 2022 / Ley 1702 de 2013
* **Enfoque Adoptado:** Visión Cero / Sistema Seguro (recomendado por la OMS y el Foro Internacional de Transporte)
* **Portal Oficial:** [Agencia Nacional de Seguridad Vial (ansv.gov.co)](https://ansv.gov.co/agencia/pnsv/presentacion)

> **Nota:** El acceso automatizado al sitio oficial de la ANSV está restringido (bloqueo por robots.txt). El documento fue descargado y consultado manualmente para la extracción de las metas de reducción utilizadas en el simulador DAX.

## Hallazgos Clave

### La Paradoja de Severidad Vial

A través del cruce de variables cronológicas y de gravedad, se identificó un comportamiento crítico en el municipio: **a pesar de registrarse una disminución paulatina en el volumen total de accidentes año tras año, la severidad de estos ha aumentado considerablemente.**

* **Incremento Sostenido:** Entre 2017 y 2022, la tasa de siniestros graves (aquellos que involucran heridos o víctimas fatales) creció a un ritmo promedio del **5% anual**.
* **Impacto Post-Pandemia:** Este fenómeno se tornó crítico en la etapa de reactivación económica (2022), donde los accidentes con heridos y muertes desplazaron drásticamente a los choques simples de "Solo Daños", representando más del **74%** del total de casos.
* **Conclusión Analítica:** Aunque hay menos colisiones físicas en las vías, los incidentes actuales ocurren bajo condiciones de mayor riesgo (como excesos de velocidad o mayor flujo de carga pesada), transformando choques comunes en tragedias humanas.

### Proyección Inercial vs. Escenario Intervenido (2030)

* **Escenario Base (Inercial):** Al aplicar modelos de extrapolación estadística hacia el año 2030, se evidencia que, de mantenerse la inercia actual sin intervenciones, el municipio experimentará picos cíclicos agresivos de accidentalidad que replicarán los peores años históricos.
* **Escenario Intervenido:** El simulador interactivo demuestra matemáticamente cómo la adopción de las metas del PNSV (ej. una reducción del 50%) altera la curva de proyección en tiempo real, permitiendo cuantificar los accidentes directamente evitados en el mediano plazo.

### Anomalía en la Distribución Semanal

Al analizar el comportamiento cronológico de la fuente, se identificó un sesgo estructural en la recolección de datos: el sistema solo registra 6 de los 7 días de la semana, excluyendo por completo los domingos y mostrando un descenso atípico los sábados, mientras que los lunes concentran el mayor volumen de registros del dataset. Sin confirmación directa del ente rector sobre el proceso de captura, no es posible determinar con certeza si esta distribución responde a una menor siniestralidad real o a dinámicas en los flujos de carga/ingreso de información al sistema.

## Tecnologías y Conceptos Aplicados

* **Power BI Desktop:** Modelado de datos, diseño de interfaz de usuario (UI/UX) y visualización interactiva.
* **Modelado de Datos:** Implementación de tablas de hechos y dimensiones (Tablas de fechas expandidas para análisis predictivo).
* **Expresiones DAX:**
  * Uso de funciones de cálculo avanzado (`CALCULATE`, `DIVIDE`, `COUNT`).
  * Creación de parámetros dinámicos para la simulación de hipótesis (*What-If analysis*).
  * Programación de medidas híbridas de series temporales para el cálculo de tasas de variación anual acumulada.

## Fuente de Datos y Linaje (Data Lineage)

Los datos procesados son oficiales, públicos y pertenecen al marco de transparencia del Estado Colombiano.

* **Portal Oficial:** [Datos Abiertos Colombia (datos.gov.co)](https://www.datos.gov.co/)
* **Nombre del Dataset:** ACCIDENTES DE TRANSITO DESDE MARZO 2017 A DICIEMBRE DE 2022
* **Identificador de Dataset:** `wacd-xkg8`
* **Entidad Emisora / Cobertura:** Alcaldía Municipal de Calarcá / Instituto Departamental de Tránsito del Quindío (IDTQ)

## Fuente Normativa: Plan Nacional de Seguridad Vial (PNSV)

El escenario de simulación e intervención (2030) presentado en este análisis se fundamenta en las metas oficiales establecidas por el Gobierno Nacional de Colombia.

* **Documento de Referencia:** Plan Nacional de Seguridad Vial 2022-2031
* **Entidad Responsable:** Agencia Nacional de Seguridad Vial (ANSV), adscrita al Ministerio de Transporte de la República de Colombia
* **Marco Normativo:** Decreto 1430 de 2022 / Ley 1702 de 2013
* **Enfoque Adoptado:** Visión Cero / Sistema Seguro (recomendado por la OMS y el Foro Internacional de Transporte)
* **Portal Oficial:** [Agencia Nacional de Seguridad Vial (ansv.gov.co)](https://ansv.gov.co/agencia/pnsv/presentacion)

> **Nota:** El acceso automatizado al sitio oficial de la ANSV está restringido (bloqueo por robots.txt). El documento fue descargado y consultado manualmente para la extracción de las metas de reducción utilizadas en el simulador DAX.

## Recomendaciones para Fases Futuras

1. **Muestreo y Validación en Fuente Original:** Entrevistar o consultar formalmente a la entidad emisora (Secretaría de Movilidad / Policía de Tránsito) para auditar el protocolo de registro del IPAT en fines de semana.
2. **Cruce con Fuentes Complementarias:** Contrastar este dataset con registros de atención hospitalaria/urgencias o ingresos a fiscalía de los mismos periodos para determinar la tasa real de siniestralidad de los días domingo.
3. **Normalización del Sesgo:** En caso de confirmarse el desfase en las fechas de ingreso, aplicar un modelo de ajuste o redistribución probabilística para los picos registrados los días lunes.
