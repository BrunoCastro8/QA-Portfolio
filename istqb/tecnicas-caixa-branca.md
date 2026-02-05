# Técnicas de Teste Caixa-Branca

Testa a estrutura interna do código. Concebe testes a partir da implementação ou estrutura interna do sistema. O objetivo é garantir que os diferentes caminhos e partes do programa são executados pelos testes até atingir um nível definido de cobertura.

Existem técnicas rigorosas para ambientes críticos de segurança e funcionalidade ou que exigem ambientes de elevada integridade, permitindo obter uma cobertura de código mais abrangente. Existe também técnicas muito utilizadas em níveis de teste mais elevados como o exemplo, testes de API.

## Exemplos de técnicas de teste caixa-branca

- Teste de instruções  
- Teste de ramos  

## Teste de Instruções e Cobertura de Instruções

**Itens de cobertura**  
- Instruções executáveis  

**Objetivo**  
- Conceber casos de teste que executem instruções no código até ser obtido um nível de cobertura aceitável  

**Medida como**  
- O número de instruções executáveis pelos casos de teste, dividido pelo número total de instruções executáveis no código, em percentagem  

Após 100% de cobertura de instruções, é possível assegurar que todas elas foram executadas, pelo menos, uma vez. Isto permite que instruções com defeito sejam executadas e, com isto, mostrar os defeitos presentes. Mas não significa que o programa foi bem testado. Pode ocorrer erros derivados de decisões lógicas que não foram testadas, bem como defeitos dependentes dos dados como por exemplo, divisão por zero.

## Teste de Ramos e Cobertura de Ramos

Um ramo é um caminho possível que o programa pode seguir entre duas instruções. Estes caminhos estão presentes no grafo de fluxo de controlo, que é um diagrama. Esses caminhos podem ser sempre executados (incondicional) ou depender de decisões(condicional).

**Itens de cobertura**  
- Ramos  

**Objetivo**  
- Conceber casos de teste para executar os ramos no código até ser obtido um nível de cobertura aceitável  

**Medida como**  
- Número de ramos executados pelos casos de teste, dividido pelo número total de ramos, em percentagem  

Após 100% de cobertura de ramos, todos os ramos no código, incondicionais e condicionais, são executados pelos casos de teste. Os ramos condicionais correspondem normalmente a um resultado de verdadeiro ou falso, a partir de uma decisão “se...então/if...else”, “caso/switch” ou uma decisão para sair ou continuar num ciclo.

Executar um ramo com um caso de teste, não significa detetar defeitos em todos os casos. Não garante que todos os caminhos completos do código foram percorridos e todos os defeitos expostos. Por vezes, só aparecem numa sequência específica de ramos ou em certas decisões combinadas de uma certa forma.

A cobertura de ramos inclui a cobertura de instruções. Casos de teste que obtenham 100% de cobertura de ramos também obtém 100% de cobertura de instruções.

## Valor do Teste de Caixa-Branca

Um ponto forte das técnicas de teste de caixa-branca é o facto de que toda a implementação do software foi considerada nos testes, o que facilita de deteção de defeitos mesmo quando a especificação de software é vaga, desatualizada ou incompleta. O seu ponto fraco poderá ser o facto de o software não implementar um ou mais requisitos, o que faz com que o teste não detete os defeitos por omissão.

As técnicas de caixa-branca podem ser utilizadas nos testes estáticos. Estas, são adequadas para revisão de código que ainda não está para execução, revisão de pseudocódigo e outras lógicas de alto nível ou lógicas top-down.

Ao contrário dos testes de caixa-preta, os testes de caixa-branca, fornecem uma medição objetiva da cobertura de código e disponibilizam as informações necessárias para permitir a criação de testes adicionais para aumentar esta cobertura e, consequentemente, aumentar a confiança no código.
