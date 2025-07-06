# 📊 Análisis de Datos de Ventas Regionales para Optimización de Comisiones - ADL Company

## Resumen Ejecutivo (Executive Summary)

Este proyecto aborda el análisis de los datos de ventas de **ADL Company**, una empresa dedicada a la venta de productos a nivel regional en los Estados Unidos. [cite_start]El objetivo principal es comprender el rendimiento de sus equipos de ventas, analizar la eficiencia en los tiempos de entrega y evaluar el impacto de su sistema de comisiones, que busca incentivar la venta de productos de alto margen. [cite: 1]

Como Analista de Datos, se me solicitó examinar información detallada sobre productos vendidos, clientes, fechas de pedidos y plazos de entrega. [cite_start]A través de la manipulación, transformación y visualización de datos, este análisis busca responder preguntas clave de negocio como: [cite: 1]
* ¿Cuál es la distribución de los tiempos de entrega de los productos a los clientes?
* ¿Cómo se distribuyen las órdenes en función de los días de entrega y qué equipo de ventas tiene el mejor desempeño en cada intervalo?
* ¿Cuál es la contribución de cada equipo de ventas en términos de margen bruto, comisión y margen neto?

Los resultados de este análisis proporcionarán `insights` accionables para la dirección de ADL, permitiendo optimizar la cadena de suministro, evaluar la efectividad de las políticas de comisiones y mejorar el rendimiento general de los equipos de ventas.

## 📁 Contenido del Repositorio

Este repositorio contiene los siguientes archivos:

* `analisis_ventas_adl_cristian_gaete.ipynb`: El Jupyter Notebook principal con todo el código de análisis, explicaciones, transformaciones de datos y visualizaciones.
* `US_Regional_Sales_Data.xlsx`: El archivo de datos original con la información de órdenes de venta, clientes, ubicaciones de tiendas, productos y equipos de ventas.
* `reportes.xlsx`: Un archivo de referencia con los reportes esperados (Reporte1 y Reporte2) para validación de los resultados.

## 🛠️ Tecnologías Utilizadas

* **Python**: Lenguaje de programación principal para el análisis.
* **Pandas**: Librería fundamental para la manipulación y análisis de datos en Python.
* **NumPy**: Librería para operaciones numéricas avanzadas.
* **Matplotlib**: Librería para la creación de visualizaciones estáticas.
* **Seaborn**: Librería para la creación de gráficos estadísticos más atractivos.
* **Microsoft Excel / Google Sheets**: Utilizado para la gestión y provisión de los datos de origen.

## 🚀 Cómo Ejecutar el Proyecto

Para replicar el análisis de este proyecto en tu entorno local, sigue estas instrucciones:

1.  **Clona el Repositorio:**
    ```bash
    git clone [https://github.com/tu_usuario/analisis_ventas_adl_company.git](https://github.com/tu_usuario/analisis_ventas_adl_company.git)
    ```
    (Asegúrate de reemplazar `tu_usuario` con tu nombre de usuario de GitHub).
2.  **Navega al Directorio del Proyecto:**
    ```bash
    cd analisis_ventas_adl_company
    ```
3.  **Instala las Dependencias:**
    Asegúrate de tener Python instalado (versión 3.x recomendada). Puedes instalar las librerías necesarias con pip:
    ```bash
    pip install pandas numpy matplotlib seaborn openpyxl
    ```
    (Nota: `openpyxl` es necesario para leer archivos `.xlsx` con Pandas).
4.  **Abre el Jupyter Notebook:**
    ```bash
    jupyter notebook analisis_ventas_adl_cristian_gaete.ipynb
    ```
    Esto abrirá el notebook en tu navegador web. Puedes ejecutar las celdas secuencialmente para ver el análisis completo.

## 📈 Hallazgos Clave y Visualizaciones

A continuación, se presentan algunas de las visualizaciones generadas y los hallazgos más relevantes del análisis.

### **1. Conteo de Órdenes por Equipo de Ventas e Intervalo de Días de Cliente**

Este `heatmap` muestra la distribución de la cantidad de órdenes según el equipo de ventas y el tiempo de entrega al cliente. Permite identificar rápidamente qué equipos gestionan entregas más rápidas o más lentas.

![Conteo de Órdenes por Equipo de Ventas e Intervalo de Días de Cliente](images/heatmap_reporte1.png)

**Hallazgo:** La mayoría de las órdenes se entregan en el rango de **15 a 30 días**, seguido por el rango de **0 a 15 días**. [cite_start]Los intervalos superiores a 45 días no registran órdenes, lo que sugiere una gestión de entrega relativamente eficiente, aunque con oportunidades de optimización en los tiempos más largos. [cite: 1]

### **2. Márgenes y Comisiones Totales por Equipo de Ventas**

Este gráfico de barras apiladas compara el Margen Bruto (`GrossMargin`), el Margen Neto (`NetMargin`) y el Monto de Comisiones (`CommissionsAmount`) generados por cada equipo de ventas.

![Márgenes y Comisiones Totales por Equipo de Ventas](images/bar_chart_reporte2.png)

**Hallazgo:** El análisis de los márgenes y comisiones revela que algunos equipos de ventas contribuyen significativamente más al `GrossMargin` y, consecuentemente, generan mayores `CommissionsAmount` y `NetMargin`. [cite_start]Esto valida la efectividad del modelo de comisiones en incentivar la venta de productos de mayor rentabilidad. [cite: 1]

### **3. Relación entre Margen Bruto y Monto de Comisión por Orden**

Este gráfico de dispersión visualiza la relación directa entre el `GrossMargin` de una orden y el `CommissionsAmount` calculado para la misma, con una escala logarítmica para manejar el amplio rango de valores.

![Relación entre Margen Bruto y Monto de Comisión por Orden](images/scatterplot_grossmargin_commissions.png)

[cite_start]**Hallazgo:** La distribución de los `CommissionsPercentage` muestra que la mayoría de las transacciones se encuentran en los rangos de margen bruto medio a alto (10% y 15%), lo que es positivo para la rentabilidad de la empresa. [cite: 1]

## 💡 Recomendaciones

1.  **Optimización de Tiempos de Entrega:** Investigar los factores que contribuyen a los envíos que caen en el intervalo de **30 a 45 días** para identificar cuellos de botella y buscar estrategias de reducción, como la optimización de rutas de envío o la mejora de los procesos de almacén. [cite_start]Esto podría traducirse en mayor satisfacción del cliente y potencial aumento de ventas. [cite: 1]
2.  **Incentivos por Margen:** Continuar monitoreando la correlación entre `GrossMargin` y `CommissionsAmount`. [cite_start]Considerar si ajustes finos en los umbrales o porcentajes de comisión podrían incentivar aún más la venta de los productos de más alto margen sin desmotivar las ventas de menor margen. [cite: 1]
3.  [cite_start]**Capacitación de Equipos:** Analizar los equipos de ventas con menor `GrossMargin` o `NetMargin` y ofrecer capacitación específica en técnicas de venta de productos de alto margen o estrategias para reducir los descuentos aplicados sin afectar el volumen de ventas. [cite: 1]

## 🚀 Próximos Pasos

* Explorar el impacto de otras variables disponibles en el dataset, como el canal de ventas (`Sales Channel`) o la categoría de producto (`Product Name`), en el desempeño de las ventas y la eficiencia operativa.
* Realizar un análisis de series de tiempo para identificar patrones estacionales o tendencias a lo largo del tiempo.
* Integrar datos adicionales (ej. demográficos del cliente, feedback de satisfacción) para un análisis más holístico y la construcción de modelos predictivos.

## 📧 Contacto

Cristian Gaete
* [Tu LinkedIn](https://www.linkedin.com/in/cgaeter)
* [Tu Correo Electrónico](mailto:cristian.gaeter@gmail.com)
