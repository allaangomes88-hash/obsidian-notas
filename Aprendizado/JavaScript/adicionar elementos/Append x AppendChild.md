
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

    const p = document.[[createElement]]("p")

    p.classList.add("app__section-task-list-item-description")

    p.textContent = tarefa.descricao

    const botaoEditar = document.createElement("button")

    botaoEditar.classList.add("app_button-edit")

    const imagemDoBotao = document.createElement("img")

    imagemDoBotao.setAttribute("src", "/imagens/edit.png")

    botaoEditar.append(imagemDoBotao)

    ==li.append(svg)==

    ==li.append(p)==

    ==li.append(botaoEditar)==

    return li

}

O app