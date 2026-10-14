# format-card-m2 (Card Refinado INVEST — Bill Wake)

## Input esperado
- Card M1 existente
- Decisões tomadas na conversa de refinamento com o time completo:
  - [V] Métricas de observabilidade e eventos de telemetria refinados
  - [I] Alinhamento de dependências e estratégia de release
  - [N] Ambiguidades resolvidas com dono e decisões de UX/UI (desktop, mobile, 4 estados)
  - [E] Contrato de dados/API (schemas Zod, endpoints/handlers MSW), regras firmes atualizadas e riscos
  - [S] Intensidade acordada por todos (escopo do esqueleto confirmado)
  - [T] Critérios de Aceitação BDD co-escritos com mensagem exata e visual

## Output gerado

```markdown
══════════════════════════════════════════════════════════════════════════
[HEADLINE] — REFINADO em [Data]
Participantes: [PO · UX/UI · Frontend · Backend]
Status: Pronto para Planning · Todas as ambiguidades resolvidas
══════════════════════════════════════════════════════════════════════════

[V] VALIOSO (Valuable & Observability)
--------------------------------------------------------------------------
• Valor de Negócio: [Confirmação do impacto esperado]
• Observabilidade & Eventos de Telemetria:
  - [Métrica HEART / Sinal]: [Comportamento esperado pós-lançamento]
  - Evento de produto 1: `event: "[nome_do_evento]"` (disparado ao [ação])
  - Evento de produto 2: `event: "[nome_do_evento]"` (disparado ao [ação])

[I] INDEPENDENTE (Independent & Release Strategy)
--------------------------------------------------------------------------
• Dependências Mapeadas: [Status das dependências e mitigações acordadas]
• Estratégia de Deploy: [Deploy independente, feature flag ou preview isolado]

[N] NEGOCIÁVEL — RESOLVIDO NO REFINAMENTO (Negotiable Closed)
--------------------------------------------------------------------------
• Ambiguidades Resolvidas:
  A1 "[Descrição original]" → [Decisão tomada · Quem decidiu · Por quê]
  A2 "[Descrição original]" → [Decisão tomada · Quem decidiu · Por quê]

• Decisões de Experiência & Design System:
  - Layout Desktop: [Estrutura dos blocos e hierarquia]
  - Layout Mobile: [Comportamento responsivo / gavetas / navegação]
  - Mapeamento dos 4 Estados:
    · Loading: [Skeleton loader / spinner]
    · Erro: [Feedback visual em linha / banner de retry]
    · Vazio: [Placeholder com mensagem orientadora]
    · Sucesso / Default: [Aparência estável]
  - Acessibilidade & Contraste: [Diretrizes WCAG AA / tokens Dark e Light]
• Figma:
  → [Link atualizado] — Ajustes que UX/UI atualizará antes do sprint

[E] ESTIMÁVEL — ESPECIFICAÇÃO TÉCNICA (Estimable Specifications)
--------------------------------------------------------------------------
• Regras Firmes Consolidadas:
  [Regras originais do M1 mantidas]
  + NOVO (Refinamento): [Novas regras acordadas pelo time]

• Contratos de Dados & API:
  - Schemas / Contratos (Zod / TypeScript):
    `[Definição tipada dos payloads e contratos]`
  - Endpoints / Handlers (MSW / REST):
    `[Método, rota, status codes e payloads esperados]`

• Decisões Arquiteturais & Riscos:
  - Decisões: [Estratégia de cache, parser, persistência]
  - Riscos Sinalizados: [Risco técnico mapeado com mitigação acordada]

[S] SMALL / PEQUENO — INTENSIDADE ACORDADA (Small Agreement)
--------------------------------------------------------------------------
• Escopo Desta Iteração (Esqueleto / Fatia Mínima):
  [Lista exata do que entra nesta entrega — validado por devs e PO]
• Fora Desta Iteração (Próximas Intensificações):
  [Lista do que fica explicitamente para os próximos ciclos]

[T] TESTÁVEL — CRITÉRIOS DE ACEITAÇÃO (Testable CAs)
--------------------------------------------------------------------------
CA1 — [Título do Cenário]
Dado [contexto inicial],
quando [ação do usuário ou sistema],
então [resultado observável]
→ Mensagem: "[texto exato exibido na tela]"
→ Visual: [estado visual do componente, cores e posicionamento]
→ Telemetria: `event: "[nome_do_evento]"` (se aplicável)

CA2 — [Título do Cenário]
Dado [contexto],
quando [ação],
então [resultado]
→ Mensagem: "[texto exato]"
→ Visual: [comportamento na tela]
══════════════════════════════════════════════════════════════════════════
```

## Regras de aplicação
- Substitui a Descrição do Work Item no Azure DevOps (coluna `Refinement`).
- O bloco [T] deve ser copiado integralmente no campo `Acceptance Criteria` do Azure DevOps.
- Cada CA deve ter obrigatoriamente **Mensagem Exata** e **Comportamento Visual**.
