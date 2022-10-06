## Como rodar o container
```
docker run --name httpd -p 8080:80 httpd:alpine3.15
```

## Comando para copiar o arquivo
```
docker cp httpd:/usr/local/apache2/ /usr/app/apache-bruno/apache2/
```

## Comando para subir meu container bonitinho
```
docker run --name httpd \
-p 8080:80 \
-v /usr/app/apache-bruno/apache2/:/usr/local/apache2/ \
-v /usr/app/apache-bruno/pjbruno/:/var/www/html/pjbruno/ \
httpd:alpine3.15
```

## Limptar os espaço dos arquivos de config
```
cat /etc/apache2/conf/httpd.conf | egrep -v '(#|//|^[[:space:]]*$)'
```
