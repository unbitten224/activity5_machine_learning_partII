# Lab 3.5: Machine Learning Pipeline with Amazon SageMaker  
  
  
Información general[¶](https://mynotebook-umft.notebook.us-east-1.sagemaker.aws/lab/tree/es_es/3_5-machinelearning_es.ipynb#Informaci%C3%B3n-general)  
Este laboratorio es una continuación de los laboratorios guiados del Módulo 3.  
En este laboratorio, implementará un modelo entrenado y realizará una predicción en relación con el modelo. A continuación, eliminará el punto de enlace y realizará una transformación por lotes en el conjunto de datos de prueba.  
  
  
**Previo a comenzar el laboratorio**  
  
![Lab 3.5: Machine](pantallazos/22CEBCFB-6386-4C22-A5A9-1F2B134582AF.png)  
  
  
  
Inicia el servicio de Amazon SageMaker AI  
  
![Pasted Graphic 57.png](pantallazos/3805DDFA-3454-47D4-B192-5A851F4387F7.png)  
  
Estado inicial del laboratorio  
  
  
![Pasted Graphic 59.png](pantallazos/148DC0C9-9384-4DFB-A26F-F725C0B4BCF4.png)  
  
  
  
Entramos al laboratorio  
  
![Laboratorio 315: Bloc de notas del estudiante](pantallazos/295A7FB7-5B92-46BE-B571-D968C0D1BD48.png)  
  
Preparamos el repositorio  
  
* Inicializamos el repositorio local  
* Sincronizamos credenciales usuario, email  
* Creamos la rama dev_jurbano18  
  
* ![Pasted Graphic 61.png](pantallazos/9BB9559C-A3C7-49CA-A565-AE07ABD5E17E.png)  
  
Subimos el primer comit con los archivos ya presentes  
![Pasted Graphic 62.png](pantallazos/1E02B2C1-D562-416C-B653-173AFE1D56B8.png)  
  
  
  
Configuración del laboratorio  
  
  
Descargamos las dependencias necesarias  
# instalar de pendencia scipy, scikit-learn  
  
  
![Pasted Graphic 63.png](pantallazos/977C0AEC-2BAA-42E9-A6D5-2D07DE5450B2.png)  
  
  
  
Ahora importamos librerías y preparamos el flujo de entrenamiento del model  
  
Para qué se realiza esto?  
El objetivo de este flujo de trabajo es **entrenar un modelo de Machine Learning (utilizando el algoritmo XGBoost en Amazon SageMaker) capaz de clasificar de manera automática si un paciente tiene una columna vertebral normal o anormal**  
  
![Pasted Graphic 65.png](pantallazos/B0C88153-8CB5-430D-BF57-87E20C342267.png)  
  
  
  
El resultado indica  
* Muestra los pasos que siguió AWS (crear el trabajo, preparar la computadora virtual, descargar tus datos desde S3, entrenar el modelo y guardar el resultado)  
* En este punto significa que el modelo de inteligencia artificial ya aprendió de los datos y está listo para ser alojado y empezar a hacer predicciones  
  
![Pasted Graphic 66.png](pantallazos/F6B988D7-822B-4C9D-973C-155CEA799310.png)  
  
Guardamos cambios  
  
Sobre los archivos descargados que va a necesitar el modelo, creamos un comit más  
  
![Pasted Graphic 67.png](pantallazos/D24F679B-462F-42F4-B9C2-317D073602DC.png)  
  
  
  
Alojar el modelo  
  
En este punto levanta una computadora virtual con una copia del modelo entrenado lista para responder consultas  
**Entonces **configura un traductor (CSVSerializer) para que los datos que le envíes en el futuro viajen correctamente en formato de texto CSV  
  
  
![Paso 2: Realizar predicciono:](pantallazos/889DD596-0AD7-449B-B494-8233FDD50BC8.png)  
  
  
¿Para qué ?  
para preparar las futuras predicciones:  
* Confirma que el grupo de prueba tiene **31 filas (pacientes)** y **7 columnas** (la clase más 6 mediciones médicas)  
*  Explica que para que el modelo pueda adivinar, **no se le debe dar la respuesta** es decir, la columna class por lo que enseña a aislar únicamente las medidas físicas usando comandos como  
![Paso 2: Realizar predicciones](pantallazos/1825729F-C427-4A43-8FF7-04268DA12E3D.png)  
