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
- Total de Empleados:
  Cuenta el total de empleados dentro de la tabla.
```excel
=CONTARA(employees!A2:A)
```
- Total pagos mensuales:
  suma el total de los pagos realizados a los empleados en el mes.
```excel
=SUMA(employees!K2:K)
```
- Salario promedio:
  suma el total de los pagos mensuales y los divide entre el total de empleados.
```excel
=PROMEDIO(employees!K2:K)
```
  

