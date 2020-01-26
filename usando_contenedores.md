# Ejercicio 1

**Buscar alguna demo interesante de Docker y ejecutarla localmente, o en su defecto, ejecutar la imagen anterior y ver cómo funciona y los procesos que se llevan a cabo la primera vez que se ejecuta y las siguientes ocasiones.**


El programa será creado en *Python*, el fichero correspondiente a este es [programa.py](), su contenido es el siguiente:

```python
suma = 3 + 3
print(suma)

```

El Dockerfile que creamos será muy sencillo:

```dockerfile
FROM python:3.7
COPY programa.py programa.py
CMD ["python", "programa.py"]

```


Se ejecutará con el siguiente comando:

```shell
docker build -t python:3.7 -f Dockerfile1

```

Los resultados son los siguiente:


```


```

# Ejercicio 2

**Tomar algún programa simple, “Hola mundo” impreso desde el intérprete de línea de órdenes, y comparar el tamaño de las imágenes de diferentes sistemas operativos base, Fedora, CentOS y Alpine, por ejemplo.**


Rellenar ejercicio 2


# Ejercicio 3

**Crear a partir del contenedor anterior una imagen persistente con commit.**

Rellenar ejercicio 3

# Ejercicio 4

**Examinar la estructura de capas que se forma al crear imágenes nuevas a partir de contenedores que se hayan estado ejecutando.**


Rellenar ejercicio 4


# Ejercicio 5

**Crear un volumen y usarlo, por ejemplo, para escribir la salida de un programa determinado.**


Rellenar ejercicio 5


# Ejercicio 6

**Usar un miniframework REST para crear un servicio web y introducirlo en un contenedor, y componerlo con un cliente REST que sea el que finalmente se ejecuta y sirve como “frontend”.**

Rellenar ejercicio 6

# Ejercicio 7

**Reproducir los contenedores creados anteriormente usando un Dockerfile.**


Rellenar ejercicio 7


# Ejercicio 8

**Crear con docker-machine una máquina virtual local que permita desplegar contenedores y ejecutar en él contenedores creados con antelación.**


Rellenar ejercicio 8
