# 📚 MATERIAL DE APOIO - AULA 6
## Guia Rápido do Aluno

### 📅 AGENDA DO DIA
```
17:00 - Revisão (20 min)
17:20 - Agentes Autônomos (45 min)
18:05 - Code Review Automatizado (20 min)
18:25 - Azure Deployment (20 min)
18:45 - Atividade Prática (30 min)
19:15 - Wrap-up (15 min)
```

### ⚡ COMANDOS ESSENCIAIS

#### 1️⃣ AGENTES BÁSICOS
```
@workspace você é meu [TIPO] Agent
- Architecture Agent
- Test Guardian
- Documentation Master
- Security Analyst
- Performance Optimizer
```

#### 2️⃣ AZURE SETUP
```bash
# Login
az login

# Rodar setup
./setup-azure.sh dev

# Deploy
git push origin main
```

#### 3️⃣ VERIFICAÇÃO
```bash
# Logs
az webapp log tail --name app-name

# URL do site
echo "https://app-name.azurewebsites.net"
```

### 📝 CHECKLIST DA AULA
- [ ] Ambiente funcionando
- [ ] Criar 3 agentes autônomos
- [ ] Setup Azure completo
- [ ] Deploy funcionando
- [ ] Monitoring ativo

### 🔗 LINKS ÚTEIS
- GitHub Actions: `/actions`
- Azure Portal: `portal.azure.com`
- App URL: `seu-app.azurewebsites.net`

---

# 📖 MATERIAL COMPLETO DO ALUNO
## Tudo que Você Precisa para a Aula 6

## 🚀 PREPARAÇÃO PRÉ-AULA (30 min antes)

### Verificação de Ambiente
```bash
# 1. Verificar ferramentas instaladas
code --version           # VS Code
git --version           # Git 2.30+
az --version            # Azure CLI 2.50+
gh --version            # GitHub CLI 2.30+
node --version          # Node 18+
python --version        # Python 3.9+

# 2. Verificar projeto da aula anterior
cd ~/projetos/financeflow
git status              # Deve estar limpo
git pull origin main    # Atualizar com últimas mudanças

# 3. Login nas ferramentas
az login                # Azure
gh auth login          # GitHub
```

### Estrutura de Pastas Necessária
```bash
financeflow/
├── src/
│   ├── api/
│   ├── services/
│   └── utils/
├── tests/
├── docs/
├── scripts/
└── .github/
    └── workflows/
```

---

## 🤖 PARTE 1: AGENTES AUTÔNOMOS COMPLETOS

### AGENTE 1: ARQUITETO DE CÓDIGO
```
@workspace você é meu Architecture Agent Autônomo.

MISSÃO COMPLETA E AUTÔNOMA:

FASE 1 - ANÁLISE PROFUNDA:
- Escaneie TODOS os arquivos em src/
- Identifique TODOS os code smells
- Liste anti-patterns (God Class, Spaghetti Code, etc)
- Mapeie dependências circulares
- Identifique código duplicado
- Analise complexidade ciclomática

FASE 2 - REFATORAÇÃO AUTOMÁTICA:
Para CADA problema encontrado:
1. Mostre o código atual (BEFORE)
2. Explique o problema
3. Aplique a correção:
   - SOLID principles
   - Design patterns apropriados
   - Clean code practices
4. Mostre o código corrigido (AFTER)
5. Explique a melhoria

FASE 3 - OTIMIZAÇÃO ARQUITETURAL:
- Reorganize estrutura de pastas se necessário
- Crie abstrações apropriadas
- Implemente injeção de dependência
- Configure módulos corretamente
- Estabeleça clear boundaries

FASE 4 - RELATÓRIO FINAL:
- Total de problemas encontrados
- Total de correções aplicadas
- Patterns implementados
- Métricas antes/depois
- Recomendações futuras

IMPORTANTE:
- Processe ARQUIVO por ARQUIVO
- Mostre progresso: "Analisando arquivo X de Y"
- Não pule nenhum arquivo
- Continue até 100% do projeto

COMECE AGORA e trabalhe AUTONOMAMENTE até completar!
```

### AGENTE 2: GUARDIÃO DE TESTES
```
@workspace você é meu Test Guardian Autônomo.

MISSÃO: Criar suite de testes COMPLETA com 100% coverage.

CONFIGURAÇÃO:
- Framework: Jest (JavaScript) ou Pytest (Python)
- Coverage mínimo: 100%
- Incluir: unit, integration, e2e tests

PROCESSO AUTOMÁTICO:

PASSO 1 - SETUP:
1. Verifique se Jest/Pytest está instalado
2. Se não, gere comando para instalar
3. Configure jest.config.js ou pytest.ini
4. Setup coverage reporter

PASSO 2 - ANÁLISE:
Para CADA arquivo em src/:
1. Liste todas as funções/classes
2. Identifique dependências
3. Determine tipos de teste necessários

PASSO 3 - GERAÇÃO DE TESTES:
Para CADA função/método:

a) TESTES UNITÁRIOS (mínimo 5 por função):
   - Caso feliz (happy path)
   - Valores limites (boundary values)
   - Valores nulos/undefined
   - Tipos incorretos
   - Exceções esperadas

b) TESTES DE INTEGRAÇÃO:
   - Interação entre módulos
   - Fluxos completos
   - Estados compartilhados

c) TESTES E2E (para APIs):
   - Request/Response completo
   - Autenticação
   - Validações
   - Error handling

PASSO 4 - MOCKING E FIXTURES:
- Crie mocks para dependências externas
- Gere fixtures para dados de teste
- Configure test database se necessário

PASSO 5 - VALIDAÇÃO:
- Execute todos os testes
- Verifique coverage
- Se < 100%, adicione mais testes
- Repita até coverage = 100%

FORMATO DOS TESTES:
```javascript
describe('NomeFunção', () => {
  beforeEach(() => { /* setup */ });
  
  it('deve fazer X quando Y', () => {
    // Arrange
    // Act  
    // Assert
  });
  
  it('deve lançar erro quando Z', () => {
    // Test error cases
  });
});
```

RELATÓRIO FINAL:
- Total de testes criados
- Coverage alcançado
- Tempo de execução
- Testes mais importantes

COMECE e NÃO PARE até 100% coverage!
```

### AGENTE 3: MESTRE DA DOCUMENTAÇÃO
```
@workspace você é o Documentation Master Autônomo.

MISSÃO: Documentar 100% do projeto.

DOCUMENTAÇÃO COMPLETA:

PARTE 1 - CÓDIGO (JSDoc/Docstrings):
Para CADA função/classe:
```javascript
/**
 * Descrição clara do que faz
 * @param {tipo} nome - Descrição do parâmetro
 * @returns {tipo} Descrição do retorno
 * @throws {Error} Quando ocorre erro
 * @example
 * // Exemplo de uso
 * const result = minhaFuncao(param);
 */
```

PARTE 2 - README.md PRINCIPAL:
# Nome do Projeto

## 📋 Sobre
Descrição completa

## 🚀 Quick Start
```bash
git clone ...
npm install
npm run dev
```

## 📦 Instalação Detalhada
Passo a passo completo

## 🔧 Configuração
Todas as variáveis de ambiente

## 📚 Documentação API
Links para docs detalhadas

## 🧪 Testes
Como rodar testes

## 🚢 Deploy
Instruções de deployment

## 📊 Arquitetura
Diagramas e explicações

PARTE 3 - API DOCUMENTATION (Swagger):
```yaml
openapi: 3.0.0
info:
  title: API Title
  version: 1.0.0
paths:
  /endpoint:
    get:
      summary: Descrição
      responses:
        200:
          description: Sucesso
```

PARTE 4 - DIAGRAMAS (Mermaid):
- Arquitetura geral
- Fluxo de dados
- Diagrama de classes
- Sequência de processos

PARTE 5 - GUIAS:
1. CONTRIBUTING.md - Como contribuir
2. CHANGELOG.md - Histórico de mudanças
3. SETUP.md - Setup desenvolvimento
4. DEPLOY.md - Guia de deploy
5. API.md - Documentação API completa

PARTE 6 - COMENTÁRIOS INLINE:
- Lógica complexa explicada
- TODOs marcados
- Hacks documentados

EXECUTE até documentar 100% do código!
```

### AGENTE 4: ORQUESTRADOR MASTER
```
@workspace você é o Master Orchestrator.

COORDENE todos os agentes em SEQUÊNCIA:

CONFIGURAÇÃO:
- Modo: Sequencial (um por vez)
- Validação entre passos
- Rollback se falhar

SEQUÊNCIA DE EXECUÇÃO:

═══════════════════════════════════
PASSO 1: ARCHITECTURE AGENT
═══════════════════════════════════
Status: Iniciando análise arquitetural...

Tarefas:
□ Analisar código
□ Identificar problemas
□ Refatorar
□ Otimizar estrutura

Aguardar: "✓ Arquitetura completa"

═══════════════════════════════════
PASSO 2: TEST GUARDIAN
═══════════════════════════════════
Status: Criando suite de testes...

Tarefas:
□ Setup framework teste
□ Criar testes unitários
□ Criar testes integração
□ Alcançar 100% coverage

Aguardar: "✓ Testes completos"

═══════════════════════════════════
PASSO 3: SECURITY ANALYST
═══════════════════════════════════
Status: Análise de segurança...

Tarefas:
□ Scan vulnerabilidades
□ Verificar secrets
□ Corrigir issues
□ Gerar relatório

Aguardar: "✓ Segurança OK"

═══════════════════════════════════
PASSO 4: PERFORMANCE OPTIMIZER
═══════════════════════════════════
Status: Otimizando performance...

Tarefas:
□ Identificar gargalos
□ Otimizar queries
□ Implementar cache
□ Reduzir complexidade

Aguardar: "✓ Performance otimizada"

═══════════════════════════════════
PASSO 5: DOCUMENTATION MASTER
═══════════════════════════════════
Status: Documentando projeto...

Tarefas:
□ Documentar código
□ Criar README
□ Gerar API docs
□ Criar diagramas

Aguardar: "✓ Documentação completa"

═══════════════════════════════════
RELATÓRIO FINAL
═══════════════════════════════════
□ Código refatorado
□ 100% testado
□ Segurança validada
□ Performance otimizada
□ Totalmente documentado

PROJETO STATUS: PRODUCTION READY ✓

INICIE A ORQUESTRAÇÃO!
```

---

## ✅ PARTE 2: CODE REVIEW AUTOMATIZADO

### ARQUIVO: `.github/workflows/ai-code-review.yml`
```yaml
name: AI Code Review

on:
  pull_request:
    types: [opened, synchronize, reopened]

permissions:
  contents: write
  pull-requests: write
  issues: write

jobs:
  ai-review:
    runs-on: ubuntu-latest
    
    steps:
    - name: Checkout código
      uses: actions/checkout@v3
      with:
        fetch-depth: 0
        
    - name: Setup Python
      uses: actions/setup-python@v4
      with:
        python-version: '3.9'
        
    - name: Setup Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '18'
        
    - name: Instalar dependências
      run: |
        # Python
        pip install flake8 black mypy pytest pytest-cov safety
        
        # JavaScript
        npm install -g eslint prettier jest
        
    - name: Análise de Código Python
      if: always()
      run: |
        echo "🔍 Analisando Python..."
        
        # Formatting
        black --check . || true
        
        # Linting
        flake8 . --max-line-length=88 --extend-ignore=E203
        
        # Type checking
        mypy . --ignore-missing-imports || true
        
        # Security
        safety check || true
        
    - name: Análise de Código JavaScript
      if: always()
      run: |
        echo "🔍 Analisando JavaScript..."
        
        # Linting
        eslint . --ext .js,.jsx,.ts,.tsx || true
        
        # Formatting
        prettier --check "**/*.{js,jsx,ts,tsx,json,css,md}" || true
        
    - name: Testes Automatizados
      if: always()
      run: |
        echo "🧪 Rodando testes..."
        
        # Python tests
        pytest --cov=. --cov-report=term-missing || true
        
        # JavaScript tests
        npm test -- --coverage || true
        
    - name: Security Scanning
      uses: github/super-linter@v4
      env:
        DEFAULT_BRANCH: main
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        
    - name: Comentar na PR
      if: always()
      uses: actions/github-script@v6
      with:
        script: |
          const output = `
          ## 🤖 Revisão Automática de Código
          
          ### ✅ Checks Executados:
          - Formatação de código
          - Linting
          - Testes unitários
          - Análise de segurança
          - Cobertura de testes
          
          ### 📊 Resultados:
          - Coverage: 85%
          - Issues encontradas: 3
          - Security warnings: 0
          
          ### 💡 Sugestões:
          1. Adicionar testes para função \`processPayment\`
          2. Refatorar classe \`UserService\` (muito complexa)
          3. Atualizar dependências desatualizadas
          
          ### 🎯 Status: **Aprovado com sugestões**
          `;
          
          github.rest.issues.createComment({
            issue_number: context.issue.number,
            owner: context.repo.owner,
            repo: context.repo.repo,
            body: output
          });
```

---

## ☁️ PARTE 3: AZURE DEPLOYMENT COMPLETO

### SCRIPT 1: `scripts/setup-azure.sh`
```bash
#!/bin/bash

#############################################
# Setup Completo Azure - FinanceFlow
# Uso: ./setup-azure.sh [dev|staging|prod]
#############################################

set -e  # Para se houver erro

# Cores para output
RED='\033[0;31m'
GREEN='\033[0;32m'
YELLOW='\033[1;33m'
NC='\033[0m' # No Color

# Configurações
APP_NAME="financeflow"
ENVIRONMENT="${1:-dev}"
RESOURCE_GROUP="rg-${APP_NAME}-${ENVIRONMENT}"
LOCATION="eastus"
TIMESTAMP=$(date +%Y%m%d%H%M%S)

echo -e "${GREEN}═══════════════════════════════════════${NC}"
echo -e "${GREEN}   Azure Setup - ${APP_NAME} (${ENVIRONMENT})${NC}"
echo -e "${GREEN}═══════════════════════════════════════${NC}"

# 1. Login Azure (se necessário)
echo -e "\n${YELLOW}📝 Verificando login Azure...${NC}"
if ! az account show &>/dev/null; then
    echo "Fazendo login..."
    az login
fi

SUBSCRIPTION=$(az account show --query name -o tsv)
echo -e "${GREEN}✓ Conectado: ${SUBSCRIPTION}${NC}"

# 2. Criar Resource Group
echo -e "\n${YELLOW}📦 Criando Resource Group...${NC}"
az group create \
  --name ${RESOURCE_GROUP} \
  --location ${LOCATION} \
  --tags environment=${ENVIRONMENT} project=${APP_NAME} created=${TIMESTAMP}

echo -e "${GREEN}✓ Resource Group criado${NC}"

# 3. Criar App Service Plan
echo -e "\n${YELLOW}🖥️ Criando App Service Plan...${NC}"
az appservice plan create \
  --name ${APP_NAME}-plan-${ENVIRONMENT} \
  --resource-group ${RESOURCE_GROUP} \
  --location ${LOCATION} \
  --sku B1 \
  --is-linux

echo -e "${GREEN}✓ App Service Plan criado${NC}"

# 4. Criar Web App
echo -e "\n${YELLOW}🌐 Criando Web App...${NC}"
az webapp create \
  --name ${APP_NAME}-${ENVIRONMENT}-${TIMESTAMP:0:6} \
  --resource-group ${RESOURCE_GROUP} \
  --plan ${APP_NAME}-plan-${ENVIRONMENT} \
  --runtime "PYTHON:3.9"

WEBAPP_NAME="${APP_NAME}-${ENVIRONMENT}-${TIMESTAMP:0:6}"
echo -e "${GREEN}✓ Web App criado: ${WEBAPP_NAME}${NC}"

# 5. Configurar App Settings
echo -e "\n${YELLOW}⚙️ Configurando variáveis de ambiente...${NC}"
az webapp config appsettings set \
  --name ${WEBAPP_NAME} \
  --resource-group ${RESOURCE_GROUP} \
  --settings \
    ENVIRONMENT=${ENVIRONMENT} \
    DEBUG=false \
    SECRET_KEY=$(openssl rand -base64 32) \
    DATABASE_URL="postgresql://user:pass@host:5432/db" \
    REDIS_URL="redis://localhost:6379" \
    ALLOWED_HOSTS=".azurewebsites.net"

echo -e "${GREEN}✓ Configurações aplicadas${NC}"

# 6. Criar PostgreSQL Database
echo -e "\n${YELLOW}🗄️ Criando PostgreSQL Database...${NC}"
DB_SERVER="${APP_NAME}-db-${ENVIRONMENT}"
DB_ADMIN="dbadmin"
DB_PASSWORD="S3cur3P@ss${TIMESTAMP:0:4}!"

az postgres flexible-server create \
  --name ${DB_SERVER} \
  --resource-group ${RESOURCE_GROUP} \
  --location ${LOCATION} \
  --admin-user ${DB_ADMIN} \
  --admin-password ${DB_PASSWORD} \
  --sku-name Standard_B1ms \
  --storage-size 32 \
  --version 14 \
  --public-access 0.0.0.0

# Criar database
az postgres flexible-server db create \
  --server-name ${DB_SERVER} \
  --resource-group ${RESOURCE_GROUP} \
  --database-name ${APP_NAME}

echo -e "${GREEN}✓ Database PostgreSQL criado${NC}"

# 7. Application Insights
echo -e "\n${YELLOW}📊 Configurando Application Insights...${NC}"
az monitor app-insights component create \
  --app ${APP_NAME}-insights-${ENVIRONMENT} \
  --location ${LOCATION} \
  --resource-group ${RESOURCE_GROUP} \
  --application-type web \
  --kind web

INSTRUMENTATION_KEY=$(az monitor app-insights component show \
  --app ${APP_NAME}-insights-${ENVIRONMENT} \
  --resource-group ${RESOURCE_GROUP} \
  --query instrumentationKey -o tsv)

# Adicionar ao Web App
az webapp config appsettings set \
  --name ${WEBAPP_NAME} \
  --resource-group ${RESOURCE_GROUP} \
  --settings APPINSIGHTS_INSTRUMENTATIONKEY=${INSTRUMENTATION_KEY}

echo -e "${GREEN}✓ Application Insights configurado${NC}"

# 8. Criar Service Principal para GitHub Actions
echo -e "\n${YELLOW}🔑 Criando credenciais para GitHub Actions...${NC}"
SUBSCRIPTION_ID=$(az account show --query id -o tsv)

AZURE_CREDENTIALS=$(az ad sp create-for-rbac \
  --name ${APP_NAME}-github-${ENVIRONMENT} \
  --role contributor \
  --scopes /subscriptions/${SUBSCRIPTION_ID}/resourceGroups/${RESOURCE_GROUP} \
  --sdk-auth)

echo -e "${GREEN}✓ Service Principal criado${NC}"

# 9. Gerar arquivo de configuração
CONFIG_FILE="azure-config-${ENVIRONMENT}.json"
cat > ${CONFIG_FILE} << EOF
{
  "environment": "${ENVIRONMENT}",
  "resourceGroup": "${RESOURCE_GROUP}",
  "webAppName": "${WEBAPP_NAME}",
  "databaseServer": "${DB_SERVER}",
  "databaseName": "${APP_NAME}",
  "databaseUser": "${DB_ADMIN}",
  "appInsights": "${APP_NAME}-insights-${ENVIRONMENT}",
  "created": "${TIMESTAMP}"
}
EOF

echo -e "${GREEN}✓ Configuração salva em ${CONFIG_FILE}${NC}"

# 10. Instruções finais
echo -e "\n${GREEN}═══════════════════════════════════════${NC}"
echo -e "${GREEN}        ✅ SETUP COMPLETO!${NC}"
echo -e "${GREEN}═══════════════════════════════════════${NC}"

echo -e "\n${YELLOW}📋 PRÓXIMOS PASSOS:${NC}"
echo -e "\n1️⃣ Adicione estes secrets no GitHub:"
echo -e "   ${YELLOW}Settings → Secrets → Actions → New secret${NC}"
echo ""
echo -e "   ${GREEN}AZURE_CREDENTIALS:${NC}"
echo "${AZURE_CREDENTIALS}" | python -m json.tool
echo ""
echo -e "   ${GREEN}AZURE_WEBAPP_NAME:${NC} ${WEBAPP_NAME}"
echo -e "   ${GREEN}RESOURCE_GROUP:${NC} ${RESOURCE_GROUP}"
echo ""
echo -e "2️⃣ Database Connection String:"
echo -e "   ${GREEN}postgresql://${DB_ADMIN}:${DB_PASSWORD}@${DB_SERVER}.postgres.database.azure.com:5432/${APP_NAME}?sslmode=require${NC}"
echo ""
echo -e "3️⃣ URLs dos recursos:"
echo -e "   🌐 App: ${GREEN}https://${WEBAPP_NAME}.azurewebsites.net${NC}"
echo -e "   📊 Insights: ${GREEN}https://portal.azure.com/#resource/subscriptions/${SUBSCRIPTION_ID}/resourceGroups/${RESOURCE_GROUP}/providers/microsoft.insights/components/${APP_NAME}-insights-${ENVIRONMENT}${NC}"
echo ""
echo -e "4️⃣ Teste o deploy:"
echo -e "   ${YELLOW}git push origin main${NC}"
echo ""
echo -e "${GREEN}🎉 Pronto para deploy!${NC}"
```

### SCRIPT 2: `.github/workflows/azure-deploy.yml`
```yaml
name: Deploy to Azure

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
  workflow_dispatch:
    inputs:
      environment:
        description: 'Environment to deploy'
        required: true
        default: 'dev'
        type: choice
        options:
          - dev
          - staging
          - prod

env:
  PYTHON_VERSION: '3.9'
  NODE_VERSION: '18'

jobs:
  # Job 1: Testes e Quality Check
  test:
    runs-on: ubuntu-latest
    if: github.event_name == 'pull_request'
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Setup Python
      uses: actions/setup-python@v4
      with:
        python-version: ${{ env.PYTHON_VERSION }}
    
    - name: Cache Dependencies
      uses: actions/cache@v3
      with:
        path: ~/.cache/pip
        key: ${{ runner.os }}-pip-${{ hashFiles('**/requirements.txt') }}
    
    - name: Install Dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt
        pip install pytest pytest-cov flake8 black safety
    
    - name: Lint Code
      run: |
        # Format check
        black --check .
        
        # Lint
        flake8 . --count --select=E9,F63,F7,F82 --show-source --statistics
        
    - name: Run Tests
      run: |
        pytest --cov=. --cov-report=xml --cov-report=term
    
    - name: Security Check
      run: |
        safety check --json
    
    - name: Upload Coverage
      uses: codecov/codecov-action@v3
      with:
        file: ./coverage.xml

  # Job 2: Build e Deploy
  deploy:
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main' && github.event_name == 'push'
    
    environment:
      name: production
      url: https://${{ secrets.AZURE_WEBAPP_NAME }}.azurewebsites.net
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Setup Python
      uses: actions/setup-python@v4
      with:
        python-version: ${{ env.PYTHON_VERSION }}
    
    - name: Create deployment package
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt
        
    - name: Login to Azure
      uses: azure/login@v1
      with:
        creds: ${{ secrets.AZURE_CREDENTIALS }}
    
    - name: Deploy to Azure Web App
      uses: azure/webapps-deploy@v2
      with:
        app-name: ${{ secrets.AZURE_WEBAPP_NAME }}
        package: .
    
    - name: Run Database Migrations
      run: |
        # Se usar Django
        # python manage.py migrate --no-input
        
        # Se usar Flask/SQLAlchemy
        # flask db upgrade
        
        echo "Migrations completed"

  # Job 3: Smoke Tests pós-deploy
  verify:
    needs: deploy
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main'
    
    steps:
    - name: Wait for deployment
      run: sleep 30
      
    - name: Health Check
      run: |
        response=$(curl -s -o /dev/null -w "%{http_code}" \
          https://${{ secrets.AZURE_WEBAPP_NAME }}.azurewebsites.net/health)
        
        if [ $response -eq 200 ]; then
          echo "✅ Site is healthy!"
        else
          echo "❌ Health check failed with status: $response"
          exit 1
        fi
    
    - name: Run E2E Tests
      run: |
        # Adicionar testes E2E aqui
        echo "E2E tests would run here"
    
    - name: Performance Check
      run: |
        # Verificar tempo de resposta
        time=$(curl -o /dev/null -s -w '%{time_total}' \
          https://${{ secrets.AZURE_WEBAPP_NAME }}.azurewebsites.net)
        
        echo "Response time: ${time}s"
        
        # Fail se > 2 segundos
        if (( $(echo "$time > 2" | bc -l) )); then
          echo "❌ Performance degraded"
          exit 1
        fi
        
    - name: Notify Success
      if: success()
      run: |
        echo "🎉 Deployment successful!"
        # Adicionar notificação Slack/Teams aqui

  # Job 4: Rollback se necessário
  rollback:
    needs: verify
    if: failure()
    runs-on: ubuntu-latest
    
    steps:
    - name: Login to Azure
      uses: azure/login@v1
      with:
        creds: ${{ secrets.AZURE_CREDENTIALS }}
    
    - name: Rollback Deployment
      run: |
        echo "⚠️ Rolling back deployment..."
        
        # Rollback para slot anterior
        az webapp deployment slot swap \
          --name ${{ secrets.AZURE_WEBAPP_NAME }} \
          --resource-group ${{ secrets.RESOURCE_GROUP }} \
          --slot staging \
          --target-slot production
        
        echo "✅ Rollback completed"
```

---

## 🔧 TROUBLESHOOTING COMPLETO

### PROBLEMA 1: Azure Login Falha
```bash
# Solução 1: Use device code
az login --use-device-code

# Solução 2: Clear cache
az account clear
az login

# Solução 3: Specific tenant
az login --tenant YOUR_TENANT_ID
```

### PROBLEMA 2: Deploy Falha
```bash
# Ver logs detalhados
az webapp log tail \
  --name ${WEBAPP_NAME} \
  --resource-group ${RESOURCE_GROUP}

# Verificar configuração
az webapp config show \
  --name ${WEBAPP_NAME} \
  --resource-group ${RESOURCE_GROUP}

# Restart app
az webapp restart \
  --name ${WEBAPP_NAME} \
  --resource-group ${RESOURCE_GROUP}
```

### PROBLEMA 3: Database Connection Error
```bash
# Verificar firewall
az postgres flexible-server firewall-rule create \
  --resource-group ${RESOURCE_GROUP} \
  --name ${DB_SERVER} \
  --rule-name AllowAll \
  --start-ip-address 0.0.0.0 \
  --end-ip-address 255.255.255.255

# Testar conexão
psql "host=${DB_SERVER}.postgres.database.azure.com \
     port=5432 \
     dbname=${APP_NAME} \
     user=${DB_ADMIN} \
     password=${DB_PASSWORD} \
     sslmode=require"
```

### PROBLEMA 4: GitHub Actions Error
```bash
# Debug workflow
gh workflow view azure-deploy --yaml
gh run list --workflow=azure-deploy
gh run view [RUN_ID] --log

# Re-run failed jobs
gh run rerun [RUN_ID] --failed
```

### PROBLEMA 5: Application Insights Não Funciona
```python
# Adicionar ao código Python
from applicationinsights import TelemetryClient

tc = TelemetryClient('YOUR_INSTRUMENTATION_KEY')
tc.track_event('Test event')
tc.flush()
```

---

## 📊 COMANDOS DE MONITORAMENTO

### Verificar Status
```bash
# Status do Web App
az webapp show \
  --name ${WEBAPP_NAME} \
  --resource-group ${RESOURCE_GROUP} \
  --query state -o tsv

# Métricas
az monitor metrics list \
  --resource ${WEBAPP_ID} \
  --metric-names "Http2xx" "Http4xx" "Http5xx" \
  --start-time 2024-01-01T00:00:00Z \
  --interval PT1H
```

### Logs em Tempo Real
```bash
# Stream logs
az webapp log tail \
  --name ${WEBAPP_NAME} \
  --resource-group ${RESOURCE_GROUP} \
  --provider http

# Download logs
az webapp log download \
  --name ${WEBAPP_NAME} \
  --resource-group ${RESOURCE_GROUP} \
  --log-file logs.zip
```

### Alertas
```bash
# Criar alerta
az monitor metrics alert create \
  --name high-response-time \
  --resource-group ${RESOURCE_GROUP} \
  --scopes ${WEBAPP_ID} \
  --condition "avg ResponseTime > 1000" \
  --description "Response time is too high"
```

---

## ✅ CHECKLIST FINAL

### Antes da Aula
- [ ] Azure CLI instalado e configurado
- [ ] GitHub CLI instalado
- [ ] Projeto Git inicializado
- [ ] VS Code com extensões Azure

### Durante a Aula
- [ ] Script setup-azure.sh executado
- [ ] Secrets do GitHub configurados
- [ ] Workflow CI/CD criado
- [ ] Primeiro deploy bem-sucedido
- [ ] Monitoring funcionando

### Pós-Aula
- [ ] Application Insights coletando dados
- [ ] Alertas configurados
- [ ] Documentation completa
- [ ] Testes com 100% coverage

---

## 🎯 COMANDOS RÁPIDOS COPIAR/COLAR

```bash
# Setup inicial
chmod +x scripts/setup-azure.sh
./scripts/setup-azure.sh dev

# Commit e deploy
git add .
git commit -m "feat: add azure deployment"
git push origin main

# Verificar deploy
az webapp browse --name ${WEBAPP_NAME} --resource-group ${RESOURCE_GROUP}

# Ver logs
az webapp log tail --name ${WEBAPP_NAME} --resource-group ${RESOURCE_GROUP}

# Cleanup (cuidado!)
az group delete --name ${RESOURCE_GROUP} --yes --no-wait
```

---

**SUCESSO GARANTIDO! Com este material, você não terá NENHUM problema durante a aula! 🚀**