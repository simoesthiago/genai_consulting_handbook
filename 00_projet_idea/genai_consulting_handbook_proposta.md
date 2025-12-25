# Proposta de Projeto — **genai-consulting-handbook**
Guia prático (“handbook”) para consultores estratégicos dominarem **GenAI/Agentic AI** em contexto corporativo, com foco em **decisão, arquitetura, governança, delivery e escolha de plataformas**.

---

## 1) Objetivo do repositório
O **genai-consulting-handbook** é um repositório estruturado para:
- Padronizar linguagem e entendimento (executivo e técnico) sobre GenAI/Agentic AI.
- Servir como referência prática para **pré-venda**, **discovery**, **desenho**, **MVP/POC**, **piloto** e **escala**.
- Acelerar criação de **artefatos consulting-ready** (checklists, perguntas, templates, storylines, matrizes).
- Apoiar decisão pragmática de stack e vendors com critérios e sinais de lock-in.

---

## 2) Estrutura final do repositório (como “fonte de verdade”)
A estrutura abaixo é a “ideal” (conforme você definiu):

```text
genai-consulting-handbook/
├── README.md
├── GLOSSARY.md
├── 01-foundations/
│   ├── llm_fundamentals.md
│   ├── prompt_engineering.md
│   └── hallucinations_basics.md
│
├── 02-solution-components/
│   ├── rag.md
│   ├── tool_calling.md
│   ├── mcp.md
│   ├── guardrails.md
│   ├── evals.md
│   ├── observability_llmops.md
│   ├── agentic_ai.md
│   └── multi_agent_systems.md
│
├── 03-consulting-workflows/
│   ├── discovery_and_research.md
│   ├── problem_structuring.md
│   ├── analysis_and_modeling.md
│   ├── slidewriting_and_storytelling.md
│   ├── client_comms_and_emails.md
│   └── project_management.md
│
├── 04-use-case-archetypes/
│   ├── genai_copilots_internal.md
│   ├── knowledge_management.md
│   ├── customer_experience_bots.md
│   ├── process_automation.md
│   └── agentic_automation.md
│
├── 05-enterprise_digital_transformation/
│   ├── business-led-digital-roadmap.md
│   ├── talent.md
│   ├── operating_model.md
│   ├── technology.md
│   ├── data.md
│   └── adoption_and_scaling.md
│
├── 06-risk-governance-ethics/
│   ├── data_privacy_and_security.md
│   ├── quality_and_evals_governance.md
│   └── change_management.md
│
├── 07-tools-and-platforms/
│   ├── productivity_tools.md
│   ├── enterprise_stack_examples.md
│   └── vendor_selection_matrix.md
│
└── 08-resources/
    ├── books_and_papers.md
    ├── courses_and_videos.md
    └── further_reading.md
```

> **Observação de consistência (opcional, mas recomendada):** padronizar nomes de arquivo (ex.: `snake_case` em tudo). Se desejar, mude `business-led-digital-roadmap.md` para `business_led_digital_roadmap.md`.

---

## 3) Princípios editoriais (para manter MECE e evitar duplicação)

### 3.1 Regra do “capítulo canônico” (DRY)
Cada tema deve ter **um arquivo canônico** (a “casa principal”). Outros arquivos podem:
- referenciar com link,
- citar 1–2 bullets,
- **não reexplicar** o mesmo conteúdo em profundidade.

### 3.2 Separação “técnico vs governança”
- `02-solution-components/*` descreve **como construir** (padrões técnicos, arquitetura, trade-offs, métricas).
- `06-risk-governance-ethics/*` descreve **como controlar** (políticas, responsabilidades, gates, LGPD, auditoria).

### 3.3 Obrigatório responder “So what?”
Cada arquivo deve responder explicitamente:
- Por que isso importa em empresa (custo, risco, operação, reputação)?
- Quais decisões reais isso habilita?
- Quais erros (anti‑padrões) isso previne?

---

## 4) Convenções do repositório (para ser “consulting-ready”)

### 4.1 Header padrão em todos os arquivos
Use este bloco no topo de cada `.md`:

```md
# <Título>

**Objetivo:** <1 frase>
**Para quem:** <consultor / arquitetura / segurança / produto>
**Quando usar:** <2–3 bullets>
**Pré-requisitos:** <links internos>
**Relacionados:** <links internos>

## TL;DR (30 segundos)
- ...
- ...
- ...

## O que entra / O que não entra
**Entra:** ...
**Não entra:** ...
```

### 4.2 Estratégia de links internos (navegabilidade)
- `README.md` deve ter **índice** + **trilhas por persona**:
  - Estratégia/Executivo
  - Arquitetura/Engenharia
  - Delivery/PMO
- Cada arquivo deve terminar com:
  - **Próximos passos** (links para 2–3 páginas recomendadas)

### 4.3 Glossário como “fonte única de verdade”
- `GLOSSARY.md` deve ser a referência de termos.
- Regra: novos termos importantes devem aparecer no glossário.

### 4.4 Definition of Done (DoD) para qualquer arquivo
Um arquivo é “pronto” quando contém:
- TL;DR
- **1 diagrama OU 1 checklist prático**
- Trade-offs e anti‑padrões
- Um bloco de **Perguntas de discovery** OU **Exercício prático**
- Links relacionados (para evitar repetição)

---

## 5) Templates por tipo de página

### 5.1 Template para páginas de conceito (ex.: fundamentos)
```md
## Resumo executivo (5 bullets)
## Definição e o que NÃO é
## Por que importa em empresa
## Exemplo simples
## Anti‑padrões comuns
## Checklist de decisão (quando usar/evitar)
## Exercícios práticos
## Perguntas de discovery (para cliente)
## Leituras adicionais (links internos)
```

### 5.2 Template para padrões técnicos (ex.: RAG, tool calling, agentes)
```md
## Quando usar / quando evitar
## Arquitetura (diagrama)
## Componentes e fluxo (end-to-end)
## Controles e segurança (técnicos)
## Métricas e evals (linkar para evals)
## Trade-offs e decisões (mini ADR)
## Pitfalls (como diagnosticar)
## Checklist “MVP” e “Produção”
## Exercícios práticos / cenários adversariais
```

**Mini ADR (para decisões e trade-offs)**
```md
## Decisões e trade-offs (mini ADR)
- Decisão: ...
- Alternativas: ...
- Por que escolhemos: ...
- Riscos: ...
- Como monitorar: ...
```

### 5.3 Template para playbook de caso de uso (arquétipos)
```md
## Problema e valor (KPIs)
## Personas e jornada (as-is / to-be)
## Arquitetura sugerida (diagrama + componentes)
## Dados e integrações
## Guardrails e governança (link para 06)
## MVP (4–6 semanas) + extensões
## Evals e critérios de aceite
## Riscos e mitigação
## Demo script (3–5 min)
## Perguntas de discovery específicas
```

### 5.4 Template para vendor/stack (visão pragmática)
```md
## Quando faz sentido escolher (sinais positivos)
## Quando evitar (sinais de alerta)
## Stack típico (componentes canônicos)
## Integrações e pontos fortes
## Riscos / lock-in e mitigação
## Checklist de decisão
## Perguntas para TI/Sec/Legal/Procurement
```

---

## 6) Plano de montagem — como criar os arquivos

### Etapa 1 — Skeleton completo (rápido: 1–2 dias)
Crie **todos os arquivos** com:
- header padrão,
- TL;DR vazio,
- seções principais,
- links em “Relacionados” e “Próximos passos”.

Resultado: repositório navegável e consistente.

### Etapa 2 — Conteúdo essencial (v0.1: 1–2 semanas)
Priorize estes arquivos para ter uma versão “usável com cliente”:
- `01-foundations/llm_fundamentals.md`
- `01-foundations/prompt_engineering.md`
- `02-solution-components/rag.md`
- `02-solution-components/tool_calling.md`
- `02-solution-components/guardrails.md`
- `02-solution-components/evals.md`
- `03-consulting-workflows/discovery_and_research.md`
- `03-consulting-workflows/slidewriting_and_storytelling.md`
- `06-risk-governance-ethics/data_privacy_and_security.md`
- `07-tools-and-platforms/vendor_selection_matrix.md`

### Etapa 3 — Completar arquétipos e transformação (v0.2: 2–4 semanas)
- Preencher os arquétipos (pasta `04`) com:
  - 1 diagrama,
  - 1 demo script,
  - 1 checklist de discovery por arquétipo.
- Completar a pasta `05` para conectar com escala (roadmap, operating model, adoção).

---

## 7) Como montar o conteúdo por pasta (orientação por arquivo)

## 7.1 `README.md` (porta de entrada)
**Objetivo:** orientar navegação, trilhas e como usar em projeto real.

**Estrutura recomendada:**
1) O que é este handbook (1 parágrafo)
2) Como usar (3 modos):
   - Pré-venda (qualificação + proposta/POC)
   - Discovery e desenho
   - Build/pilot/scale (com governança)
3) Trilhas sugeridas (por persona)
4) Índice por pasta (links)
5) Padrão editorial (DoD resumido)
6) Avisos (não é aconselhamento jurídico; adaptar ao cliente)

## 7.2 `GLOSSARY.md` (glossário operacional)
**Objetivo:** padronizar termos e reduzir ruído em projetos/clientes.

**Formato por termo:**
```md
## <Termo>
**Definição:** ...
**Por que importa:** ...
**Relacionados:** ...
```

---

## 7.3 Pasta `01-foundations/` (conceitos base)
> Regra: “o que é e por que importa”. “Como implementar” vai para `02`.

### `llm_fundamentals.md`
- Modelo mental: tokens, next-token prediction, contexto
- Limites: alucinação, contexto, custo/latência
- Implicações enterprise (segurança, auditoria, confiabilidade)
- Anti‑padrões de expectativa
- Exercícios: estimativa tokens/custo, teste temperatura, política de abstenção

### `prompt_engineering.md`
- Padrões: Role/Task/Constraints/Output Format/Few‑shot/Rubric
- Saída estruturada (JSON) e contratos
- Prompt injection (visão; mitigação detalhada em `guardrails.md`)
- Checklist de qualidade do prompt
- Exercícios: schema+parse, rubric+avaliação, prompt versioning

### `hallucinations_basics.md`
- Definição operacional (para empresa)
- Causas frequentes
- Mitigações em camadas (alto nível)
- Como explicar para C-level
- Exercício: casos de abstenção correta vs resposta com evidência

---

## 7.4 Pasta `02-solution-components/` (engenharia aplicada)

### `rag.md`
- Pipeline E2E (ingestão → chunking → index → retrieval → rerank → geração)
- Qualidade: diagnóstico (context recall/precision)
- Graphrag x rag tradicional
- Segurança: ABAC no retrieval + citações + sanitização do contexto recuperado
- Métricas/evals (link para `evals.md`)
- Trade-offs: chunk size, top-k, híbrida, rerank
- Checklists “MVP” e “Produção”

### `tool_calling.md`
- Contratos: schemas, validação, idempotência
- Confiabilidade: retries/backoff, rate limit, circuit breaker
- Segurança: allowlist, auditoria, “confused deputy”
- Observabilidade de tool calls

### `mcp.md`
- Problema que resolve e onde encaixa na arquitetura
- Governança: autenticação, catálogo, permissões
- Riscos e checklists
- Template: catálogo de servidores MCP (nome, propósito, permissões, owner)

### `guardrails.md`
- Taxonomia: conteúdo, ferramenta, dados
- Controles técnicos: validação, políticas, sanitização, abstenção, HITL
- Mitigação de prompt injection (usuário e documento)
- Logging seguro (o que logar / o que nunca logar)
- Link canônico para governança: `../06-risk-governance-ethics/data_privacy_and_security.md`

### `evals.md`
- Offline vs online
- Rubricas, golden set e regressão em CI
- Métricas por tipo: RAG, tool calling, agentes
- Adversarial tests e red teaming básico

### `observability_llmops.md`
- Instrumentação: request ID, tokens, retrieval IDs, tool calls
- Tracing end-to-end (visão)
- FinOps: token budget, caching, roteamento por modelo
- Runbooks e SLOs (link para governança)

### `agentic_ai.md`
- Workflow vs agentic (decisão orientada a risco)
- Padrões single-agent
- Budget e stopping criteria (obrigatório)
- HITL para ações críticas
- Métricas (success rate, custo por tarefa, escalonamento)

### `multi_agent_systems.md`
- Quando faz sentido (especialização, validação independente, separação de contexto)
- Padrões: supervisor/worker, critic/validator, handoffs com contratos
- Riscos: loops, custo, coordenação
- Controles: quotas e termination detection

---

## 7.5 Pasta `03-consulting-workflows/` (método de consultoria)

### `discovery_and_research.md`
- Objetivos e agenda do workshop
- Checklist de informações (sistemas, dados, IAM, compliance)
- Perguntas por stakeholder
- Saídas: backlog, riscos, hipóteses, métricas
- Template: “Discovery Notes”

### `problem_structuring.md`
- Como transformar “queremos GenAI” em problema operacional
- Fronteiras in/out e definição de caso de uso
- Value hypothesis e riscos
- Template: “Use Case Card”

**Use Case Card**
```md
**Use case:** ...
**Usuários:** ...
**Decisão/tarefa:** ...
**Dados/fonte de verdade:** ...
**Ações (tools):** ...
**Risco:** baixo/médio/alto (por quê)
**Métrica:** ...
**MVP (4–6 semanas):** ...
```

### `analysis_and_modeling.md`
- ROI e custo (ordens de grandeza)
- Modelo de benefício vs custo operacional (FinOps)
- “Custo por caso/jornada”
- Template: narrativa executiva de business case

### `slidewriting_and_storytelling.md`
- Storyline padrão para GenAI (problema → abordagem → risco → plano → métricas)
- Templates de títulos e slides
- Checklist de clareza e evidência
- Estrutura de deck para POC, para transformação e para governança

### `client_comms_and_emails.md`
- Modelos de e-mail: recap, pedido de dados, alinhamento, decisão
- Tom e call to action
- Anti‑padrões: prometer performance sem evidência

### `project_management.md`
- Plano 30/60/90
- RACI mínimo e cadências
- RAID log (risks, assumptions, issues, decisions)
- Controle de mudanças (prompt/modelo/pipeline)

---

## 7.6 Pasta `04-use-case-archetypes/` (playbooks replicáveis)
> Regra: cada arquivo deve ser copiável para um cliente (problema, arquitetura, dados, métricas, riscos, demo).

Arquivos:
- `genai_copilots_internal.md`: copiloto interno com RAG + ACL + citações
- `knowledge_management.md`: curadoria, atualização, expiração e governança do corpus
- `customer_experience_bots.md`: atendimento ao cliente com escalonamento e compliance
- `process_automation.md`: workflow determinístico com IA (previsível)
- `agentic_automation.md`: automação agentic com budget, stopping criteria e HITL

---

## 7.7 Pasta `05-enterprise_digital_transformation/` (ponte para escala)

### `business-led-digital-roadmap.md`
- Roadmap orientado a valor (portfolio)
- Sequenciamento: quick wins vs foundations
- Template: roadmap por ondas (0–3 / 3–6 / 6–12 meses)

### `talent.md`
- Papéis e competências (produto, eng, sec, data, ops)
- Estruturas de time (AI product vs AI platform)
- Template: matriz de skills

### `operating_model.md`
- AI Factory (intake → build → eval → pilot → prod → monitor → retire)
- RACI e gates
- Artefatos por fase (ex.: prompt cards, DPIA quando aplicável)

### `technology.md`
- Arquitetura de plataforma (model gateway, tool gateway, observability)
- Buy vs build (critérios)
- Links para `07-tools-and-platforms/*`

### `data.md`
- “Data readiness” para GenAI (qualidade, lineage, classificação)
- Dados estruturados vs não estruturados
- Estratégia do corpus e governança de documentos

### `adoption_and_scaling.md`
- Adoção e mudança: treinamento, comunicação, incentivos
- Métricas de adoção e qualidade
- Anti‑padrões: “pilotos eternos”, “Shadow AI”

---

## 7.8 Pasta `06-risk-governance-ethics/` (controle e governança)

### `data_privacy_and_security.md`
- LGPD (minimização, necessidade, retenção)
- IAM: RBAC/ABAC e “confused deputy”
- DLP e logging seguro
- Threat model leve (STRIDE-lite)
- Checklist de segurança mínima do MVP

### `quality_and_evals_governance.md`
- Definição de qualidade por categoria
- Gates: POC → piloto → produção
- Red teaming e testes adversariais
- Gestão de mudanças (prompt/modelo/pipeline)
- Link para `../02-solution-components/evals.md`

### `change_management.md`
- Rollout (canary, feature flags)
- Runbook de incidentes (qualidade caiu, custo explodiu, vazamento suspeito)
- Políticas de uso e comunicação organizacional

---

## 7.9 Pasta `07-tools-and-platforms/` (stack e seleção)

### `productivity_tools.md`
- Ferramentas do consultor (pesquisa, escrita, slides)
- Uso seguro e redaction
- Workflows prontos (do workshop ao one-pager)

### `enterprise_stack_examples.md`
- Exemplos de stack por contexto (Microsoft-centric, AWS-centric, data-platform-centric)
- Componentes canônicos e trade-offs
- “Onde dá ruim” + mitigação

### `vendor_selection_matrix.md`
- Critérios e pesos (IAM, residência, integrações, custo, observabilidade, lock-in)
- Perguntas de procurement e segurança
- Template de matriz + 2 exemplos preenchidos

---

## 7.10 Pasta `08-resources/` (curadoria)
- `books_and_papers.md`: lista curada com “por que ler” e nível
- `courses_and_videos.md`: top 3 por tema, por persona
- `further_reading.md`: links complementares com justificativa

---

## 8) Resumo final do projeto (pastas, finalidades e propósitos)

### Visão geral
O **genai-consulting-handbook** é um handbook estruturado para consultores aplicarem GenAI/Agentic AI com rigor corporativo. Ele combina:
- Fundamentos claros,
- Padrões técnicos de solução,
- Métodos de consultoria,
- Arquétipos de casos de uso,
- Transformação para escala,
- Governança e risco,
- Critérios de stack e vendor,
- Curadoria de recursos.

### Pastas e finalidade
- **`01-foundations/`**: fundamentos (o que é e por que importa).
- **`02-solution-components/`**: componentes técnicos (como construir) com trade-offs, métricas e checklists.
- **`03-consulting-workflows/`**: método de consultoria e entregáveis para discovery, análise, storytelling e gestão.
- **`04-use-case-archetypes/`**: playbooks replicáveis por tipo de caso (problema → arquitetura → métricas → demo).
- **`05-enterprise_digital_transformation/`**: conexão com transformação e escala (roadmap, talento, operating model, dados, adoção).
- **`06-risk-governance-ethics/`**: governança, segurança, privacidade e gates de qualidade.
- **`07-tools-and-platforms/`**: visão pragmática de ferramentas, stacks e matriz de seleção de vendors.
- **`08-resources/`**: bibliografia e materiais complementares (apêndice).

---

## 9) Próximos passos recomendados
1) Criar skeleton de todos os arquivos com o header padrão e links.
2) Preencher v0.1 com os 10 arquivos prioritários.
3) Expandir arquétipos e transformação (v0.2) com foco em “copy/paste para cliente”.
