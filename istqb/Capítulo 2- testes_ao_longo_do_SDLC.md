# 2. Testes ao Longo do Ciclo de Vida de Desenvolvimento de Software

## Testes no Contexto dos Ciclos de Vida de Desenvolvimento de Software

Define como as fases do desenvolvimento e os tipos de atividades realizadas no processo se interligam logicamente e cronologicamente.

Modelo de desenvolvimento sequencial (Waterfall, modelo em V)

Modelo de desenvolvimento iterativo (modelo em espiral, criação de protótipos)

Modelo de desenvolvimento incremental (Unified Process)

Também podem ser descritas por métodos de desenvolvimento de software mais detalhados e práticas Agile.

Desenvolvimento orientado para testes de aceitação (ATDD)  
Desenvolvimento orientado para comportamento (BDD)  
Conceção orientada para domínio (DDD)  
EXtreme Programming (XP)  
Desenvolvimento orientado para funcionalidades (FDD)  
Kanban  
Lean IT  
Scrum  
Desenvolvimento orientado para testes (TDD)

---

## Impacto do Ciclo de Vida de Desenvolvimento de Software nos Testes

Os testes são adaptados ao SDLC. Esta escolha, tem impacto nos seguintes aspetos:

- Âmbito e calendarização das atividades de teste (níveis e tipos de teste)
- Nível de detalhe para a documentação de teste
- Escolha das técnicas de teste e abordagens de teste
- Extensão da automação de testes
- Função e responsabilidade do testador

### Nos modelos Sequenciais e nas fases iniciais os testadores participam:
- Revisões de requisitos
- Análises de teste
- Conceções de teste

### Em modelos iterativos e incrementais
Cada iteração fornece um protótipo funcional ou um incremento do produto.

Em cada iteração, os testes dinâmicos e estáticos, podem ser efetuados em todos os níveis.

Logo, cada incremento requer feedback rápido e testes de regressão extensos.

### Modelo Agile
Mudanças ocorrem ao longo do projeto.

É dada preferência à documentação de produto menos detalhada e à automação de testes extensa para simplificar o teste de regressão nos projetos.

Testes exploratórios baseada na experiência.

---

## Ciclo de vida de desenvolvimento de software e boas práticas de teste

### Boas práticas:
- Para cada atividade de desenvolvimento de software existe uma atividade de teste correspondente, havendo assim um controlo de qualidade
- Diferentes níveis de teste, pressupõe objetivos de teste específicos e distintos. Assim, torna-se mais abrangente e evita-se redundâncias.

> "A análise e a conceção de testes para um determinado nível de teste começam durante a fase de desenvolvimento correspondente do SDLC, para que os testes possam aderir ao princípio dos testes antecipados".

Seguir o princípio de encontrar problemas o mais cedo possível.

Os testers ajudam na revisão dos produtos de trabalho, requisitos e documentação, assim que são criados. Conseguem assim, encontrar problemas cedo e apoiar a estratégia shift-left. Os testes são feitos o mais cedo possível no processo.

---

## Testes enquanto orientador do desenvolvimento de software

TDD, ATDD e BDD também executam o princípio dos testes antecipados e seguem uma abordagem shift-left, pois são definidos antes da escrita do código.

Suportam um modelo de desenvolvimento iterativo.

Podem ser executados testes automatizados para assegurar a qualidade do código nas atualizações futuras.

### Características

### TDD
- Orienta a codificação através de casos de teste
- Os testes são escritos em primeiro lugar. Código satisfaz os testes e ambos são restruturados no final.

### ATDD
- Derivam dos critérios de aceitação, fazendo parte do processo de conceção do sistema.
- Os testes são escritos antes da aplicação ser desenvolvida, de forma a os satisfazer.

### BDD
- Expressa o comportamento pretendido de uma aplicação, com casos de teste escritos de uma forma simples e natural, compreensível para os stakeholders, utilizando o formato Given/Then/Then.
- Os casos de teste são automaticamente traduzidos para testes executáveis.

---

## DevOps e Testes

É uma abordagem organizacional que promove a colaboração entre o desenvolvimento (incluindo testes) e as operações de forma a cumprir objetivos comuns.

Os DevOps requerem uma mudança organizacional para suprimir lacunas entre o desenvolvimento e as operações e ao mesmo tempo tratando as suas funções com o mesmo valor.

Isto permite às equipas criar, testar e entregar código de alta qualidade em menor tempo através do pipeline de entrega do DevOps.

QA + Equipa de desenvolvimento.

### Promove também:
- Autonomia da equipa
- Feedback rápido
- Ferramentas integradas
- Integração contínua (CI)
- Entrega contínua (CD)

### Vantagens
- Feedback rápido sobre a qualidade de código
- A CI incentiva os programadores a enviar código de alta qualidade juntamente com testes de componentes e análises estáticas
- Promove processos automatizados como CI/CD para facilitar ambientes de teste estáveis
- Aumenta a visibilidade das características de qualidade não funcional
- Através de um pipeline de entrega, a necessidade de testes manuais é reduzida
- O risco de regressão é minimizado através dos testes de regressão automatizados

### Riscos e Desafios
- Definir e estabelecer o pipeline de entrega do DevOps
- Introduzir e manter as ferramentas de CI/CD
- A automação de testes requer recursos adicionais e pode ser difícil de estabelecer e manter

DevOps inclui muitos testes automatizados, mas não exclui testes manuais na ótica do utilizador.

---

## Abordagem Shift-left

Consiste em testes efetuados mais cedo no SDLC, antes de implementar o código ou da integração dos componentes.

Isto não implica a necessidade de realizar testes mais tarde.

Esta abordagem resulta em formação, esforços e/ou custos adicionais no início, mas espera-se que poupe esforços mais tarde.

### Boas práticas:
- Rever a especificação na perspetiva de teste, de forma a detetar potenciais defeitos
- Escrever casos de teste antes do código e executá-los num equipamento de teste durante a sua implementação
- Utilizar CI e uma melhor CD, pois fornece feedback rápido e fornece testes de componentes automatizados para acompanhar o código-fonte quando este é enviado para o repositório
- Concluir análise estática do código-fonte antes de efetuar teste dinâmico
- Efetuar testes não funcionais no início do nível de teste de componentes, sempre que possível

---

## Retrospetivas e Melhoria de Processos

São reuniões e retrospetivas pós-projeto, realizadas no final do projeto ou iteração, num marco de entrega ou sempre que necessário.

A sua realização depende do modelo de SDLC utilizado.

São importantes para uma melhoria contínua.

### Incluem:
- Testadores
- Programadores
- Arquitetos
- Responsáveis pelos produtos
- Analistas de negócio

### Debatem:
- Quais os aspetos que foram bem-sucedidos e devem ser mantidos?
- Quais os aspetos que não foram bem-sucedidos e devem ser melhorados?
- Como incluir as melhorias e manter os aspetos bem-sucedidos no futuro?

Os resultados são registados e incluídos no relatório de conclusão de teste.

---

## Níveis de Teste e Tipos de Teste

## Níveis de teste

Grupos de atividades de teste organizadas e geridas em conjunto. Cada nível de teste é uma instância do processo de teste.

Estão relacionados com outras atividades do SDLC.

### Teste unitário
- Testa funções/métodos isoladamente e muitas vezes requer suportes específicos, tais como equipamentos de teste ou frameworks de teste unitário
- Realizados normalmente por programadores

### Teste de integração
- Testa comunicação entre módulos/interfaces e as interações entre componentes
- Existe 3 maneiras de testar:
  - Bottom-up (ascendente)
  - Top-down (descendente)
  - Bigbang
- Feito principalmente por QAs (integração de sistemas) e Programadores (integração de componentes)

### Teste de sistema
- Testa o sistema como um todo
- Inclui frequentemente testes funcionais do princípio ao fim e testes não funcionais das características de qualidade
- Pode ser efetuado por uma equipa de teste independente
- Feito por QAs

### Teste de integração de sistemas
- Testa a interface do sistema bem como outros sistemas e serviços externos
- Requer ambientes de teste adequados semelhantes ao ambiente operacional

### Teste de aceitação
Valida se o sistema atende às necessidades.

As principais formas do teste de aceitação são:
- Testes de aceitação de utilizador (UAT)
- Testes de aceitação operacional
- Testes de aceitação contratual e de regulamentação
- Testes alfa
- Testes beta

Feitos por Cliente, Product Owner ou utilizadores-chave.

### Os níveis de teste distinguem-se por:
- Objeto de teste
- Objetivos de teste
- Base para testes
- Defeitos e falhas
- Abordagem e responsabilidade

Para evitar sobreposição de atividades de teste.

---

## Tipos de Teste

### Teste funcional
Testa o que deve ser efetuado pelo objeto de teste.

O objetivo é verificar a completude funcional, correção funcional e adequação funcional.

O site está a fazer o que é suposto? Atende às necessidades do utilizador?

### Teste não funcional
Avalia como o sistema se comporta sob diferentes aspetos que não estão relacionados com a lógica funcional.

O quão bem o sistema se comporta.

O objetivo principal é verificar a qualidade das características não funcionais do software.

Por vezes deve ser feito mais cedo no SDLC.

Em certas situações, dependem de ambientes de teste específicos.

### Norma ISO/IEC
- Eficiência de desempenho
- Compatibilidade
- Usabilidade
- Confiabilidade
- Segurança
- Manutenibilidade
- Portabilidade

Muitos dos testes não funcionais derivam de testes funcionais.

### Exemplo

Teste funcional:  
O botão de login realiza o login?

Teste não funcional:  
O login demora menos de 2 segundos?  
Funciona tanto no telemóvel, como no tablet e no computador?

---

## Teste de caixa preta
Não se preocupam com o código.

É baseado em especificações e concebe os testes a partir da documentação que é externa ao próprio objeto de teste.

O objetivo é verificar o comportamento do sistema em relação às suas especificações.

---

## Testes caixa branca
Testa a estrutura interna do código.

Concebe testes a partir da implementação ou estrutura interna do sistema.

O objetivo é garantir que os diferentes caminhos e partes do programa são executados pelos testes até atingir um nível definido de cobertura.

---

## Teste de confirmação
Confirma se um defeito original foi corrigido com êxito.

Dependendo do risco, é possível efetuar um teste da versão corrigida do software de várias formas:
- Executando todos os casos de teste que falharam anteriormente devido ao defeito
- Adicionando novos casos para abranger todas as alterações necessárias para corrigir o defeito
- Caso haja escassez de tempo, podem ser limitados apenas à realização dos passos que reproduzem a falha e verificar se a falha não ocorre

---

## Teste de regressão
Garantem que as funcionalidades existentes não foram afetadas por alterações ou atualizações no sistema.

As consequências adversas podem afetar o componente que foi alterado, outros componentes do sistema ou até mesmo sistemas que tenham interligação.

É aconselhado efetuar primeiro uma análise de impacto para otimizar a extensão do teste de regressão.

Estes testes devem ser automatizados e devem começar no início do projeto.

Quando a integração contínua (CI) é utilizada, tal como DevOps, deve-se incluir testes de regressão automatizados.

Os testes de confirmação e regressão devem ser efetuados em qualquer nível, se os defeitos forem corrigidos e/ou alterados.

---

## Testes de Manutenção

Pode implicar implementações/lançamentos planeados e não planeados (hot fixes).

Testar as alterações num sistema em produção inclui avaliar o sucesso da implementação da mudança.

### O âmbito dos testes de manutenção depende dos seguintes fatores:
- Grau de risco da alteração
- Dimensão do sistema existente
- Dimensão da alteração

### Triggers
- Modificações (melhorias planeadas/versões), alterações para correção ou hot fixes)
- Atualizações ou migrações do ambiente operacional, testes de conversão de dados
- Desativação, quando uma aplicação atinge o fim da sua vida útil
