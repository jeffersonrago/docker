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
Com isso o usuário adicionado terá o mesmo privilégio do usuário ROOT em oprações relacionadas ao docker.


