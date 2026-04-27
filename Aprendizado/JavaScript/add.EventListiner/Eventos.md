Quando for usar um add.EventListiner pra passar uma function que tenho algum parametro deve-se usar: ( ), ficando : 

`addEventListener("click", () => tarefaEmFoco(tarefa))`

se essa function tivesse um e.target ficaria assim:   

`addEventListener("click", (e) => tarefaEmFoco(tarefa, e))`


---

uso em:[[fokus]] [[gameShelf]]

**click** -> detecta o click do usuario

---

**change** -> quando o usuario terminar de fazer uma ação:

**`<input type="text">` e `<textarea>`** → dispara quando o usuário **sai do campo** (perde o foco) _e_ o valor mudou.

**`<input type="checkbox">` e `<input type="radio">`** → dispara **imediatamente** ao clicar.

**`<select>`** → dispara **imediatamente** ao escolher uma opção.


---
**keydown** -> Dispara no momento em que uma tecla é pressionada, antes do caractere aparecer no campo.

`input.addEventListener('keydown', (event) => {` 
`if (event.key === 'Enter'){` 

`console.log('Usuário pressionou Enter!');`

`} if (event.key === 'Escape') {`

`input.value = ''; // limpa o campo }`

`});`

---
```js
DOMContentLoaded
```