# Minhas Finanças - Projeto Final

Este projeto é uma aplicação web de controle de finanças pessoais. Ele permite o registro de transações financeiras, como depósitos e gastos, exibindo o saldo atual e o histórico de transações. O projeto utiliza o **JSON Server** para simular uma API RESTful, e faz uso de conceitos como **assíncronicidade**, **promises**, **tratamento de erros** e **comunicação via HTTP**.

## Funcionalidades

- **Cadastro de Transações**: Adicionar, editar e excluir transações financeiras.
- **Exibição de Saldo**: Calcula o saldo total com base nas transações cadastradas.
- **Histórico de Transações**: Exibe uma lista com todas as transações cadastradas.
- **Integração com API**: Consumo de uma API RESTful para persistência de dados.

## Tecnologias Utilizadas

- **HTML5**: Estruturação do conteúdo da página.
- **CSS3**: Estilização da interface.
- **JavaScript**: Manipulação do DOM, comunicação com a API e lógica do projeto.
- **JSON Server**: Simulação de uma API RESTful para armazenamento das transações.

## Como Rodar o Projeto

Para rodar o projeto localmente, siga as instruções abaixo:

1. **Clone o repositório**:

   Abra o terminal e execute o comando:

   ```bash
   git clone git@github.com:DarllysonS/minhas-financas.git
   ```

2. **Instale as dependências**:

   Navegue até o diretório do projeto e execute o comando para instalar as dependências:

   ```bash
   npm install
   ```

3. **Inicie o servidor de desenvolvimento**:

   Com as dependências instaladas, inicie o servidor utilizando o JSON Server com o comando:

   ```bash
   npm run json-server
   ```

   O servidor será iniciado e estará disponível em http://localhost:3000, servindo a API para o seu front-end.

4. **Abra o projeto no navegador:**:

   Abra o arquivo index.html no seu navegador preferido e a aplicação estará rodando localmente.

## Como Funciona

O projeto permite adicionar, editar e excluir transações financeiras. As transações podem ser de dois tipos:

- **Créditos** (entrada de dinheiro).
- **Débitos** (gastos de dinheiro).

### Fluxo de Funcionalidades

1. **Criar uma Transação**:

   Ao preencher o formulário e salvar, uma nova transação será registrada na API e exibida na lista de transações.

   **Exemplo de Transação**:

   - Nome: "Salário"
   - Valor: 3200

2. **Editar uma Transação**:

   Ao clicar em "Editar" em uma transação existente, você pode modificar o nome e o valor da transação.

3. **Excluir uma Transação**:

   Ao clicar em "Excluir", a transação será removida da lista e a API será atualizada.

4. **Exibição do Saldo**:

   O saldo é atualizado automaticamente, refletindo o total de todas as transações, levando em consideração créditos (positivos) e débitos (negativos).

### Como a Comunicação com a API Funciona

- A aplicação faz uso de **fetch** para enviar e receber dados da API.
- A API é simulada utilizando o **JSON Server**, que permite salvar as transações no arquivo `db.json`.
- O saldo é atualizado ao somar os valores de todas as transações.
