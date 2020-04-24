# geoserver-susanna2
Dockerfile per creazione di una immagine di un container di Geoserver (a partire da una immagine appositamente creata con i plugins _WMTS-multi-dimension_ e _Backup&Restore_ installati: 
[Docker Hub: susannagrasso/geoserver](https://hub.docker.com/repository/docker/susannagrasso/geoserver) ) con copia di backup dei dati.

La suddetta immagine è stata creata a partire dall'immagine [Docker Hub:geosolutionsit/geoserver](https://hub.docker.com/r/geosolutionsit/geoserver/) a cui è stata aggiunta l'installazione dei plugin sopra menzionati.

## How to run it
Lanciare il container impostando la cartella dell'host da condividere con il container (dati da condividere con Geoserver):

`docker run -d -v DATADIR_HOST_FOLDER:/var/geoserver/datadir/ --name geoserver-susanna2 -it -p 8080:8080`

Open your browser and point it to:

http://localhost:8080/geoserver

GeoServer web interface will show up:

_User:_ admin
_Pass:_ geoserver
