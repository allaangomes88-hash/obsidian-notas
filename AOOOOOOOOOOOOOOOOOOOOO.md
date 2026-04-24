
NEW CUSTOM

mandar pro claude pq isso funciona:
```
document.addEventListener("tarefa finalizada", () =>{

    if(liDaTarefaSelecionada){

        liDaTarefaSelecionada.classList.remove("app__section-task-list-item-active")

        liDaTarefaSelecionada.classList.add("app__section-task-list-item-complete")

        liDaTarefaSelecionada.querySelector("button"). setAttribute("disabled", "disabled")

    }

})
```

do pq ter q colocar ponto e nao virgula quando adiciona mais coisa em uma unica linha de codigo ali em setAttribute)

e quando q devo criar um evento