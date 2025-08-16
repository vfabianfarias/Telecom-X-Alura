# Informe Final - Análisis de Evasión de Clientes (Churn) en Telecom-X

## Introducción

El presente informe tiene como objetivo analizar la evasión de clientes (*Churn*) en la empresa ficticia **Telecom-X**.  
El churn es un problema recurrente en las compañías de telecomunicaciones, ya que implica la pérdida de clientes hacia la competencia, lo que se traduce en disminución de ingresos y mayores costos de adquisición de nuevos usuarios.  

Este análisis busca identificar los patrones de cancelación, variables críticas y factores de riesgo que influyen en la evasión, con el fin de proponer estrategias que permitan reducirla.

---

## Limpieza y Tratamiento de Datos

1. **Extracción**  
   - Se utilizó un archivo JSON con los registros de clientes, importado directamente desde GitHub.  
   - Los datos fueron normalizados a un `DataFrame` de Pandas.  

2. **Transformación**  
   - Expansión de campos anidados en subcolumnas (ejemplo: `customer`, `phone`, `account`).  
   - Normalización de nombres de columnas a minúsculas y traducción al español.  
   - Conversión de variables binarias a formato numérico (`0` = No, `1` = Sí, `-1` = No definido).  
   - Traducción de categorías de inglés a español (ejemplo: *Month-to-month* → *Mes a mes*).  
   - Creación de una variable derivada: **cuenta.cuentas_diarias**, a partir de `cuenta.cargos_mensuales / 30`.  

3. **Manejo de inconsistencias**  
   - Revisión de nulos y valores vacíos.  
   - Conversión de columnas numéricas (`cargos_totales`, `cargos_mensuales`) a formato `float`.  

---

## Análisis Exploratorio de Datos (EDA)

1. **Distribución general del churn**  
   - Aproximadamente **27% de los clientes cancelaron**, mientras que un 73% permanecen activos.  

2. **Variables categóricas**  
   - **Tipo de contrato**: Los clientes con contrato *Mes a mes* presentan la tasa de cancelación más alta.  
   - **Método de pago**: El pago con *Cheque electrónico* se asocia a mayor cancelación, mientras que *Transferencia bancaria automática* muestra menor churn.  
   - **Género**: No se identificaron diferencias significativas entre hombres y mujeres.  

3. **Variables numéricas**  
   - **Antigüedad**: Los clientes con menor tiempo en la compañía tienen más probabilidades de cancelar.  
   - **Cargos mensuales**: Los cargos más altos se relacionan con mayor churn, mientras que los cargos acumulados (*cargos_totales*) más bajos indican clientes recientes que abandonan pronto.  

4. **Visualizaciones**  
   - Gráficos de pastel y barras para proporción de churn.  
   - Barras apiladas para distribución de cancelación según contrato y método de pago.  
   - Histogramas con `hue` de cancelación para cargos y antigüedad.  

---

## Conclusiones e Insights

- El **contrato de corto plazo (mes a mes)** es un fuerte predictor de evasión.  
- El **método de pago electrónico** incrementa la probabilidad de churn, posiblemente por falta de fidelización.  
- Los clientes con **antigüedad baja (< 12 meses)** cancelan con mayor frecuencia.  
- Los clientes con **cargos mensuales elevados** también presentan una mayor propensión a cancelar.  

Estos hallazgos permiten comprender mejor los perfiles de riesgo y anticipar la evasión de clientes.

---

## Recomendaciones

1. **Fidelización de clientes nuevos**  
   - Implementar programas de bienvenida, beneficios iniciales y ofertas de permanencia para clientes con menos de 12 meses.  

2. **Contratos más atractivos a largo plazo**  
   - Promover planes anuales o bianuales con descuentos o beneficios exclusivos.  

3. **Revisión de cargos mensuales**  
   - Analizar si los planes de mayor costo generan una percepción de sobreprecio que incentive la fuga.  

4. **Optimización de métodos de pago**  
   - Incentivar el uso de pagos automáticos por transferencia o tarjeta, que muestran menores tasas de churn.  

---

## Archivo y reproducibilidad

Este informe se generó a partir del notebook `Telecom-X-Alura.ipynb`, utilizando Python, Pandas, Matplotlib y Seaborn.  
Todos los gráficos y análisis pueden reproducirse ejecutando dicho notebook.  

---
