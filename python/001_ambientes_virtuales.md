# Ambientes virtuales

Los ambientes virtuales son muy importantes en Python. Python opera de manera global en nuestro sistema opeartivo. Mediante ambientes virtuales evitamos contaminar nuestro ambiente global.

Siempre instala nuevos paquetes de manera virtual

- Para importar librerías de terceros debemos de utilizar ambientes virtuales. 
- En Python3 se incluye de manera estándar ambientes virtuales: `pip`

`pip` permite:

- Descargar paquetes de terceros para utilizarlos en nuestros programas
- Permite compartir nuestros paquetes con terceros
- Permite especificar la versión del paquete que necesitamos.

## Crear ambientes virtuales

```python
python -m venv env
```

## Activar un ambiente virtual

```python
source env/bin/activate
```

## Desactivar un ambiente virtual

```python
deactivate
```

## Instalación de una librería

Una vez con nuestro ambiente virtual podemos instalar la librería que queramos

Ejemplo: Instalamos la librería bokeh` 

```python
pip install bokeh
```

Para conocer que tenemos intalado en el ambiente virtual utilizamos:

```python
pip freeze
```
