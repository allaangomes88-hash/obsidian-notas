
`e` é o objeto do evento — ele guarda tudo que aconteceu no clique (posição do mouse, tecla pressionada, etc). E `target` é uma propriedade dele que aponta pro elemento que disparou o evento.

```js
li.addEventListener("click", (e) => {
    console.log(e.target) // o elemento clicado
})
```
[[Eventos]]

`e` é o objeto do evento — ele guarda tudo que aconteceu no clique (posição do mouse, tecla pressionada, etc). E `target` é uma propriedade dele que aponta pro elemento que disparou o evento.

```js
input.addEventListener("keydown", (e) => {
    console.log(e.target) // o input que recebeu a tecla
    console.log(e.key)    // qual tecla foi pressionada
})
```


```js
form.addEventListener("submit", (e) => {
    e.preventDefault()
    console.log(e.target) // o form que foi submetido
})
```

Em qualquer evento o `e.target` é sempre o elemento que disparou — só muda o tipo de evento (`keydown`, `submit`, `input`, `focus`...).