# Reverse Proxy e web server
Semplice prova di un sito Web servito attraverso un reverse proxy NGINX cofigurato anche per certificati ssl.

Il web server e NGINX sono eseguiti su due container docker distinti chiamati rispettivamente "webserver" e "reverseproxy"


# Istruzioni per l'uso:

dopo aver scaricato il repository in locale con

`git clone git@github.com:naddi96/NGNX-reverse-proxy-docker-configuration.git`

tutti i comandi vanno eseguiti nella root del progetto potrebbero richiedere il sudo 
per avviare entrambi basta eseguire

`docker-compose up -d`

mentre se si vuole stoppare ma non cancellare i due container

`docker-compose stop`

se si vuole stoppare e cancellare i container

`docker-compose down`

per generare un altro certificato autogenerato

`openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-config-cert/cert.key -out nginx-config-cert/cert.crt`

