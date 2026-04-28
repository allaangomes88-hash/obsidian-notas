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