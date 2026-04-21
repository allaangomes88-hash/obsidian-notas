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
   
  lista.[[push]](tarefas)-- o push sempre adiciona um objeto no final da lista (lista) que no caso até não adicionar ninguem ela esta vazia


-> `localStorage.setItem("lista", JSON.stringify(lista))`

    

---
Para sempre que carregar a página mostrar o foi salvo ou se n tiver nada ficar vazio:

`const lista: JSON.parse(localStorage.getItem("lista")) || [ ]`

O parse `JSON.parse` converte uma **string JSON** de volta pra um objeto/array JavaScript.

É o caminho inverso do `JSON.stringify`

Se converte o array em string (stringify) dps converto essa string em um objeto (parse) se n tiver nada, mostra nulo ( [ ] )