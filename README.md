# mysql-docker-compose

Até a agora só existe o script de instalação para sistemas baseados em debian (Ubuntu, Xubuntu, etc)
Nesse repositório existem dois arquivos, [docker.sh](docker.sh), um script para instalar o [docker](https://pt.wikipedia.org/wiki/Docker_(software)) e [docker-compose.yml](docker-compose.yml) para instalar o [docker-compose](https://docs.docker.com/compose/)

Execute o arquivo `docker.sh` e finalize a instalação com:
```sh
sh docker.sh
```
Com `docker ps` teste se o script instalou corretamente, ele deve dar um output como:
```sh
$ docker ps  
CONTAINER ID   IMAGE     COMMAND              CREATED       STATUS       PORTS 
```
Se der algum erro, use os comandos abaixo:
```sh
systemctl start docker
systemctl enable docker
systemctl restart docker
```

Agora com o docker e docker-compose instalado, você pode, dentro da pasta que contém o arquivo `docker-compose.yml`, usar o comando para subir o container em modo detached (-d)

```
docker-compose up -d
``` 

Para descer o container, é só usar na pasta com o arquivo `docker-compose.yml` o comando 
```
docker-compose down
```
