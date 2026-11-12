<div align="center">

# 16S-FenrirPipeline

**Rizobioma de la gulupa con secuenciación 16S en Oxford Nanopore y predicción de interacciones bacteria-fago**

</div>

## Introducción

Esta rama describe el pipeline desarrollado para el trabajo de grado *Análisis del microbioma de Passiflora edulis f. edulis mediante secuenciación dirigida al gen 16S usando MinION, y predicción de las posibles interacciones bacteria-fago* (Johann Sebastian Gallego Sierra, Universidad El Bosque). El pipeline procesa lecturas del gen 16S rRNA completo obtenidas con MinION, desde la señal cruda hasta la diversidad microbiana.

Por motivos de confidencialidad, los códigos del pipeline y la totalidad de los datos utilizados no están abiertos al público. Aquí solo se publican la descripción de los pasos y sus diagramas. Los códigos y los datos pueden solicitarse al autor bajo acuerdo académico. Los anexos del documento están en la rama [`anexos`](../../tree/anexos).

## Pasos del pipeline

El pipeline se aplicó a dos conjuntos de datos: las 88 muestras públicas del BioProject PRJNA1020132 (Erlandson et al., 2024), que sirvieron para validarlo (Objetivo 1), y las muestras propias de rizobioma de gulupa (Objetivo 3).

<p align="center">
  <img src="imagenes/flujo_objetivos.jpg" alt="Flujo del pipeline para los Objetivos 1 y 3" width="900">
</p>

| Paso | Herramientas |
|---|---|
| 1. Basecalling y demultiplexing | Dorado |
| 2. Reporte de estadísticas básicas | Estadísticas por muestra de las lecturas (número, longitud, N50, GC y QScore) |
| 3. Limpieza: denoising y trimming | Pychopper y Filtlong |
| 4. Taxonomía | EMU |
| 5. Diversidad | Diversidad alfa y beta (Shannon, riqueza observada, Bray-Curtis, Jaccard, PCoA y PERMANOVA) |

### 1. Basecalling y demultiplexing

<p align="center">
  <img src="imagenes/paso1_basecalling.jpg" alt="Diagrama de caja del basecalling y demultiplexing con Dorado" width="700">
</p>

### 2 y 3. Estadísticas y limpieza

<p align="center">
  <img src="imagenes/paso2-3_estadisticas_limpieza.jpg" alt="Diagrama de caja del reporte de estadísticas y la limpieza con Filtlong y Pychopper" width="700">
</p>

### 4. Taxonomía

<p align="center">
  <img src="imagenes/paso4_taxonomia.jpg" alt="Diagrama de caja de la clasificación taxonómica con EMU: minimap2 y esperanza-maximización" width="800">
</p>

### 5. Diversidad

<p align="center">
  <img src="imagenes/paso5_diversidad.jpg" alt="Diagrama de caja de las estadísticas poblacionales: diversidad alfa y beta" width="650">
</p>

<details>
<summary><b>Diagrama detallado del pipeline</b></summary>
<br>
<p align="center">
  <img src="imagenes/flujo_pipeline.jpg" alt="Diagrama detallado del pipeline: Dorado, Filtlong, Pychopper, EMU y cálculo de diversidad" width="650">
</p>
</details>

<details>
<summary><b>Revisión bibliográfica para escoger las herramientas</b></summary>
<br>

Las herramientas de cada paso se escogieron a partir de una búsqueda en Google Scholar, ScienceDirect, SpringerLink y la Biblioteca Juan Roa Vázquez con la ecuación `bioinformatics AND 16S oxford nanopore AND (soils OR passiflora)`. Solo seis estudios tenían una metodología bioinformática completa y las lecturas 16S disponibles en un repositorio.

<p align="center">
  <img src="imagenes/prisma_objetivo1.jpg" alt="Diagrama de flujo PRISMA de la búsqueda bibliográfica: 11 483 registros identificados y 6 estudios incluidos" width="700">
  <br><sub>Diagrama de flujo PRISMA de la búsqueda bibliográfica</sub>
</p>
</details>
