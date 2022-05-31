# Prueba 1

Para esta prueba se comenzó investigando las plataformas que ofrecen servicios en la nube, **Amazon Web Services (AWS) y Google Cloud Platform (GCP)**. Se optó por elegir GCP ya que en varios videos recomiendan comenzar con GCP por ser más fácil de configurar y en general más sencillo para aprender, además de que ofrece un curso de capacitación gratuito con pequeños logros llamados Badges, que preparan al estudiante para rendir el examen de certificación que si es pago.

De acuerdo con el artículo sobre [Hosting Web Apps in GCP](https://medium.com/google-cloud/hosting-web-applications-on-google-cloud-an-overview-46f5605eb3a6), se emplearon los siguientes elementos que ilustra el diagrama:

- **Cloud Load Balancing**: El balanceador de carga que redirige el tráfico web hacia el contenedor apropiado para no saturar los recursos de ninguno de ellos, evitando así la pérdida momentánea de servicio para los clientes.
- **App Engine**: El frontend del servicio web, diseñado en Js. Funciona bien si la demanda es baja.
- **Container Engine**: El orquestador de contenedores Kubernetes, ofrece crear o eliminar contenedores de la aplicación para escalar bajo demanda y sólo pagar por lo que efectivamente se necesita en ese momento.
- **Compute Engine**: El backend representa los servidores que procesan la información importante y que emplean más recursos computacionales, ya que se encargan de logear, comunicarse con los microservicios y leer y escribir en las bases de datos.
- **Microservicios**:
    - **Monitoring**: Permite monitorear el uso de recursos de la aplicación.
    - **Translation API**: Ofrece una API para realizar traducciones en varios idiomas.
- **Databases**:
    - **Relational**: Por ejemplo MySQL.
    - **Non-Relational**: Por ejemplo Mongo-DB.

![GCP WebApp Diagram](/prueba1/GCP-Diagram.png "GCP WebApp Diagram")

## Referencias
- [Hosting Web Apps in GCP](https://medium.com/google-cloud/hosting-web-applications-on-google-cloud-an-overview-46f5605eb3a6)
- [GCP Overview](https://www.youtube.com/watch?v=pxp7uYUjH_M)