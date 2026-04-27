em sua forma mais simples de pega algo em uma api: 

```
const fonteDeDdos= "link"

const formatacao= await fetch(fonteDeDados)

-->o fetch busca os dados

const formatada= await formatacao.json( )
-->aqui o json abre os dados
```