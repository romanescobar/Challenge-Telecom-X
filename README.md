# Análisis de Evasión de Clientes (Churn) - Telecom X

## 📊 Descripción del Proyecto

Este proyecto tiene como objetivo principal identificar y analizar los factores clave que influyen en la evasión de clientes (también conocido como "Churn") en una empresa de telecomunicaciones, Telecom X. A través de un exhaustivo Análisis Exploratorio de Datos (EDA), se buscan patrones y relaciones entre las características de los clientes y su propensión a cancelar el servicio, con el fin de informar estrategias de retención.

## 🎯 Objetivos del Análisis

* Comprender la distribución general de la evasión de clientes.
* Identificar variables categóricas y numéricas que están fuertemente asociadas con la evasión.
* Determinar los segmentos de clientes con mayor riesgo de evasión.
* Proporcionar insights accionables y recomendaciones estratégicas para reducir la tasa de churn.

## 🚀 Fases del Proyecto

El análisis se llevó a cabo siguiendo las siguientes fases:

### 1. Carga y Estructura Inicial de Datos
* Carga de datos desde un archivo JSON para construir el DataFrame inicial.
* Verificación de la estructura y tipos de datos de las columnas.

### 2. Limpieza y Preprocesamiento de Datos
* **Desanidado de Columnas:** Las columnas anidadas (`customer`, `phone`, `internet`, `account`) fueron desanidadas para acceder fácilmente a sus atributos.
* **Verificación de Duplicados:** Se comprobó la existencia de filas completamente duplicadas y de IDs de cliente duplicados, asegurando la unicidad de los registros. No se encontraron duplicados.
* **Tratamiento de Valores Nulos:** Se identificaron y gestionaron 11 valores no numéricos en `Charges.Total`, convirtiéndolos a `NaN` y posteriormente asegurando su tipo de dato `float64`.
* **Conversión de Tipos de Datos:** Las variables categóricas binarias (ej., `gender`, `Partner`) fueron convertidas a formato numérico (0 y 1). Las variables categóricas multi-clase (ej., `InternetService`, `Contract`, `PaymentMethod`) fueron transformadas usando One-Hot Encoding.
* **Creación de `Cuentas_Diarias`:** Se añadió una nueva columna calculando los cargos diarios a partir de `Charges.Monthly` para un análisis más granular.

### 3. Análisis Exploratorio de Datos (EDA)

* **Distribución de Evasión:** Se visualizó la proporción de clientes que evaden (26.58%) versus los que permanecen (73.42%).
* **Análisis por Variables Categóricas:** Se exploró la tasa de evasión en función de diversas características binarias y categóricas (género, tipo de contrato, método de pago, servicios adicionales, etc.) mediante gráficos de barras.
* **Análisis por Variables Numéricas:** Se examinó la distribución de la permanencia (`tenure`), cargos mensuales (`Charges.Monthly`) y cargos totales (`Charges.Total`) para clientes que evaden y no evaden, utilizando box plots.
* **Análisis de Correlación (Opcional):** Se calculó y visualizó una matriz de correlación para entender las relaciones lineales entre las variables clave y la evasión, incluyendo la relación de `Cuentas_Diarias` y `Num_Services` con `Churn`.

### 4. Conclusiones e Insights

Los hallazgos clave incluyen:

* **Contratos Mes a Mes:** Clientes con contratos mensuales presentan la tasa de evasión más alta (42.71%).
* **Método de Pago:** El "Cheque Electrónico" es el método de pago con mayor tasa de evasión (45.29%).
* **Servicio de Internet Fibra Óptica:** Los clientes de fibra óptica evaden significativamente más (41.89%).
* **Permanencia (`tenure`):** La mayoría de las evasiones ocurren en los primeros meses de servicio.
* **Servicios Adicionales:** La ausencia de servicios como seguridad en línea y soporte técnico aumenta la probabilidad de evasión.
* **Cargos Mensuales:** Clientes con cargos mensuales más altos tienden a evadir más.
* **Otros Factores:** `Senior Citizens`, clientes sin pareja o dependientes, y aquellos con facturación sin papel también muestran mayor riesgo.

### 5. Recomendaciones Estratégicas

* **Incentivar Contratos Largos:** Ofrecer beneficios para fomentar contratos de 1 o 2 años.
* **Revisar el Pago con Cheque Electrónico:** Investigar y abordar las posibles causas de insatisfacción asociadas a este método.
* **Mejorar la Experiencia de Fibra Óptica:** Monitorear la calidad del servicio y la satisfacción de estos clientes.
* **Programas de Bienvenida:** Implementar un seguimiento proactivo y soporte intensivo durante los primeros meses del cliente.
* **Promover Servicios de Valor Añadido:** Destacar la importancia de servicios como seguridad y soporte técnico.
* **Estrategias Segmentadas:** Desarrollar acciones de retención específicas para segmentos de alto riesgo.

## 🛠️ Herramientas Utilizadas

* **Lenguaje de Programación:** Python
* **Librerías:**
    * `pandas` para manipulación y análisis de datos.
    * `matplotlib` para visualización de datos.
    * `seaborn` para visualizaciones estadísticas avanzadas.

## 📞 Contacto

Para cualquier consulta o colaboración, no dudes en contactar.
