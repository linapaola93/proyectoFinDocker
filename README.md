# proyectoFinDocker
docker build -t paolac23/proyecto .

luego, lo ejecutamos con el comando:

docker run -P --name postgres -e USER=foo -e PASSWORD=bar -e :x
SCHEMA=foo -e ENCODING=UTF8 -d paolac23/proyecto

dejandolo con:
USER=foo 
PASSWORD=bar
PORT: 5432
IP:172.17.0.3

Una vez lo ejecutamos ya podemos crear la instancia en postgres para ver la base de datos.
docker run --name linkweb --link postgres:dbpaola -d paolac23/nginx
docker run --rm --link postgres:dbpaola paolac23/nginx env

ejecutamos paola.com
