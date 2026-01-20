# Casos de Teste — E-commerce Worten

Este documento contém uma suite de testes manuais criada como exercício prático de QA para simular um ambiente real de testes num site de e-commerce.

## Índice
- TC-LOGIN-001 — Login com dados válidos
- TC-LOGIN-002 — Login com dados inválidos
- TC-CARRINHO-003 — Adicionar ao carrinho
- TC-PESQUISA-004 — Pesquisa de produtos
- TC-SEGURANCA-005 — Alterar palavra-passe/verificação de funcionamento de requisitos de palavra-passe. 

## Contexto
Site testado: https://www.worten.pt  
Tipo de testes: Funcionais e Não Funcionais  
Ferramenta: Manual (documentação em Markdown)  
Ambiente: Produção (simulação)

## ID: TC-LOGIN-001  
**Título:** Login com dados válidos  

### Pré-requisitos
- Ter registo no site  
- Página de login aberta  

### Passos
1. Inserir dados válidos nos campos corretos (email e palavra-passe)  
2. Clicar no botão de login  

### Resultado Esperado
- Ser redirecionado para a página inicial com o login realizado com sucesso  

## ID: TC-LOGIN-002  
**Título:** Login com dados inválidos  

### Pré-requisitos
- Ter registo no site  
- Página de login aberta  

### Passos
1. Inserir dados inválidos nos campos de email e palavra-passe  
2. Clicar no botão de login  

### Resultado Esperado
- Apresentar uma mensagem de erro na página de login, por exemplo:  
  "A tua palavra-passe não está correta. Recuperar palavra-passe"

## ID: TC-CARRINHO-003  
**Título:** Artigos selecionados são inseridos no carrinho de compras  

### Pré-requisitos
- Haver artigos disponíveis para compra  
- Página do artigo a funcionar  
- Botão para adicionar ao carrinho visível  

### Passos
1. Escolher um artigo para compra  
2. Na página do artigo, clicar em "Adicionar ao carrinho"  

### Resultado Esperado
- O artigo é adicionado ao carrinho de compras com sucesso  

## ID: TC-PESQUISA-004  
**Título:** Motor de pesquisa da página em funcionamento  

### Pré-requisitos
- Secção de motor de pesquisa visível  
- Campo de pesquisa disponível para escrita  

### Passos
1. Clicar no motor de pesquisa  
2. Escrever o nome de um artigo  
3. Confirmar a pesquisa (Enter ou botão de pesquisa)  

### Resultado Esperado
- Ser redirecionado para uma página com as opções de compra relacionadas com o artigo pesquisado  

## ID: TC-SEGURANCA-005  
**Título:** Verificar se os requisitos de palavra-passe estão a funcionar  

### Pré-requisitos
- Realizar login no site  
- Página das definições de conta / gerir logins em funcionamento  
- Botão "Alterar palavra-passe" disponível  
- Campos "Palavra-passe atual", "Nova palavra-passe" e "Confirmar nova palavra-passe" disponíveis  
- Requisitos para criação de palavra-passe visíveis para o utilizador  

### Passos
1. Após efetuar login no site, entrar na Área Pessoal do utilizador  
2. Escolher a opção "Gestão de logins" dentro da opção "Conta"  
3. Clicar em "Alterar palavra-passe"  
4. Preencher o campo "Palavra-passe atual"  
5. Escolher uma "Nova palavra-passe"  
6. Confirmar a "Nova palavra-passe"  

### Resultado Esperado
- Após clicar no campo "Nova palavra-passe", o utilizador deverá visualizar os requisitos para escolher uma palavra-passe  
- Após a alteração e com os requisitos cumpridos, a alteração deverá ser realizada com sucesso  
