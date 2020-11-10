<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios-new.png" />

<h3 align="center">
  Desafio 05: Primeiro projeto Node.js
</h3>

## :rocket: Sobre o desafio

Esse projeto consiste em uma aplicação Node na qual são armazenadas transações financeiras de entrada e saída, onde é possível realizar tanto o cadastro quanto a listagem dessas transações


## :motorway: Rotas da aplicação

- **`Listagem dos repositórios`**: O aplicativo todos os repositórios já cadastrados na API.

- **`Curtir um repositório`**: O botão "Curtir" permite que o usuário curta qualquer um dos repositórios listados.



- **`POST /transactions`**: A rota recebe os campos `title`, `value` e `type` dentro do corpo da requisição, sendo `type` o tipo da transação, que deve ser `income` para entradas (depósitos) e `outcome` para saídas (retiradas). Ao cadastrar uma nova transação, ela é ser armazenada dentro de um objeto com o seguinte formato :

```json
{
  "id": "uuid",
  "title": "Salário",
  "value": 3000,
  "type": "income"
}
```

- **`GET /transactions`**: Essa rota retorna uma listagem com todas as transações que você cadastrou até agora, junto com o valor de soma de entradas, retiradas e total de crédito. Ao fazer uma requisição você receberá como retorno um objeto com o formato a seguir:

```json
{
  "transactions": [
    {
      "id": "uuid",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freela",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Pagamento da fatura",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Cadeira Gamer",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}
```

## :computer: Instruções de instalação e teste
Clone o repositório usando o `git` ou faça o download no formato zip. 
Antes de tudo, certifique-se de que você tem um gerenciador de pacotes (como o yarn) e o `Node.js` instalados em sua máquina.

Após baixar o projeto, abra uma aba do terminal e execute os seguintes comandos:

```Bash
# ../pasta-de-destino
$ cd gostack-fundamentos-node
# ../pasta-de-destino/gostack-fundamentos-node
$ yarn
```

Para iniciar a aplicação na porta 3333:

```Bash
# ../pasta-de-destino/gostack-fundamentos-node
$ yarn dev:server
```

Para rodar os testes da aplicação:
```Bash
# ../pasta-de-destino/gostack-fundamentos-node
$ yarn test
```
