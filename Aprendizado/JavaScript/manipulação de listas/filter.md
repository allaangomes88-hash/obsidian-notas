o filter serve para remover itens de um array:

```
    const itensFiltrados= lista.filter(objFiltrado => !objFiltrado.concluida)

    // faz uma lista dos q n estao concluida

    lista = itensFiltrados

    salvar()

  
```

Todos os itens desse exemplo que possuem a categoria "concluida" vao ser removidos em uma nova lista q ele irá retornar. No entando ele passa essa lista pra "lista" uma variavel global.