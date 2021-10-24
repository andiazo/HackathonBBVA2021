# HackathonBBVA2021
Buscador de datos financieros

Analizar la competencia es fundamental para mantenerse relevante en el mercado, para este reto, nuestra propuesta es un sistema soportado con tecnologías de AWS, en el cual el usuario puede:
Subir archivos pdf de información financiera de bancos, y obtener datos estructurados de manera ágil y eficiente para, posteriormente, convertirlos en información valiosa.
Visualizar estadísticas y comparativos entre distintos bancos, por fecha de reporte para obtener información relevante de la situación financiera de cada banco.
Realizar comparativos de estados de resultados y balances generales, ya sea del mismo banco en diferentes trimestres como en distintos bancos.

## Herramientas

- Python
- Pandas
- PyPDF2
- Amazon S3
- Amazon Textract
- Amazon Lambda
- Amazon QuickSight


## Arquitectura

Para la arquitectura de esta solución, nos basamos en la siguiente guía: https://docs.aws.amazon.com/prescriptive-guidance/latest/automated-pdf-analysis-solution/welcome.html

Consiste en 4 fases:

1. Ingestión de archivos PDF:  Guardamos los archivos en un bucket de S3

2. Procesamiento de los archivos: Con funciones Lambda tomamos esos archivos, extraemos los datos con Amazon Textract, y procesamos esos datos.

3. Almacenamiento de datos: Los datos porcesados los guardamos en S3 y DynamoDB

4. Analítica y visualización: Con QuickSight, realizamos visualizaciones y analíticas de esos datos.

![image](https://user-images.githubusercontent.com/36974713/138585312-a517d314-36bb-48ec-8ae4-bc0ce23e41d8.png)
