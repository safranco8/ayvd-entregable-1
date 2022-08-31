# Grupo 31 
## Integrantes: 
•	Victor Nicolas Rocco

•	Maria Mercedes Silva

•	Santiago Franco

•	Williams Gremoliche

 
## 1. Criterios de exclusión (o inclusión) de filas 
 

Se eliminan los outliers de las variables numéricas dejando solo los valores menores a Ls o mayores a Li del siguiente gráfico:

![image](https://user-images.githubusercontent.com/101225396/187695541-60622a98-4594-42eb-bd62-83a14aa9bea4.png)

## 2. Interpretación de las columnas presentes

a.    Rooms: cantidad de habitaciones.

b.    Distance: distancia al centro de la ciudad.

c.    Price: precio de compra/venta de la propiedad.

d.    Landsize: tamaño del terreno.

e.    BuildingArea: metros cuadrados construidos.

f.    YearBuilt: año de construcción.

g.    avg_price: se agrega el precio promedio diario de publicaciones de la plataforma AirBnB en el mismo código postal.

h.    avg_weekly_price: se agrega el precio semanal diario de publicaciones de la plataforma AirBnB en el mismo código postal.

i.    avg_monthly_price: se agrega el precio promedio mensual de publicaciones de la plataforma AirBnB en el mismo código postal.

j.    Type: tipo de propiedad. 3 valores posibles.  h=house,cottage,villa, semi,terrace; u= unit, duplex; t=townhouse 

k.    Suburb 314 valores posibles de suburbios

l.    Regionname 8 valores posibles de regiones (West, North West, North, North east …etc)



## 3. Las transformaciones realizadas son:

1. Se redujo el Dataframe y se trató las variables categóricas con OneHotEncoding.
2. Todas las características numéricas fueron escaladas usando MinMaxScaler previo a ser imputadas, solo los valores distintos a NaN. Al aplicar MinMaxScaler, reemplazaba los NaN por 0, así que solo se les aplicó a los valores no nulos, manteniendo los NaN para luego ser imputados.  
3. Las columnas ‘YearBuilt’ y ‘BuildingArea’ fueron imputadas utilizando el algoritmo IterativeImputer, con el estimador KNeighborsRegressor. Se optó por un K=2  ya que imputaba más próximo a los datos originales.
4. Se escalaron los datos con MinMaxScaler entre -1 y 1
5. Se aplicó el método PCA para reducir la dimensionalidad y se calculó la varianza de las primeras 20 componentes.
6. Se agregan las 5 primeras columnas obtenidas a través del método de PCA, ya que estas representan prácticamente el 80% de las componentes principales, para luego ser aplicado sobre el conjunto de datos totalmente procesado.
7. El dataset se lo pasa a CSV.
8. Se descarga el archivo *.csv con los datos procesados. 
