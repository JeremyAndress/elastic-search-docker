# Elastic Search Stack :rainbow:

Este [repositorio](https://github.com/JeremySilvaSilva/elastic-search-docker) cuenta con una implementacion de Elastic Search utilizando Elastic y Kibana en su version mas actual(7.7). Creado como template para el futuro uso de proyectos que necesiten de elastic search. :shipit:

## Dependencias 

Para hacer funcionar este template es necesario tener las siguientes herramientas instaladas en su maquina. Este template fue generado en un entorno Fedora, pero gracias al uso de Docker, su funcionamiento debe ser casi el mismo en otros entornos UNIX.

- Docker :whale: - version 19+
- Docker Compose :whale2: - version 1.18

## Levantando servicio :coffee:

- Primero debes clonar el repositorio en tu entorno UNIX
- Una vez clonado el repositorio debes situarte en la raiz del proyecto y correr el siguiente comando:

```sh
$ docker-compose -f local.yml up -d
```
Este comando nos permitira crear las imagenes de elastic search y kibana y ademas levantar los servicios :rocket:. 
> *NOTA*: Los servicios toman un tiempo en levantarse.

- Puedes revisar el correcto funcionamiento de elastic search utilizando el siguiente comando:

```sh
$ curl -X GET "localhost:9200/_cat/nodes?v&pretty"
```

![Elastic Response](/screenshots/elastic_response.png)

- Para revisar la interfaz de usuario(Kibana) debes acceder e la ruta [http://0.0.0.0:5601](http://0.0.0.0:5601)

- Se desplegara un dashboard para elegir data de prueba:


![Kibana Response](/screenshots/kibana_dashboard.png)