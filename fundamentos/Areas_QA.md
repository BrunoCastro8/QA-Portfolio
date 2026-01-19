# Tipos de Teste em QA — Fundamentos

Este documento apresenta os principais tipos de teste em QA, explicados de forma simples, com exemplos práticos e a diferença entre testes manuais e automatizados.

---

## Testes Funcionais

Os testes funcionais testam o que o sistema faz. O objetivo é garantir que as funcionalidades se comportam conforme os requisitos definidos.

São testes do tipo **caixa preta**, ou seja, não interessa como o sistema foi construído internamente, apenas o resultado que apresenta ao utilizador.

### Exemplos
- Verificar se o login funciona com credenciais válidas e inválidas  
- Confirmar se o envio de um formulário apresenta a mensagem correta  
- Validar se um desconto é aplicado corretamente numa compra  

---

## Testes Não Funcionais

Os testes não funcionais avaliam como o sistema se comporta, em vez de apenas o que ele faz. O foco é a qualidade da aplicação.

### Incluem
- **Desempenho** — Tempo de resposta do sistema  
- **Carga** — Funcionamento com muitos utilizadores ao mesmo tempo  
- **Stress** — Limites máximos que o sistema consegue suportar  
- **Segurança** — Proteção contra acessos não autorizados  
- **Usabilidade** — Facilidade de uso para o utilizador  
- **Compatibilidade** — Funcionamento em diferentes dispositivos e navegadores  

### Exemplo
Testar se um site continua a funcionar corretamente quando muitas pessoas fazem compras ao mesmo tempo.

---

## Testes Estruturais (Caixa Branca)

Os testes estruturais analisam a estrutura interna do código. O foco é perceber se as partes do programa funcionam corretamente por dentro.

Normalmente são feitos a nível **unitário e de integração**.

### Foco
- Cobertura de código  
- Condições (IF / ELSE)  
- Loops  
- Tratamento de exceções  

### Ferramentas Comuns
- JavaScript: Jest, Istanbul  
- Java: JUnit, JaCoCo  

---

## Testes de Regressão

Os testes de regressão garantem que o que já funcionava continua a funcionar depois de uma alteração no sistema.

São usados após:
- Correções de bugs  
- Atualizações do sistema  
- Refatoração de código  
- Novos deploys  

A automatização é muito recomendada neste tipo de teste, porque eles são repetitivos e precisam de ser executados muitas vezes.

---

## Testes Exploratórios

Os testes exploratórios são feitos sem um plano rígido. O QA explora o sistema como se fosse um utilizador real, tentando encontrar problemas que não estavam previstos nos testes formais.

### Benefícios
- Encontram problemas inesperados  
- Simulam o comportamento real do utilizador  
- Complementam os testes planeados  

---

## Testes de Aceitação

Os testes de aceitação validam se o sistema atende às necessidades do utilizador e do negócio.

Normalmente são realizados pelo:
- Cliente  
- Product Owner  
- Utilizadores finais  

### Exemplo
Verificar se, depois de uma compra:
- O pagamento é processado corretamente  
- O e-mail de confirmação é enviado  
- O stock é atualizado no sistema  

---

## Testes Manuais vs Testes Automatizados

| Aspeto | Manual | Automatizado |
|--------|--------|--------------|
| Execução | Realizado por uma pessoa | Executado por scripts e ferramentas |
| Repetição | Custo mais alto | Baixo custo por execução |
| Adaptação | Alta flexibilidade | Requer manutenção |
| Melhor uso | Testes exploratórios e visuais | Testes repetitivos, regressão e unitários |

---

## Tipos de Teste por Nível

| Nível | Foco |
|------|------|
| **Unitário** | Testa funções ou métodos isoladamente |
| **Integração** | Testa a comunicação entre módulos |
| **Sistema** | Testa o sistema como um todo |
| **Aceitação** | Valida se o sistema atende às necessidades do utilizador |

### Quem Normalmente Testa
- **Unitário** — Programadores  
- **Integração** — Programadores e QA  
- **Sistema** — QA  
- **Aceitação** — Cliente / Product Owner  
