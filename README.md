PROYECTO: Predicción del desempeño en las Pruebas Saber Pro

INTEGRANTES DEL EQUIPO

| Nombre Completo        			 | Cédula         | Programa Académico                 |
|---------------------------------|----------------|------------------------------------|
| Maria Camila Bravo     			 | 1085943131     | Bioingeniería					       |            
| Sebastian Bedoya Restrepo       | 1040048038     | Ingeniería de Sistemas			    |                    
| Jasmin Juliana Jaramillo Tapias | 1017163639     | Ingeniería de Sistemas 			    |

DESCRIPCIÓN DEL PROYECTO

Este proyecto forma parte de la competencia "Predicción del Desempeño en las Pruebas Saber Pro" de Kaggle.
El objetivo es desarrollar un modelo de clasificación supervisado que prediga el nivel de desempeño de los estudiantes
en las pruebas Saber Pro, categorizado en cuatro niveles:

- Bajo
- Medio-Bajo
- Medio-Alto
- Alto

EJECUCIÓN DEL NOTEBOOK

- Tener descargado el archivo kaggle.json (API KEY)
- Abrir el notebook 01 - exploración.ipynb en Google Colab
- Ejecuta cada una de las celdas, el orden de la información esta estructurada así:
   * Cargar Datos
   * FUNCIONES
   * Visualización
- Librerías necesarias: pandas, numpy, scikit-learn, matplotlib, seaborn, kaggle

CONFIGURACIÓN DE LA API KEY DE KAGGLE

1. Inicia sesión en Kaggle: https://www.kaggle.com/
2. Acepta las reglas/condiciones de la competición
3. En tu perfil, selecciona "Account".
4. Busca la sección "API".
5. Crea un nuevo token con "Create New Token".
   Esto descargará el archivo kaggle.json.
6. Coloca el archivo kaggle.json en una ruta elegida
7. Al ejecutar la primera celda del notebook 01 - exploración.ipynb te pedirá la ubicación del archivo kaggle.json 

ESTRUCTURA DEL PROYECTO

SaberPro-Classifier/
│
├── README.md
├── 01 - exploración.ipynb

CRÉDITOS

Proyecto desarrollado como parte de la competencia de aprendizaje automático
para la predicción del desempeño en las Pruebas Saber Pro.

RESUMEN TÉCNICO DEL NOTEBOOK

El notebook "01 - exploración.ipynb" desarrolla la primera fase del proyecto,
centrada en la exploración y análisis de los datos (EDA). A continuación se
detallan las etapas y procedimientos principales:

1. Extracción de datos desde Kaggle
   - Configuración de la API Key (`kaggle.json`) en Google Colab.
   - Descarga automática del dataset de la competencia.
   - Descompresión de los archivos y verificación de su contenido.

2. Carga de librerías y datasets
   - Librerías: pandas, numpy, matplotlib, seaborn, scikit-learn.
   - Archivos cargados: `train.csv`, `test.csv`, `submission_example.csv`.
   - Se verifican dimensiones, tipos de datos y estructura general.

3. Funciones auxiliares
   - resumen(): genera un resumen con tipos de datos, valores nulos, únicos y
     cantidad de registros no nulos.
   - encabezado(): muestra las primeras filas del dataset con estilo visual
     personalizado.
   - visualizacion_datos(): permite explorar rápidamente la relación entre una
     variable categórica y el rendimiento académico, identificando patrones o diferencias
     en la distribución de las categorías respecto al desempeño global

4. Análisis Exploratorio de Datos (EDA)
   - Análisis descriptivo de variables numéricas mediante `describe()`.
   - Clasificación de variables:
       - Binarias: se identifican y visualizan distribuciones.
       - Categóricas: se analizan columnas con alta cardinalidad.
       - Numéricas: se extraen variables de tipo continuo para estudio.
   - Visualización de la distribución de variables socioeconómicas:
       - Estrato de vivienda (`F_ESTRATOVIVIENDA`).
       - Educación del padre y madre (`F_EDUCACIONPADRE`, `F_EDUCACIONMADRE`).
       - Horas de trabajo semanal (`E_HORASSEMANATRABAJA`).

5. Identificación de la variable objetivo
   - La columna RENDIMIENTO_GLOBAL se establece como target para el modelo.
 

En conclusión, este notebook constituye la base exploratoria del proyecto,
proporcionando una visión detallada del dataset y preparando el terreno para las
siguientes etapas de limpieza, preprocesamiento y modelado predictivo.
