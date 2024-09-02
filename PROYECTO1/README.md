Laboratorio: Preparación Modelo de datos Predictivos

Objetivo

Utilizando un entorno virtual, crear un modelo predictivo de un DataFrame Seleccionado.

Requisitos Previos

    Conocimientos básicos de Python.
    Familiaridad con la línea de comandos.
    Visual Studio Code instalado.

Instrucciones
Paso 1: Preparación del Entorno

    Verificar la Instalación de Python: Ejecuta python --version o python3 --version en la terminal.
    Instalar Visual Studio Code: Asegúrate de que VS Code esté instalado y con la extensión de Python.
    Crear Carpeta de Proyecto: Crea y abre una carpeta para el proyecto en VS Code.

    En este paso lo que hicimos fue crear una carpeta en el que dentro ibamos a realizar nuestro entorno virtual y nuestro informe en un ipynb mostrando con pantallazos el proceso que se iba realizando

Paso 2: Creación del Entorno Virtual

    Crear el Entorno Virtual: Ejecuta python3 -m venv proyectoIA en la terminal dentro de la carpeta del proyecto.
    Activar el Entorno Virtual: Ejecuta source parcial1/bin/activate.

    Cuando ya teníamos el entorno virtual activado, podiamos proseguir trabajando e instalando todas las dependencias dentro de ese entorno virtual.

Paso 3: Instalación y Verificación de Dependencias

    Instalar Librerías: Con el entorno activado, instala las librerías necesarias con pip install numpy pandas scikit-learn matplotlib y todas las necesarias en el notebook para el desarrollo del modelo.
    Verificar la Instalación: Usa pip list para listar las dependencias instaladas.


Paso 4: Buenas Prácticas y Mantenimiento

    Crear requirements.txt: Genera un archivo requirements.txt con pip freeze > requirements.txt.
    Desactivar el Entorno Virtual: Usa deactivate cuando termines.

    Cuando escribiamos el comando, en la carpeta que estamos trabajando se nos crea un txt donde están todas las versiones y paquetes instalados del entorno virtual. Esto nos va a servir posteriormente para poder utilizar ese entorno virtual en otro sistema.


Paso 5: Seleccionamiento de Variable Predictiva y Analisis de variables predictoras

    Como variable a predecir se eligió Risk.

    Mediante gráficas plotly y tablas de contingencía mirar la relación de todas las variables que se deseen analizar.

    Una vez analizados los valores obtenidos, se seleccionaron 3 variables.
    Housing-Checking_account-Saving_accounts


Paso 6: Realizar el modelo predictivo con las 3 variables seleccionadas

    Dividir el DataFrame con train_test_split

    Separar las variables categoricas y numéricas para así poder realizar el OneHotEncoder y OrdinalEncoder

    Definir nuestro x_train, y_train, x_test, y_test

    Dropear todas las columnas que no vamos a utilizar.

    Creamos el Pipeline con Procesor, el Scaler, la estrategia del imputado y el DecisionTreeClassifier que es el metodo que vamos a utilizar en nuestro modelo.

    Entrenamos el modelo para poder realizar la prediccion y así guardarla en una variable para poder sacar la precisión del modelo

    Utilizando Cross_validate, obtenemos la media y el mse de cada "score" obtenido. Tanto train como test.

    Graficamos los resultados de esta media para ver la profundidad de arbol mas optima para nuestro modelo.


Paso 7: Probar el modelo con nuevos datos

    Creamos nuevos datos para un nuevo cliente y le aplicamos el modelo para realizar la prediccion si el cliente tiene buen "Risk" crediticio.

    Guardamos los datos en un nuevo DatraFrame