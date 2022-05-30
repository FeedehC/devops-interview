# Prueba 3

Para esta prueba se comenzó por configurar un **webserver Nginx** sencillo siguiendo los pasos de este [articulo](https://thatdevopsguy.medium.com/how-to-create-a-static-web-server-for-html-with-nginx-99bf8226bce6). El archivo **index.html** tiene unicamente un párrafo orientativo. El objetivo es que cuando se modifique este archivo, y se pushee la modificación a la rama **master**, se desencadene automáticamente el pipeline CI/CD indicado en **.github/workflows/docker-image.yml**.

Para ello se comenzó buscando los templates que ofrece el mismo GitHub, en este caso el template docker-image.yml contiene las instrucciones básicas para buildear una imagen de Docker. Lo que le falta son las acciones para subir esta imagen a un repositorio en DockerHub. Para ello se crea un nuevo repositorio y se agregan las actions oficiales de la web de [GitHub Docker Actions](https://github.com/marketplace/actions/build-and-push-docker-images#usage).

Se presentaron algunos problemas con la autenticación, ya que al probar con varias actions diferentes, algunas solicitan usuario y contraseña, mientras que otras solicitan un PAT (Personal Access Token), en concreto, el pipeline no funcionó hasta que se agregó un PAT a GitHub secrets creado desde DockerHub. Una vez funcional se modificó el evento desencadenante para que solo se desencadene al pushear o crear un pull request que involucre cambios en **/prueba3/index.html**.

## Referencias
- [Dockerized Nginx](https://thatdevopsguy.medium.com/how-to-create-a-static-web-server-for-html-with-nginx-99bf8226bce6)
- [GitHub Docker Actions](https://github.com/marketplace/actions/build-and-push-docker-images#usage)
- [DockerHub Access Token](https://docs.docker.com/docker-hub/access-tokens/)