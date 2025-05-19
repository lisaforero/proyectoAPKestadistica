# AppEst 

APK móvil para el análisis exploratorio de datos, entrenamiento de modelos de regresión y clasificación, y visualización de correlaciones. Desarrollada en Kotlin.

## Características principales
- Carga de archivos CSV

- Mini EDA

  - Conteo de filas, tipos de columnas, valores nulos

  - Estadísticos descriptivos

  - Visualizaciones automáticas:

      - Boxplot para numéricas

      - Barras para categóricas (detecta variables dicotómicas también)

- Análisis de correlación

  - Selección de dos variables (numéricas o categóricas)

  - Recomendación automática del mejor tipo de correlación:

      - Pearson

      - Spearman

      - Punto biserial (para dicotómicas)

  - Gráficos correspondientes:

      - Dispersión con línea de tendencia

      - Boxplot para correlaciones biseriales

- Modelo de Regresión Lineal

  - Selección de variable respuesta y predictoras

  - Muestra:

    - Ecuación del modelo

    - R² y RMSE

    - Gráfico de residuos

    - ANOVA, F-statistic, p-valor

- Modelo de Clasificación (LDC)
  - Selección de variable respuesta y predictoras
    
  - Si se tiene una variable de respuesta categórica se puede tratar

  - Muestra:

    - Regla del modelo

    - Accuracy, Precision, Recall, F1-Score

    - Matriz de confusión (multiclase incluida)

    - Validación cruzada (usando un 80% de los datos para entrenamiento y 20% para el test)

- Heat Map

## Tecnologías utilizadas
- Kotlin (es un lenguaje de programación moderno, conciso, y seguro, desarrollado por JetBrains. Se usa principalmente para desarrollar apps Android. Es completamente interoperable con Java)

- ViewModel + StateFlow (se usan juntos para manejar y emitir el estado de la UI de forma reactiva y segura. El ViewModel expone un StateFlow, y la UI lo observa para actualizarse automáticamente cuando los datos cambian)

- MVVM (Model-View-ViewModel es un patrón de arquitectura de software utilizado principalmente en el desarrollo de aplicaciones con interfaces gráficas de usuario)

## Cómo ejecutar
1. Clona este repositorio:
   ```
   git clone https://github.com/lisaforero/proyectoAPKestadistica.git
   ```
2. Ejecuta **app-debug.apk** en un emulador o dispositivo físico.

3. Carga un archivo .csv desde la memoria del dispositivo. Y ¡explora!

## Notas adicionales
- Se limita la cantidad de filas a 1000 para evitar cuelgues o sobrecarga.
- El sistema evita cerrar la app si el usuario carga un archivo inválido, mostrando un mensaje amigable.
- El botón "Limpiar" borra el dataset cargado y todos los cálculos anteriores.
- Soporta variables con etiquetas de texto (ej. "Yes", "No") y las transforma automáticamente.

## Autoras
Este proyecto se llevo a cabo durante el semestre de 2025-1 para la asignatura Modelos Regresión perteneciente al programa académico Ingeniería Estadística de la Universidad Escuela Colombiana de Ingeniería Julio Garavito.
Es una idea desarrollada por:
- Paula Andrea Gacha García
- Lina Janeth Sánchez Forero
