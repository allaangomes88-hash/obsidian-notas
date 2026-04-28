```
quando fazemos:  const id= document.getElementById("pensamento-id").value

    const conteudo= document.getElementById("pensamento-conteudo").value.trim()

    const autoria= document.getElementById("pensamento-autoria").value.trim()
```

as variaveis ja estao com o value. Caso eu queira deixar sem value( " " ), eu teria q copiar todo  o elemento e adicionar no final:

```
  document.getElementById("pensamento-id").value=""

    document.getElementById("pensamento-conteudo").value=""

    document.getElementById("pensamento-autoria").value=""
```