# projeto_final_revisao

### boas nomeclaturas:

---
#### nomes de arquivos:
---
bom exemplo

```
musica-schema.js

ou 

musicaSchema.js

```

exemplo não recomendável

```
musicaschema.js
MUSICASCHEMA.js
mu.js

```
---
#### nomes para varaivels
---
der nomes que faca sentido ao contexto

como por exemplo:

professorModel: para a model do professor

ou até mesmo ProfessorModel por se tratar de uma classe


um mal exemplo:

prof: 

neste caso prof pode ser profissao, professor, profile... ,
isso acaba deixando o código confuso.


### URL

- defina as url em letras minusculas
- evite usar verbos na url como por exemplo /filmes/`create` um exemplo ideal seria /filmes/
- use hífen `-` para separar os substantivos da url, exemplo:  http://`veterinaria-da-bea`.com/
- use `query` para consultas( req.query ).  /filmes/`?titulo=peter%20pan&idioma=pt` 
- use `params`para recursos( req.parmas, o famoso id ). /filmes/`123456` 


### Capriche no readme

um README é a forma como mostramos ao o desenvolvedor que vai utilizar a nossa api
como ele pode consumi-la, utilizada. Pensando nisso, precisamos ter um readme empático,
imagina precisar usar uma API ela ter a documentacao confunsa ou faltar dados?


#### dicas gerais

 - informe o payload( body ) que é necessário para criar ou atualizar um recurso no sistema
 - caso possua endpoits protegidos, indique o tipo de autorização que foi utilizado
 - descreva os payload (body) de resposta
 - descreva os payload (body) de erro
 - Sem tempo? O postman gera uma documentacao a partir da nossa colecao

---
#### Exemplo para exemplo de descricao de GET
---

GET /filmes/:id

headers

| Key | Value | Description
| ----------- | ----------- | ----------- |
| Authorization | Baerer token | token de autorizacao |


response: `200  - ok`

```json
{
    "titulo" : "peter pan",
    "ano_de_lancamento" : "2000-01-01",
    "visualizacoes" : "1000"
}
```
---

#### Exemplo para exemplo de POST / PATCH

---
POST /filmes

headers

| Key | Value | Description
| ----------- | ----------- | ----------- |
| Athorization | Baerer token | token de autorizacao |


body:

```json
{
    "titulo" : "peter pan",
    "ano_de_lancamento" : "2000-01-01",
    "visualizacoes" : "1000"
}
```

response: `201 - create`

```json
{
    "titulo" : "peter pan",
    "ano_de_lancamento" : "2000-01-01",
    "visualizacoes" : "1000",
    "id" : 1,
}
```

