# Configuração do Ambiente de Desenvolvimento com Docker

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

# Criação de Projeto Laravel

Este manual fornece um guia passo a passo para criar um projeto Laravel. Ele abrange desde a instalação do Laravel até a configuração inicial do projeto. Siga as instruções abaixo:

## 1. Instalação do Laravel

### Passo 1: Verifique os requisitos do sistema
Certifique-se de que sua máquina atenda aos requisitos mínimos de sistema para a instalação do Laravel. Verifique a documentação oficial do Laravel para obter detalhes sobre os requisitos de sistema.

### Passo 2: Instale o Composer
O Laravel usa o Composer como gerenciador de dependências. Certifique-se de que o Composer esteja instalado em sua máquina. Faça o download e instale o Composer a partir do site oficial: [https://getcomposer.org/](https://getcomposer.org/).

### Passo 3: Crie um novo projeto Laravel
Abra o terminal e navegue até o diretório onde deseja criar o projeto Laravel. Em seguida, execute o seguinte comando para criar um novo projeto Laravel:
```bash
composer create-project --prefer-dist laravel/laravel nome-do-projeto
```
Substitua "nome-do-projeto" pelo nome que deseja dar ao seu projeto.

### Passo 4: Acesse o diretório do projeto
Navegue até o diretório do projeto recém-criado usando o seguinte comando:
```bash
cd nome-do-projeto
```

## 2. Configuração do Projeto Laravel

### Passo 1: Configuração do arquivo .env
O Laravel usa o arquivo `.env` para armazenar as configurações específicas do ambiente. Faça uma cópia do arquivo `.env.example` e renomeie-a para `.env` usando o seguinte comando:
```bash
cp .env.example .env
```

Em seguida, gere uma nova chave de aplicativo usando o comando:
```bash
php artisan key:generate
```
Isso definirá uma chave de criptografia para seu aplicativo Laravel.

### Passo 2: Configuração do banco de dados
No arquivo `.env`, configure as variáveis relacionadas ao banco de dados de acordo com as configurações do seu ambiente. Certifique-se de definir corretamente as variáveis `DB_HOST`, `DB_PORT`, `DB_DATABASE`, `DB_USERNAME` e `DB_PASSWORD`.

### Passo 3: Migrações do banco de dados (opcional)
Se você planeja usar um banco de dados com seu projeto Laravel, pode executar as migrações do banco de dados para criar as tabelas necessárias. Use o seguinte comando:
```bash
php artisan migrate
```
Isso executará todas as migrações pendentes.

## 3. Teste de Funcionamento

### Passo 1: Execute o servidor embutido do Laravel
Para testar se seu projeto Laravel está funcionando corretamente, execute o seguinte comando para iniciar o servidor embutido do Laravel:
```bash
php artisan serve
```
Isso iniciará o servidor na porta padrão 8000.

### Passo 2: Acesse o aplicativo no navegador
Abra um navegador da web e acesse `http://localhost:8000` (ou a porta em que o servidor está sendo executado). Se você vir a página inicial do Laravel, isso significa que o projeto foi criado corretamente e está funcionando.

Parabéns! Você concl
