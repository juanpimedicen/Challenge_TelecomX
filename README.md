# 📉 Análisis de Evasión de Clientes (Churn) en Telecomunicaciones

## 📝 Descripción General del Proyecto

Este proyecto se enfoca en un análisis exhaustivo para comprender y predecir la **evasión de clientes (churn)** en una empresa de servicios de telecomunicaciones. La finalidad es identificar los factores y comportamientos que llevan a los clientes a cancelar sus servicios, proporcionando insights accionables para la retención.

## ⚠️ El Problema del Churn

La evasión de clientes representa una **pérdida directa de ingresos** y es un indicador crítico de insatisfacción, deficiencias en los servicios o una baja efectividad en las estrategias de fidelización. El objetivo principal de este análisis es **identificar patrones y perfiles de clientes** con mayor propensión a la cancelación, permitiendo a la empresa anticipar y mitigar estas bajas a través de acciones estratégicas basadas en datos.

## ⚙️ Preparación y Preprocesamiento de Datos

Los datos fueron obtenidos de un archivo JSON y se sometieron a un riguroso proceso de limpieza y transformación para asegurar su calidad y consistencia:

* Conversión de valores numéricos de formato *string* a tipos de datos apropiados.
* Manejo de valores faltantes (eliminación de registros).
* Estandarización y conversión de categorías (ej. `churn` de "Sí"/"No" a `0`/`1`, `gender`, `payment_method`).

## 📊 Análisis Exploratorio de Datos (EDA) y Hallazgos Clave

El análisis exploratorio reveló información valiosa sobre el comportamiento de los clientes y los factores asociados al churn:

### Tasa General de Evasión
* Aproximadamente el **26.58%** de los clientes en la base de datos han cancelado el servicio.

### Factores Influyentes
* **Tipo de Contrato:** Se observó una **mayor tasa de evasión entre clientes con contratos de modalidad mensual**, sugiriendo una menor fidelización en comparación con contratos anuales.
* **Método de Pago:** Los clientes que utilizan **"Electronic check"** como método de pago presentan una **tasa de evasión considerablemente más alta**.
* **Gasto Total (`total_charges`) y Antigüedad (`tenure`):**
    * Los clientes que cancelan tienden a tener **montos acumulados de gasto (total_charges) significativamente menores**. Esto indica que muchos abandonan el servicio poco después de su inicio o son usuarios de bajo consumo.
    * Confirmando lo anterior, la mayoría de los clientes que churnean también exhiben un **tiempo de permanencia (tenure) más corto**.
    * El análisis de la distribución de `total_charges` para los clientes que churnean mostró una fuerte concentración en rangos de gasto bajos, con una cola extendida de clientes de mayor gasto que también se desvinculan.
* **Género:** El análisis no mostró **diferencias significativas** en la tasa de evasión entre hombres y mujeres.

## 💡 Conclusiones Principales

* La **baja antigüedad del contrato** y la preferencia por **contratos mensuales** son indicadores clave de riesgo de churn.
* El **método de pago por cheque electrónico** está fuertemente asociado con una mayor propensión a la evasión.
* Un **menor gasto total acumulado** es una característica predominante de los clientes que cancelan, lo que subraya la importancia de la fidelización temprana.

## 🚀 Recomendaciones Estratégicas

Para mitigar la tasa de churn, se proponen las siguientes acciones:

1.  **Incentivar Contratos a Largo Plazo:** Diseñar ofertas y beneficios exclusivos para clientes que se comprometan con contratos de mayor duración.
2.  **Mejorar la Experiencia Inicial del Cliente:** Implementar programas de bienvenida y soporte proactivo durante los primeros meses para reducir la deserción temprana.
3.  **Optimizar el Proceso de Pago Electrónico:** Realizar una revisión y mejora del proceso de pago con "Electronic check" para identificar y eliminar posibles puntos de fricción.
4.  **Campañas de Retención Focalizadas:** Desarrollar iniciativas de retención dirigidas específicamente a clientes con baja antigüedad (`tenure`) y bajos montos de `total_charges`.
5.  **Encuestas de Salida Dirigidas:** Implementar encuestas post-churn con clientes recientes para obtener feedback directo y entender las razones específicas de su cancelación.

## 💻 Tecnologías Utilizadas

* **Python**
* **Pandas** (para manipulación y análisis de datos)
* **Matplotlib** (para visualización de datos)
* **Seaborn** (para visualización de datos estadísticos)

## 👤 Autor

### Juan Guilarte, juanpimedicen
Ingeniero en telecomunicaciones
