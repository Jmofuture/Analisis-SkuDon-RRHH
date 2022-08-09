# Análisis de RRHH Sku-Don <img src="https://user-images.githubusercontent.com/78714438/183740603-f42cbe82-32c6-4aab-89e2-91e1d92b90f3.png" alt="drawing" width="40"/> 


Se busca visualizar indicadores de Colaboradores, Sueldos y Desempeño con el uso de un Reporte de Recursos Humanos de la compañía (ficticia) SKU-DON. Este reporte requiere ser compartido a usuarios por medio de un enlace web.
Se requiere analizar:

<li>Análisis por empleado (Tabla).</li>
<li>Total de empleados (Conteo).</li>
<li>Promedio de Edad, Sueldo y Desempeño.</li>
<li>Costos totales por Sueldos, Relación-Sueldo edad.</li>
<li>Evaluación de desempeño Max-Min por jefe.</li>

Se dispone de un dataset **Datos+Empleados**, dispone de 3 tablas **Empleados**, **Evaluación** y **Sueldo** 

Con pocas transformaciones en Power Query se cargan las tablas 

### Tabla 1 - Empleados

![Tabla 1](https://user-images.githubusercontent.com/78714438/183729128-74e02653-9db6-4fae-874a-34f4ab4572d8.png)


#### Transformaciones


![Tabla 1 2](https://user-images.githubusercontent.com/78714438/183729657-045bb2ee-84c4-4526-9282-4fef4ec23c9a.png)


### Tabla 2 - Sueldos


![Tabla 2](https://user-images.githubusercontent.com/78714438/183729865-516ea47e-7270-49f8-a2bd-6924d5dde27c.png)


#### Transformaciones


![Tabla 2 2](https://user-images.githubusercontent.com/78714438/183729969-964e9284-b0e1-45b1-80d1-c199128a4ab7.png)


### Tabla 3 - Evaluaciones


![Tabla 3](https://user-images.githubusercontent.com/78714438/183730136-e11308fe-5491-4ac1-8e0f-d9a4bae12525.png)


#### Transformaciones


![Tabla 3 2](https://user-images.githubusercontent.com/78714438/183730270-9c2d63ca-f755-4693-9f9b-0a6997458bff.png)


## Cálculos con DAX 

Se generan 3 columnas calculadas con **DAX**, una por cada tabla:

**Rango Etario**

![Columna Calculada Grupo Etario](https://user-images.githubusercontent.com/78714438/183733725-376d8bd9-5167-4a96-ba64-f22b62a82ebc.svg)

**Rango Salarial**

![Columna Calculada Grupo Sueldo](https://user-images.githubusercontent.com/78714438/183733796-045f2a19-579f-4ed7-98fe-f9f09fe447ec.svg)

**Rango de Evaluaciones**

![Columna Calculada Grupo Evaluación](https://user-images.githubusercontent.com/78714438/183733832-918ffe9d-bd26-4dc6-8196-4f514db2020c.svg)


También se crea una tabla llamada **_Medidas**, donde se crean 4 medidas:

![Medidas DAX](https://user-images.githubusercontent.com/78714438/183734434-88561164-1c33-4742-aa5e-d8fac504ad0d.svg)


## Reportes

### Con estas 3 tablas se realizan 3 reportes

## Reporte 1 - Análisis Empleados

Está compuesto por 4 Tarjetas y 7 Visualizaciones :

##### Tarjetas

<li>Total Empleados.</li>
<li>Edad Promedio.</li>
<li>Sueldo Promedio.</li>
<li>Evaluación Promedio.</li>

##### Visualizaciones

<li><strong>Gráfico de anillos</strong>, detallando la proporción de empleados por Género.</li>
<li><strong>Mapa</strong>, detallando la cantidad de empleados por Estado.</li>
<li><strong>Gráfico de barras</strong>, Rango Etario.</li>
<li><strong>Gráfico de barras</strong>, Rango Salarial.</li>
<li><strong>Gráfico de barras</strong>, Rango de Evaluación.</li>
<li><strong>Gráfico de columnas</strong>, con detalle de la cantidad de empleados por Departamento.</li>
<li><strong>Tabla</strong>, con el detalle de todos los empleados.</li>


![Reporte 1](https://user-images.githubusercontent.com/78714438/183735654-85d9cde3-4aeb-4261-96f6-2899507d788c.png)


## Reporte 2 - Análisis Sueldos

Está compuesto por 3 Tarjetas y 5 Visualizaciones :

##### Tarjetas

<li>Total Empleados.</li>
<li>Sueldo Total.</li>
<li>Sueldo Promedio.</li>


##### Visualizaciones

<li><strong>Gráfico de anillos</strong>, detallando la proporción de empleados por Sueldo y Género.</li>
<li><strong>Mapa</strong>, detallando el Sueldo Total por Estado.</li>
<li><strong>Gráfico de dispersión</strong>, evaluando la relación entre la edad de los emplados y el Sueldo.</li>
<li><strong>Gráfico de columnas</strong>, con detalle del Sueldo Promedio por Departamento.</li>
<li><strong>Tabla</strong>, con el detalle de todos los empleados.</li>


![Reporte 2](https://user-images.githubusercontent.com/78714438/183737828-d75a5889-d0c5-4725-8ba0-9d975268c69d.png)


## Reporte 2 - Análisis Desempeño

Está compuesto por 4 Tarjetas y 5 Visualizaciones :

##### Tarjetas

<li>Total Empleados.</li>
<li>Evaluación Máxima.</li>
<li>Evaluación Mínima.</li>
<li>Evaluación Promedio.</li>

##### Visualizaciones

<li><strong>Mapa</strong>, detallando Evaluaciones por Estado.</li>
<li><strong>Gráfico de barras</strong>, evaluando el desempeño de promedio de los empleados por Jefe directo.</li>
<li><strong>Gráfico de columnas</strong>, con detalle de promedio de Evaluación por Género.</li>
<li><strong>Gráfico de columnas</strong>, con detalle de promedio de Evaluación por Departamento.</li>
<li><strong>Tabla</strong>, con el detalle de todos los empleados.</li>

![Reporte 3](https://user-images.githubusercontent.com/78714438/183738757-ee34bc38-8733-4c25-8367-0a0d5a90872d.png)


