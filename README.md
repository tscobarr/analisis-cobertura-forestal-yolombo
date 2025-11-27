# Análisis de Cobertura Forestal en Yolombó, Antioquia

Este repositorio contiene el proyecto completo para analizar el estado actual del paisaje forestal del municipio de Yolombó (Antioquia, Colombia), utilizando imágenes satelitales, QGIS y Python. El proceso combina geotecnologías e inteligencia artificial para obtener índices de vegetación, segmentación automática del paisaje y métricas de fragmentación.

## 1. Contexto del Proyecto

El propósito del proyecto es evaluar la cobertura vegetal de Yolombó a partir de mosaicos satelitales generados en QGIS. El análisis permite identificar:

- Zonas con cobertura boscosa conservada  
- Áreas abiertas o transformadas  
- Patrones de fragmentación  
- Evidencias de degradación o presión antrópica  

Yolombó se encuentra en una región ecológica importante del nordeste de Antioquia. Su paisaje ha sido modificado por actividades como la ganadería y la agricultura. Evaluar su estado actual ayuda a:

1. La planificación territorial sostenible  
2. La conservación de la biodiversidad  
3. La restauración de áreas degradadas  
4. El monitoreo de servicios ecosistémicos  

## 2. Metodología General

### 2.1 Procesamiento Geográfico en QGIS

- Carga del shapefile de Antioquia y recorte del municipio de Yolombó  
- Uso de Google Satellite como base raster  
- Creación de una cuadrícula regular de 5×5 km  
- Filtrado de celdas que intersectan con el municipio  
- Configuración de un layout  
- Exportación automática de los mosaicos raster en formato PNG  

### 2.2 Análisis en Python

- Lectura de todos los mosaicos PNG  
- Cálculo de índices de vegetación basados en RGB  
- Análisis estadístico por tile  
- Segmentación con K-Means  
- Clasificación del paisaje  
- Métricas de fragmentación  
- Visualizaciones  

## 3. Estructura del Repositorio

```
analisis-cobertura-forestal-yolombo/
│
├── notebooks/
│   └── analisis_yolombo.ipynb
│
├── tiles/
│
├── resultados
│
└── README.md
```

## 4. Librerias

```bash
!pip install opencv-python-headless numpy pandas scikit-learn matplotlib seaborn scipy
```

## 5. Resultados Generales

- 69 mosaicos exportados  
- Más del 90% del territorio con vegetación  
- Cerca del 4% corresponde a áreas abiertas o transformadas  
- Fragmentación notable en varios sectores  

## 6. Licencia

MIT License

## 7. Autor

Desarrollado por:  
Tomás Escobar Rivera
