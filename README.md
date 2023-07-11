# my-second-pip-package

En Python se usa PIP para utilizar bibliotecas de terceros.

Aunque conseguí crea [mi primer paquete en Python](https://github.com/egarciarey1981/my-first-pip-package) utilizando la guía de Python, he visto que otros consiguen hacer lo mismo de forma distinta.

Este segundo paquete lo he creado utilizando [un video que encontre en YouTube](https://www.youtube.com/watch?v=AczMuVzUrkE).

## Crear el paquete

Básicamente, lo que hay que hacer es crear una carpeta con el nombre del paquete y dentro de ella crear un fichero `__init__.py` con el código del paquete.

Para que el paquete se pueda instalar con PIP, hay que crear un fichero `setup.py` con la información del paquete.

```python
from setuptools import setup, find_packages

setup(
    name='math2-egarciarey1981',
    description='My second pip package',
    version='0.1.0',
    url='https://github.com/egarciarey1981/my-second-pip-package',
    packages=find_packages(),
)
```

**NOTA:** El nombre del paquete utiliza guión (`-`) en vez de guión bajo (`_`) porque PIP no permite guión bajo en el nombre del paquete. Si se utiliza guión bajo, PIP lo sustituye por guión.

## Instalar el paquete

Una vez subido a un repositorio de GitHub, para instalar el paquete, hay que ejecutar el siguiente comando:

```bash
pip install git+https://github.com/egarciarey1981/my-second-pip-package
```

Para comprobar que se ha instalado correctamente, hay que ejecutar el siguiente comando:

```bash
pip list | grep math2-egarciarey1981
```

## Uso del paquete

Para usar el paquete, hay que importarlo:

```python
from math2_egarciarey1981.math2 import Math2

math2 = Math2()
result = math2.sum(1, 2)
print(result)
```
