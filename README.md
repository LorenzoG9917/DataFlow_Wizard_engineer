# DataFlow Wizard

## Objetivo
Este repositorio tiene como propósito presentar un proyecto de ingeniería de datos ETL (Extract, Transform, Load) centrado en el procesamiento de datos en el contexto de operaciones comerciales. El proyecto hace uso de diversas tecnologías, como Python, pandas y PostgreSQL, para llevar a cabo una serie de tareas que incluyen la normalización y organización de datos, la construcción de un modelo entidad-relación, la definición de una estructura de base de datos y la carga de información en ella.
## Arquitectura
![Arquitectura DataFlow ETL](https://github.com/LorenzoG9917/DataFlow_Wizard_engineer/assets/121797266/4ae239d6-0607-4e85-a122-4d2368b7cbb9)
## Descripción
Este proyecto simula un proceso integral de Ingeniería de Datos ETL que podría ser relevante en el mundo laboral. Incluye las siguientes etapas:

1. **Obtención del Conjunto de Datos**: Se comienza con un archivo plano llamado `sales_data_sample.csv` que contiene datos sin estructurar.
2. **Modelo Entidad-Relación**: Para organizar estos datos de manera eficiente, primero se diseña un modelo entidad-relación utilizando herramientas visuales como Lucidchart. Este modelo define la estructura de la base de datos, incluyendo las tablas, las relaciones y las restricciones.
3. **Normalización de Datos con Pandas**: Se utiliza la biblioteca de Python, Pandas, para normalizar los datos. Se crean DataFrames separados para cada tabla definida en el modelo entidad-relación. Estos DataFrames se exportan a archivos Excel ubicados en la carpeta `output_data`.
4. **Creación de la Base de Datos**: Se establece una conexión a una base de datos PostgreSQL utilizando las credenciales por defecto. Se crea una nueva base de datos llamada `sales_db` utilizando SQL. Luego, se definen las tablas y sus restricciones mediante consultas SQL.
5. **Carga de Datos en la Base de Datos**: Los datos normalizados, almacenados en archivos CSV en la carpeta `output_data`, se cargan en las tablas correspondientes de la base de datos PostgreSQL mediante consultas SQL de carga.

## Conjunto de Datos Utilizado
Este conjunto de datos se relaciona con operaciones comerciales, específicamente ventas en el sector minorista o mayorista. Los datos están organizados en torno a pedidos de productos y clientes, lo que sugiere que se utilizan en un contexto empresarial para gestionar y rastrear las transacciones comerciales. 

## Contenido
El proyecto incluye los siguientes archivos y carpetas:

- **create_rbdfiles.ipynb**: Un script Python que extrae datos de ventas desde un archivo CSV, realiza transformaciones y crea archivos CSV con los datos transformados en la carpeta `output_data`.

- **etl_project.ipynb**: Un script Python que crea una base de datos PostgreSQL, define tablas y carga datos desde los archivos CSV en la base de datos.

- **output_data**: Una carpeta que contiene los archivos CSV generados después de la transformación de datos que se realiza en el programa **create_rdbdfiles.ipynb**.

## Requisitos
Para ejecutar este proyecto, necesitarás:

- Python 3.x
- PostgreSQL instalado y configurado con las credenciales adecuadas.
- Las bibliotecas de Python mencionadas en los scripts (por ejemplo, psycopg2, pandas).

## Ejecución
Se utiliza Jupyter Notebook como una herramienta clave para visualizar y trabajar con los dataframes de manera eficiente durante todo el proceso.
Sigue estos pasos para ejecutar el proyecto:
1. Crear nueva carpeta llamada project_etl_sales y configurar un ambiente virtual.

```shell
mkdir project_etl_sales
cd project_etl_sales
python -m venv env
```
2. Activar el ambiente virtual (Windows activación):
```shell
env/Scripts/activate
```
3. Instalar las librerias requeridas para el proyecto:
```shell
pip install notebook # install notebook
ipython kernel install --user --name=venv 
pip install pandas
pip install psycopg2
```
4. Ejecutar jupyter notebook:
```shell
jupyter notebook #execute to deploy jupyter notebook in localhost
```
5. Crear directorio `output_data`:
```shell
mkdir output_data
```

5. Ejecuta notebook `create_rdbdfiles.ipynb` para generar los archivos CSV con datos transformados en la carpeta `output_data`.

2. Asegúrate de que PostgreSQL esté en ejecución y tenga la configuración adecuada.

3. Ejecuta notebook `etl_project.ipynb` para crear la base de datos, definir las tablas y cargar los datos en la base de datos PostgreSQL.



## Autor
Este proyecto ha sido desarrollado por [Lorenzo Guerrero](https://www.linkedin.com/feed/) con fines educativos.

---

**Nota:** Este proyecto es un ejemplo educativo y puede requerir adaptaciones para su uso en un entorno de producción. Los datos utilizados aquí son ficticios y se proporcionan solo con fines de demostración.
