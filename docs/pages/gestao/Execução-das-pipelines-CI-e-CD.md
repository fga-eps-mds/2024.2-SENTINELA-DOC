# Execução das pipelines de CI e CD


A orquestração das pipelines de Integração Contínua (CI) e Entrega Contínua (CD) foi essencial para garantir a qualidade e estabilidade do sistema ao longo do desenvolvimento. O fluxo automatizado permitiu a validação de código, execução de testes e deploys, reduzindo erros manuais e otimizando o tempo de entrega.

# Registro de Métricas do Projeto
## Frontend


| Métrica                                       | Medida |
|-----------------------------------------------|--------|
| Quantidade de vezes que o pipeline de CI foi executado  | 226     |
| Quantidade de vezes que o pipeline de CI falhou        | 136    |
| Quantidade de vezes que o pipeline de Release foi executado | 96     |
| Quantidade de vezes que o pipeline de Release falhou   | 43     |
| Quantidade de PRs abertos                              | 49     |
| Quantidade de PRs revisados                            | 41     |
| Quantidade de Releases                                 | 3      |


## Backend Usuários

| Métrica                                       | Medida |
|-----------------------------------------------|--------|
| Quantidade de vezes que o pipeline de CI foi executado  | 190     |
| Quantidade de vezes que o pipeline de CI falhou        | 89    |
| Quantidade de vezes que o pipeline de Release foi executado | 86     |
| Quantidade de vezes que o pipeline de Release falhou   | 43     |
| Quantidade de PRs abertos                              | 33     |
| Quantidade de PRs revisados                            | 30     |
| Quantidade de Releases                                 | 3      |


## Backend Benefícios

| Métrica                                       | Medida |
|-----------------------------------------------|--------|
| Quantidade de vezes que o pipeline de CI foi executado  | 48     |
| Quantidade de vezes que o pipeline de CI falhou        | 11    |
| Quantidade de vezes que o pipeline de Release foi executado | 28     |
| Quantidade de vezes que o pipeline de Release falhou   | 5     |
| Quantidade de PRs abertos                              | 7     |
| Quantidade de PRs revisados                            | 7     |
| Quantidade de Releases                                 | 3      |


## Backend Financeiro

| Métrica                                       | Medida |
|-----------------------------------------------|--------|
| Quantidade de vezes que o pipeline de CI foi executado  | 130     |
| Quantidade de vezes que o pipeline de CI falhou        | 21    |
| Quantidade de vezes que o pipeline de Release foi executado | 42     |
| Quantidade de vezes que o pipeline de Release falhou   | 5     |
| Quantidade de PRs abertos                              | 20     |
| Quantidade de PRs revisados                            | 18     |
| Quantidade de Releases                                 | 3      |


# Análise das Falhas nos Pipelines  

Um fator relevante para as falhas foi a significativa **evolução da funcionalidade de permissões**, que passou por mudanças frequentes em todos os repositórios. Diante desse cenário, a equipe optou por priorizar a **entrega das releases** em detrimento da execução exaustiva dos testes, garantindo que as novas funcionalidades chegassem aos usuários sem atrasos significativos.  

As falhas no pipeline de **CI** ocorreram, em grande parte, devido a **flaky tests**, que representaram um desafio significativo para a equipe durante algumas semanas. Esses testes, embora passassem localmente e, na maioria das vezes, também no pipeline, apresentavam falhas esporádicas sem uma causa aparente. Esse problema foi investigado e corrigido nas últimas semanas, não sendo mais identificado pelos membros do time.  

Além disso, algumas execuções do CI falharam devido a **testes quebrados e problemas de formatação**, como padronização de código e estilização, que foram gradualmente corrigidos para garantir a estabilidade da pipeline.  

No caso do pipeline de **Release**, as falhas iniciais foram causadas por uma configuração incorreta do arquivo **sonar-metrics.py**, que não estava devidamente ajustado para processar corretamente **branches e tags (versões)**. Esse problema exigiu ajustes na lógica do pipeline para garantir que as métricas fossem capturadas corretamente.  

Esses desafios foram superados ao longo do desenvolvimento, e as otimizações realizadas nas pipelines contribuíram para a melhoria contínua do fluxo de integração e entrega.  


### **Histórico de Versões**

| **Versão** | **Nome da Versão**      | **Data**      | **Responsável**         | **Descrição/Alterações**                                 |
|------------|-------------------------|---------------|-------------------------|----------------------------------------------------------|
|   1.0      | Criação do documento    | 09/02/2025    | Daniela Soares        | Criação do documento   