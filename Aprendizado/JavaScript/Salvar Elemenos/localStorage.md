É onde fica salvo no site informações sem precisar coloca-las novamente
Existem 4 metodos de usada-lo:

```
// Salvar
localStorage.setItem("chave", "valor")

// Ler
localStorage.getItem("chave")

// Remover um item
localStorage.removeItem("chave")

// Limpar tudo
localStorage.clear()

```

Precisamos converter par JSON pois ele só salva string:


`const lista= []`

`const tarefas = {` 
`descricao: textTearea.value` 
`}`
   
  lista.[[push]](tarefas)


-> `localStorage.setItem("lista", JSON.stringify([{descricao: "estudar"}]))`

    