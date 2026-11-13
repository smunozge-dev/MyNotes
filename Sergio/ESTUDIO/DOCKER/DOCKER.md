


## IMAGENES


### CONSTRUCCIÓN DE IMAGEN


#### SINTAXIS BÁSICA (CONSTRUCCIÓN DE UNA IMAGEN)
Para la construcción de imágenes con la herramienta de Docker la sintaxis básica es la siguiente:

``` bash
:'
DESFRAGMENTACIÓN
1.- docker : utilizar la herramienta docker
2.- build: Instrucción que indica construir, hecha para la construcción de una imagen
3.- -t nombre_imagen: Indica la tag o el nombre de nuestra imagen.
4.- .: El punto, indica que se construira la imagen desde este directorio y buscara desde ese punto el Dockerfile correspondiente.
'
docker build -t miholamundo .

```


De esta forma podemos ya correr un contenedor a partir de la miniatura o copia del contenido que montamos en nuestra imagen, por ejemplo:

ver sección contenedores si interesa: [[DOCKER#CONTENEDORES|CONTENEDORES]]

```bash
docker run --rm nombreimagen

```

#### RECONSTRUCCIÓN IMAGEN

Eventualmente se construirá mal una imagen, ya sea por una mala declaración de variable de entorno, volumen, o lo que sea, por lo que vamos a querer corregir ese error. Docker, nos permite volver a construir la misma imagen pero con los cambios ya corregidos en el archivo correspondiente, ya sea el Dockerfile o docker-compose.yaml

Para ello debemos de encontrarnos en el mismo directorio de origen de donde levantamos la imagen con el archivo correspondiente, para este ejemplo el Dockerfile del proyecto y ejecutamos:

``` bash
: << 'INSTRUCCIONES'
A continuación desglose de las instrucciones en la terminal
1.- docker; indica que usaremos la herramienta docker de nuestro sistema
2.- build; la instrucción build en docker, indica que vamos a construir una imagen
3.- -t; este argumento indicara que nuestra imagen, le asignaremos una tag para que apunte mejor, para este caso, usaremos la misma tag que utilizamos en la construcción de la imagen anterior erronea, para reconstruir la imagen con los cambios buenos sobreescribiendo la mala.
4.- nombre_imagen_mala; construiremos la misma imagen, con la misma tag que asignamos a la imagen erronea construida anteriormente, de esta forma, reconstruiremos con los cambios corregidos.
5.- .; este argumento indica que el archivo Dockerfile que debe utilizar se encuentra en el mismo directorio que te encuentras en la terminal.
INSTRUCCIONES

# supongamos que anteriormente levantamos una imagen mala con la etiqueta 01-holamundo
docker buid -t 01-holamundo .

```
## CONTENEDORES

## DOCKER FILE




## DOCKER COMPOSE





