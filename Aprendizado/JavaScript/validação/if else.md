adicionar no if o nome de alguma variavel, e msm que dizer "se tiver valor faz algo se não não"

```javascript
botao.onclick = () => {
        const novaDescricao = prompt("Qual é o novo nome da tarefa?")
        console.log('Nova descrição da tarefa: ', novaDescricao)
        if (novaDescricao) {            
                paragrafo.textContent = novaDescricao
                tarefa.descricao = novaDescricao
                atualizarTarefas()
        }
}
```