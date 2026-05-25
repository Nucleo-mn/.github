# Núcleo MN

**Núcleo Mundial de Negócios e Intermediações Internacionais** — empresa de tecnologia com foco em automação com IA, business intelligence, analytics e intermediação de negócios internacionais.

Sede: Florianópolis / São Paulo — Brasil.

---

## Projetos ativos

### WolfOps — Plataforma de automações

Hub centralizado para gerenciar automações Python em produção. Dashboard com tema dark, autenticação Supabase, controle de processos via subprocess, agendamento (cron substituto), métricas em tempo real via WebSocket, sistema de alertas e CRM integrado.

| Repo | Descrição |
|------|-----------|
| [`wolfops`](https://github.com/nucleo-mn/wolfops) | Hub principal — FastAPI backend + Next.js frontend |
| [`wolfops-bsf`](https://github.com/nucleo-mn/wolfops-bsf) | Automação BSF (Beneficio Social Familiar) — consultas Target via Playwright |
| [`wolfops-cnae-cnpj`](https://github.com/nucleo-mn/wolfops-cnae-cnpj) | Automação CNAE/CNPJ — processa planilhas e consulta portal interno |

Filtro de discovery: [`topic:wolfops`](https://github.com/orgs/nucleo-mn/repositories?q=topic%3Awolfops)

---

## Engenharia / Padrões

### dev-rules — Regras canônicas da Núcleo MN

Source of truth única pras regras de engenharia e operação de IA assistant em todos os projetos da org. Mudanças nas regras entram via PR no próprio repo.

| Repo | Descrição |
|------|-----------|
| [`dev-rules`](https://github.com/nucleo-mn/dev-rules) | `CONTRIBUTING.md` (engenharia) + `CLAUDE.md` (instruções de IA) + templates pra projetos novos |

Cada projeto da org consome via cópia de templates + `CONTRIBUTING.md` local curto apontando pro canônico.

---

## Stack padrão

| Camada | Tecnologia |
|--------|------------|
| Backend | Python 3.11 + FastAPI + supabase-py |
| Frontend | Next.js 16 + Tailwind + shadcn/ui |
| Database | Supabase (PostgreSQL) + DuckDB analítico |
| Automação | Playwright + N8N |
| IA | Claude API (Anthropic) — Sonnet 4.6 padrão |
| Ambiente | Docker + Docker Compose (dev e prod) |
| Deploy | VPS Linux via Docker |

---

## Convenções

> Resumo. Fonte canônica completa em [`nucleo-mn/dev-rules/CONTRIBUTING.md`](https://github.com/nucleo-mn/dev-rules/blob/main/CONTRIBUTING.md).

- **Branching**: GitHub Flow (`main` deployável, branches `feat/`, `fix/`, `docs/`, `chore/`)
- **Commits**: Conventional Commits
- **Versionamento**: SemVer via tags (`vMAJOR.MINOR.PATCH`)
- **Naming convention de repo**: `<projeto>-<componente>` (ex: `wolfops`, `wolfops-bsf`)
- **Topic obrigatório**: `<projeto>` em cada repo do mesmo projeto
- **PR obrigatório** pra `main` (sem commit direto, mesmo solo dev)
- **Self-review formal** (BLOCKER / WARNING / SUGGESTION) antes de pedir merge

---

## Clientes principais

- **SAGASP** — Sindicato do Comércio Atacadista de Alimentos de São Paulo
- **Blue World** — Empresa de eficiência hídrica
