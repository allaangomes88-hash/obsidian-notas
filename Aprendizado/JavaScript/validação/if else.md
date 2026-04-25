utilizado basicamente em tofo projeto: [[gameShelf]] [[fokus]]

Adicionar no if o nome de alguma variavel, e msm que dizer "se tiver valor faz algo se não não"

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
neste exemplo nos utiluzamos no i o nome de uma variavel. [[onClick]]

Funciona porque todo valor em JS é `truthy` ou `falsy`. O `if` não precisa de 
comparação explícita — ele avalia se o valor existe ou não:

```js
null      → falsy → if não entra
undefined → falsy → if não entra
""        → falsy → if não entra

"texto"   → truthy → if entra
123       → truthy → if entra
li        → truthy → if entra (elemento HTML existe)
```

Então `if(novaDescricao)` é o mesmo que perguntar: _"novaDescricao tem algum valor que não seja vazio/nulo?"_

se sim faz isso (if), se não, faz quilo (else)

É um atalho muito usado no JS pra checar se algo existe antes de usar.