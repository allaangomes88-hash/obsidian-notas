em sua forma mais simples de pega algo em uma api: 

```
const fonteDeDdos= "link"

const formatacao= await fetch(fonteDeDados)

-->o fetch busca os dados

const formatada= await formatacao.json( )
-->aqui o json abre os dados
```


---
`const api={`
```

     async buscarPensamentos(){

        try{

            const response= await fetch ("http://localhost:3000/pensamentos")

            return await response.json()

        }catch{

            alert("erro ao ler seus pensamentos")

            throw error

        }

     },
```

se os dados foram buscados corretamente da ok se não mostra um feedback visual [[try e catch]].

---
para buscar estes dados: 
```
import api from "../backend/api.js"

  

async function memoriasNaTela(){

    try{

        const containerDeMemoria = document.getElementById("lista-pensamentos")

        const pensamentos = await api.buscarPensamentos()

        pensamentos.forEach(memoria => criacaoDeMemoria(memoria, containerDeMemoria));

   }

    catch{

        alert("Erro ao buscar os dados")

    }

}
```

como a API estava em outra pasta a gente importa, faz um [[try e catch]] pra validar,
e o pega ali é a UL elemento pai das LI. MASSSSSS primeiro como passamos a VARIAVEL api, precisamos expessificar, falando que na api a gente quer o buscarPensamentos (api.buscarPensamentos).

A criação dos elementos que estao no forEach: [[createElement]]

```
function criacaoDeMemoria(memoria, containerDeMemoria){

    const li=document.createElement("li")

    li.classList.add("li-pensamentos")

    li.setAttribute("data-id", memoria.id)

  

    const img=document.createElement("img")

    img.src= "assets/imagens/aspas-azuis.png"

    img.alt= "Aspas azuis"

    img.classList.add("icone-aspas")

  

    const divPensamento=document.createElement("div")

    div.classList.add("pensamento-conteudo")

    div.textContend= memoria.conteudo

    const divAutoria=document.createElement("div")

    div.classList.add("pensamento-autoria")

    div.textContend= memoria.autoria

  

    li.append(img, divPensamento, divAutoria)

    pensamentos.append(li)

}
```