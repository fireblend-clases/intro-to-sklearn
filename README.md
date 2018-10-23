## Acerca de

Este es un tutorial elaborado por [PythonWorkshop](https://github.com/PythonWorkshop/), basado en el trabajo de múltiples colaboradores, y traducido parcialmente al español por Sergio Morales (@fireblend), Zucethy Obando (@Zucethy), Michael Abarca (@michaelaba10) y Andrea Torres (@amekare).

## ¿Qué hay en este tutorial?

El tutorial se divide en *notebooks*, y es una introducción para aprender *machine learning* en Python utilizando `scikit-learn` con ejemplos y recomendaciones.

El material se encuentra en formato de `jupyter notebook`, y fue diseñado para ser compatible con Python >= 2.6 o >= 3.3. Para utilizar los `jupyter notebook` de forma interactiva, se necesita instalar jupyter/ipyhton notebook (ver información abajo).

Además, se incluye una breve guía introductoria para `jupyther notebooks` en el *notebook* Notebook_anatomy. Si usted está poco familarizado con jupyter/ipython notebooks, por favor tome el tiempo necesario para consultar este archivo.

## Notas para la instalación

> Para el lanzamiento rápido de la aplicación, simplemente dé click en el enlace `launch binder` al inicio de esta página. Sin embargo, le recomendamos realizar una instalación local para configuraciones más personalizadas, flexibilidad y otras posibilidades.

### Configuración del ambiente de desarrollo

> Nota: el archivo requirements.txt es una copia de los paquetes instalados con `pip` desde el último ambiente exitoso de `machine learning`. `Conda` instala las mejores dependencias para el `scikit-learn` utilizado y también puede tener diferentes versiones.

En general una de las mejores prácticas es contar con un ambiente de desarrollo diferente por cada proyecto de Python. Hay muchas opciones disponibles para hacer esto, como virtualenv y Conda. Para este proyecto, usaremos la herramienta [Conda](https://www.continuum.io/why-anaconda).

Para iniciar, se debe instalar [miniconda3](http://conda.pydata.org/docs/install/quick.html) para tener tanto python3 como python2.

Si usted tenía instalado Python previamente, puede instalar Conda con `pip`:

```
pip install auxlib conda
```

### Inicializando un ambiente Conda

* Para configurar un ambiente de desarrollo para python 2.7, adicional al creado de python3 con Conda para el proyecto (creado después de instalar [miniconda3](http://conda.pydata.org/docs/install/quick.html)), se debe ejecutar el comando:
  * `conda create --name sklearn python=2`
  * Para Windows, el ambiente se instala en `C:\Miniconda3\envs\python2\`, por lo que se debe agregar a las variables de entorno del sistema
  * En Linux y OS/X, la instalación dependerá de donde se encuentra instalado el framework de Python. En OS/X utilizando Homebrew, se instala en `/usr/local/Cellar/python/2.7.10_2/Frameworks/Python.framework/Versions/2.7/envs/python2/bin`
  * Para ver instrucciones más detalladas, puede consultar [aquí](http://conda.pydata.org/docs/py2or3.html)

* Para activar el ambiente de desarrollo, desde el directorio `bin` en el ambiente de conda, hay que ejecutar:
  * Windows: `activate sklearn`
  * Linux/OSX: `source activate sklearn`

* Asegúrese de que ipython/ipython2 se encuentre instalado en el ambiente de Python:
  * Windows: `c:\Miniconda3\envs\python2\Scripts\ipython2.exe kernel install --name python2 --display-name "Python 2"`
  * Linux/OSX: `ipython2 kernel install --name python2 --display-name "Python 2"` (puede que ocupe `sudo`)

* Si desea desactivar el ambiente de desarrollo, simplemente digite el siguiente comando:
  * Windows: `deactivate`
  * Linux/OSX: `source deactivate`


### Instalando jupyter notebook localmente

La forma sencilla de instalar [jupyter notebook](http://jupyter.org/) es a través de `conda install`

* Ejecute `conda install jupyter` desde la interfaz de comandos. Linux/OSX puede requerir permisos de `sudo`.
* Navegue en el directorio contenido en este repositorio, y ejecute `jupyter notebook`. <b>Esto inicializará el servicio de notebook</b> localmente para accesar los notebooks desde el navegador. Puede profundizar desde la página de inicio al notebook de interés.

Para un primer acercamiento vaya a `Notebook_anatomy.ipynb` en este repositorio. La forma corta es: ejecute una celda presionando <b>Shift-Enter</b>.  Hay muchos otros atajos de teclado en el notebook.

## Instalando paquetes de python

Este tutorial requiere los siguientes paquetes:

 * numpy versión 1.5 o posterior: http://www.numpy.org/
 * scipy versión 0.10 o posterior : http://www.scipy.org/
 * pandas http://pandas.pydata.org/
 * matplotlib versión 1.3 o posterior: http://matplotlib.org/
 * scikit-learn versión 0.14 o posterior: http://scikit-learn.org
 * jupyter http://jupyter.readthedocs.org/en/latest/install.html 

Puede usar el ambiente de desarrollo de su elección, pero si utiliza `conda` como se describe arriba, simplemente ejecute:
```
	$ conda install numpy scipy matplotlib scikit-learn jupyter
```

También le brindamos el archivo requirementes.txt para usar con pip.

## Otras opciones de instalación

Hay muchas formas de instalar python y el ecosistema de paquetes para machine learning. No van a ser totalmente cubierto aquí, pero esencialmente tiene las siguientes opciones:

1. anaconda/miniconda también conocido como conda (se vió arriba)
2. descargue python y pip para instalar paquetes
3. use una imagen de docker  ([esta](https://hub.docker.com/r/wi3o/skflow-jupyternb/) configurada para jupyter+sklearn+skflow+tensorflow)
4. [Google cloud platform](https://cloud.google.com/) tiene un servicio de jupyter notebook llamado Datalab (inicio rápido [aquí](https://cloud.google.com/datalab/docs/quickstart)).  Tiene tensorflow pre-instalado (necesario para el siguiente tutorial).
5. Dé click en el enlace Binder al inicio de esta página para desplegar la configuración del notebook.

O cualquier combinación de las anteriores.

Una recomendación rápida es está instalando de una forma non-conda con `pip` y está en Windows, muchos de los paquetes de análisis de datos son engorrosos de instalar (compilar las dependencias). Un buen repositorio "no oficial" como `numpy`y numerosos otros han sido creados y mantenidos por Christoph Gohlke.  El sitio es [este](http://www.lfd.uci.edu/~gohlke/pythonlibs/).

## Que sigue

El siguiente tutorial en este taller es de `tensorflow` y las instrucciones de instalación son estas  [README](https://github.com/PythonWorkshop/intro-to-tensorflow/blob/master/README.md)

[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/PythonWorkshop/intro-to-sklearn)
