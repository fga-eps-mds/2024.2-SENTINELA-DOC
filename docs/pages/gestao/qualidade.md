# Gestão de Qualidade

## Introdução

A gestão da qualidade é um elemento fundamental no desenvolvimento de produtos e serviços, sendo especialmente relevante no contexto do desenvolvimento de software. Segundo a ISO 25010, a qualidade de um produto de software é mensurada pelo grau em que ele atende aos requisitos de seus usuários, oferecendo valor e confiabilidade. Esses requisitos abrangem características como funcionalidade, desempenho, segurança e manutenibilidade, entre outras, e são organizados em um modelo de qualidade que as categoriza em atributos principais e suas respectivas subcaracterísticas.

Para garantir que esses requisitos sejam atendidos, é imprescindível estabelecer um sistema de métricas que permita monitorar e avaliar continuamente os aspectos do produto. Esse monitoramento não apenas assegura conformidade com os objetivos definidos, mas também viabiliza melhorias ao longo do projeto. Assim, o planejamento da qualidade desempenha um papel estratégico ao delinear como as métricas serão implementadas e como o desempenho do produto será acompanhado, promovendo a entrega de software de alta qualidade e alinhado às expectativas dos usuários.

## Processo de Qualidade

O processo de qualidade adotado neste projeto foi fundamentado em uma abordagem colaborativa e iterativa, garantindo que o produto final atendesse às expectativas e necessidades do cliente. Desde o início, a validação das User Stories (US) foi conduzida em conjunto com o cliente, utilizando protótipos e critérios de aceitação para alinhar os objetivos e assegurar que os requisitos fossem claramente compreendidos. Esse ciclo contínuo de validação e aprimoramento permitiu que melhorias fossem implementadas de forma incremental, promovendo a evolução do produto ao longo do desenvolvimento.

Após a conclusão do desenvolvimento de cada funcionalidade, foram realizados testes de aceitação diretamente pelo cliente, o que possibilitou identificar ajustes necessários e incorporar novos aperfeiçoamentos ao produto. Essa dinâmica não apenas assegurou a qualidade do produto entregue, mas também reforçou a satisfação do cliente com o resultado final.

Para monitorar e garantir a qualidade técnica do projeto, cada serviço desenvolvido foi integrado com a ferramenta SonarQube, utilizando a interface SonarCloud para maior clareza e controle das métricas de qualidade. Essa integração forneceu uma visão abrangente e em tempo real do desempenho do código, possibilitando a detecção precoce de problemas e garantindo a entrega de um software robusto e alinhado aos padrões estabelecidos.

A estruturação para a observação da qualidade do produto segue um modelo baseado na ISO 25010, categorizando diferentes aspectos da qualidade em características e fatores específicos. Essa abordagem permite uma avaliação detalhada e objetiva do software, garantindo que métricas relevantes sejam monitoradas continuamente. No projeto, a manutenibilidade é avaliada por meio das métricas de complexidade, comentários e duplicação, garantindo que o código seja compreensível e fácil de modificar. Já a confiabilidade é analisada com base nos fatores Testing Status e Testing Performance, representados pelas métricas Test Success e Fast Tests, assegurando que o software funcione corretamente e que os testes sejam executados de forma eficiente. Além disso, a cobertura de código desempenha um papel essencial, verificando a extensão dos testes automatizados para garantir uma validação abrangente das funcionalidades. Essa estrutura de observação permite uma abordagem sistemática e iterativa para o controle da qualidade, facilitando a identificação precoce de problemas e a implementação de melhorias contínuas.

Foi desenvolvido um notebook com tais métricas, que pode ser acessaado por esse [link](https://github.com/fga-eps-mds/2024.2-SENTINELA-DOC/blob/main/analytics/internal_quality_analysis-sonarqube.ipynb).

## Métricas Monitoradas e Práticas de Garantia de Qualidade  

O monitoramento de métricas e a implementação de práticas estruturadas foram fundamentais para assegurar a qualidade do projeto. Dentre as principais métricas e estratégias adotadas, destacam-se:  

### Métricas Monitoradas  

**Cobertura de Código**  
   - Monitoramos a extensão em que o código-fonte foi testado, assegurando que os testes automatizados cobrissem cenários críticos e minimizassem a ocorrência de bugs não detectados.  

**Duplicidade de Código**  
   - Identificamos e reduzimos trechos de código redundantes, promovendo manutenibilidade e eficiência no desenvolvimento.  

**Vulnerabilidades e Bugs**  
   - Avaliamos continuamente o código para detectar vulnerabilidades e erros, utilizando ferramentas de análise estática integradas com o SonarCloud.  

**Integração com CI/CD**  
   - Configuramos pipelines de integração contínua para executar automaticamente as análises do SonarCloud, garantindo que problemas fossem detectados antes da fusão de branches.  

**Tempo de Execução dos Testes (`test_execution_time`)**  
   - Medimos o tempo de execução dos testes para garantir eficiência e rapidez no ciclo de desenvolvimento.

**Fast Tests**  
   - Garantimos que os testes fossem executados rapidamente, utilizando um valor de referência de 300000 microssegundos.

**Taxa de Sucesso nos Testes (`tests_success`)**  
   - Unificamos as métricas de falhas e erros de testes para avaliar a confiabilidade dos testes automatizados.

## Políticas de Código e Revisão  

**Pull Requests e Code Review**  
   - Implementamos um processo rigoroso de revisão de código, com melhores práticas que asseguraram qualidade e aderência aos padrões.  

**Padrões de Codificação**  
   - Adotamos ferramentas para verificar e reforçar regras de codificação, promovendo uniformidade e clareza no código-fonte.  

**Merge Guidelines**  
   - Só vai ser mergeado os prs que tiverem aprovação e passarem na validação de CI/CD.

Essas práticas integradas garantiram um desenvolvimento contínuo e alinhado com os objetivos de qualidade, resultando em um produto robusto, seguro e com alto nível de confiabilidade.  


## Ferramentas de Teste e Gerenciamento Utilizadas

Para garantir a qualidade e eficiência no desenvolvimento, foram utilizadas ferramentas robustas de teste e gerenciamento que se complementam, proporcionando um ambiente de trabalho estruturado e produtivo.

**Jest**
- Framework completo para testes em JavaScript, amplamente utilizado para testes de unidade, integração e ponta a ponta.
- Suporte a **mocks** e **snapshots**, permitindo simulações precisas de dependências e verificações de consistência de saída.
- Interface intuitiva, que facilita a configuração e execução de testes, acelerando o ciclo de desenvolvimento.

**Vitest**
- Framework leve e rápido, projetado para o ecossistema JavaScript moderno, com foco em integração com o **Vite**.
- Compatível com **TypeScript** e módulos **ESM**, garantindo flexibilidade no desenvolvimento de aplicações front-end.
- Ideal para cenários que exigem performance otimizada em testes.

**SonarCloud**
- Plataforma de análise de código que identifica **bugs**, **vulnerabilidades** e **code smells**, promovendo a segurança e manutenibilidade do projeto.
- Suporte a diversas linguagens de programação e integração direta com pipelines de **CI/CD**, assegurando monitoramento contínuo da qualidade.
- Relatórios detalhados e visualizações gráficas que facilitam a identificação e resolução de problemas no código.

**ZenHub**
- Ferramenta de gerenciamento de projetos integrada ao **GitHub**, permitindo um fluxo de trabalho centralizado e eficiente.
- Recursos como **quadros Kanban** e **relatórios de produtividade** possibilitam uma visão clara do progresso do projeto e o acompanhamento de tarefas.
- Facilita a comunicação entre equipes e a organização de backlog, assegurando o alinhamento com os objetivos do projeto.

Essas ferramentas foram fundamentais para implementar um processo de desenvolvimento ágil e orientado à qualidade, otimizando tanto o aspecto técnico quanto a gestão das atividades.

## Qualidade e suas Características

A qualidade do software é definida por um conjunto de características e subcaracterísticas que permitem medir e garantir um produto confiável. Seguindo o modelo da ISO 25010, a qualidade pode ser analisada com base nos seguintes aspectos:

- **Funcionalidade**: Capacidade do software de fornecer funcionalidades que atendam aos requisitos do usuário.
- **Eficiência de Desempenho**: Tempo de resposta, consumo de recursos e capacidade de processamento.
- **Confiabilidade**: Disponibilidade, tempo médio entre falhas e recuperação.
- **Usabilidade**: Facilidade de uso, acessibilidade e aprendizado.
- **Manutenibilidade**: Facilidade para modificar, corrigir ou aprimorar o software.
- **Portabilidade**: Capacidade de ser executado em diferentes ambientes.

## Modelo de Qualidade do Q-Rapids  

O modelo Q-Rapids é um framework de avaliação contínua da qualidade de software que integra diferentes métricas e fontes de dados para fornecer insights estratégicos sobre o desenvolvimento. Ele utiliza um conjunto de fatores de qualidade, como manutenibilidade, confiabilidade e produtividade, combinados com métricas extraídas de ferramentas como SonarQube. O modelo permite que equipes tomem decisões informadas com base em análises quantitativas e qualitativas, facilitando a identificação de problemas e a implementação de melhorias contínuas. Além disso, o Q-Rapids adota uma abordagem iterativa e adaptável, permitindo personalizações conforme as necessidades específicas de cada projeto, garantindo que a qualidade do software seja mantida e aprimorada ao longo do ciclo de desenvolvimento.

### Fatores e Métricas de Qualidade  
Os fatores de qualidade, como manutenibilidade, confiabilidade, usabilidade e eficiência, são pilares para avaliar o sucesso do produto, do processo e da organização. As métricas associadas fornecem dados quantitativos que:  
- Permitem monitorar e melhorar continuamente a qualidade.  
- Identificam problemas de forma precoce, reduzindo custos com retrabalho.  
- Aumentam a satisfação do cliente ao garantir um alinhamento mais forte com suas expectativas e requisitos.  

### Contribuição do SonarCloud  
O SonarCloud desempenha um papel crucial nesse modelo, fornecendo suporte contínuo ao monitoramento de métricas de qualidade e integração de diferentes fontes de dados. Sua capacidade de gerar relatórios detalhados e dashboards oferece uma visão clara da saúde do projeto, contribuindo diretamente para a execução dos objetivos do Q-Rapids.  

Esse modelo integrado reflete uma abordagem robusta para a qualidade, combinando planejamento estratégico, uso eficiente de ferramentas e monitoramento contínuo, promovendo produtos confiáveis e alinhados às demandas do mercado.


## Métricas para o Produto  

O uso de métricas permite identificar subcaracterísticas associadas e avaliar a qualidade do produto. Essa análise também possibilita medir a produtividade do projeto, gerando resultados que influenciam as decisões de desenvolvimento. No projeto, analisamos diferentes métricas que pertencem a fatores e características específicas da qualidade do software, conforme a ISO 25010.

- **Complexidade, Comentário e Duplicação**: Essas métricas pertencem ao **fator de qualidade de código**, que faz parte da **característica de manutenibilidade**. Elas permitem avaliar a facilidade de manutenção e compreensão do código, reduzindo riscos de retrabalho e melhorando a eficiência do desenvolvimento.

- **Test Success**: Essa métrica pertence ao **fator Testing Status**, que faz parte da **característica de confiabilidade**. Ela mede a taxa de sucesso dos testes automatizados, garantindo que o software funcione corretamente sem falhas inesperadas.

- **Fast Tests**: Associada ao **fator Testing Performance**, essa métrica também pertence à **característica de confiabilidade** e mede o tempo de execução dos testes para assegurar que a validação do código ocorra de forma ágil e eficiente.

- **Cobertura de Código**: Mede a porcentagem do código que é testado por testes automatizados. Uma cobertura adequada garante que a maioria das funcionalidades seja testada, reduzindo a probabilidade de falhas em produção.

Com base nas métricas especificadas no Q-Rapids, além dos dados coletados, foram definidos os valores mínimos aceitáveis para cada métrica no projeto Sentinela, conforme mostrado na tabela abaixo.

### Valores de Referência para as Métricas utilizadas

| Métrica                      | Valor de Referência |
| ---------------------------- | ------------------ |
| **Complexity**                | < 10 por função |
| **Duplicated Lines Density (%)** | Entre 10% e 30% |
| **Coverage**                  | > 60% |
| **Densidade de Duplicidade**  | < 5% |
| **Fast Tests**                | < 300000 microssegundos |

Esses valores foram definidos com base em referências do modelo Q-Rapids e no relatório do Google de boas práticas de cobertura de código, garantindo um alto padrão de qualidade no desenvolvimento do software.

## Histórico de Versões

| Alteração                    | Data       | Autor           |
| ---------------------------- | ---------- | --------------- |
| Criação do documento         | 08/12/2024   | Daniela Soares |
| Revisão do documento         | 08/12/2024  | Clara Marcelino |
| Ajuste do planejamento de qualidade         | 08/01/2025  | Clara Marcelino |

## Referências

[ISO/IEC 25010](https://iso25000.com/index.php/en/iso-25000-standards/iso-25010)

[Q-rapids](https://github.com/q-rapids)

[GOOGLE. Code Coverage Best Practices](https://testing.googleblog.com/2020/08/code-coverage-best-practices.html)
