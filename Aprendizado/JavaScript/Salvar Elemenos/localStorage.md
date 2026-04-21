uso em: [[gameShelf]]

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


---
exemplo de uso com o [[forEach]], no projeto [[fokus]]


O [[forEach]] pode servir para **renderizar na tela as tarefas que já existiam no localStorage** quando a página carrega.

Sem ele, toda vez que você abrisse a página estaria vazia — mesmo tendo tarefas salvas.

```js
// 1. recupera a lista salva no localStorage
const lista = JSON.parse(localStorage.getItem("lista")) || []

// 2. para cada tarefa salva, cria um <li> e adiciona no <ul>
lista.forEach(element => {
    ul.append(criarItemTarefa(element))
})
```
(o criarItemTarefa é todos os elementos que vao estar dentro de cada Li da UL)

Traduzindo: "pega cada objeto que estava salvo, transforma em elemento visual e coloca na tela".

Sem o [[forEach]] você até salvaria as tarefas, mas na próxima visita a lista estaria vazia visualmente — os dados existiriam no localStorage mas ninguém estaria lendo e desenhando na tela.

