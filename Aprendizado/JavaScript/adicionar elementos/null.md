variasveis com valor null, servem para ganhar valor conforme algo aconteça, algum evento

```js
let liDaTarefa = null // nenhuma tarefa selecionada ainda
```

O `null` significa "vazio, não existe nada selecionado". Aí conforme o usuário interage você atualiza:


```js
// usuário clicou numa tarefa → guarda ela
liDaTarefa = li

// usuário clicou de novo → limpa
liDaTarefa = null

// temporizador terminou → usa o que tiver guardado
if(liDaTarefa){
    // faz algo com a tarefa selecionada
}
```

É como um "carrinho de compras" — começa vazio, você coloca algo, usa, e esvazia. O `if(liDaTarefa)` funciona porque `null` é falsy — ou seja, se for `null` o `if` não entra.

Você usa esse padrão sempre que precisar **lembrar qual elemento está selecionado** entre eventos diferentes — modal aberto, item ativo, usuário logado, etc.

vc usa quando você tem um estado que começa sem valor e só ganha valor depois de uma ação do usuário. Alguns exemplos:

```js
let usuarioLogado = null
// ganha valor quando faz login
usuarioLogado = { nome: "Daenerys", id: 123 }

let modalAberto = null
// ganha valor quando abre o modal
modalAberto = document.querySelector(".modal")

let itemSelecionado = null
// ganha valor quando clica num item
itemSelecionado = li
```

A pergunta que te guia é: **esse valor existe antes do usuário fazer algo?** Se não existe, começa com `null`. Se existe desde o início, já inicializa com o valor:

---
exemplo: [[fokus]]


```
function tarefaEmFoco(tarefa, li){

    const validacaoDeCLass= li.classList.contains("app__section-task-list-item-active")

    const emAndamento=document.querySelector(".app__section-active-task-description")

  

    document.querySelectorAll("li").forEach(item => {

        item.classList.remove("app__section-task-list-item-active")

    })

  

    if(!validacaoDeCLass){

         li.classList.add("app__section-task-list-item-active")

         emAndamento.innerHTML= tarefa.descricao

         liDaTarefaSelecionada= li

    }else{

         li.classList.remove("app__section-task-list-item-active")

         emAndamento.textContent= ""

         liDaTarefaSelecionada= null

    }

  

}

  

document.addEventListener("tarefa finalizada", () =>{

    if(liDaTarefaSelecionada){

        liDaTarefaSelecionada.classList.remove("app__section-task-list-item-active")

        liDaTarefaSelecionada.classList.add("app__section-task-list-item-complete")

        liDaTarefaSelecionada.querySelector("button"). setAttribute("disabled", "disabled")

    }

})
```

so vai receber o valor quando a li n tiver classe e o if adicionar, quando o contador chegar a 0 ele vai pegar essa tarefa com a classe ativada, desativa-la e adicionar outra de tarefa finalizada.

segue contador exemplo: [[fokus]]

```
if(numeracao === 0){

        parar()

        botaoSalvarOuPausar.textContent="começar"

        imagem.setAttribute("src", "./imagens/play_arrow.png")

        const tarefaFoco= html.getAttribute("data-contexto") === "foco"

        if(tarefaFoco){

            const eventoPersona= new CustomEvent("FocoFinalizado")

             document.dispatchEvent(eventoPersona)

        }

        return

    }
```

quando o contador chegar a 0, ele cria uma const com o valor do data-contexto for igual a foco. Se for ele cria o [[new CustomEvent]]  e dispara. No `document.addEventListener("tarefa finalizada"`