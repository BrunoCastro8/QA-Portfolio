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
