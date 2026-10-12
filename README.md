# Analisis Dataset de Empleados

## 1. Dexcripcion.
Tomamos un Dataset de Kaggle sobre los empleados de una empresa Tecnologica, descargamos los archivos .CSV y los importanmos desde Google Sheets, teniendo como objetivo principal poder realizar un analisis completo usando esta herramienta.

## 2. Objetivo.
Realizar un analisis completo de un Dataset de empleados de una empresa tecnologica usando la herramienta google sheets, implementando la limpieza y transformacion de datos, los principales KPIs, y los dashboard con la informacion relevande del analisis.

## 3. Herramientas Utilizadas.
Google Sheets
- Importacion de datos.
- Limpieza y transformacion de datos.
- KPIs principales.
- Dashboards.

## 4. Fuente de Datos
Kaggle
- https://www.kaggle.com/datasets/sobrino30/empleados-renunciar-empresa-mediana


## 5. Metodologia.

### 5.1 Limpieza y Transformacion de datos.
los pasos realizados para la limpieza y transformacion de datos fueron los siguientes.
- Formato de Datos
  Una vez importados los datos se configuro el tipo de dato de cada comunna para garantizar calculos precisos en el analisis,
- Bisqueda de duplicados.
  se realizo la busqueda de datos duplicados, no encontramos datos duplicados.
- Datos vacios o nulos.
  recorrimos todas las colummnas y no se encontraron datos vacios o nulos.
<img width="1215" height="607" alt="image" src="https://github.com/user-attachments/assets/8585531e-1d91-4177-ab65-45e67e5a5b78" />


### 5.2 Integracion de Datos.
Este dataset consta de dos Archivos complementarios el cual es Employees y Departments, el proceso fue obtener los datos de la tabla Departments e integrarlo en Employees usando como dato compartido el nombre del Department.
<img width="933" height="645" alt="image" src="https://github.com/user-attachments/assets/501d490d-0f61-44e9-b307-f612c701b7f0" />

### 5.3 KPIs obtenidas
- Total de Empleados Registrados:
  Cuenta el total de empleados dentro de la tabla.
```excel
=CONTARA(employees!A2:A)
```
- Total de Empleados Activos:
  Cantidad de empleados que trabajan actualmente en la empresa.
```excel
=CONTAR.SI(employees!O2:O;"NO")
```

- Total pagos mensuales:
  suma el total de los pagos realizados a los empleados activos en el mes.
```excel
=SUMAR.SI(employees!O2:O;"NO";employees!K2:K)
```
- Salario promedio:
  suma el total de los pagos mensuales y los divide entre el total de empleados.
```excel
=PROMEDIO.SI(employees!O2:O;"NO";employees!K2:K)
```
- Porcentaje de empleados que realizan las horas extras.
```excel
=CONTAR.SI.CONJUNTO(employees!P2:P;"Yes";employees!O2:O;"No")/CONTAR.SI(employees!O2:O;"No")
```


### 5.3 Dashboard.
los componentes del dashboard son los siguientes.
- las KPIs importantes en la parte superior.
- Grafico de barras apiladas que muestra la distribucion de los empleados en cada departamento.
- Grafico de anillo el cual muestra el porcentaje de empleados registrados que ya no trabajan en la empresa.
- grafico de barras que muestra la distribucion de empleados que ya no trabajan en la empresa por rango de años trabajados.
- grafico de barras apiladas de la distribucion de empleados por departamento activos que realizan horas extras.
- Grafico circular que muestra el porcentaje de empleados activos que realizan horas extras.
<img width="1130" height="581" alt="image" src="https://github.com/user-attachments/assets/a056982d-9409-48aa-a271-a1c47f7bea78" />

## 6. Hallazgos.
### 6.1 Composicion de la plantilla de empleados.
de los 300 empleados registrados en el dataset 249 estan activos en la empresa lo cual indica que en la empresa trabajan el 83% de los empleados egistrados.

debido a este hallazgo el contexto para analizar es diferente y consideraremos los empleados activos para las KPIs importantes.

### 6.2 Distribucion de las horas extras por departamento.

De los 249 empleados activos, 66 realizan horas extra (26.5%).

El departamento de Sales presenta la mayor incidencia de horas extra, con 19 de sus 46 empleados activos (41.3%). Le sigue IT, con 13 de 45 empleados (28.9%).

Además, Sales concentra el 28.8% de todos los empleados activos que realizan horas extra, lo que lo convierte en el departamento con mayor participación e incidencia de horas extra.

Estos resultados permiten identificar una diferencia entre departamentos, aunque no son suficientes para determinar si existe sobrecarga laboral.

### 6.3 Rotación de empleados según su antigüedad.
Para investigar una posible asociación entre antigüedad y rotación, se analizaron los 300 registros, incluyendo empleados activos y quienes abandonaron la empresa.

Se identificó que:

De los 159 empleados con 0–7 años de antigüedad, 30 abandonaron la empresa (18.9%).

De los 141 empleados con 8–30 años de antigüedad, 21 abandonaron la empresa (14.9%).

La proporción de rotación es aproximadamente 4 puntos porcentuales mayor en el grupo de menor antigüedad.

Aunque existe esta diferencia, no es especialmente marcada, por lo que el análisis no permite afirmar que la antigüedad sea un factor determinante de la rotación.

## 7. Retos.
uno de los retos mas grandes era el realizar todo el proceso del analisis dentro de Goggle sheets aso poder afrontar los posibles desafios futuros que requieran el uso de esta herramienta.
ademas se presentaros diferentes retos dentro de este proceso.
- la forma en la que se investiga dentro de esta herramienta es a partor de formulas las cuales facilitan mucho el recorrido de datos extensos.
- el uso particular de los filtros.
- una forma muy distinta de SLQ, y Power query de relacionar las tablas para tener acceso a todos los datos.
- claramente el uso de las tablas dinamicas y la construccion de los dashboards.

## 8. Archivo del dashboard.
- archivo adjunto: [Analisis Empleados.zip](https://github.com/user-attachments/files/33346566/Analisis.Empleados.zip)
- Enlace Google Sheets: https://docs.google.com/spreadsheets/d/1KJBVjac44V9lgyPh7sLciLDZQ_WZHYtLl1qjixPM-yQ/edit?usp=sharing


