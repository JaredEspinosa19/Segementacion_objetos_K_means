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
Para poder realizar el siguiente paso realizaremos otro **K-means**, pero ahora basados en **coordenadas**.

<img src="img/segmentacion_figuras.png">

---
## 4 - Medición distancias
Ya con los objetos segementandos en diferentes imágenes se procede a obtender los extremos de cada unos de los tomates que deseamos medir.
- Tomate 2 
<img src="img/distancia_tomate1.png">

- Tomate 4
<img src= "img/distancia_tomate2.png">

## 5 - Resultados Finales
Una vez encontrados los extremos de los objetos, se gráfican el diametro de estos sobre la imagen final.
<img src="img/distancias_tomates.png">