# **Análisis Rápido de Áreas Afectadas por Desborde de Ríos en los Andes Venezolanos**

### **1. El Problema**

La región de los Andes venezolanos es altamente vulnerable a desbordes
de ríos, un riesgo agravado por el cambio climático. La persistente
nubosidad dificulta el monitoreo con satélites ópticos, creando una
necesidad crítica de análisis rápido y fiable de las áreas afectadas. El
pasado 24 de junio de 2025 se reportó un desbordamiento en la zona del
Páramo del estado Mérida, Venezuela. Se organizó una fuerza de trabajo
de especialistas en geomática para realizar una evaluación rápida con
fines humanitarios.

### **2. Metodología**

Para superar la limitación de la nubosidad, el producto se basa en el
**algoritmo Reactive**, aplicado a series temporales de imágenes de
**Radar de Apertura Sintética (SAR) de Sentinel-1** en la plataforma
**Google Earth Engine (GEE)**. Reactive detecta cambios en la señal SAR
que indican la presencia de agua.

Complementariamente, para la mancha de inundación del Río Chama, se
utilizó **clasificación y fotointerpretación** de imágenes ópticas
**Landsat-8 y Landsat-9 (post-evento)**, con imágenes **Worldview-2
(pre-evento)** como fondo para contextualizar vegetación e
infraestructura.

Las áreas inundadas detectadas se combinan con el dataset **Global ML
Building Footprints de Microsoft** para identificar las edificaciones
expuestas, mediante un análisis de intersección espacial.

### **3. Datos Utilizados**

-   **Imágenes SAR:** Sentinel-1 (para detección de cambios con
    Reactive).

-   **Imágenes ópticas post-evento:** Landsat-8 (26 de Junio de 2025,
    15m de resolución) y Landsat-9 (25 de Junio de 2025, 15m de
    resolución).

-   **Imágenes ópticas pre-evento (fondo):** Worldview-2 (12 de Febrero
    de 2024, 0.5m de resolución).

-   **Infraestructuras:** [Global ML Building Footprints](https://github.com/microsoft/GlobalMLBuildingFootprints) de Microsoft
    (más de 1.4 mil millones de huellas de edificios a nivel mundial).

-   **CRS:** EPSG:32618 WGS 84 / UTM zone 18N.

-   **Software:** Producto generado con ArcGIS Pro.

### **4. Resultados**

El análisis preliminar post-evento en la cuenca del río Chama identificó:

-   **241 edificaciones afectadas** a lo largo de aproximadamente **70
    kilómetros** del cauce del río, entre Mucurubá y la entrada de los
    túneles de El Vigía.

-   Se generaron **14 archivos en formato GeoPDF** para facilitar su
    distribución y lectura tanto en herramientas GIS como en lectores
    PDF sencillos.

[Serie 1 de productos: Hojas geoPDF con espaciomapas](Serie001/)  
    [Polígono de la mancha de afectación](Serie001/vectores/) interpretada a partir de datos de satélite LANDSAT.  

[Memoria descriptiva](MemoriaDescriptiva.docx)

### **5. Conclusiones**

Este producto cartográfico representa una herramienta estratégica para
la gestión de desastres, proporcionando un **análisis rápido y preciso**
de las áreas afectadas por inundaciones, incluso en condiciones de alta
nubosidad. La combinación de tecnologías SAR, algoritmos de detección de
cambios y datos de infraestructura global permite una **evaluación
preliminar del impacto** en edificaciones, lo que es crucial para la
**toma de decisiones ágil** en situaciones de emergencia y para la
**planificación de la resiliencia** a largo plazo en los Andes
venezolanos.

