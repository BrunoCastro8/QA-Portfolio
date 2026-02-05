# Técnicas de Teste Baseadas na Experiência

Este tipo de teste é frequentemente utilizado e consiste em:

- Antecipação de erros
- Testes exploratórios
- Testes baseados em checklists

## Antecipação de Erros

Esta técnica consiste em antecipar a ocorrência de erros, defeitos e falhas, com base no conhecimento e experiência do testador. Incluí:

- A forma como a aplicação funcionou no passado
- Os tipos de erros que tendem a ser cometidos pelos programadores e os tipos de defeitos que resultam desses erros
- Os tipos de falhas que ocorreram noutras aplicações semelhantes

Os erros, defeitos e falhas podem estar relacionados com:

### Entrada
- Entrada correta não aceite
- Parâmetros incorretos ou em falta

### Saída
- Formato incorreto
- Resultado incorreto

### Lógica
- Falta de um caso
- Operador incorreto

### Computação
- Incorreta operação
- Computação incorreta

### Interfaces
- Parâmetros errados
- Tipos incompatíveis

### Dados
- Inicialização incorreto
- Tipo incorreto

> “Onde é que isto provavelmente vai falhar?”

Os ataques e falhas são uma abordagem metódica para implementar a antecipação de erros. O testador cria uma lista de erros, defeitos e falhas possíveis e concebe testes que irão identificar os defeitos associados aos erros, expondo esses defeitos ou causando as falhas respetivas.

Estas listas podem ser criadas com base em:

- Experiência
- Dados de defeitos e falhas
- A partir do conhecimento comum sobre os motivos do software falhar

## Teste Exploratório

Realizados sem roteiros definidos, com base na experiência e intuição do tester. “Testar com olhos de utilizador”

### Benefícios
- Revela bugs não previstos
- Ideal para sistemas pouco documentados
- Complementa testes tradicionais

São úteis quando existe poucas especificações ou estas são inadequadas e quando o tempo de testes é escasso. Também são úteis para complementar outras técnicas de teste mais formais. Exige competências essenciais, tais como, analíticas, curiosidade e criatividade.

São concebidos, executados e avaliados simultaneamente, enquanto o testador aprende mais sobre o objeto de teste. A partir deste teste, o testador consegue obter mais informações sobre o objeto de teste e explorar profundamente com testes focados e criar testes para as áreas não testadas.

É efetuado utilizando testes baseados em sessões. Nesta abordagem, os testes são efetuados dentro de um tempo definido (time-boxing) e o testador utiliza uma carta de testes com objetivos de teste específicos para o orientar nos testes.

A seguir à sessão faz-se uma reunião de balanço (debrief). Faz-se debates entre o testador e os stakeholders.

Nesta abordagem, os itens de cobertura são identificados e executados durante a sessão. O testador utiliza as folhas de sessão de testa para documentar os passos seguidos e as descobertas feitas.

> “O que acontece se eu tentar isto agora?”

## Teste baseado em checklists

Neste tipo de teste, o testador concebe, implementa e executa os testes para abranger as condições de teste encontradas numa lista de verificação, com itens em forma de pergunta. Estas listas baseiam-se na experiência, no conhecimento sobre o que é importante para o utilizador ou na compreensão do porquê e como o software falha. Não devem conter itens que possam ser:

- Verificados automaticamente
- Itens que funcionem melhor como critérios de entrada/saída
- Itens demasiado abrangentes

Neste teste deve ser possível verificar cada item de forma separada e direta. Os itens poem ser:

- Requisitos
- Propriedades da interface gráfica
- Características de qualidade
- Outras formas de condições de teste

Suportam outras formas de teste, como testes funcionais e não funcionais.

As listas devem ser atualizadas regularmente como base na análise de defeitos, tendo a atenção para não a tornar demasiado grande. Se as listas de verificação forem de alto nível, estas, pode ocorrer alguma variabilidade nos testes reais, o que resulta numa cobertura potencialmente maior e com menos repetição.

> “Já testei tudo o que costuma causar problemas?”
