# Gestão de Qualidade

## Introdução

A gestão da qualidade é um elemento fundamental no desenvolvimento de produtos e serviços, sendo especialmente relevante no contexto do desenvolvimento de software. Segundo a ISO 25010, a qualidade de um produto de software é mensurada pelo grau em que ele atende aos requisitos de seus usuários, oferecendo valor e confiabilidade. Esses requisitos abrangem características como funcionalidade, desempenho, segurança e manutenibilidade, entre outras, e são organizados em um modelo de qualidade que as categoriza em atributos principais e suas respectivas subcaracterísticas.

Para garantir que esses requisitos sejam atendidos, é imprescindível estabelecer um sistema de métricas que permita monitorar e avaliar continuamente os aspectos do produto. Esse monitoramento não apenas assegura conformidade com os objetivos definidos, mas também viabiliza melhorias ao longo do projeto. Assim, o planejamento da qualidade desempenha um papel estratégico ao delinear como as métricas serão implementadas e como o desempenho do produto será acompanhado, promovendo a entrega de software de alta qualidade e alinhado às expectativas dos usuários.

## Processo de Qualidade

O processo de qualidade adotado neste projeto foi fundamentado em uma abordagem colaborativa e iterativa, garantindo que o produto final atendesse às expectativas e necessidades do cliente. Desde o início, a validação das User Stories (US) foi conduzida em conjunto com o cliente, utilizando protótipos e critérios de aceitação para alinhar os objetivos e assegurar que os requisitos fossem claramente compreendidos. Esse ciclo contínuo de validação e aprimoramento permitiu que melhorias fossem implementadas de forma incremental, promovendo a evolução do produto ao longo do desenvolvimento.

Após a conclusão do desenvolvimento de cada funcionalidade, foram realizados testes de aceitação diretamente pelo cliente, o que possibilitou identificar ajustes necessários e incorporar novos aperfeiçoamentos ao produto. Essa dinâmica não apenas assegurou a qualidade do produto entregue, mas também reforçou a satisfação do cliente com o resultado final.

Para monitorar e garantir a qualidade técnica do projeto, cada serviço desenvolvido foi integrado com a ferramenta SonarQube, utilizando a interface SonarCloud para maior clareza e controle das métricas de qualidade. Essa integração forneceu uma visão abrangente e em tempo real do desempenho do código, possibilitando a detecção precoce de problemas e garantindo a entrega de um software robusto e alinhado aos padrões estabelecidos.

## Métricas Monitoradas e Práticas de Garantia de Qualidade  

O monitoramento de métricas e a implementação de práticas estruturadas foram fundamentais para assegurar a qualidade do projeto. Dentre as principais métricas e estratégias adotadas, destacam-se:  

### Métricas Monitoradas  

**Cobertura de Código**  
   - Monitoramos a extensão em que o código-fonte foi testado, assegurando que os testes automatizados cobrissem cenários críticos e minimizassem a ocorrência de bugs não detectados.  

**Duplicação de Código**  
   - Identificamos e reduzimos trechos de código redundantes, promovendo manutenibilidade e eficiência no desenvolvimento.  

**Vulnerabilidades e Bugs**  
   - Avaliamos continuamente o código para detectar vulnerabilidades e erros, utilizando ferramentas de análise estática integradas com o SonarCloud.  

**Integração com CI/CD**  
   - Configuramos pipelines de integração contínua para executar automaticamente as análises do SonarCloud, garantindo que problemas fossem detectados antes da fusão de branches.  

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


## Modelo de Qualidade do Q-Rapids  

O modelo de qualidade do Q-Rapids combina objetivos estratégicos e científicos para melhorar a qualidade do software e otimizar o ciclo de vida de desenvolvimento. Segundo o projeto Q-Rapids (2024), os objetivos estratégicos gerais (GO1-GO3) concentram-se em melhorar os níveis de qualidade do software, aumentar a produtividade e reduzir o tempo de lançamento no mercado. Esses objetivos são desdobrados em objetivos científicos (SO1-SO4) que detalham ações práticas e técnicas para alcançar os resultados desejados.  

### Objetivos Estratégicos Gerais (GO1-GO3)  
**Melhorar os níveis de qualidade do software**: Garantir que os produtos entregues atendam aos requisitos técnicos e superem as expectativas dos usuários.  
**Aumentar a produtividade no ciclo de vida do software**: Otimizar processos para reduzir desperdícios e acelerar a entrega de valor.  
**Reduzir o tempo de lançamento do software no mercado**: Minimizar prazos para lançamento de novas funcionalidades e produtos completos, mantendo a qualidade.  

### Objetivos Científicos (SO1-SO4)  
**Coletar e analisar dados de tempo de execução e de tempo de design**: Integrar informações de diferentes etapas do desenvolvimento para obter uma visão abrangente do desempenho.  
**Definir o ciclo de vida do software integrando requisitos de qualidade e funcionais**: Promover um alinhamento claro entre os aspectos técnicos e as necessidades dos usuários.  
**Elaborar indicadores-chave estratégicos (KPIs)**: Permitir que os tomadores de decisão gerenciem o desenvolvimento com base em dados precisos.  
**Fornecer suporte de ferramentas**: Implementar soluções, como o SonarCloud, que facilitem um ciclo de vida voltado à qualidade.  

### Fatores e Métricas de Qualidade  
Os fatores de qualidade, como manutenibilidade, confiabilidade, usabilidade e eficiência, são pilares para avaliar o sucesso do produto, do processo e da organização. As métricas associadas fornecem dados quantitativos que:  
- Permitem monitorar e melhorar continuamente a qualidade.  
- Identificam problemas de forma precoce, reduzindo custos com retrabalho.  
- Aumentam a satisfação do cliente ao garantir um alinhamento mais forte com suas expectativas e requisitos.  

### Contribuição do SonarCloud  
O SonarCloud desempenha um papel crucial nesse modelo, fornecendo suporte contínuo ao monitoramento de métricas de qualidade e integração de diferentes fontes de dados. Sua capacidade de gerar relatórios detalhados e dashboards oferece uma visão clara da saúde do projeto, contribuindo diretamente para a execução dos objetivos do Q-Rapids.  

Esse modelo integrado reflete uma abordagem robusta para a qualidade, combinando planejamento estratégico, uso eficiente de ferramentas e monitoramento contínuo, promovendo produtos confiáveis e alinhados às demandas do mercado.


### Métricas para o produto

O uso de métricas permite identificar subcaracterísticas associadas e avaliar a qualidade do produto. Essa análise também possibilita medir a produtividade do projeto, gerando resultados que influenciam as decisões de desenvolvimento. Com base nas métricas especificadas no SonarCloud e Q-Rapids, além dos dados coletados, foram definidos os valores mínimos aceitáveis para cada métrica no projeto Sentinela, conforme mostrado na tabela abaixo.


| Métrica                      | Descrição                                                                                                                                               |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Complexity**                | Mede a complexidade do código, geralmente baseada na quantidade de caminhos possíveis no código. Valores mais baixos indicam código mais simples e de fácil manutenção. A meta é manter a complexidade abaixo de 10 para facilitar a leitura e a manutenção do código. |
| **Duplicated Lines Density (%)** | Mede a porcentagem de código duplicado no projeto. O código duplicado pode aumentar o esforço de manutenção e gerar inconsistências. A meta é que a densidade de linhas duplicadas não ultrapasse 5%, incentivando a reutilização de código e a eliminação de redundâncias. |
| **Coverage**                  | Refere-se à porcentagem de código coberta por testes automatizados. Um valor acima de 80% é considerado ideal para garantir que a maioria do código seja testada, minimizando a chance de bugs não detectados. |
| **Test Failures**             | Número de falhas nos testes automatizados. O objetivo é que não haja falhas nos testes (valor 0), indicando que o código está funcionando conforme o esperado e sem regressões. |
| **Test Errors**               | Refere-se ao número de erros encontrados durante a execução dos testes, como falhas de configuração ou problemas inesperados. A meta é que o número de erros seja 0, garantindo que os testes sejam executados corretamente. |
| **Security Rating**           | Classificação de segurança do código, geralmente em uma escala de A (melhor) a D (pior). A meta é que o rating de segurança seja A, indicando que o código está livre de vulnerabilidades críticas e segue boas práticas de segurança. |
| **Satisfação do usuário**     | Mede a satisfação dos usuários finais com o produto, geralmente coletada por meio de pesquisas ou feedbacks diretos. A meta é que a satisfação esteja acima de 3 (em uma escala de 1 a 5), refletindo que os usuários estão satisfeitos com o funcionamento e a experiência do produto. |


## Histórico de Versões

| Alteração                    | Data       | Autor           |
| ---------------------------- | ---------- | --------------- |
| Criação do documento         | 08/12/2024   | Daniela Soares |
| Revisão do documento         | 08/12/2024  | Clara Marcelino |


## Referências

[ISO/IEC 25010](https://iso25000.com/index.php/en/iso-25000-standards/iso-25010)

[Q-rapids](https://github.com/q-rapids)