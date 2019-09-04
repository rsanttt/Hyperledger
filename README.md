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
