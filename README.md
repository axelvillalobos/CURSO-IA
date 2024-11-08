Los paquetes que vamos a utilizar para esta demostración son los siguientes:

Datasets: Este paquete, nos ofrece varios de los datasets más famosos para el estudio de algoritmos de Machine Learning. Esta demostración en particular esta basada en el Digits Dataset. Esta distribución de datos se compone de 1797 imágenes de 8x8. Cada imagen, es de un dígito escrito a mano. Esta imagen es presentada como vector de 64 características.
Preprocessing: Este paquete, proporciona algunas herramientas de estandarización (como mean removal and variance scaling), para preprocesar las distribuciones de datos a ser analizadas por los algoritmos de machine learning.
Cluster: Este paquete, proporciona diferentes algoritmos utilizados para realizar una de las tareas clásicas del aprendizaje no supervisado (Clustering), entre ellos el algoritmo de k-means.
Decomposition: Este paquete, proporciona diferentes técnicas utilizadas para reducir la dimensionalidad de una distribución de datos, etre ellos el algoritmo de Principal Component Analysis.

Iris Flower Dataset

Utilizando el Iris Dataset, utilice las herramientas anteriormente mostradas en este tutorial para separar la distribución de datos, en los 3 diferentes tipos de esta flor (Setosa, Versicolour, y Virginica). Esta distribución de datos está compuesta por una matriz de 150x4, es decir, contiene 150 muestras con 4 características cada una.

Explicación del código:
1.	Reducción de dimensionalidad con PCA:
o	PCA(n_components=3): Reduce el conjunto de datos a 3 dimensiones (o componentes principales) que capturan la mayor parte de la variabilidad del conjunto de datos original.
o	X_reduced = pca.fit_transform(X): Se aplica PCA para obtener los datos reducidos en X_reduced.
2.	Aplicación de K-means:
o	KMeans(n_clusters=3, random_state=42): Crea un modelo de K-means con 3 clusters (porque el dataset Iris tiene 3 especies).
o	kmeans.fit(X_reduced): Ajusta el modelo de K-means a los datos de 3 dimensiones.
o	labels = kmeans.labels_: Etiquetas de los clusters asignados por el modelo para cada punto de datos.
3.	Visualización:
o	El gráfico muestra los puntos en el espacio 3D reducido, coloreados según el cluster asignado.
