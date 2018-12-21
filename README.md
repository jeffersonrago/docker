# Criando Lab Docker

## Server
Ubuntu 18.04.1 LTS

## Kernel
4.15.0-39-generic

## Instalando Docker
```
curl -fsSL https://get.docker.com/ | sh
```

## Consultando Versão Instalada

```
docker --version
```

Resultado:
Docker version 18.09.0, build 4d60db4

## Adicionando Usuário Grupo DOCKER

```
sudo usermod -aG docker USER_NAME
```
Com isso o usuário adicionado terá o mesmo privilégio do usuário **ROOT** em oprações relacionadas ao docker.



## Criando o primeiro container

```
docker container run -it --name primeiro_container nginx
```
ou

```
docker container run -d --name primeiro_container_deamon nginx
```
**Parametros**
- t: Disponibiliza um console para acesso do container
- i: Mantém o STDIN aberto mesmo sem que você esteja conectado 
- d: O container fica executando em modo deamon, sem interatividade

## Iniciando/Parando Container

```
docker container start ID_CONTAINER OU NAME_CONTANER
```

Além de iniciar (start) também é possível executar os comandos:

- stop
- restart

## Acessando um Container

```
docker container attach NAME_CONTAINER
```

## Removendo um container

```
docker container rm NAME_CONTAINER
```

O container pode ser excluir tambpém fornecendo o parametro *-f*

```
docker container rm -f --name primeiro_container nginx

``` 

## Listando as Imagens Docker

```
docker image ps
```

Para sair do modo interativo é necessario que preciona
 ```
 CRTL + Q _ P
 ```
 
## Verificar Processamento

```
docker container stats
``` 

É possível indicar também o container que deseja verificar

```
docker container stats NAME_CONTAINER
```

## Verificar o Processo em execução no Container

```
docker container top CONTAINER_ID
```

## Visualizando Log

```
docker logs -f CONTAINER_ID
```

## Limitando Recurso do Container

```
docker container run -it -m 512M --cpus=0.5 teste nginx
```

Além de limitar é possível realizar atualização do recurso

```
docker container update -m 256M --cpus=0.5 teste nginx
```

