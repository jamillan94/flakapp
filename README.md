# Aplicacion Flask con Docker image y CI/CD

## Temas
- Descripcion
- Instalacion
- App Flask
- Creacion Docker Images CI
- Despliegue en azure CD


## Descripcion
<p>Este proyecto muestra como de desarrollo el despligue continuo y la integegracion continua de una aplicacion realizado en python-flask
haciendo uso de la herramienta docker</p>

## Instalacion
<p>Para iniciar el proyecto fue necesario hacer uso de las herramientas Docker y el framework para pytho flask, en el caso de docker el instalador de descargo de la pagina oficial de <strong>docker</strong> [Sitio oficial Docker](https://www.docker.com/products/docker-desktop), para el caso de el framework de flask fue necesario por medio de la consola ingresar el comando <code>pip install flask</code></p>

## App Flask
<p>Esta aplicacion se desarrollo con  el framework flask y lo que hace es utilizar los datos contenidos en una lista y mostrarlos en formato Json cuando se utiliza url_base/users, por otro lado cuando se utiliza esta en la ur base  este muestra un mensaje en formato json el cual dice  Hola,Chicos!</p>
![url_base](/assets/imagenes_readme/Imagen1.jpg)
![users](/assets/imagenes_readme/Imagen2.jpg)

## Creacion Docker Images CI
<p>Para la creacion del docker se creo un archivo Docker file en el cual se descarga la version 3.8.10 de python y apartir  de esta se instalan las librerias necesarias las cuales se encuentran en el archivo requirements, se expone por el purto y se de ejecuta app.py, se ejecunta el comando <code>docker build -t flaskapp  .</code>
para clear la imagen y luego de creada la imagen se el ejecuta el comando <code>docker push ivanser90/flaskapp:latest</code>, para crear el registro en docker hub, adicionalmente se creo en accion  de github el pipeline por el cual carga el el readme crea la imagen y este mismo se encarga de publicar la imagen en docker hub</p>
![dockerhub](/assets/imagenes_readme/Imagen3.jpg)

## Despliegue en azure CD
<p>Para desplegar el proyecto en Azure se creo una cuenta en azure [Porta Azure](https://portal.azure.com/)  donde se creo un app service el cual se encarga de obtner el docker que se encuentra en docker hub y desplegarlo en una instancia configurada y mostrarlo en un browser</p>
![azure](/assets/imagenes_readme/Imagen4.jpg)
