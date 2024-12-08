# Configuração do Projeto

Este sistema foi desenvolvido com uma arquitetura de microsserviços, composta por quatro repositórios principais, cada um com um propósito específico:

- **Front-End**: Interface gráfica do usuário, permitindo acesso e interação com as funcionalidades do sistema.
- **API de Usuários**: Responsável pela gestão de dados de usuários, incluindo autenticação e controle de acessos.
- **API de Benefícios**: Gerencia informações relacionadas a benefícios, como cadastros.
- **API de Financeiro**: Gerencia informações relacionadas aos trâmites financeiros, como geração de relatórios de gastos.

Esta página foi criada para facilitar a configuração e execução do projeto localmente. Cada seção fornece instruções detalhadas para rodar cada repositório, incluindo:

- **Pré-requisitos**: Ferramentas e dependências necessárias.
- **Configuração**: Passos para instalar dependências, configurar variáveis de ambiente e preparar o ambiente local.
- **Execução**: Comandos e dicas para iniciar o serviço e verificar se ele está funcionando corretamente.

## **Pré-requisitos**

Antes de iniciar a configuração do projeto localmente, certifique-se de que os seguintes pré-requisitos estão instalados em sua máquina:

### **1. Git**
O Git é essencial para clonar os repositórios e gerenciar o controle de versão do código.

- **Instalação**:
  - No Windows: [Baixe aqui](https://git-scm.com/download/win) e siga as instruções do instalador.
  - No macOS: Utilize o Homebrew com o comando:
    ```bash
    brew install git
    ```
  - No Linux (Debian/Ubuntu):
    ```bash
    sudo apt update && sudo apt install git
    ```
- **Verificação da instalação**:
    ```bash
    git --version
    ```

### **2. Docker**
O Docker é usado para criar, gerenciar e executar containers, que são essenciais para rodar os microsserviços de maneira isolada.

- **Instalação**:
  - Acesse [Docker Desktop](https://www.docker.com/products/docker-desktop/) e siga as instruções de instalação.
  - No Linux:
    ```bash
    sudo apt update
    sudo apt install docker.io
    ```
- **Verificação da instalação**:
    ```bash
    docker --version
    ```

### **3. Docker Compose**
O Docker Compose facilita o gerenciamento de múltiplos containers.

- **Instalação**:
  - Docker Compose geralmente vem incluso no Docker Desktop.
  - Caso seja necessário instalar manualmente, siga as instruções da [documentação oficial](https://docs.docker.com/compose/install/).
  - No Linux:
    ```bash
    sudo curl -L "https://github.com/docker/compose/releases/download/$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep 'tag_name' | cut -d '"' -f4)/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    sudo chmod +x /usr/local/bin/docker-compose
    ```
- **Verificação da instalação**:
    ```bash
    docker-compose --version
    ```

### **4. Node.js**
O Node.js é necessário para executar scripts JavaScript no lado do servidor e instalar dependências do Front-End.

- **Instalação**:
  - Baixe a versão LTS do [site oficial](https://nodejs.org/).
  - No macOS/Linux, use o nvm (Node Version Manager):
    ```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
    source ~/.bashrc
    nvm install --lts
    ```
- **Verificação da instalação**:
    ```bash
    node --version
    npm --version
    ```

## **Configuração**

Após garantir que os pré-requisitos estão atendidos, siga os passos abaixo para configurar o projeto localmente:

### **1. Clonar os repositórios**
O projeto é composto por quatro repositórios principais. Clone cada um deles utilizando os comandos abaixo:

- **Front-End**:
    ```
      git clone https://github.com/fga-eps-mds/2024.2-SENTINELA-FRONT.git
    ```
- **API de Usuários**:
    ```
      git clone https://github.com/fga-eps-mds/2024.2-SENTINELA-BACKEND-USUARIOS.git
    ```
- **API de Benefícios**:
    ```
      git clone https://github.com/fga-eps-mds/2024.2-SENTINELA-BACKEND-BENEFICIOS.git
    ```
- **API de Financeiro**:
    ```
      git clone https://github.com/fga-eps-mds/2024.2-SENTINELA-BACKEND-FINANCEIRO.git
    ```

Após clonar os repositórios, navegue até cada pasta para continuar a configuração.

### **2. Configurar as variáveis de ambiente**
Os repositórios de [Usuários](https://github.com/fga-eps-mds/2024.2-SENTINELA-BACKEND-USUARIOS.git), [Benefícios](https://github.com/fga-eps-mds/2024.2-SENTINELA-BACKEND-BENEFICIOS.git) e [Financeiro](https://github.com/fga-eps-mds/2024.2-SENTINELA-BACKEND-FINANCEIRO.git) requerem um arquivo `.env` com as variáveis de ambiente necessárias para o funcionamento do projeto.

1. Crie um arquivo `.env` em cada um dos repositórios, seguindo esse modelo:

```bash
  MONGO_URI=
  MONGO_INITDB_ROOT_USERNAME=
  NODE_ENV=
  MONGO_INITDB_ROOT_PASSWORD=
  DB_HOST=
  PORT=
```

### **3. Instale as dependências no front**
No repositório de front end não precisamos configurar as variáveis de ambiente, mas devemos instalar as dependências do projeto. Para fazer isso, basta entrar na pasta raiz do projeto e rodar o comando:

  ```
    npm install
  ```

## Execução

Para conseguir rodar o projeto em sua totalidade localmente, você deverá rodar os repositórios de [Usuários](https://github.com/fga-eps-mds/2024.2-SENTINELA-BACKEND-USUARIOS.git), [Benefícios](https://github.com/fga-eps-mds/2024.2-SENTINELA-BACKEND-BENEFICIOS.git) e [Financeiro](https://github.com/fga-eps-mds/2024.2-SENTINELA-BACKEND-FINANCEIRO.git) usando docker e o repositório de [Front-End](https://github.com/fga-eps-mds/2024.2-SENTINELA-FRONT.git) usando o npm.

### 1. Rodando os repositórios de back-end

Para cada um dos repositórios de back-end, entre na pasta raiz e execute:

```
  docker-compose up --build
```

Se você estiver usando o Docker Desktop, será necessário inicializá-lo primeiro.

### 2. Rodando o repositório de front-end

Para o repositório de front-end, é necessário executar o comando:

```
  npm run dev
```

Seguindo esses passos você será capaz de rodar o projeto Sentinelas localmente!

### **Histórico de Versões**

| **Versão** | **Nome da Versão**      | **Data**      | **Responsável**         | **Descrição/Alterações**                                 |
|------------|-------------------------|---------------|-------------------------|----------------------------------------------------------|
|   1.0      | Criação do documento    | 07/12/2024    | Clara Marcelino         | Criação do documento de configuração do projeto          |
