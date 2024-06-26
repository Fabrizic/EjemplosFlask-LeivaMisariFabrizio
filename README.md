# Ejemplos de uso de Flask
Flask Python - Ejemplos Básicos
Este repositorio contiene dos ejemplos básicos de aplicaciones web creadas con Flask, un microframework de Python.

Ejemplo 1: Hola Mundo
El primer ejemplo es una aplicación simple de "Hola Mundo". Cuando se accede a la ruta raíz ("/"), la aplicación devuelve un mensaje de "Hola Mundo" en HTML.

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
 return '<h1>Hello World!</h1>'

if __name__ == '__main__':
    app.run(debug=True)
```

Ejemplo 2: Ruta Dinámica
El segundo ejemplo muestra cómo crear rutas dinámicas en Flask. En este caso, la aplicación devuelve un saludo personalizado a la ruta "/user/nombre".

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
 return '<h1>Hello World!</h1>'
 
@app.route('/user/<name>')
def user(name):
 return '<h1>Hello, %s!</h1>' % name

if __name__ == '__main__':
    app.run(debug=True)
```

Cómo ejecutar los ejemplos
Para ejecutar estos ejemplos, sigue estos pasos:

- Clona este repositorio a tu máquina local.
- Navega hasta el directorio del repositorio en tu terminal.
- Ejecuta python Ejemplo1.py o python Ejemplo2.py para iniciar la aplicación.
- Abre un navegador web y ve a http://localhost:5000 para ver la aplicación en acción.
- Requisitos
- Para ejecutar estos ejemplos, necesitarás Python 3 y Flask instalados en tu máquina.
