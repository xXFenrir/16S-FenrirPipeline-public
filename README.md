# 16S-FenrirPipeline — Anexos del trabajo de grado

Trabajo de grado: *Análisis del microbioma de Passiflora edulis f. edulis mediante secuenciación dirigida al gen 16S usando MinION, y predicción de las posibles interacciones bacteria-fago*. Johann Sebastian Gallego Sierra, Universidad El Bosque.

## Contenido del repositorio

Este repositorio público reúne los anexos del documento. Los Anexos 1 a 14 se publican completos. De los Anexos 15, 17, 18, 19, 21 y 22 solo se publican las imágenes, y los Anexos 16 y 20 no están abiertos al público.

La totalidad de los datos utilizados no está abierta al público, y tampoco los códigos con los que se procesaron. Los códigos del pipeline 16S ONT (basecalling, estadísticas, limpieza, taxonomía y diversidad) y del algoritmo de predicción de interacciones bacteria-fago (DeepPBI-KG) se mantienen en un repositorio privado por motivos de confidencialidad. Las ramas `pipeline` y `algoritmo` de este repositorio solo contienen la descripción de los pasos y sus diagramas. Los datos y los códigos pueden solicitarse al autor bajo acuerdo académico.

| Rama | Contenido |
|---|---|
| `anexos` (Aquí) | Anexos del documento |
| [`pipeline`](../../tree/pipeline) | Descripción y diagramas del pipeline 16S ONT (sin código) |
| [`algoritmo`](../../tree/algoritmo) | Descripción y diagramas de la predicción con DeepPBI-KG (sin código) |

## Índice de anexos

Los anexos reúnen los resultados y la información que no pudieron incluirse en el cuerpo del texto. Están numerados en el orden en que aparecen las secciones de Resultados del documento con las que se relacionan, indicadas en la última columna.

| Anexo | Carpeta | Contenido principal | Sección de Resultados donde se usa |
|---|---|---|---|
| 1 | [Anexo_01_Herramientas_pipelines_referencia](Anexo_01_Herramientas_pipelines_referencia) | Herramientas por etapa en seis pipelines 16S de referencia | Obj. 1 › Caracterización de herramientas bioinformáticas |
| 2 | [Anexo_02_Metadata_PRJNA1020132](Anexo_02_Metadata_PRJNA1020132) | Metadata del BioProject, SraRunTable y datos de muestra del artículo | Obj. 1 › Selección de repositorios; Diseño conceptual: Reporte de estadísticas básicas |
| 3 | [Anexo_03_Estadisticas_pre_limpieza](Anexo_03_Estadisticas_pre_limpieza) | Estadísticas básicas de las 88 muestras crudas | Obj. 1 › Diseño conceptual: Reporte de estadísticas básicas; Diseño conceptual: Denoising y trimming |
| 4 | [Anexo_04_Estadisticas_post_limpieza](Anexo_04_Estadisticas_post_limpieza) | Estadísticas tras Filtlong + Pychopper y retención por muestra | Obj. 1 › Diseño conceptual: Denoising y trimming |
| 5 | [Anexo_05_Abundancia_generos_referencia](Anexo_05_Abundancia_generos_referencia) | Abundancias relativas por género del artículo | Obj. 1 › Diseño conceptual: Taxonomía |
| 6 | [Anexo_06_Abundancia_especies_referencia](Anexo_06_Abundancia_especies_referencia) | Abundancias relativas por especie del artículo | Obj. 1 › Diseño conceptual: Taxonomía |
| 7 | [Anexo_07_Diferencias_por_familia](Anexo_07_Diferencias_por_familia) | Abundancias relativas por familia (propias y del artículo), medias y correlación de Pearson (familia) | Obj. 1 › Diseño conceptual: Taxonomía |
| 8 | [Anexo_08_Diferencias_por_genero](Anexo_08_Diferencias_por_genero) | Medias propias vs. artículo y correlación de Pearson (género) | Obj. 1 › Diseño conceptual: Taxonomía |
| 9 | [Anexo_09_Diferencias_por_especie](Anexo_09_Diferencias_por_especie) | Medias propias vs. artículo y correlación de Pearson (especie) | Obj. 1 › Diseño conceptual: Taxonomía |
| 10 | [Anexo_10_Diversidad_PRJNA1020132](Anexo_10_Diversidad_PRJNA1020132) | Shannon y riqueza observada, Bray-Curtis/Jaccard, PCoA y PERMANOVA del conjunto de referencia | Obj. 1 › Diseño conceptual: Diversidad |
| 11 | [Anexo_11_Comparacion_articulo_guia](Anexo_11_Comparacion_articulo_guia) | Comparación por muestra con el artículo guía en cada paso del pipeline | Obj. 1 › Diseño conceptual: Denoising y trimming; Diseño conceptual: Diversidad |
| 12 | [Anexo_12_Genomas_bacterianos_Obj2](Anexo_12_Genomas_bacterianos_Obj2) | 192 genomas descargados para el Objetivo 2 | Obj. 2 › Preparación de datos de entrada |
| 13 | [Anexo_13_Predicciones_DeepPBI-KG_Obj2](Anexo_13_Predicciones_DeepPBI-KG_Obj2) | Matriz completa de predicciones y tablas filtradas (umbral 0.85) | Obj. 2 › Filtrado de probabilidades; Comprobación con literatura |
| 14 | [Anexo_14_Redes_Gephi_Obj2](Anexo_14_Redes_Gephi_Obj2) | Grafos de Gephi (red completa y top 4) | Obj. 2 › Filtrado de probabilidades |
| 15 | [Anexo_15_Comparacion_modelos_Dorado](Anexo_15_Comparacion_modelos_Dorado) | Solo las figuras (lecturas aprobadas y QScore por modelo) | Obj. 3 › Basecalling y evaluación de calidad de secuencias |
| 16 | Anexo_16_Reportes_pycoQC_HAC_SUP | No abierto al público | Obj. 3 › Basecalling y evaluación de calidad de secuencias |
| 17 | [Anexo_17_Limpieza_gulupa_HAC_SUP](Anexo_17_Limpieza_gulupa_HAC_SUP) | Solo las gráficas comparativas de la limpieza (HAC, SUP y HAC frente a SUP) | Obj. 3 › Filtrado de calidad y remoción de ruido (Denoising y Trimming) |
| 18 | [Anexo_18_Taxonomia_EMU_gulupa](Anexo_18_Taxonomia_EMU_gulupa) | Solo las curvas de rarefacción | Obj. 3 › Clasificación taxonómica y análisis de rarefacción |
| 19 | [Anexo_19_Diversidad_gulupa_HAC_SUP](Anexo_19_Diversidad_gulupa_HAC_SUP) | Solo las figuras (diversidad alfa, mapas de calor, PCoA) | Obj. 3 › Diversidad Alfa y Beta |
| 20 | Anexo_20_Genomas_bacterianos_gulupa | No abierto al público | Obj. 3 › Interacciones bacteria-fago en muestras de gulupa |
| 21 | [Anexo_21_Predicciones_DeepPBI-KG_gulupa](Anexo_21_Predicciones_DeepPBI-KG_gulupa) | Solo las gráficas de densidad y reducción | Obj. 3 › Interacciones bacteria-fago en muestras de gulupa; Comprobación de interacciones en gulupa |
| 22 | [Anexo_22_Redes_Gephi_gulupa](Anexo_22_Redes_Gephi_gulupa) | Solo las imágenes de las redes | Obj. 3 › Interacciones bacteria-fago en muestras de gulupa |

## Descripción de los anexos

**Anexo 1. Herramientas bioinformáticas reportadas por artículo en cada etapa del procesamiento del gen 16S**

Resume las herramientas empleadas en seis estudios que analizan el gen 16S rRNA secuenciado con *Oxford Nanopore Technologies*, organizadas por etapa: basecalling, demultiplexing, denoising y trimming, clustering, asignación taxonómica, filogenia y diversidad.

**Anexo 2. Metadata del proyecto PRJNA1020132**

Contiene la información contextual y experimental del proyecto de referencia empleado para la comparación taxonómica, incluyendo códigos de acceso, descripción de muestras, condiciones de secuenciación y origen de los datos públicos utilizados como referencia (Erlandson et al., 2024).

**Anexo 3. Estadísticas básicas antes del proceso de limpieza**

Resume las métricas de calidad obtenidas en las lecturas crudas de las 88 muestras del proyecto PRJNA1020132, previas al filtrado, como número total de lecturas, longitud promedio, contenido GC, N50 y Q-scores. Permite evaluar la calidad inicial de las secuencias obtenidas mediante tecnología *Oxford Nanopore Technologies*.

**Anexo 4. Estadísticas básicas después del proceso de limpieza**

Presenta las mismas métricas del Anexo 3 calculadas sobre las lecturas que superaron el recorte de primers y filtrado por calidad con Pychopper (Q ≥ 12) y por longitud con Filtlong (1.000–1.700 pb). Incluye, para cada muestra, el porcentaje de lecturas y bases retenidas y removidas, lo que permite valorar el efecto de la limpieza.

**Anexo 5. Abundancia relativa de géneros del conjunto de referencia**

Contiene las abundancias relativas por género reportadas por Erlandson et al. (2024) para cada muestra del proyecto PRJNA1020132. Sirve como punto de comparación para validar la clasificación taxonómica obtenida con el pipeline propio.

**Anexo 6. Abundancia relativa de especies del conjunto de referencia**

Contiene las abundancias relativas por especie reportadas por Erlandson et al. (2024) para cada muestra del proyecto PRJNA1020132. Complementa el Anexo 5 en la comparación a nivel de especie.

**Anexo 7. Diferencia de abundancias relativas por familia**

Compara la abundancia relativa media de las 125 familias presentes en ambos análisis, obtenida con el pipeline propio y reportada en el artículo, junto con la correlación de Pearson entre ambas series. Incluye las abundancias por familia de cada muestra, tanto propias como del artículo. Contiene además las dos figuras de la comparación para los tres niveles taxonómicos (A, familia; B, género; C, especie): la dispersión de las abundancias medias de este estudio frente a las del artículo y las barras pareadas de los 10 taxones más abundantes en cada nivel.

**Anexo 8. Diferencia de abundancias relativas por género**

Compara la abundancia relativa media de los 328 géneros presentes en ambos análisis, obtenida con el pipeline propio y reportada en el artículo, junto con la diferencia entre ellas. Incluye la correlación de Pearson entre ambas series y las abundancias por género de cada muestra procesada en este estudio. Sus figuras están en el Anexo 7.

**Anexo 9. Diferencia de abundancias relativas por especie**

Presenta la misma comparación del Anexo 8 a nivel de especie, para las 788 especies detectadas tanto en este estudio como en el artículo de referencia. Incluye la correlación de Pearson y las abundancias por especie de cada muestra. Sus figuras están en el Anexo 7.

**Anexo 10. Diversidad microbiana del proyecto PRJNA1020132**

Reúne el análisis de diversidad del conjunto de referencia procesado con el pipeline propio: índices de Shannon y riqueza observada por muestra, prueba de Wilcoxon entre las rotaciones de cultivo CS y CSSwP, matrices de disimilitud de Bray-Curtis y Jaccard, coordenadas del PCoA y resultado de la PERMANOVA. Incluye además las tablas de abundancia y de conteos de EMU con las que se calcularon.

**Anexo 11. Comparación paso a paso con el artículo guía**

Compara, muestra por muestra, los resultados del pipeline propio con los de Erlandson et al. (2024) para las 88 muestras del proyecto PRJNA1020132 con datos en ambos análisis. Contrasta las bases de los archivos descargados con las del BioProject; las lecturas antes y después de la limpieza y las asignadas por EMU con las lecturas asignadas en el artículo; la disimilitud de Bray-Curtis, la correlación de Pearson y las especies compartidas entre los perfiles de una misma muestra en ambos análisis; los índices de Shannon y la riqueza observada; la prueba de Mantel entre las matrices de distancia, y la PERMANOVA por tipo de muestra y semana con el mismo método del artículo. Como el artículo no publicó estadísticas por etapa para 2020, las lecturas de cada paso se comparan con las que asignó EMU en el artículo. Incluye la figura con los ocho pasos de la comparación y las tablas de resumen, por muestra, de medias por tipo de muestra y de PERMANOVA.

**Anexo 12. Genomas bacterianos descargados para el Objetivo 2**

Lista los 192 genomas bacterianos descargados de NCBI para los taxones del proyecto PRJNA1020132 con abundancia relativa promedio de al menos 0,1 %, indicando su TaxID y si corresponden a la especie o a un genoma representante del género. Incluye el histograma de abundancias con el umbral de corte empleado.

**Anexo 13. Predicciones de DeepPBI-KG para el Objetivo 2**

Contiene la matriz completa de predicciones de DeepPBI-KG para los 674 496 pares fago-bacteria evaluados (3513 fagos y 192 bacterias), con las probabilidades de los modelos de genes clave y de genoma completo. Incluye las interacciones que superaron el umbral de 0,85, su reducción a los cuatro taxones dominantes, las cinco interacciones con mayor puntaje por taxón y las gráficas de densidad y reducción.

**Anexo 14. Redes de interacción bacteria-fago del Objetivo 2**

Contiene los grafos de Gephi de las interacciones predichas para el conjunto de referencia: la red completa con umbral de 0,85 y la red reducida a los cuatro taxones bacterianos dominantes, en formato editable y como imagen.

**Anexo 15. Comparación de los modelos de basecalling de Dorado**

Resume el desempeño de los modelos FAST, HAC y SUP de Dorado en la corrida de las muestras de gulupa: lecturas totales, aprobadas (*pass*) y rechazadas (*fail*), bases, longitud media, N50 y QScore medio. Incluye el detalle por muestra y gráficas de lecturas aprobadas y de calidad, que sustentan la elección de los modelos HAC y SUP. En este repositorio solo se publican las dos figuras; las tablas no están abiertas al público.

**Anexo 16. Reportes de calidad pycoQC de los modelos HAC y SUP**

Contiene los reportes interactivos de pycoQC generados a partir del resumen de secuenciación de Dorado para los modelos HAC y SUP. Muestran el resumen general de la corrida, la distribución de longitud y calidad de las lecturas, su evolución durante el tiempo de secuenciación y el número de lecturas por código de barras. Este anexo no está abierto al público.

**Anexo 17. Limpieza de las lecturas de gulupa con los modelos HAC y SUP**

Detalla, para cada una de las 73 muestras de gulupa y para ambos modelos, el número de lecturas antes de la limpieza, después de Pychopper y después de Filtlong, junto con las bases, la longitud, el N50 y el QScore antes y después del proceso. Incluye los reportes de NanoPlot de las lecturas limpias y gráficas comparativas entre HAC y SUP. En este repositorio solo se publican las gráficas comparativas; las tablas por muestra y los reportes de NanoPlot no están abiertos al público.

**Anexo 18. Clasificación taxonómica con EMU de las muestras de gulupa**

Contiene los resultados de EMU para las muestras de gulupa con al menos 500 lecturas limpias (28 con HAC y 26 con SUP): abundancias relativas, conteos y taxonomía de cada taxón, y los 20 taxones más abundantes por especie, género y familia. Incluye las curvas de rarefacción y un resumen general por modelo. En este repositorio solo se publican las curvas de rarefacción; las tablas de EMU no están abiertas al público.

**Anexo 19. Diversidad microbiana del rizobioma de gulupa**

Presenta el análisis de diversidad de las muestras de gulupa con los modelos HAC y SUP, agrupadas por sistema de manejo (Empresarial, Campesina y Agroecológica): índices de Shannon y riqueza observada por muestra y por sistema, valores p de la prueba de Wilcoxon (Mann-Whitney U), matrices de Bray-Curtis y Jaccard, PCoA y PERMANOVA. En este repositorio solo se publican las figuras; las tablas no están abiertas al público.

**Anexo 20. Genomas bacterianos descargados para gulupa**

Lista los 79 genomas bacterianos descargados de NCBI para los taxones de gulupa (modelo HAC) con abundancia relativa promedio de al menos 0,1 %, junto con el resultado de cada búsqueda. Incluye el registro completo de la descarga. Este anexo no está abierto al público.

**Anexo 21. Predicciones de DeepPBI-KG para gulupa**

Contiene la matriz completa de predicciones para los 277 527 pares evaluados entre los 3513 fagos de referencia y las 79 bacterias de gulupa, con las probabilidades de genes clave y de genoma completo. Incluye las interacciones que superaron el umbral de 0,85, su reducción a los cuatro taxones dominantes, hasta cinco interacciones con mayor puntaje por taxón y las gráficas de densidad y reducción. En este repositorio solo se publican las gráficas de densidad y reducción; las matrices y tablas no están abiertas al público.

**Anexo 22. Redes de interacción bacteria-fago de gulupa**

Contiene los grafos de Gephi de las interacciones predichas para gulupa con el modelo HAC: la red completa y la red de los cuatro taxones dominantes, en formato editable, PDF e imagen. Incluye las estadísticas de las redes construidas con HAC (nodos, aristas, densidad y grado promedio). En este repositorio solo se publican las imágenes de las redes; los grafos editables y las estadísticas no están abiertos al público.

## Notas

- En la tabla del Anexo 1, el guion (-) indica que la etapa no se reportó en el estudio o no aplica.
- La tabla *Top5_interacciones_por_taxon* (Anexo 13) está ordenada por puntaje y tiene columnas vacías de "Nivel de evidencia" y "Referencia" para completar con la verificación bibliográfica.
- Los archivos .zip contienen matrices CSV de gran tamaño; se descomprimen con cualquier gestor de archivos.
- Los archivos .gephi se abren con Gephi 0.10 o superior; los .html se abren con cualquier navegador.
- En los Anexos 7 a 9, del artículo se usan solo sus 88 muestras; sus controles (barcode01, 24, 36, 48, 60 y 72) se excluyen, como en el propio artículo.
- Los datos del artículo usados en el Anexo 11 (salidas de EMU por barcode, tabla de conteos final, datos de muestra y resultados de PERMANOVA) provienen de su repositorio público, [serlandson/sterile_sentinels](https://github.com/serlandson/sterile_sentinels). La figura y las tablas se generan con un script del pipeline propio, cuyo código no está abierto al público.
