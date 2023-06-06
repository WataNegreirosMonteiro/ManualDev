# Manual de Configuração do Ambiente de Desenvolvimento com Docker

Este manual fornece um guia passo a passo para configurar uma máquina para o desenvolvimento usando Docker. Ele inclui desde a instalação do Docker até o teste de funcionamento. Siga as instruções abaixo:

## 1. Instalação do Docker

### Passo 1: Verifique os requisitos do sistema
Certifique-se de que sua máquina atenda aos requisitos mínimos de sistema para a instalação do Docker. Verifique a documentação oficial do Docker para obter detalhes sobre os requisitos de sistema.

### Passo 2: Baixe o Docker
Faça o download da versão mais recente do Docker para o seu sistema operacional a partir do site oficial do Docker: [https://www.docker.com/get-docker](https://www.docker.com/get-docker).

### Passo 3: Instale o Docker
Siga as instruções específicas para o seu sistema operacional para instalar o Docker.

## 2. Configuração do Docker

### Passo 1: Verifique a instalação
Após a instalação, verifique se o Docker foi instalado corretamente. Abra o terminal e execute o seguinte comando:
```bash
docker --version
```
Isso deve exibir a versão do Docker instalada.

### Passo 2: Verifique a configuração
Execute o seguinte comando para verificar se o Docker está sendo executado corretamente:
```bash
docker run hello-world
```
Isso baixará uma imagem de teste e a executará em um contêiner. Se o Docker estiver configurado corretamente, você verá uma mensagem de saudação indicando que o Docker está em execução.

## 3. Configuração Adicional (opcional)

### Passo 1: Configuração de permissões (Linux)
Se você estiver usando Linux, pode ser necessário adicionar seu usuário ao grupo "docker" para executar comandos Docker sem a necessidade de usar o "sudo". Execute os seguintes comandos no terminal:
```bash
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```
Faça logout e faça login novamente para que as alterações tenham efeito.

## 4. Teste de Funcionamento

### Passo 1: Crie um contêiner de teste
Para garantir que o Docker esteja funcionando corretamente, vamos criar um contêiner de teste. No terminal, execute o seguinte comando:
```bash
docker run -it --rm ubuntu /bin/bash
```
Isso criará um contêiner do Ubuntu e abrirá um shell dentro dele.

### Passo 2: Execute comandos dentro do contêiner
Dentro do contêiner, execute alguns comandos básicos para verificar se tudo está funcionando corretamente. Por exemplo, você pode executar o seguinte comando:
```bash
ls /
```
Isso listará o conteúdo do diretório raiz do contêiner.

### Passo 3: Saia do contêiner
Para sair do contêiner, digite o seguinte comando:
```bash
exit
```
Isso o levará de volta ao prompt de comando do seu sistema.
