
Os dois adicionam elementos filhos. As diferenças são:

**`appendChild`** — só aceita um nó por vez, e não aceita texto puro:

```js
ul.appendChild(li) // ✅
ul.appendChild("texto") // ❌ erro
```

**`append`** — mais flexível, aceita múltiplos elementos e texto puro:


```js
ul.append(li1, li2, li3) // ✅ vários de uma vez
ul.append("texto simples") // ✅ funciona
```

o append faz mais que o appendChild faz. É mais moderno usa-lo

---
Usado no projeto [[fokus]]

```
    const p = document.[[createElement]]("p")

    p.classList.add("app__section-task-list-item-description")

    p.textContent = tarefa.descricao
    
     const svg = document.createElement("svg")
    svg.innerHTML = `<svg class="app__section-task-icon-status" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">

        <circle cx="12" cy="12" r="12" fill="#FFF"></circle>

        <path d="M9 16.1719L19.5938 5.57812L21 6.98438L9 18.9844L3.42188 13.4062L4.82812 12L9 16.1719Z" fill="#01080E"></path>

    </svg>`
    const botaoEditar = document.createElement("button")

    botaoEditar.classList.add("app_button-edit")

    const imagemDoBotao = document.createElement("img")

    imagemDoBotao.setAttribute("src", "/imagens/edit.png")

    botaoEditar.append(imagemDoBotao)

    li.append(svg)

    li.append(p)

    li.append(botaoEditar)

    return li

```
}

O append dentro da li COLOCOU na ordem, svg, p, botaoEditar ficando assim:

```html
<li class="app__section-task-list-item">
    <svg>
        <svg class="app__section-task-icon-status" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="12" cy="12" r="12" fill="#FFF"></circle>
            <path d="M9 16.1719L19.5938 5.57812L21 6.98438L9 18.9844L3.42188 13.4062L4.82812 12L9 16.1719Z" fill="#01080E"></path>
        </svg>
    </svg>
    <p class="app__section-task-list-item-description">
        Estudando localStorage
    </p>
    <button class="app_button-edit">
        <img src="/imagens/edit.png">
    </button>
</li>
```

o svg que a gente cria, fica sendo pai do outro svg que está com o class