# Prueba 2

Se siguio el capitulo 1 del Curso Devops Craftech

## Backend
Se investigó para dar con la posibilidad de usar python 3.7, la cual es una version mas vieja pero despues de haber probado con otras imagenes base como ubuntu, alpine y python latest se optó por usar python3.7 ya que no tiene demasiados problemas con los requerimientos solicitados.

Luego se tuvo fallo en pygraphviz por lo tanto se agregó a la lista de instalación en el Dockerfile

## Frontend 

Se indagó sobre react.js en docker y llegue al post [React.js in Docker](https://medium.com/@marvels0098/how-to-include-reactjs-app-in-docker-container-2e73068ce2d5). Sorprendentemente el docker build funciono a la primera, pero con el error **django.core.exceptions.ImproperlyConfigured: The SECRET_KEY setting must not be empty.** Parece que faltaba una secret key, que se puede encontrar en **/backend/backend/.env**.

## Instalación
Se debe clonar el repositorio, abrir una terminal en la carpeta clonada y ejecutar el siguiente comando:
- **sudo docker-compose up --build**

Para visualizar la aplicación, abrir un navegador y acceder a la dirección:
- **http://localhost:3000**

## Referencias

- [Docker Django](https://docs.docker.com/samples/django/)
- [Docker Hub Python](https://hub.docker.com/_/python)
- [Docker Hub Node](https://hub.docker.com/_/node)
- [Python Requirements](https://stackoverflow.com/questions/59626068/running-pip-install-requirements-txt-fails-in-docker-build)
- [Django Env](https://alicecampkin.medium.com/how-to-set-up-environment-variables-in-django-f3c4db78c55f)
- [React.js in Docker](https://medium.com/@marvels0098/how-to-include-reactjs-app-in-docker-container-2e73068ce2d5)
