**Try/catch é literalmente "tenta / se der erro":**

javascript

```javascript
try {
    // tenta fazer isso aqui
} catch {
    // se der qualquer erro, cai aqui
}
```

---

**Sem try/catch**, se a fake API cair ou der qualquer erro:

javascript

```javascript
const pensamentos = await api.buscarPensamentos() // 💥 erro aqui
pensamentos.forEach(...) // nem chega aqui
// o programa trava e o usuário não vê nada, só um erro no console
```

**Com try/catch:**

javascript

```javascript
try {
    const pensamentos = await api.buscarPensamentos() // 💥 erro aqui
    pensamentos.forEach(...)
} catch {
    alert('Erro ao carregar') // usuário vê isso em vez de tela quebrada
}
```

---

É basicamente um **plano B**. O try é o plano A, o catch é o plano B caso algo dê errado.

---
exemplo usado em [[memoteca]]
```
import api from "../backend/api.js"

  

async function memoriasNaTela(){

    try{

        const containerDeMemoria = document.getElementById("lista-pensamentos")

        const pensamentos = await api.buscarPensamentos()

        pensamentos.forEach(memoria => {

            containerDeMemoria.innerHTML += `<li class="li-pensamento" data-id="${memoria.id}">

            <img src="assets/imagens/aspas-azuis.png" alt="Aspas azuis" class="icone-aspas">

            <div class="pensamento-conteudo">${memoria.conteudo}</div>

            <div class="pensamento-autoria">${memoria.autoria}</div>

            </li>`

        });

   }

    catch{

        alert("Erro ao buscar os dados")

    }

}

```
  
Se a busca dos dados na API for ok ele executa se não ele mostra o erro. se n tivesse a tela iria travar e não mostrar nenhum feedback visual