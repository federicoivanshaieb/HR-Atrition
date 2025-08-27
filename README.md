# Análisis de Rotación de Personal de Recursos Humanos

### Descripción del Proyecto
Este proyecto de ciencia de datos se enfoca en el análisis y la predicción de la rotación de empleados en una empresa. Utilizando datos de Recursos Humanos, el objetivo principal es identificar los factores clave que influyen en que un empleado decida dejar la compañía y, a partir de esos hallazgos, proponer recomendaciones estratégicas para la retención del talento.

### Objetivo
El objetivo principal es construir un modelo de aprendizaje automático capaz de predecir la rotación de empleados y, al mismo tiempo, interpretar dicho modelo para entender qué variables son más importantes en este proceso.

---

### Conjunto de Datos
El análisis se realiza sobre el archivo `HR_Analytics.csv`, que contiene información detallada sobre empleados, incluyendo datos demográficos, rol de trabajo, desempeño, salario, y otros factores relevantes.

Puedes acceder al conjunto de datos directamente desde este repositorio, asegurándote de que tu código apunte a la URL "raw" de GitHub.

---

### Tecnologías y Librerías
* **Lenguaje:** Python
* **Librerías:**
    * `Pandas` y `NumPy` para la manipulación y el análisis de datos.
    * `Matplotlib` y `Seaborn` para la visualización de datos.
    * `Scikit-learn` para el preprocesamiento, modelado y evaluación.
    * `XGBoost` y `LightGBM` para la creación de modelos de alta precisión.
    * `Imblearn` para el manejo de desbalance de clases (uso de `SMOTE`).

---

### Hallazgos Clave del Análisis

Después de un exhaustivo análisis exploratorio y la interpretación del modelo, se identificaron los siguientes puntos cruciales que influyen en la rotación:

* **Horas Extras (`OverTime`):** Los empleados que trabajan horas extras tienen una tasa de rotación significativamente más alta.
* **Rol de Trabajo (`JobRole`):** Roles como `Sales Representative` muestran una tasa de rotación desproporcionadamente alta en comparación con otros puestos.
* **Años desde la Última Promoción (`YearsSinceLastPromotion`):** La falta de oportunidades de crecimiento es un factor importante; a mayor tiempo sin promoción, mayor es el riesgo de rotación.
* **Años con el Mismo Gerente (`YearsWithCurrManager`):** La relación con el líder directo es crítica, y un estancamiento en esta variable puede indicar un riesgo de salida.

---

### Resultados del Modelo

Se entrenaron varios modelos de clasificación para predecir la rotación, utilizando una tubería (`Pipeline`) que incluye el preprocesamiento de datos y el manejo de desbalance de clases. El modelo de **[nombre del mejor modelo, ej. LightGBM]** fue seleccionado como el de mejor rendimiento, alcanzando una métrica de **ROC AUC** de **[tu valor de ROC AUC]**.

---

### Recomendaciones Accionables para RRHH

Basado en los hallazgos del análisis, se proponen las siguientes acciones estratégicas para mejorar la retención de talento:

1.  **Gestión de Roles Críticos y Horas Extras:** Implementar programas de soporte específicos para los roles con alta rotación. Limitar las horas extras y evaluar la carga de trabajo para reducir el agotamiento.
2.  **Planes de Carrera y Oportunidades de Crecimiento:** Establecer rutas de avance claras para los empleados, con programas de mentoría y oportunidades de desarrollo. Monitorear a los empleados con largos periodos sin promoción para intervenir a tiempo.
3.  **Revisión de Política de Viajes:** Evaluar si la frecuencia de viajes está impactando negativamente a los empleados y buscar alternativas que mejoren su equilibrio entre vida personal y laboral.
4.  **Mejora del Liderazgo y la Satisfacción:** Realizar encuestas de clima laboral y brindar capacitación a gerentes para mejorar la satisfacción y el compromiso de sus equipos.

---

### Cómo Ejecutar el Notebook

1.  Clona este repositorio en tu máquina local.
2.  Instala las dependencias necesarias (`pip install pandas numpy scikit-learn matplotlib seaborn imblearn-learn xgboost lightgbm`).
3.  Abre el archivo `1HR_Atrition.ipynb` en tu entorno de desarrollo (`Jupyter`, `VS Code`, etc.) y ejecuta las celdas una por una.
