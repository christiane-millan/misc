# Ambientes virtuales

Los ambientes virtuales son muy importantes en Python. Python opera de manera global en nuestro sistema opeartivo. Mediante ambientes virtuales evitamos contaminar nuestro ambiente global.

Siempre instala nuevos paquetes de manera virtual

- Para importar librerías de terceros debemos de utilizar ambientes virtuales. 
- En Python3 se incluye de manera estándar ambientes virtuales: `pip`

`pip` permite:

- Descargar paquetes de terceros para utilizarlos en nuestros programas
- Permite compartir nuestros paquetes con terceros
- Permite especificar la versión del paquete que necesitamos.

## Ambientes virtuales en python

### Crear ambientes virtuales

```python
python -m venv venv
```

### Activar un ambiente virtual

En Linux o macOS
```python
source venv/bin/activate
```
En Windows 
```terminal
.\venv\Scripts\activate
```

Tip: Crear alias en Windows
```terminal
alias avenv =  .\venv\Scripts\activate
```
En sistemas basados en Unix los alias se tienen que agregar al perfil de la configuración inicial de la terminal `bashrc` o `zshrc`.
```terminal
alias avenv =  source venv/bin/activate
```

### Desactivar un ambiente virtual

```python
deactivate
```

### Instalación de dependencias con PIP (Package Installer for Python)

Una vez con nuestro ambiente virtual podemos instalar las dependencias requeridas. Ejemplo: Requests, BeautifulSoup4, Pandas, Numpy, Pytest

Ejemplo: Instalamos algunas dependencias 

```python
pip install bokeh
pip install pandas
```

Para conocer que tenemos intalado en el ambiente virtual utilizamos:

```python
pip freeze
```
Si no funciona pip, puedes utilizar pip3

Para compartir las dependencias de mi proyecto se crea un archivo requirements.txt

```terminal
pip freeze > requirements.txt
```

Recuperar las dependencias en otro computador

```terminal
pip install -r requirements.txt
```

## Ambientes virtuales en Conda

Es una alternativa a PIP, es un software orientado a Data Sciences. Incluye una GUI

### Crear ambientes virtuales

```python
conda create --name cmdpy37 python=3.7
```

### Activar un ambiente virtual

```python
conda activate cmdpy37
```

### Desactivar un ambiente virtual

```python
conda deactivate
```

### Listar ambiente virtual

```python
conda env list
```

para mandar requirements.txt a un archivo

```terminal
conda list --export > requirements.txt
```

### Eliminar un ambiente virtual

```python
conda env remove --name cmdpy37
```

### Instalación de dependencias con Anaconda

```terminal
conda install pandas
```
o desde un archivo requirements.txt

```terminal
conda install --file requirements.txt
```
