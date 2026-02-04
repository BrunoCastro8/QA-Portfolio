# Descrição Geral das Técnicas de Teste

## 1. Introdução

As técnicas de teste suportam as análises de teste (o que testar?) e as conceções de teste (como testar?). Contribuem para o desenvolvimento de casos de teste de uma forma sistemática e ajudam o testador a definir as condições de teste, bem como a identificar os itens de cobertura e os dados de teste durante a análise e a conceção do teste.

## 2. Tipos de Técnicas de Teste

### 2.1 Técnicas de caixa-preta

Não se preocupam com o código. É baseado em especificações e concebe os testes a partir da documentação que é externa ao próprio objeto de teste. O objetivo é verificar o comportamento do sistema em relação às suas especificações. Se existirem alterações na implementação, mas o comportamento necessário permanecer o mesmo, os casos de teste ainda são úteis.

### 2.2 Técnicas de caixa-branca

Testa a estrutura interna do código. Concebe testes a partir da implementação ou estrutura interna do sistema. O objetivo é garantir que os diferentes caminhos e partes do programa são executados pelos testes até atingir um nível definido de cobertura.

### 2.3 Técnicas de teste baseadas na experiência

Realizados sem roteiros definidos, com base na experiência e intuição do tester. “Testar com olhos de utilizador”. O nível de eficácia destas técnicas depende muito das competências do testador. Revela:

- bugs não previstos
- Ideal para sistemas pouco documentados
- Complementa testes tradicionais

## 3. Técnicas de Teste Caixa-Preta

As técnicas de teste caixa-preta frequentemente utilizadas e abordadas nas seguintes secções são:

- Particionamento por Equivalências
- Análise de Valor Fronteira
- Teste de Tabelas de Decisão
- Teste de Transição de Estados

## 4. Particionamento por Equivalências

Em vez de testar todos os valores possíveis, divide-se os valores em grupos que se comportam da mesma forma. Assim, basta um testar um exemplo de cada grupo. Se um destes valores testados de cada grupo funcionar ou falhar, os outros do mesmo grupo, também irão funcionar ou falhar.

Podem ser identificadas qualquer dado relacionado com o objeto de teste, incluindo dados de entrada, saída, dados de configuração, valores internos, valores relacionados com o tempo e perâmetros de interface.

Podem ter diferentes “formatos”, não se podem sobrepor e têm de ser conjuntos não vazios:

- Contínuas – valores que seguem uma escala contínua, normalmente números ou tempo
- Discretas – valores separados em categorias, exemplo, tipo de utilizador (cliente, admin, convidado)
- Ordenadas – têm uma ordem lógica, exemplo, Nível de prioridade (baixa-média-alta)
- Não ordenadas – não existe uma ordem natural, exemplo, método de pagamento (MB Way, cartão, paypal)
- Finitas – têm um nº limitado de valores, exemplo, Idioma de site (PT, EN, ES)
- Infinitas – Têm valores sem fim, exemplo, Quantidade (1,2,3,4,5,... sem limite)

Compreender a forma como o objeto de teste irá tratar os diferentes valores é muitas vezes desafiador. A partição deve ser efetuada com atenção.

### 4.1 Partição válida

Partição de equivalência com valores válidos. Podem ser interpretados como os valores que devem ser processados pelo objeto de teste ou como os valores em que a especificação define o processamento esperado.

### 4.2 Partição invalida

Partição de equivalência com valores inválidos. Podem ser interpretados como valores que devem ser ignorados ou rejeitos pelo objeto de teste ou como os valores em que não existe nenhum processamento definido na especificação.

NA EP, os itens de cobertura são estas partições de equivalência e não os valores individuais. Após o teste de todas as partições identificadas, a cobertura estará a 100% (válidas e invalidas).

### 4.3 Exemplo

Regra – Pagamento por cartão de débito/crédito

Partições: 4 campos

1º campo – Número de cartão (Discreta/não ordenada e finita)
Válido ou inválido  
Formato correto ou incorreto

2º campo – CVV (Discreta/não ordenada e finita)
Válido ou inválido  
3 ou 4 números / mais ou menos números ou Formato incorreto

3º campo – Data (Discreta/não ordenada e finita)
Válido ou inválido  
Data válida futura / expirada ou no formato incorreto

4º campo – Saldo interno (Discreta/ordenada e finita)
Disponível ou não disponível

Total de Partições: 8  
Se cobrir metade destas partições – 4:8 = 50%

Quando um sistema tem vários campos e cada um com as suas partições, um conjunto de casos de teste pode cobrir todas elas, através da “Cobertura de cada escolha” (Each Choice coverage). Isto pressupõe que cada partição de cada campo, aparece pelo menos uma vez em algum caso de teste, sem necessidade de testar todas as combinações possíveis.

CT1 – Sucesso  
Todos os campos são válidos

CT2 – Cartão Inválido  
Nº de Cartão – Inválido  
CVV – Válido  
Data – Válida  
Saldo – Suficiente

CT3 – CVV inválido  
Nº de cartão – Válido  
CVV – Inválido  
Data – Válida  
Saldo – Suficiente

...

## 5. Análise de Valor Fronteira

BVA – Boundary Value Analysis, consiste na execução dos valores das fronteiras das partições de equivalência e é apenas utilizada em partições ordenadas. Os valores mínimos e máximos são as fronteiras dessas partições. Os defeitos comuns encontrados pela BVA estão localizados onde a implementação destas fronteiras está mal colocada. Poderão estar implementadas acima ou abaixo das posições pretendidas ou estão omissas.

### 5.1 BVA de 2 valores

Para cada limite entre as partições é testado dois valores: o valor fronteira mais o valor imediatamente fora dela. A cobertura é atingida quando todos estes valores são executados.

Exemplo:  
Idade válida (18-60)  
Valores fronteira possíveis – 17 / 18 / 60 / 61

Se testar apenas 18 e 60 testei apenas 50% de cobertura  
Se testei todos – 100% de cobertura

### 5.2 BVA de 3 valores

Para cada limite entre as partições é testados 3 valores: o valor fronteira mais os valores vizinhos dentro e fora dela. Neste caso, conseguimos detetar defeitos que não seriam encontrados apenas testando valores no limite e valores fora do da fronteira.

Exemplo:  
Idade válida (18-60)  
Valores fronteira possíveis – 17 / 18 / 19 / 59 / 60 / 61

Se testar apenas 18 e 60, testei apenas 33% de cobertura  
Se testei todos – 100% de cobertura
## 6. Teste de Tabelas de Decisão

As tabelas de decisão focam-se na combinação de condições de entrada que resultam em diferentes ações ou resultados de saída. São uma forma eficaz de sistematizar lógicas complexas, como pode ser o caso da implementação de regras de negócio. Uma tabela de decisão completa tem colunas suficientes para cobrir todas as combinações possíveis de condições, seja combinações exequíveis ou inexequíveis.

Começa-se por definir as condições (entradas) e ações (resultados) resultantes do sistema (linhas da tabela)

Regras de decisão ou itens de cobertura (Colunas da tabela)

Estas definem combinações únicas de condições. Nas tabelas de decisão com entradas limitadas, todos os valores das condições e ações, são apresentados com valores booleanos (verdadeiro ou falso). Quando as entradas são alargadas, algumas ou todas as condições e ações podem também assumir vários valores (intervalos de números, partições de equivalência, valores discretos, ...)

Neste caso a cobertura total é alcançada quando se divide o número total de colunas executadas pelo número total de colunas exequíveis, expresso em percentagem.

Este tipo de teste proporciona uma abordagem sistemática para:

- Identificar combinações que poderiam ser negligenciadas
- Detetar lacunas nos requisitos
- Encontrar contradições nas regras de negócio

Caso haja muitas condições, o que leva à execução de muitas regras de decisão e muito tempo, pode-se reduzir o número de regras a ser executadas, utilizando uma tabela de decisão minimizada ou uma abordagem baseada na avaliação do risco.
“A tabela pode ser simplificada ao eliminar as colunas que contêm combinações inexequíveis de condições. A tabela também pode ser minimizada ao juntar colunas, nas quais algumas das condições não afetam o resultado, numa única coluna.”

## 7. Teste de Transição de Estados

Um caso de teste num diagrama de transição de estados e numa tabela de estados é representado como uma sequência de eventos, resultando em alterações de estados (e ações, se aplicável). Um caso de teste, por norma, pode abranger várias transições entre estados.

### 7.1 Diagrama de transição de estados

Modela o comportamento de um sistema ao mostrar os possíveis estados e as transições de estados válidas. Uma transição instantânea é iniciada por um evento que pode ser adicionalmente qualificada por uma condição de guarda e podem levar o software a tomar uma ação.

Evento → Condição de guarda → Ação

### 7.2 Tabela de estados

Filas – Estados  
Colunas – Eventos, juntamente com as condições de guarda, se existirem  
Células – Entradas de tabela. Representam transições e contêm o estado de destino, bem como as condições de guarda e as ações resultantes, se definidas  
Células vazias – Transições invalidas

## 8. Critérios de Cobertura no Teste de Transição de Estados

### 8.1 Cobertura de todos os estados

Itens de cobertura – Estados

Para 100% de cobertura, todos os estados têm de ser assegurados por casos de teste.

Número de estados percorridos, dividido pelo número total de estados, normalmente expresso em percentagem.

### 8.2 Cobertura de transições válidas (cobertura 0-switch)

Itens de cobertura – Transições válidas numa perspetiva individual

Para obter 100% de cobertura de transições válidas, os casos de teste têm de executar todas as transições válidas.

Número de transições válidas executadas, dividido pelo número total de transições válidas, em percentagem.

### 8.3 Cobertura de todas as transições

Itens de cobertura – Todas as transições apresentadas na tabela de estados

Para obter 100% de cobertura de todas as transições, os casos de teste têm de executar todas as transições válidas e tentar executar todas as transições inválidas.

Número de transições válidas e inválidas executadas ou com tentativa de execução, dividido pelo número total de transições válidas e inválidas, em percentagem.

A cobertura de todos os estados é mais fraca que a cobertura de transições válidas, pois pode ser obtida sem executar todas as transições. A cobertura de transições válidas é o critério mais utilizado e assegura a cobertura total de todos os estados. A cobertura de todas as transições assegura a cobertura total de todos os estados e a cobertura total de transições válidas e deve ser requisito mínimo para o software crítico em termos de funcionalidade e de segurança.
