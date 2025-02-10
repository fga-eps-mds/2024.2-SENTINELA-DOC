# Planejado x Realizado

## Escopo

Durante o desenvolvimento do projeto, foram planejadas diversas histórias de usuário e melhorias, com o objetivo de atender às necessidades do usuário. A seguir, apresentamos a comparação entre o escopo planejado e o efetivamente entregue.  

### Histórias de Usuário e Melhorias Planejadas  

A tabela abaixo apresenta todas as histórias de usuário e melhorias inicialmente previstas no escopo do projeto, juntamente com seus respectivos pontos de complexidade.  

| **Categoria**                          | **História de Usuário**                                                                                             |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Gerar carteirinha do sindicalizado** | Como afiliado, desejo gerar minha carteira digital com informações pessoais para usá-la como prova de participação. | 
| **Gerar carteira digital de participação do sindicalizado** | Disponibilizar o download da carteirinha do sindicalizado. |
| **Validar status do sindicalizado por QR Code** | Como gestor ou parceiro do sindicato, desejo escanear o QR Code na carteirinha para validar se o afiliado está ativo, garantindo autenticidade. |
| **Exibir os benefícios de ser filiado em uma página pública** | Como um não filiado, desejo visualizar os benefícios da filiação antes de me filiar na página inicial. | 
| **Exibir preços e detalhes dos benefícios para os usuários logados** | Como filiado, desejo visualizar os preços associados a cada benefício de forma detalhada em uma página específica. | 
| **Informação de contato** | Como usuário, desejo encontrar informações de contato do sindicato no rodapé para esclarecer dúvidas ou obter mais informações. | 
| **Melhoria da tela de login** | Como usuário, desejo visualizar as vantagens na página inicial (login) e me informar sobre os benefícios de me filiar ao sindicato. | 
| **Visualizar dados sobre os sindicalizados através de dashboards (melhoria)** | Como administrador, desejo acessar dashboards com informações sobre os sindicalizados (ex.: quantidade por categoria, idade), para ter uma visão geral. |
| | Como administrador, desejo filtrar dados no dashboard (ex.: por data ou localização) para encontrar informações relevantes rapidamente. |
| **Importar extrato do BRB para o sistema e filtrar o relatório de entradas e saídas por mês** | Como administrador, desejo tratar os dados vindos da consulta para inseri-los no banco de dados. |
| | Como administrador, desejo importar dados do BRB para manter o sistema atualizado. |
| | Como administrador, desejo gerar um relatório com base nos dados importados do BRB. |
| **Solicitar benefícios** | Como afiliado, desejo selecionar benefícios dentre uma lista para solicitar vínculo. |
| | Como administrador, desejo ter acesso a todos os benefícios cadastrados e avaliar cada pedido. | 
| **Importar arquivo retorno do BRB** | Como administrador, desejo tratar o arquivo retorno do BRB para importá-lo em nosso banco de dados. |
| | Como administrador, desejo importar o arquivo de retorno tratado no banco de dados. |
| | Como administrador, desejo um relatório com base nesses arquivos retornos. |
| **Gerir patrimônio** | Como administrador, desejo cadastrar, visualizar, editar e deletar os patrimônios. |
| | Como administrador, desejo que haja uma área específica no site para gerir os patrimônios cadastrados. |
| | Como administrador, desejo gerar um relatório com todos os patrimônios cadastrados. |

### Histórias de Usuário e Melhorias Entregues  

A tabela a seguir apresenta as histórias de usuário e melhorias que foram efetivamente entregues ao final do projeto.  

| **Categoria**                          | **História de Usuário**                                                                                             |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Gerar carteirinha do sindicalizado** | Como afiliado, desejo gerar minha carteira digital com informações pessoais para usá-la como prova de participação. | 
| **Gerar carteira digital de participação do sindicalizado** | Disponibilizar o download da carteirinha do sindicalizado. |
| **Validar status do sindicalizado por QR Code** | Como gestor ou parceiro do sindicato, desejo escanear o QR Code na carteirinha para validar se o afiliado está ativo, garantindo autenticidade. |
| **Exibir os benefícios de ser filiado em uma página pública** | Como um não filiado, desejo visualizar os benefícios da filiação antes de me filiar na página inicial. | 
| **Exibir preços e detalhes dos benefícios para os usuários logados** | Como filiado, desejo visualizar os preços associados a cada benefício de forma detalhada em uma página específica. | 
| **Informação de contato** | Como usuário, desejo encontrar informações de contato do sindicato no rodapé para esclarecer dúvidas ou obter mais informações. | 
| **Melhoria da tela de login** | Como usuário, desejo visualizar as vantagens na página inicial (login) e me informar sobre os benefícios de me filiar ao sindicato. | 
| **Visualizar dados sobre os sindicalizados através de dashboards (melhoria)** | Como gestor, desejo visualizar informações detalhadas sobre os sindicalizados e os órgãos, como idade, local de residência e tempo de filiação, para compreender melhor o perfil dos sindicalizados e tomar decisões mais embasadas. |
| | Como administrador, desejo visualizar um gráfico com o uso dos benefícios. |
| **Importar extrato do BRB para o sistema** | Como administrador, desejo importar um arquivo de extrato bancário e salvá-lo no sistema. |
| | Como administrador, desejo selecionar o tipo de documento de cada movimentação financeira que estiver sem esse dado salvo. |
| **Importar arquivo retorno** | Como administrador, desejo importar o arquivo de retorno tratado no banco de dados. |
| | Como administrador, desejo um relatório do arquivo retorno importado. |
| **Gerir patrimônio** | Como administrador, desejo cadastrar, visualizar, editar e deletar os patrimônios. |

### Alterações no Escopo  

Durante o desenvolvimento do projeto, algumas mudanças foram realizadas no escopo com base em reavaliações estratégicas e restrições de tempo.  

As histórias de usuário relacionadas ao épico **"Solicitar benefícios"** foram retiradas do escopo em comum acordo com os Product Owners (POs), uma vez que foi identificado que essas funcionalidades não se encaixavam mais no produto e não agregavam valor imediato ao sindicato.  

Além disso, algumas funcionalidades do épico **"Gerir patrimônio"** não foram entregues, pois, ao analisarmos o **gráfico Earned Value Management (EVM)**, identificamos um atraso no desenvolvimento. Diante disso, concluímos que não seria possível entregar todo o escopo inicialmente planejado dentro do prazo estabelecido. Essas funcionalidades podem ser consideradas para futuras iterações do projeto, caso haja interesse dos stakeholders.  

## Custo

Para consultar a variação do custo planejado x custo real, acesse a página do [EVM](../gestao/EVM.md).

## Tempo

### Releases Planejadas

| Release | Data de entrega |
| ------- | --------------- |
| 1       | 08/12/2024      |
| MVP     | 25/01/2025      |
| Final   | 09/02/2025      |

### Releases Entregues

| Release | Data de entrega |
| ------- | --------------- |
| 1       | 15/12/2024      |
| MVP     | 01/01/2025      |
| Final   | 09/02/2025      |

## Histórico de Versões

| Alteração                    | Data       | Autor           |
| ---------------------------- | ---------- | --------------- |
| Criação do documento         | 08/02/2025   | Clara Marcelino |