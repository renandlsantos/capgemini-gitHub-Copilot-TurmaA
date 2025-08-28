# 📝 Exercícios - Aula 5: GitHub Copilot & FinanceFlow

## **Seção 1: Fundamentos e Planos (5 questões)**

**1.** Qual a principal diferença entre os planos Copilot Individual e Business em relação aos dados?
> **R:** No plano Individual ($10), os dados são usados para treino do modelo. No plano Business ($19), os dados NÃO são usados para treino e há opções de exclusão.

**2.** Qual plano do Copilot oferece Knowledge Bases como recurso adicional?
> **R:** O plano Enterprise ($39).

**3.** Verdadeiro ou Falso: O plano Copilot Individual custa $19/mês.
> **R:** Falso. O plano Individual custa $10/mês.

**4.** Liste os três planos do GitHub Copilot e seus respectivos preços.
> **R:** Individual ($10), Business ($19), Enterprise ($39).

**5.** Qual a vantagem de segurança do plano Business sobre o Individual?
> **R:** Os dados não são usados para treinar o modelo, oferecendo mais privacidade e controle sobre informações sensíveis.

## **Seção 2: Comandos do Copilot (5 questões)**

**6.** Qual comando do Copilot você usa para gerar testes automaticamente?
> **R:** `/tests`

**7.** Complete: O comando `@workspace` é usado para ____________.
> **R:** Obter contexto do projeto inteiro / analisar o projeto completo.

**8.** Como você referencia código selecionado no Copilot?
> **R:** Usando `#selection`.

**9.** Qual comando você usaria para entender um trecho de código complexo?
> **R:** `/explain`

**10.** Verdadeiro ou Falso: O comando `/tests` explica o funcionamento do código.
> **R:** Falso. O comando `/tests` gera testes. Para explicar código, usa-se `/explain`.

## **Seção 3: Desenvolvimento do FinanceFlow (5 questões)**

**11.** Quais são as principais tecnologias do backend do FinanceFlow?
> **R:** Python + FastAPI + PostgreSQL + SQLAlchemy + JWT para autenticação.

**12.** Qual biblioteca foi escolhida para a interface do frontend React?
> **R:** Material-UI.

**13.** Liste 3 funcionalidades implementadas no backend durante a aula.
> **R:** 
> - User model + autenticação JWT
> - API endpoints (/auth, /users)
> - Validação com Pydantic

**14.** Qual ferramenta de containerização foi utilizada no projeto?
> **R:** Docker com docker-compose.

**15.** Em qual endpoint a documentação automática da API FastAPI fica disponível?
> **R:** `/docs`

## **Seção 4: Features Avançadas (5 questões)**

**16.** O que são "Copilot Edits" e qual sua principal vantagem?
> **R:** São mudanças coordenadas em múltiplos arquivos simultaneamente. A vantagem é poder fazer alterações complexas em 8-12 arquivos de uma vez.

**17.** Cite os três modelos disponíveis no Model Picker do Copilot.
> **R:** GPT-4, GPT-3.5 e Claude.

**18.** Dê um exemplo de prompt que você usaria com @workspace.
> **R:** "Analyze FinanceFlow architecture and suggest improvements" ou qualquer variação que solicite análise completa do projeto.

**19.** Quantos minutos foram dedicados ao desenvolvimento do Frontend e Backend respectivamente?
> **R:** 40 minutos para cada (Frontend: 40 min, Backend: 40 min).

**20.** Quais são as duas tarefas obrigatórias para casa antes da Aula 6?
> **R:** 
> 1. Implementar CRUD completo de Contas Bancárias (30 min)
> 2. Melhorar o Dashboard com gráficos e métricas (20 min)
> 3. Fazer commit e push no GitHub (10 min)

---

## 💡 **Dica de Estudo**
Revise estes exercícios antes da próxima aula sobre DevOps, CI/CD e Automação. Pratique os comandos do Copilot enquanto desenvolve as tarefas de casa!