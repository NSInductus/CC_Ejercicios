# Ejercicio 1

**Buscar alguna demo interesante de Docker y ejecutarla localmente, o en su defecto, ejecutar la imagen anterior y ver cómo funciona y los procesos que se llevan a cabo la primera vez que se ejecuta y las siguientes ocasiones.**

Se descargo la imagen de MongoDB, con el siguiente comandos

```shell
$ sudo docker pull mongo:latest

```

Para arrancarla en primer lugar, listamos las imágenes disponibles, con el siguiente comando:


```shell
$ sudo docker images
```

El resultado es el siguiente:



```
REPOSITORY               TAG                 IMAGE ID            CREATED             SIZE
mongo                    latest              105a8b77784b        8 days ago          364MB

```

Para ejecutarla recordamos el ID_imagen y ejecutamos en terminal:

```shell
$ sudo docker run 105a8b77784b
```

De esta forma arranca el contenedor y podemos comprobar que lo primero que muestra la terminal es:

```
2020-01-26T18:51:04.762+0000 I  CONTROL  [main] Automatically disabling TLS 1.0, to force-enable TLS 1.0 specify --sslDisabledProtocols 'none'
2020-01-26T18:51:04.764+0000 I  CONTROL  [initandlisten] MongoDB starting : pid=1 port=27017 dbpath=/data/db 64-bit host=727852665da7
2020-01-26T18:51:04.764+0000 I  CONTROL  [initandlisten] db version v4.2.2
2020-01-26T18:51:04.764+0000 I  CONTROL  [initandlisten] git version: a0bbbff6ada159e19298d37946ac8dc4b497eadf
2020-01-26T18:51:04.764+0000 I  CONTROL  [initandlisten] OpenSSL version: OpenSSL 1.1.1  11 Sep 2018
2020-01-26T18:51:04.765+0000 I  CONTROL  [initandlisten] allocator: tcmalloc
2020-01-26T18:51:04.765+0000 I  CONTROL  [initandlisten] modules: none
2020-01-26T18:51:04.765+0000 I  CONTROL  [initandlisten] build environment:
2020-01-26T18:51:04.765+0000 I  CONTROL  [initandlisten]     distmod: ubuntu1804
2020-01-26T18:51:04.765+0000 I  CONTROL  [initandlisten]     distarch: x86_64
2020-01-26T18:51:04.765+0000 I  CONTROL  [initandlisten]     target_arch: x86_64
2020-01-26T18:51:04.765+0000 I  CONTROL  [initandlisten] options: { net: { bindIp: "*" } }
2020-01-26T18:51:04.766+0000 I  STORAGE  [initandlisten]
2020-01-26T18:51:04.766+0000 I  STORAGE  [initandlisten] ** WARNING: Using the XFS filesystem is strongly recommended with the WiredTiger storage engine
2020-01-26T18:51:04.766+0000 I  STORAGE  [initandlisten] **          See http://dochub.mongodb.org/core/prodnotes-filesystem
2020-01-26T18:51:04.766+0000 I  STORAGE  [initandlisten] wiredtiger_open config: create,cache_size=7468M,cache_overflow=(file_max=0M),session_max=33000,eviction=(threads_min=4,threads_max=4),config_base=false,statistics=(fast),log=(enabled=true,archive=true,path=journal,compressor=snappy),file_manager=(close_idle_time=100000,close_scan_interval=10,close_handle_minimum=250),statistics_log=(wait=0),verbose=[recovery_progress,checkpoint_progress],
2020-01-26T18:51:05.709+0000 I  STORAGE  [initandlisten] WiredTiger message [1580064665:709954][1:0x7f96ad1b7b00], txn-recover: Set global recovery timestamp: (0,0)
2020-01-26T18:51:05.921+0000 I  RECOVERY [initandlisten] WiredTiger recoveryTimestamp. Ts: Timestamp(0, 0)
2020-01-26T18:51:06.135+0000 I  STORAGE  [initandlisten] Timestamp monitor starting
2020-01-26T18:51:06.237+0000 I  CONTROL  [initandlisten]
2020-01-26T18:51:06.237+0000 I  CONTROL  [initandlisten] ** WARNING: Access control is not enabled for the database.
2020-01-26T18:51:06.237+0000 I  CONTROL  [initandlisten] **          Read and write access to data and configuration is unrestricted.
2020-01-26T18:51:06.237+0000 I  CONTROL  [initandlisten]
2020-01-26T18:51:06.238+0000 I  STORAGE  [initandlisten] createCollection: admin.system.version with provided UUID: 43dc2e67-d124-48a8-9af8-2f09d724b9ad and options: { uuid: UUID("43dc2e67-d124-48a8-9af8-2f09d724b9ad") }
2020-01-26T18:51:06.397+0000 I  INDEX    [initandlisten] index build: done building index _id_ on ns admin.system.version
2020-01-26T18:51:06.397+0000 I  SHARDING [initandlisten] Marking collection admin.system.version as collection version: <unsharded>
2020-01-26T18:51:06.397+0000 I  COMMAND  [initandlisten] setting featureCompatibilityVersion to 4.2
2020-01-26T18:51:06.397+0000 I  SHARDING [initandlisten] Marking collection local.system.replset as collection version: <unsharded>
2020-01-26T18:51:06.397+0000 I  STORAGE  [initandlisten] Flow Control is enabled on this deployment.
2020-01-26T18:51:06.398+0000 I  SHARDING [initandlisten] Marking collection admin.system.roles as collection version: <unsharded>
2020-01-26T18:51:06.398+0000 I  STORAGE  [initandlisten] createCollection: local.startup_log with generated UUID: 616843f8-18bd-4cbd-a7d8-2d6177c91be2 and options: { capped: true, size: 10485760 }
2020-01-26T18:51:06.572+0000 I  INDEX    [initandlisten] index build: done building index _id_ on ns local.startup_log
2020-01-26T18:51:06.572+0000 I  SHARDING [initandlisten] Marking collection local.startup_log as collection version: <unsharded>
2020-01-26T18:51:06.573+0000 I  FTDC     [initandlisten] Initializing full-time diagnostic data capture with directory '/data/db/diagnostic.data'
2020-01-26T18:51:06.575+0000 I  SHARDING [LogicalSessionCacheRefresh] Marking collection config.system.sessions as collection version: <unsharded>
2020-01-26T18:51:06.575+0000 I  NETWORK  [initandlisten] Listening on /tmp/mongodb-27017.sock
2020-01-26T18:51:06.575+0000 I  NETWORK  [initandlisten] Listening on 0.0.0.0
2020-01-26T18:51:06.575+0000 I  NETWORK  [initandlisten] waiting for connections on port 27017
2020-01-26T18:51:06.576+0000 I  CONTROL  [LogicalSessionCacheReap] Sessions collection is not set up; waiting until next sessions reap interval: config.system.sessions does not exist
2020-01-26T18:51:06.576+0000 I  STORAGE  [LogicalSessionCacheRefresh] createCollection: config.system.sessions with provided UUID: 56f84b86-0c76-417a-a775-4ab9960bea05 and options: { uuid: UUID("56f84b86-0c76-417a-a775-4ab9960bea05") }
2020-01-26T18:51:06.755+0000 I  INDEX    [LogicalSessionCacheRefresh] index build: done building index _id_ on ns config.system.sessions
2020-01-26T18:51:06.972+0000 I  INDEX    [LogicalSessionCacheRefresh] index build: starting on config.system.sessions properties: { v: 2, key: { lastUse: 1 }, name: "lsidTTLIndex", ns: "config.system.sessions", expireAfterSeconds: 1800 } using method: Hybrid
2020-01-26T18:51:06.972+0000 I  INDEX    [LogicalSessionCacheRefresh] build may temporarily use up to 500 megabytes of RAM
2020-01-26T18:51:06.973+0000 I  INDEX    [LogicalSessionCacheRefresh] index build: collection scan done. scanned 0 total records in 0 seconds
2020-01-26T18:51:06.974+0000 I  INDEX    [LogicalSessionCacheRefresh] index build: inserted 0 keys from external sorter into index in 0 seconds
2020-01-26T18:51:07.000+0000 I  SHARDING [ftdc] Marking collection local.oplog.rs as collection version: <unsharded>
2020-01-26T18:51:07.009+0000 I  INDEX    [LogicalSessionCacheRefresh] index build: done building index lsidTTLIndex on ns config.system.sessions
2020-01-26T18:51:07.021+0000 I  COMMAND  [LogicalSessionCacheRefresh] command config.system.sessions command: createIndexes { createIndexes: "system.sessions", indexes: [ { key: { lastUse: 1 }, name: "lsidTTLIndex", expireAfterSeconds: 1800 } ], $db: "config" } numYields:0 reslen:114 locks:{ ParallelBatchWriterMode: { acquireCount: { r: 2 } }, ReplicationStateTransition: { acquireCount: { w: 3 } }, Global: { acquireCount: { r: 1, w: 2 } }, Database: { acquireCount: { r: 1, w: 2, W: 1 } }, Collection: { acquireCount: { r: 4, w: 1, R: 1, W: 2 } }, Mutex: { acquireCount: { r: 3 } } } flowControl:{ acquireCount: 1 } storage:{} protocol:op_msg 445ms

```

# Ejercicio 2

**Tomar algún programa simple, “Hola mundo” impreso desde el intérprete de línea de órdenes, y comparar el tamaño de las imágenes de diferentes sistemas operativos base, Fedora, CentOS y Alpine, por ejemplo.**



El programa será creado en *Python*, el fichero correspondiente a este es [programa.py](programa.py), su contenido es el siguiente (no es un hola mundo, pero es igual de simple):

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
sudo docker build -t imagen_programa_python /home/inductus/Documentos/CC/CC_Ejercicios

```

Los resultados son los siguiente:


```
Sending build context to Docker daemon  251.9kB
Step 1/3 : FROM python:3.7
 ---> de787d71ba24
Step 2/3 : COPY programa.py programa.py
 ---> ab6ad4fcff2f
Step 3/3 : CMD ["python", "programa.py"]
 ---> Running in 79d3363c8fd7
Removing intermediate container 79d3363c8fd7
 ---> 51f85e444a74
Successfully built 51f85e444a74
Successfully tagged imagen_programa_python:latest

```

A continuación comprobamos que nuestra imagen esta creada correctamente utilizando:

```shell
$ sudo docker images
```

El resultado es el siguiente:



```
REPOSITORY               TAG                 IMAGE ID            CREATED             SIZE
imagen_programa_python   latest              51f85e444a74        2 minutes ago       918MB
python                   3.7                 de787d71ba24        40 hours ago        918MB


```

Ahora se va a probar esa imagen sobre otros 2 sistemas diferentes. En primer lugar debian, el código del Dockerfile es el siguiente:

```dockerfile
FROM bitnami/minideb:latest
RUN install_packages python3
COPY programa.py programa.py
CMD ["python3", "programa.py"]

```

Y por último sobre una versión de ubuntu, el código del Dockerfile es el siguiente:


```dockerfile
FROM ubuntu:latest
RUN apt-get install python3
COPY programa.py programa.py
CMD ["python3", "programa.py"]

```

El tamaño de cada uno de los contenedors, extraído con el comando anterior se puede ver en la siguiente tabla:

|imagen_base|tamaño|
|-------|-------|
|python|918MB|
|debian|100MB|
|ubuntu|127MB|

Cada una de estos Dockerfile, se encuentran en los archivos [Dockerfile1](Dockerfile1), [Dockerfile2](Dockerfile2) y [Dockerfile3](Dockerfile3), respectivamente.


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
