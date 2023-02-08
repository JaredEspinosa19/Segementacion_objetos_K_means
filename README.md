# Segmentación de objetos mediante K-means

El proyecto consiste en la segmentación de objetos para medir el diametro de estos utilizando técnicas de segmentación de imágenes.
La segmentación de los objetos se empleo usando **k-means** sin emplear **ninguna** librería.

<img src="img/distancias_tomates.png">

---
## 1 - Segmentación de Colores
Como primer paso se deben segmentar la imágen por colores, los grupos en los que se segemento la imágen fueron 4, pero dependerá muchas veces de la calidad de la imágen.


<img src="img/colores_tomates_segmentados.png">

---
## 2 - Segmentación de componentes
Aplicando K-means se obtienen los centroides de los componentes de colores y se proceden a realizar un umbralizado con estos valores para poder segmentar la imágen.

<img src="img/segmentacion_componenetes.png">

---
## 3 - Segmentación de objetos
Una vez que se tiene los diferentes componentes, seleecionamos aquella imágen que contienen los objetos que deseamos buscar (tomates) y segmentar.
Para poder realizar el siguiente paso realizaremos otro **K-means**, pero ahora basados en **distancias**.

<img src="img/segmentacion_figuras.png">
