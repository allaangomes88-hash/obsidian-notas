O `document.addEventListener` sozinho é pra eventos globais — coisas que não pertencem a um elemento específico, como:


```js
// evento customizado
document.addEventListener("FocoFinalizado", () => {})

// tecla pressionada em qualquer lugar da página
document.addEventListener("keydown", (e) => {})

// página terminou de carregar
document.addEventListener("DOMContentLoaded", () => {})
```

Exemplo do projeto [[fokus]], sendo o evento "tarefa finalizada" sendo um [[new CustomEvent]]

```
document.addEventListener("tarefa finalizada", () =>{

    if(liDaTarefaSelecionada){

        liDaTarefaSelecionada.classList.remove("app__section-task-list-item-active")

        liDaTarefaSelecionada.classList.add("app__section-task-list-item-complete")

        liDaTarefaSelecionada.querySelector("button"). setAttribute("disabled", "disabled")

    }

})
```


---

Quando o evento pertence a um elemento específico você usa o elemento: [[Eventos]]

```js
li.addEventListener("click", () => {})
btn.addEventListener("click", () => {})
input.addEventListener("focus", () => {})
```

A regra é simples — se é algo que acontece na página inteira, usa `document`. Se é algo que acontece num elemento específico, usa o elemento. (li, btn, input etc)