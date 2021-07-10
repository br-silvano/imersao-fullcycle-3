# Imersão Full Stack & FullCycle 3.0 - Codebank

## Descrição

Repositório do Apache Kafka

## Rodar a aplicação

### Configurar Elasticsearch

```
sudo nano /etc/sysctl.conf
vm.max_map_count=262144
grep vm.max_map_count /etc/sysctl.conf
vm.max_map_count=262144
sudo sysctl -w vm.max_map_count=262144

mkdir es01
sudo chmod g+rwx es01
sudo chgrp 0 es01
```

### Configurar /etc/hosts

A comunicação entre as aplicações se dá de forma direta através da rede da máquina.
Para isto é necessário configurar um endereços que todos os containers Docker consigam acessar.

Acrescente no seu /etc/hosts (para Windows o caminho é C:\Windows\system32\drivers\etc\hosts):
```
127.0.0.1 host.docker.internal
```
Em todos os sistemas operacionais é necessário abrir o programa para editar o *hosts* como Administrator da máquina ou root.

Execute os comandos:

```
docker-compose up
```

Quando parar os containers do Kafka, lembre-se antes de rodar o `docker-compose up`, rodar o `docker-compose down` para limpar o armazenamento, senão lançará erro ao subir novamente.