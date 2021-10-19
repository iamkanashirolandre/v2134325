# v2134325

INSTALAÇÃO DO DOCKER NO UBUNTU

Fonte: https://docs.docker.com/engine/install/ubuntu/ 
# remover instalações anteriores 
$ sudo apt-get remove docker docker-engine docker.io containerd runc 

# instalar do repositório (opção mais recomendada) 
$ sudo apt-get update 

# instalar os pacotes que permitem usar apt via https 
$ sudo apt-get install \ apt-transport-https \ ca-certificates \ curl \ gnupg \ lsb-release 

# adicionar a chave GPG do Docker 
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg 

# adicionar o repositório do Docker ao sources list do apt 
$ echo \ "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null 


# atualizar o apt e instalar o Docker 
$ sudo apt-get update $ sudo apt-get install docker-ce docker-ce-cli containerd.io 

# verificar se está funcionando 
$ sudo docker run hello-world 

Caso seja necessário instalar um versão específica do Docker: 
# mostrar versões disponíveis 
$ apt-cache madison docker-ce 

# instalar a versão desejada 
$ sudo apt-get install docker-ce= docker-ce-cli= containerd.io Instalação do Docker no POP_OS 


5 de outubro de 2021 10:43 Página 1 de Docker 
