# Proyecto Telecom-X - Análisis de Evasión de Clientes (Churn)

## Descripción
Este proyecto corresponde al análisis de **evasión de clientes (Churn)** en una compañía ficticia de telecomunicaciones, **Telecom-X**.  
El trabajo sigue el enfoque **ETL (Extract, Transform, Load)** complementado con **análisis exploratorio de datos (EDA)** y generación de insights de negocio.  

El código y resultados fueron desarrollados en el marco del programa **Alura ONE - Data Science LATAM**.

## Objetivos
- Extraer y preparar los datos de clientes desde un archivo JSON.  
- Transformar y limpiar los datos para obtener un dataset estructurado.  
- Analizar patrones de evasión de clientes en variables numéricas y categóricas.  
- Generar un **informe final** con conclusiones y recomendaciones estratégicas.  

## Archivos del Proyecto
Telecom-X-Alura/

# Dataset original en formato JSON

Telecom-X-Alura.ipynb   # Notebook principal con el proceso ETL y análisis

Informe_Final.md # Informe final en formato Markdown

README.md   # Archivo principal de documentación del repositorio

## Tecnologías utilizadas
- **Python 3.10+**
- **Pandas** (procesamiento de datos)
- **NumPy** (cálculos numéricos)
- **Matplotlib** y **Seaborn** (visualización de datos)
- **Jupyter/Colab** (notebooks interactivos)

## Resultados principales
- Los clientes con **contratos mes a mes** tienen la mayor tasa de cancelación.  
- **Métodos de pago automáticos** (tarjeta o transferencia bancaria) muestran menor churn.  
- Los clientes con **antigüedad baja (< 12 meses)** cancelan más frecuentemente.  
- Los **cargos mensuales altos** se asocian a mayor evasión.  

Más detalles y visualizaciones se encuentran en el archivo `reports/informe_final.md`.

## Reproducibilidad
1. Clonar el repositorio:
   git clone https://github.com/tuusuario/Telecom-X-Alura.git
   cd Telecom-X-Alura

2. Instalar dependencias:
   pip install -r requirements.txt

3. Abrir el notebook:
   jupyter notebook notebooks/Telecom-X-Alura.ipynb

## Autor
Proyecto desarrollado por **Víctor Farías Sarango** como parte del programa **Alura ONE - Data Science LATAM**.
