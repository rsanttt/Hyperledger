# Manual funcionamiento Hyperledger Composer e Hyperledger Explorer

Una vez instalado Hyperledger Composer desde el manual de su propia página 
(https://hyperledger.github.io/composer/latest/installing/installing-index.html)

clonamos el repositorio de https://github.com/rsanttt/blockchain-explorer

`git clone https://github.com/rsanttt/blockchain-explorer.git`

Una vez descargado nos movemos a la carpeta donde lo hemos descargado

`cd blockchain-explorer`

y nos movemos a la version v0.3.5 con el siguiente comando

`git checkout v0.3.5`

ahora procederemos a configurar la base de datos

`cd blockchain-explorer/app/persistence/fabric/postgreSQL`

`sudo chmod -R 775 db`

`cd db/`

`sudo -u postgres ./createdb.sh`

nos pedirá nuestras credenciales y aceptamos
una vez hecho, iniciamos la base de datos y abrimos otra terminal sin cerrar esta
para iniciar la base de datos, desde la misma ruta utilizaremos el siguiente comando

`sudo -u postgres psql`

Ahora, ya en una nueva terminal, procederemos a la instalación

- `cd blockchain-explorer`
- `npm install`
- `cd blockchain-explorer/app/test`
- `npm install`
- `npm run test`
- `cd ..`
- `cd ..`
- `cd client/`
- `npm install`
- `npm test -- -u --coverage`
- `npm run build`

Con esto habremos finalizado la instalación. Ahora, solo nos quedaría lanzarlo desde el directorio principal:

`cd blockchain-explorer`
`./start.sh`

Con esto, ya podremos ir a un navegador a la ruta localhost:8080 y tendremos nuestro Hyperledger Explorer corriendo
Si queremos modificar el puerto donde se lanza, tendremos que modificar el fichero "appconfig.json"


# Configuración integración explorer-composer

Para que nos funcione con la instalación del manual del composer tendremos que cambiar el puerto donde se ejecuta el explorer porque composer también se ejecuta en el puerto 8080 y, aparte, también tendremos que modificar el fichero "config.json" de la carpeta "blockchain-explorer/app/platform/fabric".

En este mismo repositorio se ha subido el config.json, así que solo tendremos que clonarlo y sustituirlo por el que viene por defecto en el explorer




