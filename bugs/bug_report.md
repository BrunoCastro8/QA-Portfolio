## BUG-001

| Campo | Informação |
|-------|------------|
| ID | Bug001 |
| Título | Site não permite login mesmo com dados válidos |
| Ambiente | Sistema: Windows 11<br>Navegador: Chrome 121.0<br>Site: https://www.worten.pt |
| Severidade | Alta |
| Prioridade | Alta |
| Pré-condições | Registo efetuado com sucesso na plataforma<br>Utilizador na página de login |
| Passos para Reproduzir | 1. Abrir página de login<br>2. Introduzir os dados válidos nos campos certos<br>3. Tentativa de login no site |
| Resultado Atual | Mesmo com os dados válidos, o utilizador não consegue fazer login, dando como “dados inválidos” |
| Resultado Esperado | Utilizador introduz os dados válidos nos campos certos e consegue efetuar login com sucesso |
| Evidência | Observado após 5 tentativas e com contas diferentes |


## BUG-002

| Campo | Informação |
|-------|------------|
| ID | Bug-002 |
| Título | Software duplica artigo selecionado no carrinho de compras, apesar de se poder eliminar o artigo duplicado |
| Ambiente | Sistema: Windows 11<br>Navegador: Chrome<br>Site: https://www.worten.pt |
| Severidade | Média |
| Prioridade | Média |
| Pré-condições | Haver artigos na loja online<br>Página do artigo a funcionar<br>Botão de "Adicionar ao carrinho" a funcionar<br>Página "O meu carrinho" a funcionar |
| Passos para Reproduzir | 1. Selecionar um artigo da loja online<br>2. Adicionar ao carrinho de compras<br>3. Entrar na página "O meu carrinho" |
| Resultado Atual | Após a adição de um artigo ao carrinho de compras, este é duplicado |
| Resultado Esperado | Apenas um artigo é adicionado ao carrinho nesta ação |
| Evidência | Teste efetuado 3 vezes |
