Basicamente serve para remover algo do DOM, usado em: [[fokus]]

item.remove()

```
function limparTarefasConcluidas(){

  

    document.querySelectorAll("li").forEach(item => {

        if(item.classList.contains("app__section-task-list-item-complete")){

            item.remove()

            // tira do DOM

        }

    })

    const itensFiltrados= lista.filter(objFiltrado => !objFiltrado.concluida)

    // faz uma lista dos q n estao concluida

    lista = itensFiltrados

    salvar()

  

}
```

o [[forEach]] está pegando cada objeto da lista que tenha a classe demonstrada e a removendo do DOM

