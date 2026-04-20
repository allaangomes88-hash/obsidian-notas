Ordena os elementos de um array **no próprio array** (modifica o original).

### Com função de comparação

A função recebe dois elementos (`a` e `b`) e decide a ordem com base no retorno:

| Retorno             | Resultado            |
| ------------------- | -------------------- |
| número **negativo** | `a` vem antes de `b` |
| número **positivo** | `b` vem antes de `a` |
| `0`                 | mesma posição        |


```js
// Ordem crescente
numeros.sort((a, b) => a - b);
console.log(numeros); // [2, 5, 10, 30] ✅

// Ordem decrescente
numeros.sort((a, b) => b - a);
console.log(numeros); // [30, 10, 5, 2] ✅
```

### Ordenando strings corretamente

js

```js
const nomes = ['Carlos', 'Ana', 'Bruno'];

nomes.sort((a, b) => a.localeCompare(b));
console.log(nomes); // ['Ana', 'Bruno', 'Carlos'] ✅
```

> `localeCompare` respeita acentos e caracteres especiais