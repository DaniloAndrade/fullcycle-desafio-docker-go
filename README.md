
# Desafio Go

> Esse desafio é muito empolgante principalmente se você nunca trabalhou com a linguagem Go!
> Você terá que publicar uma imagem no docker hub. Quando executarmos:
>
> docker run <seu-user>/codeeducation
> 
> Temos que ter o seguinte resultado: Code.education Rocks!
> 
> Se você perceber, essa imagem apenas realiza um print da mensagem como resultado final, logo, vale a pena dar uma conferida no próprio site da Go Lang para aprender como fazer um "olá mundo".
> 
> Lembrando que a Go Lang possui imagens oficiais prontas, vale a pena consultar o Docker Hub.
> 
> 3) A imagem de nosso projeto Go precisa ter menos de 2MB =)
> 
> Dica: No vídeo de introdução sobre o Docker quando falamos sobre o sistema de arquivos em camadas, apresento uma imagem "raiz", talvez seja uma boa utilizá-la.


## Como buildar

```bash

docker build -t <seu usuário dockerhub>/fullcycle-desafio-go:latest . -f Dockerfile.prod

```

## Enviando imagem para o docker hub

```bash

docker login
Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.
Username: <username>
Password: 
Login Succeeded

Logging in with your password grants your terminal complete access to your account. 
For better security, log in with a limited-privilege personal access token. Learn more at https://docs.docker.com/go/access-token

```

```bash

docker push <seu usuário dockerhub>/fullcycle-desafio-go:latest 

```

## Como executar

```bash

docker pull daniloandrade/fullcycle-desafio-go

docker run -it --rm --name desafio-go daniloandrade/fullcycle-desafio-go 

```

## Como ver o tamanho da imagem

```bash

docker images

REPOSITORY                           TAG       IMAGE ID       CREATED        SIZE
daniloandrade/fullcycle-desafio-go   latest    74d842b82600   16 hours ago   1.75MB

```
...
