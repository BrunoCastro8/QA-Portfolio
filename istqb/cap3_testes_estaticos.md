# Capítulo 3 — Testes Estáticos

## Testes Estáticos

### Conceitos básicos dos testes estáticos
Neste tipo de teste não é necessário executar o software. O código, a especificação do processo, a arquitetura e outros produtos de trabalho são testados manualmente (revisões) ou automaticamente com a ajuda de uma ferramenta (ex. Análise estática). Pode ser testado tanto na verificação como na validação.

> “Tendo em conta que os testes estáticos podem ser efetuados no início do SDLC, é possível gerar um consenso entre os stakeholders envolvidos, melhorando também a comunicação entre eles. Por este motivo, é recomendado envolver uma grande variedade de stakeholders nos testes estáticos”

### Objetivo
- Melhorar qualidade  
- Detetar defeitos  
- Avaliar características como legibilidade, completude, correção, testabilidade e consistência  
- Permite identificar problemas anteriores ao teste dinâmico  

As técnicas de revisão podem ser aplicadas para assegurar que as user stories estão completas, compreensíveis e incluem critérios de aceitação testáveis. Os testadores podem assim explorar, desafiar e ajudar a melhorar as user stories propostas.

---

## Análise Estática

- Permite identificar problemas anteriores ao teste dinâmico  
- Requer menos esforço  
- Não necessita de casos de teste  
- Por norma, recorre ao uso de ferramentas  

> “A análise estática é frequentemente incorporada nos frameworks de integração contínua.”

A análise estática também é utilizada para avaliar manutenibilidade e segurança do software. Verificadores ortográficos e ferramentas de legibilidade são outros exemplos de ferramentas de análise estática.

A análise estática, por norma, é realizada por ferramentas que analisam o código sem o executar e outros tipos de teste estático, como revisões, são feitos manualmente por pessoas.

---

## Produtos de Trabalho Passíveis de Examinação pelos Testes Estáticos

- Documentos de especificação de requisitos  
- Código-fonte  
- Planos de teste  
- Casos de teste  
- Itens do backlog do produto  
- Cartas de teste  
- Documentação do projeto  
- Contratos  
- Modelos  

> “Todos os produtos de trabalhos que possam ser lidos e compreendidos podem ser sujeitos a revisão. Contudo, na análise estática, os produtos de trabalho necessitam de uma estrutura em relação à qual possam ser verificados (p. ex., modelos, código ou texto com sintaxe formal).”

### Quais não devem ser sujeitos a testes estáticos?
Os que são difíceis de interpretar pelo ser humano e os que não devem ser analisados por ferramentas, como é o caso do código executável de terceiros devido a motivos jurídicos.

---

## Valor dos Testes Estáticos

- Detetar defeitos nas fases precoces do SDLC  
- Identificar defeitos que não são detetados pelos testes dinâmicos como é o caso do código inatingível, padrões de conceção não implementados como pretendido e defeitos em produtos de trabalho não executáveis  
- Avaliar a qualidade e aumentar a confiança nos produtos de trabalho  
- Os defeitos no código podem ser detetados através da análise estática com maior eficiência do que no teste dinâmico  

---

## Diferenças entre Testes Estáticos e Testes Dinâmicos

- Existem alguns tipos de defeitos que apenas podem ser detetados nos testes estáticos ou dinâmicos  
- Os testes estáticos encontram defeitos de forma imediata, enquanto os dinâmicos provocam falhas para chegar aos defeitos associados, através de análise posterior  
- Os testes estáticos encontram erros mais facilmente em caminhos de código, quando estes são executados raramente ou são difíceis de alcançar  
- Os testes estáticos são aplicados não executando o software ou noutros produtos de trabalho. No caso dos testes dinâmicos, é necessário executar o software  
- Os testes estáticos podem medir características de qualidade como manutenibilidade e os testes dinâmicos podem medir características de qualidade que dependem do código executado, como por exemplo, eficiência de desempenho  

---

## Defeitos Típicos, Fáceis e/ou Baratos de Encontrar e Corrigir através de Testes Estáticos

- Defeitos de requisitos  
- Defeitos de conceção (ex. estruturas de bases de dados ineficientes, modularização inadequada)  
- Determinados tipos de defeitos no código (variáveis com valores indefinidos, variáveis não declaradas, código inacessível ou duplicado, complexidade excessiva do código)  
- Desvios em relação às normas (ex. falta de cumprimento das convenções de nomenclatura nas normas de codificação)  
- Especificações de interface incorretas (ex. números, tipos ou ordem de parâmetros incompatíveis)  
- Tipos específicos de vulnerabilidades de segurança (ex. buffer overflows)  
- Lacunas ou imprecisões na cobertura da base para testes (ex. testes em falta para um critério de aceitação)  

---

## Feedback e Processo de Revisão

### Vantagens do Feedback Antecipado e Frequente dos Stakeholders
O feedback antecipado e frequente permite comunicar possíveis problemas de qualidade mais cedo. A participação dos stakeholders durante o SDLC tem grande importância, porque permite que a visão atual esteja de acordo com a visão original desses mesmos stakeholders.

A falta de concordância resulta em retrabalhos dispendiosos, prazos falhados, jogos de atribuição de culpas e poderá levar ao fracasso total do projeto.

Por outro lado, o feedback constante dos stakeholders permite evitar equívocos sobre os requisitos e assegurar que as alterações efetuadas aos requisitos são compreendidas e implementadas antecipadamente. Isto permite à equipa de desenvolvimento compreender melhor o que está a ser construído e concentrar-se nas características que proporcionam um maior valor aos stakeholders.

---

## Atividades do Processo de Revisão

A norma ISO/IEC 20246 define um modelo base/geral de como fazer revisões. Estes modelos podem ser simples ou mais formais e rigorosos, logo, são adaptáveis ao contexto do projeto. Fornece uma framework estruturada, mas flexível.

Devido à grande dimensão de muitos produtos de trabalho, apenas rever uma vez seria um problema. Assim, o processo de revisão deve ser aplicado várias vezes, para se poder concluir o processo de revisão do produto de trabalho na totalidade.

### Atividades no processo de revisão
- **Planeamento**  
  É definido o âmbito da revisão (objetivo, produto de trabalho a rever, as características de qualidade a avaliar, as áreas de foco, os critérios de saída, as informações de suporte, o esforço e os prazos de revisão)

- **Início da revisão**  
  O objetivo é assegurar que todos os participantes estão preparados para a revisão. Inclui assegurar que têm acesso ao produto de trabalho, compreendem a sua função e as responsabilidades e recebem tudo o que necessitam para efetuar a revisão

- **Revisão individual**  
  Todos realizam uma revisão individual para avaliar a qualidade do produto de trabalho, identificar anomalias, recomendações e questões, aplicando as técnicas necessárias de revisão (checklist, revisão com base em cenários). Os revisores registam todas as anomalias, recomendações e questões que identificarem

- **Comunicação e análise**  
  As anomalias identificadas não são necessariamente defeitos. Estas anomalias têm de ser analisadas e debatidas. Essa decisão deve ser tomada com base no seu estado, de quem detém a posse da anomalia e das ações necessárias.  
  É feita uma reunião de revisão onde também se decide o nível de qualidade do produto de trabalho revisto e as ações a tomar de seguida. Poderá ser necessário efetuar uma revisão de seguimento (follow-up) para concluir ações

- **Correção e elaboração de relatórios**  
  Cada defeito tem o seu relatório de defeitos para dar seguimento às ações corretivas. Após concretizar os critérios de saída, o produto de trabalho pode ser aceite e os resultados da revisão podem ser comunicados

---

## Funções e Responsabilidades nas Revisões

- **Gestor**  
  Decide o que deve ser revisto e fornece recursos (colaboradores e alocação de tempo para efetuar a revisão)

- **Autor**  
  Cria e corrige o produto de trabalho em revisão

- **Moderador ou Facilitador**  
  Assegura o bom funcionamento das reuniões de revisão, incluindo a mediação, a gestão de tempo e um ambiente de revisão seguro onde todos possam participar livremente

- **Redator ou Anotador**  
  Reúne as anomalias dos revisores e regista as informações da revisão (decisões e novas anomalias encontradas na reunião)

- **Revisor**  
  Efetua as revisões (pode ser alguém que trabalha no projeto, um especialista na matéria ou qualquer outro stakeholder)

- **Líder de revisão**  
  Assume a responsabilidade global da revisão, decide quem estará envolvido e define quando e onde será efetuada a revisão
