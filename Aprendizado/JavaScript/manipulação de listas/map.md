O `map` percorre cada item de um `array` e retorna um `array` novo com o resultado do que vc fez em cada item. [[forEach]]

`const numeros= [1,2,3]`

`const dobrados=numeros.map(num=>num * 2)`

`console.log(dobrados) -> [2,4,6]`
`console.log(numeros) -> [1,2,3] - originar`

--------------------------------------------------------------

`const livros=[` 
`{titulo: "html e css", preco: 49.90}`
`]`

`const titulos= livros.map(livros=>livro.titulo)`

`console.log(titulos)-> "html e css"`

--------------------------------------------------------------------
usado em: [[Projetos/gameShelf/Aprendizado|Aprendizado]]