# Conclusão do Projeto - Post-Mortem

Este documento tem como objetivo registrar os principais aprendizados, desafios enfrentados e pendências do projeto para facilitar a continuidade do desenvolvimento no próximo semestre.

## O que deu certo

- **Integração Contínua e Qualidade do Código:** A implementação do SonarCloud e a análise de métricas ajudaram a ter um bom nível de qualidade no desenvolvimento.
- **Processo de validação iterativa:** A validação contínua das User Stories com o cliente permitiu ajustes rápidos e mais alinhados às necessidades do usuário.
- **Engajamento da equipe:** O trabalho colaborativo e o uso de ferramentas como ZenHub facilitaram a organização das tarefas e o acompanhamento do progresso do projeto.

## Desafios enfrentados

- **Banco de Dados inadequado:** Durante o desenvolvimento, percebemos que o MongoDB não estava sendo adequado para o tipo de produto que estávamos criando. MongoDB é um banco de dados NoSQL, voltado para estruturas mais flexíveis e escaláveis, porém, o projeto exigia um modelo relacional mais estruturado para lidar com transações complexas e consistência nos dados. Como resultado, foi identificado que a migração para um banco de dados relacional seria mais coerente.

- **Processamento do arquivo retorno:** O arquivo retorno atualmente está sendo usado para registro de quem está em dia com a mensalidade do sindicato, porém seu uso dever ser explorado para outras funcionalidades, sendo elas a atualização do histórico de contribuições a partir dos dados do arquivo e a implementação de um histórico dos arquivos retorno que foram subidos na plataforma.

- **Alteração na solicitação de benefícios:** No meio do projeto, identificamos que a melhor forma de solicitar benefícios para os usuários seria por meio de encaminhamento ao sindicato, em vez de um processo automatizado pelo sistema. Isso se deu porque os benefícios possuem características altamente variáveis e requerem verificações manuais, tornando inviável uma abordagem padronizada. Como consequência, todas as histórias de usuários relacionadas ao épico "Solicitar Benefícios" foram removidas do escopo do projeto.

- **Dark Mode e acessibilidade:** Com o objetivo de melhorar a experiência do usuário, foi identificada a necessidade de implementação do **Dark Mode** no sistema. Essa funcionalidade permitiria maior conforto visual, especialmente para usuários que utilizam o sistema por longos períodos ou que possuem sensibilidade à luz. No entanto, sua implementação ficou pendente devido a outras prioridades de desenvolvimento e a manifestação tardia do PO a respeito da mesma.

- **Padronização na exibição de movimentações financeiras:** Durante o desenvolvimento, os usuários relataram que a exibição da listagem de movimentações financeiras não estava alinhada ao formato já existente na aba **Extrato Bancário**. Para garantir consistência na usabilidade e facilitar a navegação dos usuários, foi solicitado que as movimentações financeiras seguissem o mesmo padrão visual e organizacional. Essa mudança exige ajustes na interface e no modelo de dados para garantir que todas as informações relevantes sejam apresentadas de maneira uniforme.

- **Status "Aposentado" para sindicalizados:** Atualmente, o sistema contempla apenas três status para sindicalizados: **ativo, pendente e cancelado**. No entanto, foi identificado que muitos sindicalizados passam para a categoria de "aposentado", o que não se encaixa nos status existentes.

### **Histórico de Versões**

| **Versão** | **Nome da Versão**      | **Data**      | **Responsável**         | **Descrição/Alterações**                                 |
|------------|-------------------------|---------------|-------------------------|----------------------------------------------------------|
|   1.0      | Criação do documento    | 09/02/2025    | Clara Marcelino         | Criação do documento                                     |
