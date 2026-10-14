---
name: invest-smart-agil
description: "Skill ágil para conduzir a criação, refinamento e planejamento de features no projeto personal-branding seguindo os 3 Cs (Card, Conversation, Confirmation), INVEST para histórias e SMART para tasks, com observabilidade de produto (HEART) integrada desde a ideação."
---

# Invest-Smart-Ágil (Personal Branding Edition)

Skill para conduzir o ciclo de vida ágil de features no projeto **personal-branding** (`The Agentic Curator`).
Garante que todo requisito nasça com valor claro, seja refinado colaborativamente sem reuniões infinitas e se desdobre em entregas verificáveis com observabilidade contínua.

---

## 🏛️ Filosofia Central (XP + Spec-Driven)

```
"A História é o bolo completo (INVEST); as Tarefas são as camadas (SMART)."
```

1. **Cartão (Card):** Lembrete digital inicial, propositalmente incompleto (`format-card-m1`).
2. **Conversa (Conversation):** Co-criação multidisciplinar (PO + UX na Fase 2A, Time completo na Fase 2B).
3. **Confirmação (Confirmation):** Critérios de Aceitação BDD verificáveis + telemetria de valor (`format-card-m2`).

> **Regra de Ouro / Teste de Completude:**
> Se o desenvolvedor precisar parar durante o desenvolvimento para perguntar regra de negócio, comportamento de tela ou mensagem de erro ao PO, o refinamento falhou.

---

## 🔄 Fluxo das Fases no Azure DevOps

```
[Proposing]         ➔ [Prototyping]      ➔ [Refinement]       ➔ [To Develop]
Fase 1: Criação       Fase 2A: PO + UX     Fase 2B: Completo    Fase 3: Planning
Card Inicial (M1)     Figma & Visual       Card Refinado (M2)   Tasks SMART (Devs)
```

1. **Fase 1 — Criação (PO Sozinho):**
   * Gatilho: PO traz uma dor bruta ou ideia.
   * Executa `po-idea` (5 dimensões + Observabilidade).
   * Validação silenciosa via `check-invest`.
   * Gera `format-card-m1` e cria/atualiza o Work Item no Azure DevOps (`Proposing`).

2. **Fase 2A — Pré-Refinamento (PO + UX/UI):**
   * Gatilho: Card inicial avança para prototipação (`Prototyping`).
   * Alinhamento visual e de fluxo usando o Figma como **referência viva** (não spec rígida).
   * Resolução das ambiguidades de design ($A_1..A_n$).
   * Mapeamento de 4 estados: Default, Loading, Erro e Vazio (Empty State).
   * Gera o **Card Pré-Refinado (PO+UX)** com pauta técnica limpa para os devs.

3. **Fase 2B — Refinamento Completo (Time Todo):**
   * Devs (Front e Back) analisam viabilidade e contratos (Zod/MSW/API).
   * Call curto e cirúrgico para sanar apenas conflitos e pendências restantes.
   * Gera `format-card-m2` com Critérios de Aceitação BDD, mensagens exatas e eventos de observabilidade (`Refinement`).

4. **Fase 3 — Planning (Quebra em Tasks SMART):**
   * Devs quebram o Card M2 em tasks técnicas autônomas (`format-task-smart`).
   * UX/UI publica entregáveis do Figma organizados pelo caminho crítico das tasks de Front.
   * Regra de Cobertura 100%: todo CA deve ser viabilizado por ao menos 1 task (`To Develop`).

---

## 📊 Observabilidade de Produto (HEART Integrado)

Nenhuma feature é considerada refinada sem **critérios objetivos de observabilidade pós-lançamento**.
Toda história deve definir como saberemos se a dor foi realmente resolvida:

* **Happiness / Adoção:** Volume de uso, novos visitantes, taxa de conversão nos CTAs de contato/CV.
* **Engagement:** Tempo de leitura real no artigo vs. tempo estimado, interações com código.
* **Task Success:** Conclusão fluida de downloads, filtros e navegação sem erros.
* **Acessibilidade:** Telemetria de alternância de tema Dark/Light e respeito a `prefers-reduced-motion`.

---

## 🛠️ Regras de Comportamento do Agente

* **Direto e objetivo:** Não narrar o processo interno ("agora estou executando o atom X").
* **Uma pergunta por vez:** Na entrevista com o PO (`po-idea`), faça uma pergunta de cada vez para manter a conversa fluida e focada.
* **Silencioso no sucesso:** O `check-invest` só gera saída visível se houver problema grave (bloqueio por falta de valor ou teste inviável) ou aviso relevante.
* **Linguagem natural:** Chamar de "Card Inicial" (não M1), "Card Refinado" (não M2), "Tasks" (não SMART tasks).
* **Respeito aos papéis:** Não pedir decisões de API para o PO nem decisões de regra de negócio para os Devs.
