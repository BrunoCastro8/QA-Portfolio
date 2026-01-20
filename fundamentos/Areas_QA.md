# Tipos de QA — Áreas e Tipos de Teste

Este documento apresenta os principais tipos de teste em QA, com foco no que o sistema faz, como se comporta e como a qualidade é validada em diferentes níveis.

---

## Testes Funcionais

Testam o que o sistema faz, tendo por base as funcionalidades e ações específicas que o software deve realizar para atender às necessidades do utilizador.

### Características
- Não se preocupam com o código (caixa preta)  
- Validam o comportamento do sistema  
- Baseiam-se em entradas e saídas  

### Exemplos
- Testar login com dados válidos  
- Verificar envio de e-mail após registo  
- Validar cálculo de desconto num carrinho  

---

## Testes Não Funcionais

Avaliam como o sistema se comporta sob diferentes aspetos que não estão diretamente relacionados com a lógica funcional.

### Subtipos Principais

### Desempenho
- Tempo de resposta  
- Uso de CPU  
- Throughput (capacidade de processamento)

### Carga
- Comportamento com grande volume de utilizadores

### Stress
- Comportamento em condições extremas

### Segurança
- Autenticação  
- Autorização  
- Ataques

### Usabilidade
- Experiência do utilizador final

### Compatibilidade
- Navegadores  
- Dispositivos  
- Sistemas operativos

---

## Testes Estruturais (Caixa Branca)

Testam a estrutura interna do código, como condições, loops, fluxos lógicos e cobertura.

### Envolvem
- Análise do código-fonte  
- Cobertura de código (linhas, condições, caminhos)

### Exemplos
- Testar se todos os ramos de um IF foram cobertos  
- Validar se exceções são corretamente tratadas  
- Cobertura de laços (for, while)

### Ferramentas
- Jest  
- JUnit  
- Istanbul  
- JaCoCo  

---

## Testes de Regressão

Garantem que as funcionalidades existentes não foram afetadas por alterações ou atualizações no sistema (correções ou novas funcionalidades).

A automatização dos testes de regressão é altamente recomendada.

### Aplicações Comuns
- Após deploys  
- Em pipelines de CI/CD (fluxos automatizados que constroem, preparam e testam o software para lançamento)  
- Quando há refatorações (reestruturação do código para melhorar qualidade interna, como design, legibilidade e manutenibilidade)

---

## Testes Exploratórios

Realizados sem roteiros definidos, com base na experiência e intuição do tester.

> “Testar com olhos de utilizador”

### Benefícios
- Revelam bugs não previstos  
- Ideais para sistemas pouco documentados  
- Complementam testes tradicionais  

---

## Testes de Aceitação

Validações feitas com a perspetiva do cliente ou do utilizador final.

### Objetivo
- Garantir que o sistema cumpre os requisitos do negócio

### Tipos
- **UAT (User Acceptance Testing)** — Executado pelo cliente  
- **Testes baseados em critérios de aceitação** — Gherkin / BDD  

### Exemplo
Utilizador realiza um pagamento com sucesso.

**Critério de sucesso:**
- Transação registada  
- E-mail enviado  
- Stock atualizado  

---

## Testes Manuais vs Testes Automatizados

Os testes manuais enquadram-se melhor em exploração, validação visual e mudanças frequentes.  
Os testes automatizados são ideais para testes repetitivos, regressão e validação em larga escala, onde a execução rápida e consistente traz valor.

| Aspeto | Manual | Automatizado |
|--------|--------|--------------|
| Execução | Humano | Scripts executados por ferramentas |
| Repetição | Custo alto | Baixo custo por execução |
| Adaptação | Alta flexibilidade | Requer manutenção |
| Melhor uso | Testes exploratórios e visuais | Testes repetitivos, regressão e unitários |

---

## Tipos de Teste por Nível

Cada nível cobre um objetivo diferente e complementa os restantes.

| Nível | Foco | Quem Faz |
|------|------|----------|
| **Unitário** | Testa funções/métodos isoladamente | Programadores |
| **Integração** | Testa comunicação entre módulos | Programadores e QAs |
| **Sistema** | Testa o sistema como um todo | Principalmente QAs / Testers |
| **Aceitação** | Valida se o sistema atende às necessidades | Cliente, Product Owner ou utilizadores-chave |

---

## Conclusão

Os diferentes tipos e níveis de teste permitem validar tanto o funcionamento do sistema como a sua qualidade, desempenho e adequação às necessidades do utilizador final.

A combinação entre testes manuais, automatizados, funcionais e não funcionais contribui para um processo de desenvolvimento mais fiável e para a entrega de software com maior qualidade.
