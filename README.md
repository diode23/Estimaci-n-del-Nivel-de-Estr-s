# Predicción del nivel de estrés

Aplicación web que estima el nivel de estrés a partir de distintos factores introducidos por el usuario. Utiliza un modelo de aprendizaje automático basado en un **árbol de decisión** y ofrece una interfaz adaptable para introducir datos y consultar los resultados.

## Índice

- [Descripción general](#descripción-general)
- [Características](#características)
- [Tecnologías utilizadas](#tecnologías-utilizadas)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Instalación y ejecución](#instalación-y-ejecución)
- [Uso de la aplicación](#uso-de-la-aplicación)
- [Conjunto de datos](#conjunto-de-datos)
- [Limitaciones y uso responsable](#limitaciones-y-uso-responsable)
- [Mejoras previstas](#mejoras-previstas)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)

## Descripción general

Este proyecto integra una aplicación web desarrollada con Flask y un modelo de clasificación implementado con scikit-learn.

El usuario introduce los valores solicitados en un formulario y la aplicación los procesa para mostrar una estimación del nivel de estrés. El sistema incorpora validación de datos y gestión de errores para los valores no válidos.

## Características

- **Formulario de entrada:** permite introducir distintos factores relacionados con el estrés.
- **Modelo predictivo:** utiliza un clasificador basado en un árbol de decisión.
- **Diseño adaptable:** incorpora una interfaz con estilos personalizados para distintos tamaños de pantalla.
- **Validación de datos:** comprueba que los valores introducidos cumplan las condiciones establecidas.
- **Gestión de errores:** muestra una página de error cuando los datos no son válidos.

## Tecnologías utilizadas

| Tecnología | Función |
| --- | --- |
| Python | Lenguaje de programación de la aplicación. |
| Flask | Desarrollo del servidor y gestión de las rutas web. |
| scikit-learn | Implementación del modelo de aprendizaje automático. |
| pandas | Carga y manipulación de datos. |
| NumPy | Operaciones numéricas. |
| HTML y CSS | Estructura y presentación de la interfaz. |
| JavaScript | Interactividad en el navegador. |

## Estructura del proyecto

```text
stress-level-predection/
├── app.py
├── StressLevelDataset.csv    # Archivo necesario; no incluido en el repositorio
├── templates/
│   ├── login.html
│   ├── result.html
│   └── error.html
└── static/
    └── styles.css
```

| Archivo o directorio | Descripción |
| --- | --- |
| `app.py` | Contiene la lógica del servidor Flask y el modelo de aprendizaje automático. |
| `templates/login.html` | Presenta el formulario de entrada de datos. |
| `templates/result.html` | Muestra el nivel de estrés estimado. |
| `templates/error.html` | Informa de los errores relacionados con los datos introducidos. |
| `static/styles.css` | Define los estilos visuales de la aplicación. |
| `StressLevelDataset.csv` | Contiene los datos utilizados para entrenar el modelo. |

> **Nota:** aunque el formulario se encuentra en un archivo llamado `login.html`, la autenticación de usuarios figura entre las mejoras previstas.

## Instalación y ejecución

### 1. Clonar el repositorio

```bash
git clone [https://github.com/venky-1710/stress-level-predection.git](https://github.com/venky-1710/stress-level-predection.git)
cd stress-level-predection
```

### 2. Instalar las dependencias

Con Python y pip disponibles en el equipo, ejecuta:

```bash
pip install flask pandas numpy scikit-learn
```

### 3. Añadir el conjunto de datos

Coloca el archivo `StressLevelDataset.csv` en el directorio raíz del proyecto, junto a `app.py`.

> **Importante:** el conjunto de datos no está incluido en el repositorio. Debes disponer de él antes de ejecutar la aplicación.

### 4. Iniciar la aplicación

```bash
python app.py
```

### 5. Acceder desde el navegador

Abre la siguiente dirección:

```text
http://localhost:5000
```

## Uso de la aplicación

1. Accede a la aplicación desde el navegador.
2. Completa el formulario con los factores solicitados.
3. Respeta el intervalo de valores indicado en cada campo.
4. Pulsa el botón de envío.
5. Consulta el nivel de estrés estimado en la página de resultados.

Si introduces valores no válidos, la aplicación mostrará una página de error.

## Conjunto de datos

El modelo se entrena con el archivo `StressLevelDataset.csv`.

Este archivo debe:

- Estar ubicado en el directorio raíz del proyecto.
- Conservar el nombre esperado por la aplicación.
- Contener las columnas y los datos requeridos por la implementación de `app.py`.

El conjunto de datos se distribuye por separado y no forma parte del contenido del repositorio.

## Limitaciones y uso responsable

La salida de la aplicación es una estimación generada por un modelo de aprendizaje automático; no debe interpretarse como un diagnóstico clínico ni como un sustituto de la evaluación de un profesional de la salud.

Esta documentación no presenta métricas de rendimiento ni resultados de validación clínica. Por tanto, no atribuye al modelo una precisión determinada ni acredita su uso sanitario.

## Mejoras previstas

- [ ] Implementar la autenticación de usuarios.
- [ ] Incorporar el almacenamiento de datos.
- [ ] Añadir explicaciones más detalladas sobre los factores del formulario.
- [ ] Comparar distintos modelos de aprendizaje automático.
- [ ] Desarrollar una función de seguimiento del nivel de estrés a lo largo del tiempo.

## Contribuciones

Las contribuciones para mejorar el proyecto son bienvenidas.

Para proponer un cambio:

1. Crea una copia del repositorio en tu cuenta mediante la opción *Fork*.
2. Crea una rama para tu propuesta.
3. Realiza los cambios y comprueba su funcionamiento.
4. Envía una solicitud de incorporación de cambios (*pull request*) con una descripción clara de la propuesta.

También puedes comunicar errores o sugerir mejoras en la sección de incidencias del repositorio.

## Licencia

Este proyecto se distribuye bajo la [licencia MIT](LICENSE). Consulta el archivo de licencia para conocer sus condiciones de uso, modificación y distribución.
