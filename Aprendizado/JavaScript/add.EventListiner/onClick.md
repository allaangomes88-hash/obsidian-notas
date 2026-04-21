Mesma coisa do addEventListiner, porem ele é menos flexivel:

add.EventListiner Com ele, você pode adicionar mais de um ouvinte para o mesmo evento. Imagine que você quer que o botão exiba um alerta e também mude de cor quando clicado. Confira:

```js

function mostrarAlerta() {
    alert('Botão clicado!');
}

function mudarCor() {
    btnExemplo.style.backgroundColor = 'red';
}

btnExemplo.addEventListener('click', mostrarAlerta);
btnExemplo.addEventListener('click', mudarCor);
```

**onclick:** Se você tentar definir mais de uma ação usando onclick, a última definida é a que permanecerá, sobrescrevendo as anteriores. Veja o risco:

```js

btnExemplo.onclick = function() {
    alert('Botão clicado!');
}

btnExemplo.onclick = function() {
    btnExemplo.style.backgroundColor = 'red';
}
```

Neste caso, apenas a função que muda a cor de fundo será executada. O alerta foi sobrescrito!


---
usado no: [[fokus]]

```
   botaoEditar.onclick= () => {

        const atualizacao= prompt("qual será sua nova tarefa?")

        if(atualizacao){

             tarefa.descricao= atualizacao

            p.textContent= atualizacao

            salvar()

        }

    }
```

se o prompt (atualizacao) tiver um valor ele ira retornar([[if else]]) o tarefa.descricao com o P e salvar ([[localStorage]])