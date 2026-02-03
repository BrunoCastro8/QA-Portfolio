# Capítulo 4 — Análise e Conceção de Testes

## 4.1 Descrição Geral das Técnicas de Teste

As técnicas de teste suportam as análises de teste (o que testar?) e as conceções de teste (como testar?). Contribuem para o desenvolvimento de casos de teste de uma forma sistemática e ajudam o testador a definir as condições de teste, bem como a identificar os itens de cobertura e os dados de teste durante a análise e a conceção do teste.

### Técnicas de Caixa-preta
Não se preocupam com o código. É baseado em especificações e concebe os testes a partir da documentação que é externa ao próprio objeto de teste. O objetivo é verificar o comportamento do sistema em relação às suas especificações. Se existirem alterações na implementação, mas o comportamento necessário permanecer o mesmo, os casos de teste ainda são úteis.

### Técnicas de Caixa-branca
Testa a estrutura interna do código. Concebe testes a partir da implementação ou estrutura interna do sistema. O objetivo é garantir que os diferentes caminhos e partes do programa são executados pelos testes até atingir um nível definido de cobertura.

### Técnicas de Teste Baseadas na Experiência
Realizados sem roteiros definidos, com base na experiência e intuição do tester. “Testar com olhos de utilizador”.

Revela:
- bugs não previstos  
- Ideal para sistemas pouco documentados  
- Complementa testes tradicionais  

---

## 4.2 Técnicas de Teste Caixa-preta

As técnicas de teste caixa-preta frequentemente utilizadas e abordadas nas seguintes secções são:

- Particionamento por Equivalências  
- Análise de Valor Fronteira  
- Teste de Tabelas de Decisão  
- Teste de Transição de Estados  

---

## Particionamento por Equivalências

Em vez de testar todos os valores possíveis, divide-se os valores em grupos que se comportam da mesma forma. Assim, basta testar um exemplo de cada grupo. Se um destes valores testados de cada grupo funcionar ou falhar, os outros do mesmo grupo também irão funcionar ou falhar.

Podem ser identificadas para qualquer dado relacionado com o objeto de teste, incluindo:
- dados de entrada  
- saída  
- dados de configuração  
- valores internos  
- valores relacionados com o tempo  
- parâmetros de interface  

### Tipos de Partições
Podem ter diferentes “formatos”, não se podem sobrepor e têm de ser conjuntos não vazios:

- **Contínuas** — valores que seguem uma escala contínua, normalmente números ou tempo  
- **Discretas** — valores separados em categorias (ex.: tipo de utilizador — cliente, admin, convidado)  
- **Ordenadas** — têm uma ordem lógica (ex.: nível de prioridade — baixa, média, alta)  
- **Não ordenadas** — não existe uma ordem natural (ex.: método de pagamento — MB Way, cartão, PayPal)  
- **Finitas** — têm um número limitado de valores (ex.: idioma do site — PT, EN, ES)  
- **Infinitas** — têm valores sem fim (ex.: quantidade — 1, 2, 3, 4, 5, …)  

Compreender a forma como o objeto de teste irá tratar os diferentes valores é muitas vezes desafiador. A partição deve ser efetuada com atenção.

### Tipos de Partições de Equivalência
- **Partição válida** — valores que devem ser processados pelo objeto de teste ou para os quais a especificação define o processamento esperado  
- **Partição inválida** — valores que devem ser ignorados ou rejeitados pelo objeto de teste ou para os quais não existe processamento definido na especificação  

Na EP, os itens de cobertura são estas partições de equivalência e não os valores individuais. Após o teste de todas as partições identificadas (válidas e inválidas), a cobertura estará a 100%.

---

## Exemplo — Pagamento por Cartão de Débito/Crédito

**Partições: 4 campos**

### 1º campo — Número de Cartão (Discreta / Não ordenada / Finita)
- Válido ou inválido  
- Formato correto ou incorreto  

### 2º campo — CVV (Discreta / Não ordenada / Finita)
- Válido ou inválido  
- 3 ou 4 números / mais ou menos números / formato incorreto  

### 3º campo — Data (Discreta / Não ordenada / Finita)
- Válido ou inválido  
- Data válida futura / expirada / formato incorreto  

### 4º campo — Saldo Interno (Discreta / Ordenada / Finita)
- Disponível ou não disponível  

**Total de Partições:** 8

Se cobrir metade destas partições:  
`4 / 8 = 50%`

Quando um sistema tem vários campos e cada um com as suas partições, um conjunto de casos de teste pode cobrir todas elas através da **Cobertura de Cada Escolha (Each Choice coverage)**. Isto pressupõe que cada partição de cada campo aparece pelo menos uma vez em algum caso de teste, sem necessidade de testar todas as combinações possíveis.

### Casos de Teste

**CT1 — Sucesso**  
- Todos os campos são válidos  

**CT2 — Cartão Inválido**  
- Nº de Cartão — Inválido  
- CVV — Válido  
- Data — Válida  
- Saldo — Suficiente  

**CT3 — CVV Inválido**  
- Nº de Cartão — Válido  
- CVV — Inválido  
- Data — Válida  
- Saldo — Suficiente  

---

## Análise de Valor Fronteira (BVA)

BVA (Boundary Value Analysis) consiste na execução dos valores das fronteiras das partições de equivalência e é apenas utilizada em partições ordenadas. Os valores mínimos e máximos são as fronteiras dessas partições.

Os defeitos comuns encontrados pela BVA estão localizados onde a implementação destas fronteiras está mal colocada. Poderão estar implementadas acima ou abaixo das posições pretendidas ou estão omissas.

### BVA de 2 Valores
Para cada limite entre as partições é testado dois valores:
- o valor fronteira  
- o valor imediatamente fora dela  

A cobertura é atingida quando todos estes valores são executados.

**Exemplo:**  
Idade válida (18–60)  
Valores fronteira possíveis: 17 / 18 / 60 / 61  

Se testar apenas 18 e 60:  
`50% de cobertura`

Se testar todos:  
`100% de cobertura`

### BVA de 3 Valores
Para cada limite entre as partições são testados 3 valores:
- o valor fronteira  
- o valor vizinho dentro da partição  
- o valor vizinho fora da partição  

Neste caso, conseguimos detetar defeitos que não seriam encontrados apenas testando valores no limite e fora da fronteira.

**Exemplo:**  
Idade válida (18–60)  
Valores fronteira possíveis: 17 / 18 / 19 / 59 / 60 / 61  

Se testar apenas 18 e 60:  
`33% de cobertura`

Se testar todos:  
`100% de cobertura`

---

## Teste de Tabelas de Decisão

As tabelas de decisão focam-se na combinação de condições de entrada que resultam em diferentes ações ou resultados de saída. São uma forma eficaz de sistematizar lógicas complexas, como pode ser o caso da implementação de regras de negócio.

Uma tabela de decisão completa tem colunas suficientes para cobrir todas as combinações possíveis de condições, seja combinações exequíveis ou inexequíveis.

### Estrutura da Tabela
- **Condições (entradas)** — Linhas da tabela  
- **Ações (resultados)** — Linhas da tabela  
- **Regras de decisão / Itens de cobertura** — Colunas da tabela  

Nas tabelas com entradas limitadas, os valores são booleanos (verdadeiro / falso).  
Quando as entradas são alargadas, podem assumir:
- intervalos de números  
- partições de equivalência  
- valores discretos  

A cobertura total é alcançada quando se divide o número de colunas executadas pelo número total de colunas exequíveis, expresso em percentagem.

Este tipo de teste proporciona uma abordagem sistemática para:
- Identificar combinações negligenciadas  
- Detetar lacunas nos requisitos  
- Encontrar contradições nas regras de negócio  

Quando existem muitas condições, a tabela pode ser reduzida:
- Eliminando colunas com combinações inexequíveis  
- Juntando colunas onde algumas condições não afetam o resultado  

---

## Teste de Transição de Estados

Um caso de teste num diagrama de transição de estados ou numa tabela de estados é representado como uma sequência de eventos que resulta em alterações de estados (e ações, se aplicável). Um caso de teste pode abranger várias transições entre estados.

### Diagrama de Transição de Estados
Modela o comportamento de um sistema ao mostrar:
- os possíveis estados  
- as transições válidas  

Uma transição é iniciada por um evento e pode ser qualificada por uma condição de guarda e levar a uma ação.

**Formato:**  
`Evento → Condição de guarda → Ação`

### Tabela de Estados
- **Linhas** — Estados  
- **Colunas** — Eventos (e condições de guarda, se existirem)  
- **Células** — Estado de destino, condições de guarda e ações  
- **Células vazias** — Transições inválidas  

---

## Critérios de Cobertura — Teste de Estados

### Cobertura de Todos os Estados
- **Itens de cobertura:** Estados  
- Para 100% de cobertura, todos os estados devem ser percorridos pelos casos de teste  
- Medição:  
  `Número de estados percorridos / Número total de estados`

### Cobertura de Transições Válidas (0-switch)
- **Itens de cobertura:** Transições válidas  
- Para 100% de cobertura, todas as transições válidas devem ser executadas  
- Medição:  
  `Número de transições válidas executadas / Número total de transições válidas`

### Cobertura de Todas as Transições
- **Itens de cobertura:** Transições válidas e inválidas  
- Para 100% de cobertura, devem ser executadas todas as transições válidas e tentadas todas as inválidas  
- Medição:  
  `Número de transições válidas e inválidas executadas / Número total de transições`

A cobertura de todos os estados é mais fraca que a cobertura de transições válidas, pois pode ser obtida sem executar todas as transições. A cobertura de transições válidas é o critério mais utilizado. A cobertura de todas as transições é recomendada para software crítico em termos de funcionalidade e segurança.

