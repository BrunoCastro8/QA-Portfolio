# Syllabus ISTQB — Capítulo 1  
**Resumo pessoal — Fundamentos de Testes de Software**

---

## Introdução

Um software que não funciona provoca perdas de tempo, dinheiro, reputação profissional e, em casos mais graves, ferimentos ou morte. Por isso, os testes de software avaliam a qualidade do software e ajudam a reduzir o risco de falha do mesmo em funcionamento.

São um conjunto de atividades que têm o propósito de detetar defeitos e avaliar a qualidade dos componentes do software. Componentes estes que são conhecidos como objetos de teste.

Os testes verificam se o sistema cumpre os requisitos específicos, mas também validam se o sistema satisfaz as necessidades dos utilizadores e dos outros stakeholders.

---

## Tipos de Testes

Os testes podem ser dinâmicos ou estáticos:

### Testes Dinâmicos
- Requerem a execução do software  
- Utilizam vários tipos de técnicas e abordagens de teste para criar casos de teste

### Testes Estáticos
- Incluem revisões e análises estáticas

---

## Planeamento e Perfil do Testador

Os testes são planeados, geridos, calculados, monitorizados e controlados.

Os testadores utilizam ferramentas, mas necessitam de conhecimento especializado, componentes analíticas e aplicar pensamento crítico e sistémico (Myers 2011 e Roman 2018).

---

## Objetivos de Teste

- Avaliar produtos de trabalho, tais como requisitos, user stories, conceções e código  
- Encontrar falhas e defeitos  
- Assegurar a cobertura requerida do objeto de teste  
- Reduzir o nível de risco de software com qualidade inadequada  
- Verificar se todos os requisitos especificados foram cumpridos  
- Verificar se o objeto de teste cumpre os requisitos contratuais, legais e regulamentares  
- Fornecer informação aos stakeholders para que possam tomar decisões informadas  
- Aumentar a confiança na qualidade do objeto de teste  
- Validar se o objeto de teste está concluído e funciona como esperado pelos stakeholders  

Estes objetivos podem variar dependendo do contexto. Isto inclui o produto de trabalho que está a ser testado, o nível de teste, os riscos, o SDLC a ser seguido e o contexto empresarial.

---

## Testes e Debugging

### Testes
- Acionam falhas causadas por defeitos no software (teste dinâmico)  
- Encontram defeitos diretamente no objeto de teste (teste estático)

### Debugging
- Os testes dinâmicos acionam a falha e o debugging encontra a causa desta falha (defeitos)  
- Analisa as respetivas causas  
- Procedem à sua eliminação  
- Reproduzem a falha  
- Fazem diagnóstico (encontram a raiz do defeito)  
- Corrigem a causa  

Posteriormente, os testes de confirmação, realizados pelo testador inicial, verificam se as correções resolveram o defeito.  
Os testes de regressão subsequentes verificam se mais alguma função foi afetada pela alteração anterior.

---

## Testes no Ciclo de Vida do Software

Os testes permitem avaliar diretamente a qualidade de um objeto de teste nas várias fases do SDLC.

Os testes podem também ser necessários para cumprir requisitos contratuais ou legais, ou normas regulamentares.

---

## QA vs QC

Os termos “testes” e “QA” são diferentes. Os testes são uma forma de controlo de qualidade (QC).

O QC segue uma abordagem corretiva, orientada para o produto. Concentra-se nas atividades que suportam a concretização dos níveis adequados de qualidade.  
Os testes são uma das principais formas de QC. Existem também métodos formais (verificação de modelos e prova de conformidade), simulação e criação de protótipos.

A garantia de qualidade (QA) segue uma abordagem preventiva, orientada para os processos. Implementa e melhora esses processos.  
Se um processo for seguido corretamente, irá gerar um bom produto. Também se aplica aos processos de desenvolvimento e de testes. É responsabilidade de todos.

Os resultados de teste são utilizados por QA e QC.

- No QC, os testes são utilizados para corrigir defeitos:  
  **“O que está errado aqui?”**  
- No QA, os testes fornecem feedback sobre o nível de desempenho dos processos de desenvolvimento e teste:  
  **“Porque é que isto está a acontecer?”**

---

## Falhas, Defeitos e Causas

Alguns defeitos irão resultar sempre numa falha se forem executados, enquanto outros apenas resultarão numa falha em circunstâncias específicas, e alguns poderão nunca resultar numa falha.

Os erros e os defeitos não são a única causa das falhas. As falhas também podem ser causadas por condições ambientais, tais como radiação e campos eletromagnéticos, que podem causar defeitos no firmware.

As causas raiz são identificadas através da análise da raiz do problema.

---

## Princípios dos Testes

- Os testes mostram a presença de defeitos, não a sua ausência
- Os testes exaustivos são impossíveis. Devem ser utilizadas técnicas de teste, priorização do caso de teste e testes baseados em avaliação de risco  
- Os testes antecipados poupam tempo e dinheiro. O teste estático e o teste dinâmico devem ser iniciados o mais cedo possível  
- Os defeitos agrupam-se. Um número reduzido de componentes do sistema normalmente apresenta a maioria dos defeitos detetados, ou é responsável pela maioria das falhas operacionais (Enders 1975). Princípio de Pareto: “cerca de 80% dos casos vêm de 20% das causas”  
- Os testes desgastam. A sua repetição torna ineficaz a deteção de novos defeitos. Para contornar a questão, deve-se alterar casos de testes existentes, mudar dados de teste, criar novos testes e explorar novos cenários (criatividade). Em alguns casos faz sentido a repetição, como nos testes de regressão automatizados, pois estes não têm o objetivo de encontrar novos defeitos, mas sim de confirmar que o que funcionava continua a funcionar  
- Os testes são dependentes do contexto.
- Falácia da ausência de defeitos. É um erro achar que a verificação de software irá assegurar o sucesso do sistema, pois o sistema produzido pode não satisfazer as necessidades e as expectativas dos utilizadores. Por isso, deve ser efetuada a validação

# Syllabus ISTQB — Capítulo 1  
**Resumo pessoal — Processo de Teste, Papéis e Competências**

---

## Processo de Teste

Processo de testes é um conjunto de atividades de teste.  
“Questões como quais são as atividades de teste que estão incluídas no processo de teste, como são implementadas e quando ocorrem, são normalmente decididas no âmbito do planeamento dos testes.”

---

## Atividades e Tarefas de Teste

Podem ser implementadas iterativamente ou paralelamente.  
São adaptadas ao sistema e ao projeto.

### Planeamento de Testes
Definir os objetivos dos testes e a melhor abordagem para concretizar esses mesmos objetivos, tendo em conta as limitações impostas no contexto geral.

### Monitorização e Controlo de Testes
Verificação contínua das atividades e comparação de progresso atual com o desejado.  
Envolve a adoção de medidas necessárias para cumprir os objetivos do teste.

### Análise de Teste
Analisar a base de testes, características passíveis de teste e definir as condições de teste, juntamente com os riscos relacionados e os níveis de risco.  
É suportada pela utilização de técnicas de teste.  
**“O que testar?”**

### Conceção de Teste
Concretização das condições de teste (o que testar?) em casos de teste e outro testware.  
Identifica-se os itens de cobertura (elementos que precisam de ser cobertos pelos testes) que ajudam a definir os dados de entrada, os resultados esperados e as pré-condições dos casos de teste.

São aplicadas as técnicas de teste.  
São definidos os requisitos de dados de teste, o ambiente de teste e as ferramentas e infraestruturas necessárias.  
**“Como testar?”**

### Implementação do Teste
Implica criar ou adquirir o testware necessário para a execução de teste.

Inclui:
- Casos de teste  
- Procedimentos de teste  
- Baterias de teste  

Nesta fase criam-se scripts e testes manuais e automatizados.  
Os procedimentos de teste são organizados e priorizados num cronograma de forma a obter a maior eficiência.  
O ambiente de teste é configurado e validado.  
**“Está tudo pronto para executar os testes?”**

### Execução de Teste
Execução de acordo com o cronograma.  
Pode ser manual ou automatizada.

Inclui:
- Testes contínuos ou sessões de teste em pares  
- Comparação dos resultados com os esperados  
- Registo dos resultados  
- Análise dos defeitos para identificar as causas prováveis  
- Comunicação dos defeitos com base nas falhas observadas  

### Conclusão do Teste
Ocorre no lançamento do projeto, fim da iteração e conclusão do nível de teste.

O objetivo é encerrar formalmente os testes.  
São revistos defeitos não resolvidos, pedidos de alteração e itens do backlog do produto criados durante os testes.

Os itens são documentados, priorizados e encaminhados para as equipas responsáveis.  
Testware que possa ser útil no futuro é arquivado e entregue às equipas para reutilização.  
O ambiente de teste é encerrado para um estado acordado.

São identificadas as lições aprendidas e as melhorias a implementar no futuro.  
É criado um relatório de conclusão do teste para os stakeholders.

---

## Fatores que Influenciam o Processo de Teste

Os testes são financiados pelos stakeholders com o objetivo final de satisfazer as necessidades do negócio.  
A forma como os testes serão realizados depende de fatores contextuais.

Estes fatores têm impacto na:
- Estratégia de teste  
- Técnicas de teste utilizadas  
- Grau de automação de testes  
- Nível de cobertura necessário  
- Nível de detalhe da documentação e dos relatórios  

### Fatores Contextuais
- Stakeholders (necessidades, expectativas, requisitos, vontade de colaborar, etc.)  
- Membros da equipa (competências, conhecimento, nível de experiência, disponibilidade, necessidades de formação, etc.)  
- Área de negócio (grau de importância, riscos identificados, necessidades de mercado, regulamentações legais, etc.)  
- Fatores técnicos (tipo de software, arquitetura do produto, tecnologia utilizada, etc.)  
- Restrições do projeto (âmbito, prazo, orçamento, recursos, etc.)  
- Fatores organizacionais (estrutura, políticas, práticas utilizadas, etc.)  
- SDLC  
- Ferramentas (disponibilidade, usabilidade, conformidade, etc.)

---

## Testware e Produtos de Trabalho

Testware resulta das atividades de teste, varia de organização para organização e deve ser gerido de maneira correta através da gestão de configurações para assegurar a consistência e a integridade dos produtos de trabalho.

### Produtos de Trabalho do Planeamento de Testes
- Plano de testes  
- Cronograma de testes  
- Registo de riscos  
- Critérios de entrada e saída  

### Produtos de Trabalho da Monitorização e Controlo de Testes
- Relatórios de progresso de testes  
- Documentação das diretivas de controlo  
- Informações dos riscos  

### Produtos de Trabalho da Análise de Teste
- Condições de teste (priorizadas)  
- Relatórios de defeitos em relação aos defeitos na base para testes  

### Produtos de Trabalho da Conceção de Teste
- Casos de teste (priorizados)  
- Cartas de testes  
- Itens de cobertura  
- Requisitos dos dados de teste  
- Requisitos do ambiente de teste  

### Produtos de Trabalho da Implementação do Teste
- Procedimentos de teste  
- Scripts de teste automatizados  
- Baterias de testes  
- Dados de teste  
- Cronogramas de execução de testes  
- Elementos do ambiente de teste (stubs, controladores, simuladores e virtualizações de serviços)  

### Produtos de Trabalho da Execução de Teste
- Registos de teste  
- Relatórios de defeitos  

### Produtos de Trabalho da Conclusão do Teste
- Relatório de conclusão de teste  
- Pontos de melhoria em projetos ou iterações futuras  
- Documentação das lições aprendidas  
- Pedidos de alteração  

---

## Rastreabilidade

É importante estabelecer e manter a rastreabilidade ao longo do processo de teste.

Inclui a ligação entre:
- Base para testes  
- Testware associado aos respetivos elementos (condições, riscos, casos de teste)  
- Resultados do teste  
- Defeitos detetados  

É bastante útil ter critérios mensuráveis de cobertura definidos na base de testes.  
Os critérios de cobertura podem funcionar como indicadores-chave de desempenho (KPI).

A rastreabilidade dos casos de teste com requisitos permite verificar se os requisitos são cobertos por casos de teste.

A rastreabilidade dos resultados do teste com riscos pode ser utilizada para avaliar o nível de risco residual num objeto de teste.

### Uma boa rastreabilidade permite:
- Avaliar a cobertura  
- Determinar o impacto das alterações  
- Facilitar auditorias de teste  
- Cumprir os critérios de governança de TI  
- Tornar os relatórios de progresso e conclusão de testes mais fáceis de compreender  
- Comunicar os aspetos técnicos dos testes aos stakeholders de forma mais compreensível  
- Fornecer informações para avaliar a qualidade do produto, capacidade do processo e progresso do projeto, relacionando-os com os objetivos de negócio  

---

## Funções nos Testes

### Função de Gestão de Teste
Responsável pelo processo de teste como um todo, pela equipa de teste e pela liderança das atividades.

Foca-se no:
- Planeamento  
- Monitorização  
- Controlo  
- Conclusão dos testes  

Tudo isto depende do contexto.  
Por exemplo, em ambientes ágeis, algumas tarefas podem ser exercidas pela equipa Agile ou por gestores de teste.

**Objetivo:** Garantir que o processo de teste é organizado, controlado e completo.

### Função de Teste
Responsável pelo aspeto técnico da engenharia de testes.

Concentra-se na:
- Análise  
- Conceção  
- Implementação  
- Execução dos testes  

Executado por testers ou engenheiros de teste.

**Objetivo:** Garantir que os testes são corretos, eficazes e cobrem os requisitos.

---

## Competências dos Testadores

### Competências Gerais
- Conhecimento de testes  
- Minucioso, cuidado, curioso, atenção ao detalhe, ser metódico a identificar defeitos  
- Boa comunicação, escuta ativa e espírito de equipa  
- Pensamento analítico, crítico e criatividade  
- Conhecimento técnico  
- Conhecimento da área de negócio  

De forma a melhorar a qualidade do produto, as informações sobre os defeitos e as falhas devem ser comunicadas de forma construtiva.

---

## Whole Team Approach e Independência de Testes

Qualquer membro da equipa com as competências e os conhecimentos necessários para as tarefas e todos os envolvidos no projeto são responsáveis pela qualidade.  
Todos partilham o mesmo espaço (físico ou virtual).  
Melhora a dinâmica, a comunicação e a colaboração da equipa.  
Cria sinergias.

### Inclui:
- Colaborar com os representantes do negócio no sentido de ajudar a criar testes de aceitação adequados  
- Trabalhar com programadores para acordar a estratégia de teste e decidir as abordagens à automação de testes a seguir  

“Em sistemas críticos, é importante que os testes sejam conduzidos por uma equipa de teste independente, garantindo maior rigor e confiabilidade (ex.: software médico, sistemas de aviação, controlos nucleares).”

“Quanto mais independente for o testador, maior a imparcialidade e menor o risco de passar erros despercebidos.”

### Níveis de Independência nos Testes
- Programadores a efetuarem testes de componentes e testes de integração de componentes  
- Equipa de teste a efetuar testes de sistema e testes de integração de sistemas  
- Representantes do negócio a efetuarem testes de aceitação  

