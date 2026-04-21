Salva coisas que só fazem sentido **enquanto o usuário tá na aba** — se fechar, pode perder sem problema.

Exemplos práticos:

- **Formulário de múltiplos passos** — salva o progresso entre as etapas enquanto o usuário navega pelas páginas do form
- **Filtros de busca** — o usuário filtrou produtos, navega pro detalhe e volta, os filtros ainda tão lá
- **Carrinho temporário** — site que não tem login, o carrinho some ao fechar mesmo
- **Aba de onboarding** — progresso de um tutorial que não precisa persistir

A lógica é: se faz sentido o usuário **perder esses dados ao fechar a aba**, usa sessionStorage. Se precisa lembrar na próxima visita, usa localStorage.

o corpo é literalmente o msm do localStorage, muda apenas o nome