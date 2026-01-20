Criei este documento como exercício prático de Qa manual e foquei-me em exemplos reais aplicados num site de e-commerce.

# Tipos de Teste — Caso de Estudo: Worten

Este documento apresenta exemplos práticos de diferentes tipos de teste aplicados ao site da Worten.

---

## Testes Funcionais

O site está a fazer o que é suposto?  
Atende às necessidades do utilizador?

### Testar Login
- Testar se ao clicar no botão de login sou redirecionado para a página de login  
- Testar se os meus dados estão efetivamente inseridos na base de dados do servidor, como o email e a palavra-passe  
- Testar se, ao inserir dados inválidos, o site deteta o erro  
- Testar se ao clicar no botão de login o sistema faz efetivamente o meu login  

### Testar Carrinho de Compras
- Testar se o botão de adicionar ao carrinho funciona  
- Verificar se o artigo fica realmente adicionado ao carrinho  

### Testar Motor de Pesquisa
- Quando pesquiso “telemóveis”, verificar se sou redirecionado para uma página com telemóveis à venda  

---

## Testes Não Funcionais

Como o site se comporta em relação ao desempenho, usabilidade e segurança?

### Testar Desempenho
- Testar o tempo de resposta ao carregar uma página no site  

### Testar Usabilidade
- Testar se a navegação pela página é intuitiva para o utilizador  

### Testar Segurança
- Testar se o servidor aceita palavras-passe fracas  

---

## Teste de Regressão

As funcionalidades do site foram afetadas por uma atualização?

### Caso Hipotético
Após uma nova atualização do site:

### Testar Login
- Verificar se o login continua a funcionar corretamente  

### Testar Carrinho de Compras
- Verificar se os artigos continuam a ser adicionados ao carrinho  

### Testar Métodos de Pagamento
- Verificar se o processo de pagamento não foi afetado pela atualização  

---

## Teste Exploratório

Teste para encontrar erros incomuns.  
Erros que possam surgir por comportamentos inesperados do utilizador.

- Testar se ao inserir dados inválidos nos formulários o site deteta os erros  
  - Exemplo: escrever letras em campos de preços  
- Verificar o que acontece se eu clicar no mesmo botão 5 vezes seguidas  
- Usar o site em vários formatos de ecrã (telemóvel e computador)  
- Verificar se ao rodar o ecrã no telemóvel o design é afetado  
