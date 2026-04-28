
  Via de regra, uma requisição HTTP possui as partes a seguir:

- **5.1. URL:** O _endpoint_ (pense que o _endpoint_ é uma espécie de “endereço) do servidor para onde a requisição será enviada;

- **5.2. Headers:** Informações adicionais enviadas junto com a requisição, como o tipo de conteúdo (Content-Type). No caso do nosso app, o tipo de conteúdo é um arquivo no formato JSON;

- **5.3. Body:** O corpo da requisição, onde os dados são enviados (principalmente usado em requisições POST).

```
     async criarPensamento(pensamento) {

        try {

            const response = await fetch("http://localhost:3000/pensamentos", {
            
                method: "POST",

                headers: {
                    "Content-Type": "application/json"
                },

                body: JSON.stringify(pensamento)
            })

            return await response.json()

        } catch (error) {

            alert("erro ao enviar seu pensamento")

            throw error
        }

    }
```

**`method: "POST"`** — é o **tipo da ação**. Existem vários:

- `GET` = buscar dados (o que o `buscarPensamentos` faz)
- `POST` = enviar dados novos
- `PUT` = atualizar
- `DELETE` = deletar

---

**`headers`** — é o **envelope da carta**, avisa o formato:

javascript

```javascript
"Content-Type": "application/json" // "ei API, vou te mandar um JSON"
```

---

**`body`** — é o **conteúdo da carta**, os dados em si:

javascript

```javascript
body: JSON.stringify(pensamento)
// pensamento é o objeto { conteudo: "...", autoria: "..." }
// JSON.stringify transforma em texto pra poder enviar
```

---

O fluxo completo:

```
você → POST → "ei API, quero criar algo"
       headers → "vou mandar em JSON"
       body → "aqui estão os dados: { conteudo, autoria }"

API → salva no db.json → devolve o objeto salvo com ID
```

No projeto [[memoteca]] utilizamos POST para enviar dados novos para a API, nos somos o client, o garçom api e a cozinha o servidor da api