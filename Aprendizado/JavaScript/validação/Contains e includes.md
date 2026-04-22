o contais ele compara basicamente:

## contains

```js
const btn = document.querySelector("button")

if(btn.classList.contains("ativo")){
    console.log("botão está ativo")
} else {
    console.log("botão não está ativo")
}
```

"os btn tem a classe "ativos"? true ou false

---
## Includes: 

```js
const tarefas = ["estudar", "comer", "dormir"]

if(tarefas.includes("comer")){
    console.log("tem comer na lista")
}
```

Mesma lógica — pergunta se o item existe e responde `true` ou `false`. A diferença é só onde procura: `includes` em array ([[forEach]], `contains` em classList.

