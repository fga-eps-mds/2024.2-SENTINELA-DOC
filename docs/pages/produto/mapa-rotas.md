# Mapa de Rotas do Projeto
A tabela abaixo descreve as rotas configuradas em um sistema Node.js. Cada rota define o método HTTP, o endpoint (URI) e a função ou controlador responsável por executar a lógica associada. Essa configuração é comum em frameworks como Express.js.



| Method     | URI               | Action                       |
|------------|-------------------|------------------------------|
| GET        | /api/user         | userController.getUser       |
| GET        | /client           | clientController.getAll      |
| POST       | /client           | clientController.create      |
| GET        | /client/create    | clientController.showCreate  |
| GET        | /client/:id       | clientController.getById     |
| PUT|PATCH  | /client/:id       | clientController.updateById  |
| DELETE     | /client/:id       | clientController.deleteById  |


### Explicação de cada rota

#### **`GET /api/user`**
- **Descrição**: Obtém informações do usuário autenticado.
- **Ação**: `userController.getUser` é a função que retorna os dados do usuário.

#### **`GET /client`**
- **Descrição**: Lista todos os clientes cadastrados.
- **Ação**: `clientController.getAll` retorna a lista completa.

#### **`POST /client`**
- **Descrição**: Cria um novo cliente no sistema.
- **Ação**: `clientController.create` executa a lógica para adicionar o cliente.

#### **`GET /client/create`**
- **Descrição**: Exibe uma interface (ou lógica) para criar um novo cliente.
- **Ação**: `clientController.showCreate` apresenta o formulário ou configuração necessária.

#### **`GET /client/:id`**
- **Descrição**: Busca os detalhes de um cliente específico com base no `id`.
- **Ação**: `clientController.getById` recupera os dados.

#### **`PUT|PATCH /client/:id`**
- **Descrição**: Atualiza as informações de um cliente específico pelo `id`.
- **Ação**: `clientController.updateById` realiza a modificação.

#### **`DELETE /client/:id`**
- **Descrição**: Remove um cliente do sistema com base no `id`.
- **Ação**: `clientController.deleteById` executa a exclusão.
