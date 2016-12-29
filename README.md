# bareos-compose

El objetivo de este compose es testar el sistema para adaptarlo a la escalabilidad de bareos con ello cada servicio es independiente no solo de si mismo sino de los demás. Lo que nos lleva a las diferentes combinaciones de servicios por ejemplo:
El director podría encontrarse con un cliente en el mismo equipo, y mantener comunicación con un storage externo y un cliente a su vez que se encuentra en el mismo nodo que sustenta al storage con lo cual podrían programarse copias de ambos nodos y en uno de ellos se encontraría el storage y en el otro el director.

Falta por hacer:

-División del compose

-Comunicación en diferentes nodos con los servicios

Se debe tener el paquete docker-engine y docker-compose instalados.

Una vez descargado el repositorio accedemos al mismo
```sh
cd bareos-compose
```
Para llamar al compose se usa el siguiente comando:

```sh
docker-compose -f docker-compose-mysql.yml up -d
```
Para ver que todo funciona correctamente podemos acceder via web:

```sh
http://localhost:8080/bareos-webui
```
Director:localhost-dir

Usuario: admin

Contraseña: ThisIsMySecretUIp4ssw0rd

Agradecimientos a Jandrada por sus recondaciones y consejos.
y a barcus promotor del proyecto sobre el que me he basado para llevar a cabo dicho compose.
