# predicciones-de-ventas
predicciones-de-ventas

Objetivo: predicción de ventas a partir de datos con las siguientes características.

8523 filas y 12 columnas:

![image](https://user-images.githubusercontent.com/60327565/200555906-a10589fc-c5f5-4020-b941-3f7ecd87c2e1.png)

No habían datos duplicados y habían un total de datos faltantes de 3873 en las columnas Item_weight y Outlet_Size. En la parte previa a la utilización de modelos estos se reemplazaron con el promedio y una nueva cateogría respectivamente; para la utilización de modelos se hizo uso de Simple Imputer con las estrategias 'mean' y 'most_frequent'.

La estadística descriptiva de los datos numéricos fueron: 

![image](https://user-images.githubusercontent.com/60327565/200556791-00ae680f-1243-4ea6-85ba-d717448b7d93.png)

A continuación se muestran algunas gráficas:

**Histograma 'Item_Visibility'**

![image](https://user-images.githubusercontent.com/60327565/200557033-097d47d2-f7fc-41d4-81ae-e163b601d6f6.png)

**Histograma 'Item_Outlet_Sales'**

![image](https://user-images.githubusercontent.com/60327565/200557136-f7483fd5-8d5e-4186-a60d-bb07d67b16e8.png)

De las gráficas anteriores se puede concluir que en general la mayoría de los productos tienen una visibilidad <0.05 y unas ventas <2000.

**BoxPlot 'Item_Weight'**

![image](https://user-images.githubusercontent.com/60327565/200557493-ed6983d2-d390-480a-afc5-bea58890c087.png)

**BoxPlot 'Item_MRP'**

![image](https://user-images.githubusercontent.com/60327565/200557573-897a2bd4-078b-494b-8bd2-d70522b3f2c1.png)

A primera vista, ambos diagramas lucen simétricos, no parecen haber sesgos significativos.

**Mapa de calor de correlación**

![image](https://user-images.githubusercontent.com/60327565/200557779-6f6a7679-fe9a-4d14-8f75-54be6c3a29f8.png)

Solo hay correlación significativa entre 'Item_MRP' (precio de catalogo) y nuestra columna objetivo.

**Gráficos con respecto al tamaño de las tiendas y su aporte en ventas**

![image](https://user-images.githubusercontent.com/60327565/200558054-48dfc4d1-767a-408b-be3e-dcb17dfc130a.png)


![image](https://user-images.githubusercontent.com/60327565/200558088-f36a2035-7898-4ea2-abed-28d5d0543bb1.png)

La mayoría de las tiendas tienen un tamaño medio y este tamaño es el que más ventas tiene.

**Modelos de machine learning utilizados: Regresión lineal y árbol de decisión (regresión)**

División de los datos en conjuntos de training (75%) y test (25%). 

Transformación de los datos con simple imputer (para las dos columans con datos faltantes), Standar Scaler para datos numéricos y OneHotEncoder para características categorícas.

![image](https://user-images.githubusercontent.com/60327565/200558892-dbdd551b-07e9-4ec7-888e-91c9e2c58680.png)


**Resultados regresión lineal**

R^2 conjunto de prueba: 56.70%
RECM conjunto de prueba: 1092.88

**Resultados árbol de decisión**

Max depth óptimo: 6
R^2 conjunto de prueba: 58.22%
RECM conjunto de prueba: 1073.54

Mejor modelos: árbol de decisión.

**Recomendaciones:**
- Investigación para la recolección de datos faltantes.
- Implementación de más modelos.
- Realización de más gráficos.






