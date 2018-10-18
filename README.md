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

The easiest way to install [jupyter notebook](http://jupyter.org/) is via `conda install`
* Run `conda install jupyter` from your terminal. Linux/OSX may require `sudo` permissions.
* Navigate to the directory containing this repository, and execute `jupyter notebook`. <b>This will start a notebook service</b> locally for accessing notebooks in your browser. Drill down on the home page to your notebook of interest.

For a notebook primer go to `Notebook_anatomy.ipynb` on this repo.  The very short story is: to execute a cell just hit <b>Shift-Enter</b>.  There are many more shortcuts in primer.

## Installing python packages

This tutorial requires the following packages:

 * numpy version 1.5 or later: http://www.numpy.org/
 * scipy version 0.10 or later: http://www.scipy.org/
 * pandas http://pandas.pydata.org/
 * matplotlib version 1.3 or later: http://matplotlib.org/
 * scikit-learn version 0.14 or later: http://scikit-learn.org
 * jupyter http://jupyter.readthedocs.org/en/latest/install.html

You can use your development environment of choice, but if you used `conda` as described above, simply run:
```
	$ conda install numpy scipy matplotlib scikit-learn jupyter
```

We have also provided a requirements.txt file above for use with pip.

## Other install options

There are many different ways to install python and the package ecosystem for machine learning.  They are not all going to be covered here, but essentially you have the following choices:

1. anaconda/miniconda aka conda (shown above)
2. download python and pip install packages
3. use a docker image ([this](https://hub.docker.com/r/wi3o/skflow-jupyternb/) is one for jupyter+sklearn+skflow+tensorflow)
4. [Google cloud platform](https://cloud.google.com/) has a jupyter notebook service called Datalab (quickstart [here](https://cloud.google.com/datalab/docs/quickstart)).  It has tensorflow pre-installed (needed for next tutorial).
5. Click the Binder link at the bottom of this page to deploy a notebook setup.

Or a combination of the above.

A quick tip if you are installing in a non-conda way with `pip` and are on Windows, many of the data analysis packages are tricky (compiled dependencies) to install.  A nice "unofficial" repository for binaries of packages like `numpy` and a myriad of others was created and maintained by Christoph Gohlke.  This site is [here](http://www.lfd.uci.edu/~gohlke/pythonlibs/).

## What's next

The next tutorial in this workshop is on `tensorflow` and the installation instructions are in this [README](https://github.com/PythonWorkshop/intro-to-tensorflow/blob/master/README.md)

[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/PythonWorkshop/intro-to-sklearn)
