# Arquitetura

## Visão Geral

O sistema foi projetado com uma arquitetura baseada em microsserviços, dividida em uma interface principal que interage com três serviços especializados: Usuários, Financeiro e Benefícios. Cada microsserviço é responsável por uma área funcional específica e estabelece comunicação de forma segura e assíncrona por meio de APIs. Essas APIs servem como ponto de integração, permitindo que a interface principal e os demais microsserviços realizem operações de maneira eficiente e independente.

Essa abordagem modular, com cada microsserviço gerenciando seu próprio banco de dados, possibilita escalabilidade individual dos componentes. Isso significa que melhorias, correções ou atualizações em um serviço podem ser feitas sem impactar diretamente os outros, tornando a arquitetura flexível e adaptável às necessidades do sistema.

Nesse documento será apresentado a arquitetura do projeto e, por não haver nenhuma mudança na arquitetura em relação ao semestre de 2024.1, iremos manter os mesmos diagramas.

## Diagrama de relações dos microsserviços, tecnologias e dispositivos

<img src="https://raw.githubusercontent.com/fga-eps-mds/2024.2-SENTINELA-DOC/main/docs/assets/Diagrama.png">

## Estrutura da Arquitetura

### Interface do Sistema

A interface funciona como o ponto principal de interação entre os usuários e o sistema. Essa camada desempenha papéis cruciais, como:

- **Gestão de Requisições**: Recebe e valida todas as solicitações enviadas pelos usuários ou sistemas externos.
- **Controle de Acesso**: Implementa autenticação e autorização, garantindo a segurança e o acesso restrito às funcionalidades do sistema.
- **Coordenação de Processos**: Gerencia as interações entre os microsserviços, consolidando as respostas para que sejam apresentadas ao usuário de forma clara e integrada.

### Microsserviços Especializados

#### Microsserviço de Usuários
Este serviço é responsável pela administração das informações dos usuários do sistema. Ele mantém um banco de dados dedicado, onde são armazenados detalhes como perfis, credenciais e outras informações relevantes.

#### Microsserviço Financeiro
O serviço financeiro lida com a gestão de todas as operações e transações financeiras do sistema. Seu banco de dados é especializado em armazenar informações como históricos de pagamentos, contas e dados de fornecedores.

#### Microsserviço de Benefícios
Responsável pela gestão dos benefícios e convênios oferecidos, este microsserviço organiza os dados relativos aos benefícios disponíveis no sistema. Seu banco de dados é estruturado para armazenar informações detalhadas sobre as ofertas acessíveis aos usuários.

### Ferramentas e Tecnologias

#### React com ViteJS
O frontend é desenvolvido com React, uma biblioteca que possibilita a criação de interfaces dinâmicas e moduladas. A integração com o ViteJS proporciona um ambiente de desenvolvimento mais rápido e eficiente, com suporte para ESModules e atualizações instantâneas. Essa combinação resulta em uma interface moderna e responsiva, garantindo uma experiência fluida para o usuário.

#### Node.js
No backend, o Node.js é utilizado por sua capacidade de executar código assíncrono e não bloqueante, ideal para gerenciar múltiplas requisições simultâneas. Sua compatibilidade com diversas plataformas e a extensa biblioteca de pacotes NPM tornam o desenvolvimento rápido e flexível.

#### Express
Para organizar as APIs do backend, o Express é empregado como framework. Ele facilita a construção de rotas, middlewares e APIs RESTful, proporcionando uma camada robusta e eficiente para comunicação entre o frontend, banco de dados e os diferentes microsserviços.

#### MongoDB
O MongoDB, um banco de dados NoSQL, é usado para armazenar os dados do sistema. Sua estrutura baseada em documentos JSON permite uma manipulação direta e flexível dos dados, adaptando-se facilmente ao crescimento e à complexidade das informações exigidas pelo projeto.

#### Mongoose
O Mongoose atua como uma camada de abstração sobre o MongoDB, simplificando o gerenciamento de esquemas e interações com o banco de dados. Ele garante a consistência e a validação dos dados antes do armazenamento, contribuindo para a organização e segurança do backend.

### Benefícios da Arquitetura
Essa abordagem modular, com componentes separados e especializados, permite maior escalabilidade e flexibilidade. A comunicação entre os serviços ocorre de forma eficiente, enquanto a independência de cada microsserviço assegura que alterações ou problemas em uma parte do sistema não impactem o restante.

## Estrutura Lógica do Sistema

### Organização de Pacotes

#### Estrutura de Pastas do Frontend

**Diagrama Ilustrativo**

<img src="https://raw.githubusercontent.com/fga-eps-mds/2024.2-SENTINELA-DOC/main/docs/assets/diagrama-pacotes-front.png">

Os principais diretórios e suas funções no frontend são:

- **src**: Diretório raiz que contém todo o código-fonte do projeto.
- **Components**: Local onde ficam os componentes reutilizáveis da aplicação. Esses componentes encapsulam a lógica e o estilo de pedaços da interface que podem ser usados em diferentes partes do projeto.
- **Pages**: Contém os componentes que representam as páginas da aplicação. Cada página funciona como um grande componente que agrupa outros menores.
- **Service**: Reúne a lógica de negócios, como requisições a APIs e manipulação de dados.
- **Context**: Define o contexto global do projeto, usado para gerenciar estados compartilhados sem a necessidade de passar propriedades manualmente entre componentes.
- **Utils**: Contém funções utilitárias para tarefas como formatação, validação e outras operações comuns.
- **Assets**: Armazena arquivos estáticos como imagens, fontes e ícones.
- **App**: O componente raiz do projeto, responsável por organizar e renderizar toda a estrutura da aplicação.

#### Estrutura de Pastas do Backend

**Diagrama Ilustrativo**  
<img src="https://raw.githubusercontent.com/fga-eps-mds/2024.2-SENTINELA-DOC/main/docs/assets/diagrama-pacotes-back.png">

Os principais diretórios do backend são:

- **src**: Diretório raiz que abriga todo o código do servidor.
- **Controllers**: Implementa a lógica de negócios para os diferentes recursos (usuários, produtos, etc.). Cada controlador define métodos específicos que são expostos como endpoints da API. Exemplo: Um controlador de usuários pode conter métodos como `createUser`, `getUserById`, e `updateUser`.
- **Models**: Define as estruturas de dados da aplicação, mapeando para tabelas ou documentos no banco de dados.
- **Utils**: Inclui funções auxiliares para tarefas comuns, como envio de e-mails, geração de tokens ou validações específicas.
- **Routes**: Configura as rotas disponíveis na aplicação. Cada rota é associada a um controlador e a métodos específicos.
- **index.js**: Arquivo principal que inicia o servidor, configura o Express e conecta os serviços.

### Representação Lógica de Dados (DLD)

O Diagrama Lógico de Dados (DLD) detalha a organização das informações no banco de dados, mostrando como elas estão estruturadas e suas relações. Essa abordagem facilita a recuperação e a manipulação dos dados de maneira eficiente. Abaixo, os DLDs de cada microsserviço:

#### Microsserviço de Usuários

**Diagrama Representativo**
<img src="https://raw.githubusercontent.com/fga-eps-mds/2024.2-SENTINELA-DOC/main/docs/assets/diagrama-conceitual-usuarios.png">

O Diagrama Lógico de Dados (DLD) do microsserviço de usuários ilustra as principais entidades e relações que compõem o sistema. A entidade central é o **User**, que armazena informações fundamentais, como identificador único (`id`), e-mail, telefone, senha, nome, função (*role*) e status. Cada usuário está associado a uma **Role**, que define suas permissões e responsabilidades no sistema, estabelecendo uma relação de cardinalidade (1,1) entre essas entidades. Além disso, a entidade **Membership** conecta usuários a seus registros específicos, contendo informações como CPF, RG, sexo e data de nascimento. O diagrama também inclui dependências do usuário, representadas pela entidade **Dependent**, que armazena dados relacionados a parentes ou pessoas associadas, como nome completo, CPF, parentesco e data de nascimento. Por fim, a estrutura organiza usuários em **Lotação**, que, por sua vez, estão relacionadas a **Órgãos**, refletindo a hierarquia e alocação organizacional.

#### Microsserviço Financeiro

**Diagrama Representativo**  
<img src="https://raw.githubusercontent.com/fga-eps-mds/2024.2-SENTINELA-DOC/main/docs/assets/diagrama-conceitual-financas.png">

O Diagrama Lógico de Dados (DLD) do microsserviço de finanças representa as entidades e relações essenciais para o gerenciamento de movimentações financeiras e fornecedores. A entidade central, **financialMovement**, registra as transações financeiras, incluindo informações como CPF/CNPJ, tipo de documento, nomes de origem e destino, e as contas envolvidas na operação (conta de origem e conta de destino). Esta entidade está diretamente relacionada às entidades **supplier** e **bankAccount**.

A entidade **supplier** armazena informações de fornecedores, como cidade, CEP, chave Pix, telefone, e-mail e natureza da transação, além de dados específicos de identificação, como CPF/CNPJ e tipo de pessoa. Já a entidade **bankAccount** organiza os detalhes das contas bancárias, incluindo nome do banco, número da conta, tipo, agência, dígito verificador (DV), status da conta e se possui chave Pix.

#### Microsserviço de Benefícios

**Diagrama Representativo**  
<img src="https://raw.githubusercontent.com/fga-eps-mds/2024.2-SENTINELA-DOC/main/docs/assets/diagrama-conceitual-beneficios.png">

O Diagrama Lógico de Dados (DLD) do microsserviço de benefícios descreve a estrutura da entidade **Benefits**, que centraliza as informações relacionadas aos benefícios oferecidos. Cada benefício é identificado por um **id** único e inclui detalhes importantes, como:

- **nome** e **descrição**: especificam a identidade e informações detalhadas sobre o benefício.
- **teleCelular** e **site**: fornecem dados de contato e acesso relacionados ao benefício.
- **categoria**: classifica o tipo de benefício.
- **cpfCnpj** e **tipoPessoa**: identificam o responsável ou a organização que oferece o benefício, permitindo distinção entre pessoa física e jurídica.
- **ans**: referência a dados específicos de regulamentação (como benefícios relacionados à saúde).
- **contratoSit**: indica o status contratual do benefício.
- **razaoSocial** e **logotipo**: fornecem a identidade visual e jurídica da entidade responsável.

# Visões do Sistema: Implantação

## Visão Geral

A visão de implantação do sistema se concentra nos aspectos relacionados à gestão de configuração, contemplando como o sistema é organizado para garantir uma operação estável e escalável. Com a arquitetura baseada em microsserviços, cada componente do sistema é independente e gerenciado de maneira individualizada, o que facilita a adaptação e evolução das partes do sistema sem impactar os demais serviços.

A implantação é feita de forma a garantir que cada microsserviço esteja em constante sincronização com as suas dependências, de forma segura e eficiente. A gestão de configuração visa assegurar que as versões de cada serviço estejam atualizadas, além de permitir um controle rigoroso sobre os ambientes de desenvolvimento, teste e produção.

## Gerenciamento de Configuração

### Ferramentas de Gestão de Configuração

A gestão de configuração é crucial para manter a integridade e a consistência do sistema, especialmente considerando que ele é composto por diversos microsserviços independentes. As ferramentas de gestão de configuração utilizadas no projeto incluem:

- **Git**: Para controle de versão de código, permitindo o acompanhamento de mudanças e a colaboração entre equipes.
- **Docker**: Para a criação de containers que encapsulam os microsserviços e suas dependências, garantindo que o ambiente de execução seja o mesmo em todas as etapas de desenvolvimento, teste e produção.
- **CI/CD**: O processo de integração contínua e entrega contínua é implementado utilizando ferramentas como Jenkins, GitHub Actions ou GitLab CI, que garantem a automação de testes e deploys.

### Controle de Versões

Para garantir que o sistema funcione de maneira harmoniosa, é fundamental o controle adequado das versões dos microsserviços. Cada serviço tem sua própria versão, e o controle de versões é feito da seguinte maneira:

- **Versionamento Semântico**: Cada microsserviço segue o versionamento semântico (SemVer), com a incrementação de versões maiores, menores e de patch dependendo das mudanças feitas.
- **Gerenciamento de Dependências**: As dependências entre microsserviços são controladas e gerenciadas por meio de arquivos de configuração, como `package.json` para o backend Node.js e `docker-compose.yml` para a configuração dos containers Docker.

### Monitoramento e Manutenção

Além de garantir a implantação do sistema, o gerenciamento de configuração também abrange o monitoramento da infraestrutura e a manutenção contínua dos serviços:

- **Monitoramento**: Ferramentas como Prometheus, Grafana e ELK Stack (Elasticsearch, Logstash e Kibana) são utilizadas para monitoramento em tempo real dos microsserviços e coleta de logs.
- **Alertas**: Configuração de alertas automáticos para identificar falhas ou degradações de performance, utilizando serviços como PagerDuty ou Slack.
- **Backup e Recuperação**: Processos automáticos de backup e recuperação de dados são configurados para garantir a integridade do sistema e a continuidade dos serviços.

## Estratégia de Implantação

A implantação do sistema é realizada de forma gradual e controlada. A cada nova versão de microsserviço, é feito um processo de teste em ambiente de staging antes de ser promovido para produção. O uso de containers Docker facilita a automação de deploys e o rollback caso haja falhas.

A visão de implantação foca no gerenciamento de configuração, assegurando que o sistema seja implantado de maneira eficiente, segura e escalável. Com o uso de ferramentas e processos como Docker, CI/CD, e monitoramento contínuo, garantimos a consistência e integridade do sistema durante todo o seu ciclo de vida.

A estratégia de implantação inclui:

1. **Criação e Testes Locais**: Cada desenvolvedor trabalha localmente com containers Docker para testar suas alterações.
2. **Deploy em Ambiente de Staging**: Após os testes locais, a versão é promovida para o ambiente de staging, onde realiza-se mais testes de integração.
3. **Deploy em Produção**: Após aprovação em staging, o deploy é realizado em produção utilizando Kubernetes para gerenciar os microsserviços.
4. **Monitoramento Pós-Deploy**: Após o deploy, a equipe de operações monitora o comportamento do sistema, ajustando configurações e realizando manutenção contínua conforme necessário.



### Referências

- AMAZON AWS. *O que são microsserviços?*. Disponível em: [https://aws.amazon.com/pt/microservices/](https://aws.amazon.com/pt/microservices/).  

- Arquitetura - 2024.1 - SENTINELA. Disponível em: <https://fga-eps-mds.github.io/2024.1-SENTINELA-DOC/gestao/arquitetura/>. Acesso em: 9 dez. 2024.

- Compreender Estratégias de Implantação. Disponível em: <https://docs.oracle.com/pt-br/solutions/plan-mad-strats-devops/understand-depoyment-architectures.html#GUID-D0B793EE-1E28-42F5-BCCB-9E1465E85886> Acesso em: 9 FEV. 2025.

### **Histórico de Versões**

| **Versão** | **Nome da Versão**      | **Data**      | **Responsável**         | **Descrição/Alterações**                                 |
|------------|-------------------------|---------------|-------------------------|----------------------------------------------------------|
|   1.0      | Criação do documento    | 08/12/2024    | Clara Marcelino         | Criação do documento                                     |
|   2.0      | Atualização do documento    | 09/02/2025    | Daniela Soares        | Atualização do documento                                     |