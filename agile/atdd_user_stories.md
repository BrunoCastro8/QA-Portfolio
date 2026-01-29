# Abordagens de Teste Baseadas na Colaboração

Concentra-se em evitar os defeitos através de colaboração e comunicação.

---

## Escrita de User Stories Colaborativas

A user story representa uma característica valiosa para o utilizador ou comprador de sistema ou software. Estas incluem três aspetos importantes, denominados de **“3 C’s”**:

- **Cartão**  
  Suporte onde está escrito a story (normalmente ticket)

- **Conversão**  
  O que a equipa discute sobre ela. Explica a forma como o software será utilizado (documentada ou verbalizada)

- **Confirmação**  
  Critérios de aceitação

---

## Formato Mais Utilizado

Enquanto (função), pretendo (objetivo a utilizar), para poder (valor de negócio resultante da função), seguido dos critérios de aceitação.

### Exemplo

**User Story:**
> Enquanto utilizador, quero adicionar um artigo ao carrinho de compras para poder comprá-lo mais tarde.

---

## Critérios de Aceitação

### Checklist
- O utilizador deverá estar logado  
- O artigo deverá estar disponível  
- Após selecionar o artigo, este deverá ser direcionado para o carrinho  
- O carrinho deve conter o artigo selecionado  
- Caso não esteja, deverá aparecer mensagem de erro  

### Cenário (BDD – Given/When/Then)
> Dado que o utilizador está logado e o artigo está disponível,  
> quando o utilizador adiciona o artigo ao carrinho,  
> então este deve aparecer no carrinho.

---

## Colaboração na Escrita da User Story

Uma user story deve ser escrita em conjunto, onde todos dão ideias livremente. Vista pelas três perspetivas:
- Negócio  
- Programadores  
- QA  

Assim fica mais fácil terem a mesma visão do que vai ser desenvolvido e testado.

---

## Características de uma Boa User Story

Uma boa user story deve ser:
- Independente  
- Negociável  
- Valiosa  
- Estimável  
- Pequena  
- Testável  

---

## Critérios de Aceitação — Definição

São condições que uma implementação da user story deve cumprir para ser aceite pelos stakeholders. São as condições de teste que devem ser executadas por estes testes.  
Valida se o sistema atende às necessidades dos stakeholders. Validações feitas com a perspetiva do cliente ou utilizador final.

### São utilizados para:
- Definir o âmbito da user story  
- Obter um consenso entre os stakeholders  
- Descrever os cenários positivos e negativos  
- Servir como base para testes de aceitação  
- Permitir estimativas e planeamentos exatos  

---

## Formatos Mais Comuns

- **Orientado para cenários**  
  Given/When/Then (utilizado em BDD)

- **Orientado para regras**  
  Checklist com tópicos ou tabela com mapeamento entre entrada-saída

---

## Desenvolvimento Orientado para Testes de Aceitação (ATDD)

Nesta abordagem, os casos de teste são criados antes da implementação da user story.  
São criados pelos membros da equipa com a perspetiva de cliente, programador e testadores.  
Podem ser executados manualmente ou automatizados.

### Processo

O primeiro passo é a criação da user story e dos critérios de aceitação.  
É um workshop onde se debate, analisa e se documenta estes, pelos membros da equipa.

Posteriormente, são criados casos de teste efetuados por toda a equipa ou apenas pelos testadores.

Os casos de teste devem ser expressos de uma forma compreensível e com linguagem natural.  
São baseados nos critérios de aceitação e podem ser vistos como exemplos de funcionamento do software.

Incluem:
- Pré-condições (se existirem)  
- Entradas  
- Pós-condições  

---

## Estratégia de Criação dos Casos de Teste

Geralmente:
- Primeiro são criados os casos de teste **positivos**, confirmando o comportamento correto  
- Depois os casos de teste **negativos**  
- Por último, são abrangidas as características de qualidade **não funcionais**  
  - Eficiência no desempenho  
  - Usabilidade  

Os casos de teste devem abranger todas as características da user story e não devem exceder o seu conteúdo.  
Não deve existir casos de teste duplicados.

---

## Automação no ATDD

Quando os casos de teste são escritos num formato que a framework de testes consegue ler e executar, os programadores conseguem automatizar esses testes e escrever o código dos testes ao mesmo tempo que desenvolvem a funcionalidade descrita na user story.
## Fluxo da User Story (ATDD)

User story → Workshop (analisar, debater, clarificar critérios) → Criar casos de teste → Escrever código → Executar código

---

## Papel do QA na User Story

- Validar os critérios de aceitação  
- Identificar possíveis cenários negativos e casos limite  
- Garantir que não há equívocos ou incertezas nos requisitos  
- Ajudar a equipa a transformar os critérios em casos de teste  
- Apoiar a criação de testes automatizados quando possível  
