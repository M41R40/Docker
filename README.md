# Oque é Docker ?

É uma plataforma aberta para desenvolvimento, envio e execução de aplicativos, permitindo que separe seus softwares de forma rápida.

## Arquitetura Docker.

Usa um sistema tipo cliente-servidor, onde o cliente se comunica com o *daemon* Docker, que constroi, executa e distribui seus *contêiners* Docker, que se conecta utilizando uma API REST.

- **Daemon Docker** : Escuta as solicitações da API, gerencia imagens, contêiners, redes e volumes. 

- **Contêiners** : é uma instância executavel de uma imagem, isolado, controlavel, gerenciavel, quando um *contêiner* é removido todas as alterações em seu estado de armazenamento são excluidos. 
 
 - **Docker Compose** : É o cliente do Docker que permite trabalhar com varios aplicativos juntos com vários contêineres. 


# Instalação e configuração do Docker. 

Recomenda-se que instale dessa forma em um sistema operacional como o ubuntu ou Debian, para windows e macos há versões Desktop próprias. 

```html
https://www.docker.com/get-started
```

Atualize o sistema com o comando:

```bash
sudo apt-get update
```

Instale os requisitos necessários com o comando:

```bash 
sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common -y
```

Baixe a chave GPG para a instalação do Docker com o comando:

```bash 
curl -fsSL https://download.docker.com/linux/$(. /etc/os-release; echo "$ID")/gpg | sudo apt-key add -
```

Verifique a chave e sua assinatura com o comando:

```bash 
apt-key fingerprint 0EBFCD88
```

Adicionando o docker ao repositorio do sistema:

```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/$(. /etc/os-release; echo "$ID") $(lsb_release -cs) stable"
```

Atualize novamente o sistema com o comando:

```bash
sudo apt-get update
```

Pesquise pelo Docker no repositorio com o comando:

```bash 
sudo apt-cache search docker-ce
```

Realize a instalação do Docker com o comando:

```bash 
sudo apt-get install docker-ce -y
```

Instale tambem o Docker compose com o comando:

```bash
sudo apt-get install docker-compose -y
```

Pronto, para verificar a instalação use o comando:

```bash
docker -v
```

![](./imagens/-v.png)


Todos esses comandos estão prontos em um script montado pelo Greenmind em seu git, de onde tambem eu tirei todos esses comandos e o principal inspirador para eu estudar docker.  :green_heart:

Use o comando para baixar o script dele caso não queira fazer comando por comando como à cima:

```bash 
wget https://gist.githubusercontent.com/greenmind-sec/e191481b4fa6ab33b3ed1250e9aaf66a/raw/c701da9ec1b8bb65038c80d55b972598c21058af/install-docker.sh
```

Lembre-se de dar permissão de execução tambem:

```bash 
chmod +x install-docker.sh
```

E execute o script com o comando:

```bash
sudo ./install-docker.sh
```

> Não faça duas instalações, pode dar problemas.


# Criando uma pilha LAMP com o Docker Compose

Vamos relembrar oque é LAMP ? :raised_hands: :raised_hands: :raised_hands: :raised_hands: 

**L**inux, **A**pache, **M**ySQL, **P**HP.

Caso você não esteja associado a este assunto, visite meu repositório no meu perfil @M41R40 :ok_woman:

```html
https://github.com/M41R40/Servidor-ubuntu-c-pilha-LAMP---DigitalOcean
```





