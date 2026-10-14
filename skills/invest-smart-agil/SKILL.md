---
name: invest-smart-agil
description: "Skill ágil universal para conduzir a criação, refinamento e planejamento de features em qualquer projeto de software seguindo os 3 Cs (Card, Conversation, Confirmation), INVEST (Bill Wake) para histórias e SMART para tasks, com observabilidade de produto integrada desde a ideação."
---

# Invest-Smart-Ágil (Universal Agile Framework)

Skill ágil e agnóstica para orquestrar o ciclo de vida completo de features em **qualquer projeto de produto digital ou engenharia de software**.
Combina os **3 Cs de Ron Jeffries** (Card, Conversation, Confirmation), os critérios **INVEST de Bill Wake (2003)** para Histórias de Usuário e **SMART** para Tarefas Técnicas, com **Observabilidade e Métricas de Produto** integradas desde a ideação.

---

## 🏛️ Filosofia Central (XP + Spec-Driven)

```
"A História é o bolo completo (INVEST); as Tarefas são as camadas (SMART)."
```

1. **Cartão (Card):** Lembrete digital inicial, propositalmente sucinto e aberto (`format-card-m1`).
2. **Conversa (Conversation):** Co-criação multidisciplinar iterativa (PO + UX na Fase 2A, Time completo na Fase 2B).
3. **Confirmação (Confirmation):** Critérios de Aceitação BDD verificáveis + telemetria de valor pós-lançamento (`format-card-m2`).

> **Regra de Ouro / Teste de Completude:**
> Se o desenvolvedor precisar interromper a implementação para perguntar regras de negócio, comportamento de tela ou mensagem de erro ao PO, o refinamento falhou.

---

## 🔄 Fluxo de Trabalho (Das Ideias ao Código)

O fluxo se adapta aos estados padrões de qualquer ferramenta de gestão ágil (Azure Boards, Jira, Linear, GitHub Projects):

```
[Proposição / Backlog] ➔ [Prototipação / UX] ➔ [Refinamento Técnico] ➔ [Planning / To Do]
Fase 1: Criação           Fase 2A: PO + UX     Fase 2B: Time Todo      Fase 3: Planning
Card Inicial (M1)         Figma & Visual       Card Refinado (M2)      Tasks SMART (Devs)
```

1. **Fase 1 — Criação (PO Sozinho):**
   * **Gatilho:** PO apresenta uma demanda, dor de cliente ou oportunidade de produto.
   * **Execução:** Entrevista estruturada das dimensões essenciais (`po-idea`).
   * **Validação Silenciosa:** Análise interna de conformidade INVEST (`check-invest`).
   * **Saída:** Card Inicial M1 estruturado em **[V], [I], [N], [E], [S], [T]** (`format-card-m1`).

2. **Fase 2A — Pré-Refinamento (PO + UX/UI):**
   * **Gatilho:** O card avança para design/prototipação.
   * **Execução:** Alinhamento de jornada do usuário. O protótipo no Figma é tratado como **referência viva** (não como especificação rígida).
   * **Saída:** Resolução de ambiguidades visuais e mapeamento de estados de tela (Default, Loading, Erro, Vazio) (`format-card-po-ux`).

3. **Fase 2B — Refinamento Completo (Time Todo):**
   * **Gatilho:** Refinamento técnico multidisciplinar (PO, UX, Frontend, Backend/Engenharia).
   * **Execução:** Análise assíncrona/local de viabilidade e contratos técnicos + Call síncrono curto para fechar pendências e conflitos.
   * **Saída:** Card Refinado M2 com Critérios de Aceitação BDD, mensagens exatas, contratos de interface e telemetria (`format-card-m2`).

4. **Fase 3 — Planning (Quebra em Tasks SMART):**
   * **Gatilho:** Card M2 aprovado para desenvolvimento.
   * **Execução:** Especialistas quebram a história em tasks técnicas autônomas no padrão **SMART** (`task-smart`).
   * **Regra de Cobertura 100%:** Todo Critério de Aceitação (CA) deve ser viabilizado por ao menos uma task técnica.

---

## 📊 Observabilidade de Produto Integrada (Outcome vs. Output)

Nenhuma feature é considerada completa sem a definição de **como mediremos se o valor foi alcançado no mundo real**.
Toda história define hipóteses de valor mensuráveis (baseadas em frameworks como HEART ou Pirate Metrics):

* **Adoção / Aquisição:** Volume de usuários engajando com a nova funcionalidade.
* **Engajamento / Retenção:** Frequência e profundidade de uso real.
* **Taxa de Sucesso / Conversão:** Conclusão da tarefa principal sem erros ou atritos.
* **Acessibilidade & Performance:** Tempos de carregamento e respeito às preferências do usuário.

---

## 🛠️ Regras de Comportamento do Agente

* **Agnóstico e Adaptável:** Adapta-se automaticamente ao domínio do projeto ativo, às suas personas e à sua stack tecnológica.
* **Direto e Cirúrgico:** Não narra processos internos desnecessariamente.
* **Uma pergunta por vez:** Na condução de entrevistas, faz apenas uma pergunta por turno para manter o foco do usuário.
* **Silencioso no Sucesso:** O validador INVEST roda em segundo plano e só interrompe se houver bloqueios graves (ex: história sem valor externo perceptível ou critérios inviáveis).
* **Linguagem Natural:** Prioriza termos amigáveis de produto ("Card Inicial", "Card Refinado", "Tasks técnicas").
