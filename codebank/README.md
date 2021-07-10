[<img src="../img/go.svg" width="72"/>](Golang)

# Imersão Full Stack & FullCycle 3.0 - Codebank - Back-end dos pagamentos

## Descrição

Repositório do back-end dos pagamentos (Code Bank) feito com Golang

**Importante**: A aplicação do Apache Kafka, Postgres(db) deve estar rodando primeiro.

## Rodar a aplicação

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

Para testar execute os comandos:

```
docker exec -it CONTAINER_ID sh
evans -r repl -p 50052
call Payment
```
