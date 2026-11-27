# Atividade 13/11/2026 — Consumo de API REST

Atividade de Query Parameters, Request Body e Headers utilizando a API pública JSONPlaceholder e o Hoppscotch.

## 1. Query Parameters

- Método: `GET`
- URL: `https://jsonplaceholder.typicode.com/comments`
- Aba Parameters: chave `postId`, valor `1`.
- URL final: `https://jsonplaceholder.typicode.com/comments?postId=1`

Resultado observado na consulta à API: cinco comentários, com IDs de 1 a 5, todos com `postId: 1`. Status esperado: `200 OK`. Isso demonstra a filtragem dos resultados.

## 2. Request Body

- Método: `POST`
- URL: `https://jsonplaceholder.typicode.com/posts`
- Aba Body: `application/json`.

```json
{
  "title": "Minha Primeira API",
  "body": "Testando o envio de dados via POST no Hoppscotch.",
  "userId": 10
}
```

Resposta esperada (`201 Created`):

```json
{
  "title": "Minha Primeira API",
  "body": "Testando o envio de dados via POST no Hoppscotch.",
  "userId": 10,
  "id": 101
}
```

O JSONPlaceholder simula o cadastro: o recurso não fica salvo permanentemente.

## 3. Headers

Na requisição POST, verifique na aba Headers:

| Key | Value |
| --- | --- |
| Content-Type | application/json |

O cabeçalho informa o formato do corpo enviado. Para APIs que exigem autenticação, um exemplo seria `Authorization: Bearer TOKEN_EXEMPLO`. O JSONPlaceholder não precisa desse cabeçalho, portanto ele está desativado na coleção.

## Como executar no Hoppscotch

1. Abra [Hoppscotch](https://hoppscotch.io/).
2. Na seção Collections, selecione a opção de importação e o formato Postman.
3. Importe `colecao.postman_collection.json`.
4. Abra cada requisição e clique em Send. Se preferir, configure manualmente conforme as etapas acima.

O arquivo `requisicoes.http` também contém os exemplos em texto.

## Verificação

A consulta GET foi verificada diretamente na API e retornou cinco comentários da postagem 1. Os exemplos POST e Headers estão configurados, mas seus resultados são esperados, não registros de execução: ainda devem ser testados no Hoppscotch. Não foram produzidas capturas de tela de testes não executados.
