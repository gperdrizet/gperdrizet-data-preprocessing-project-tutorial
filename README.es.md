<!-- hide -->
# Análisis exploratorio de datos en Python - Guía paso a paso
<!-- endhide -->

- Descarga los datos de Airbnb de Nueva York de Kaggle.com.
- Realiza un EDA completo, incluyendo todos los pasos del proceso.
- Escribe las conclusiones de cada paso y analiza los resultados sobre las relaciones entre las variables.

<how-to-start>
  
## 🌱 Cómo iniciar este proyecto

Sigue las siguientes instrucciones:

1. Crea un nuevo repositorio basado en el [proyecto de Machine Learning](https://github.com/4GeeksAcademy/machine-learning-python-template/) o [haciendo clic aquí](https://github.com/4GeeksAcademy/machine-learning-python-template/generate).
2. Abre el repositorio creado recientemente en Codespace usando la [extensión del botón de Codespace](https://docs.github.com/es/codespaces/developing-in-codespaces/creating-a-codespace-for-a-repository#creating-a-codespace-for-a-repository).
3. Una vez que el VSCode del Codespace haya terminado de abrirse, comienza tu proyecto siguiendo las instrucciones a continuación.

</how-to-start>

## 🚛 Cómo entregar este proyecto

Una vez que hayas terminado de resolver el caso práctico, asegúrate de confirmar tus cambios, haz push a tu repositorio y ve a 4Geeks.com para subir el enlace del repositorio.

## 📝 Instrucciones

### Airbnb en Nueva York

Una empresa ha recolectado la información del alquiler de viviendas en Nueva York a través de la aplicación Airbnb durante el año 2019. Este conjunto de datos se utilizó para entrenar modelos de Machine Learning durante ese año, en una competición en abierto.

Ahora lo utilizaremos para llevar a cabo un estudio acerca de las variables que componen el dataset a fin de comprenderlo y obtener conclusiones sobre él.

#### Paso 1: Carga del conjunto de datos

Puedes descargar el conjunto de datos directamente desde Kaggle.com o en el siguiente enlace: `https://raw.githubusercontent.com/4GeeksAcademy/data-preprocessing-project-tutorial/main/AB_NYC_2019.csv`. Almacena los datos en crudo en la carpeta `./data/raw`.

#### Paso 2: Realiza un EDA completo

Este paso es vital para asegurar que nos quedamos con las variables estrictamente necesarias y eliminamos las que no son relevantes o no aportan información. Utiliza el Notebook de ejemplo que trabajamos y adáptalo a este caso de uso.

Asegúrate de dividir convenientemente el conjunto de datos en `train` y `test` como hemos visto en la lección.

#### Paso 3: Guarda el conjunto de datos procesado

Después del EDA puedes guardar los datos en la carpeta `./data/processed`. Asegúrate de agregar la carpeta de los datos en el `.gitignore`. Los datos al igual que los modelos no se deben subir a git.

> Nota: También incorporamos muestras de solución en `./solution.ipynb` que te sugerimos honestamente que solo uses si estás atascado por más de 30 minutos o si ya has terminado y quieres compararlo con tu enfoque.
