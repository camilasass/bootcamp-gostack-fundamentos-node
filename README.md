![capa](https://camo.githubusercontent.com/d25397e9df01fe7882dcc1cbc96bdf052ffd7d0c/68747470733a2f2f73746f726167652e676f6f676c65617069732e636f6d2f676f6c64656e2d77696e642f626f6f7463616d702d676f737461636b2f6865616465722d6465736166696f732e706e67)
<h3 align="center" >Bootcamp Go Stack | Fundamentos Node.js</h3>

Desafio sobre fundamentos de Node.js aplicado no Bootcamp GoStack da RocketSeat

Trata-se do back-end de uma aplicação para armazenar transações financeiras de entrada e saída, que faz o cadastro e a listagem dessas transações.

Mais informações estão disponíveis [aqui](https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-fundamentos-nodejs#rocket-sobre-o-desafio)
### Como executar
- Primeiro clone o repositório na sua máquina (o exemplo abaixo usa SSH)
```
git clone git@github.com:camilasass/bootcamp-gostack-fundamentos-nodejs.git
```

- Para executar:
```
yarn install
```


### Rotas
- `[POST] /transactions`: cria uma transação
- `[GET] /transactions`: lista as transações e o balanço 

#### POST /transactions

Requisição
```javascript
// POST /transactions
{
	"title": "Salário",
	"value": 4000,
	"type": "income"
}
```

Resposta
```javascript
{
  "id": "6571374c-0708-4482-9f80-9785306aad5c",
  "title": "Salário",
  "value": 4000,
  "type": "income"
}
```


#### GET /transactions

Requisição
```javascript
GET /transactions
```

Resposta
```javascript
{
  "transactions": [
    {
      "id": "6571374c-0708-4482-9f80-9785306aad5c",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    }
  ],
  "balance": {
    "income": 4000,
    "outcome": 0,
    "total": 4000
  }
}
```
