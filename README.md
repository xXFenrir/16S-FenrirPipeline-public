<div align="center">

# 16S-FenrirPipeline

**Predicción de interacciones bacteria-fago en el rizobioma de la gulupa con DeepPBI-KG**

</div>

## Introducción

Esta rama describe la implementación de **DeepPBI-KG** ([Wei et al., 2024](https://github.com/Tongqing-Wei/DeepPBI-KG)) desarrollada para el trabajo de grado *Análisis del microbioma de Passiflora edulis f. edulis mediante secuenciación dirigida al gen 16S usando MinION y predicción de las posibles interacciones bacteria-fago* (Johann Sebastian Gallego Sierra, Universidad El Bosque). DeepPBI-KG es un modelo de aprendizaje profundo que estima la probabilidad de que un fago interactúe con una bacteria a partir de sus genomas. Se adaptó para recibir los perfiles taxonómicos que entrega el pipeline 16S y evaluar las combinaciones entre las bacterias más abundantes y los 3513 fagos de referencia del modelo.

El modelo, sus pesos y el panel de fagos de referencia pertenecen a sus autores.

Por motivos de confidencialidad, los códigos de esta adaptación y la totalidad de los datos utilizados no están abiertos al público. Aquí solo se publican la descripción de los pasos y sus diagramas. Los códigos y los datos pueden solicitarse al autor bajo acuerdo académico. Los anexos del documento están en la rama [`anexos`](../../tree/anexos).

## Pasos del algoritmo

El algoritmo se aplicó a dos conjuntos de datos: las abundancias del BioProject PRJNA1020132, que sirvieron para validar la implementación (Objetivo 2), y las abundancias de las muestras de rizobioma de gulupa (Objetivo 3).

<p align="center">
  <img src="imagenes/flujo_deeppbi-kg.jpg" alt="Flujo de predicción con DeepPBI-KG: genomas bacterianos y de fagos, BLASTn y Prokka, predicción de interacciones" width="700">
</p>

| Paso | Descripción |
|---|---|
| 1. Selección y descarga de genomas | Genomas de referencia de los taxones con abundancia promedio de al menos 0,1 % |
| 2. Anotación y alineamiento | Prokka y BLASTn |
| 3. Predicción con DeepPBI-KG | Probabilidades de genes clave y de genoma completo para cada par fago-bacteria |
| 4. Filtrado de interacciones | Umbral de probabilidad promediada mayor a 0,85 |
| 5. Redes de interacción | Gephi |

<details>
<summary><b>Revisión bibliográfica para escoger el algoritmo</b></summary>
<br>

DeepPBI-KG se escogió tras una búsqueda en Google Scholar, ScienceDirect y Oxford Academic (2020 en adelante). De ella salieron 8 herramientas con software publicado y repositorio de acceso libre (PTBGRP, CoMPHI, PB-LKS, PHISDetector, DeepPBI-KG, GSPHI, iPHoP y PBIP), que se compararon por reproducibilidad, costo computacional e interpretabilidad biológica.

<p align="center">
  <img src="imagenes/prisma_objetivo2.jpg" alt="Diagrama de flujo PRISMA de la búsqueda del algoritmo predictivo: 47 159 registros identificados y 1 estudio incluido" width="700">
  <br><sub>Diagrama de flujo PRISMA para la búsqueda y selección del algoritmo predictivo</sub>
</p>
</details>
