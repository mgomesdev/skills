# format-card-po-ux (Fase 2A — Pré-refinamento de Design Universal)

## Input esperado
- Card M1 do projeto
- Decisões consolidadas entre PO e UX/UI na sessão de prototipação:
  - Resolução das ambiguidades de design ($A_1..A_n$ atribuídas a UX)
  - Estrutura visual e hierarquia (Desktop e Mobile)
  - Mapeamento dos 4 estados da interface (Default, Loading, Erro, Vazio)
  - Diretrizes de acessibilidade e contraste
  - Mapeamento visual dos eventos de observabilidade

## Output gerado

```markdown
══════════════════════════════════════════════════════════════════════════
[HEADLINE]: [Role/Persona] [Ação] [Contexto]
PRÉ-REFINAMENTO PO + UX/UI em [Data]
Participantes: PO · UX/UI
Status: Decisões de experiência e fluxo firmadas · Pronto para o time técnico
══════════════════════════════════════════════════════════════════════════

REGRAS FIRMES (Atualizadas)
[Regras originais do M1 mantidas]
+ NOVO (UX): [Nova regra visual ou de comportamento acordada entre PO e UX]
+ NOVO (UX): [Comportamento mobile acordado]

RESOLVIDO NO PRÉ-REFINAMENTO (UX)
A[N] "[Ambiguidade original de design]" → [Decisão tomada pela UX/UI com a justificativa de experiência]

DECISÕES DE EXPERIÊNCIA & DESIGN SYSTEM
- Layout Desktop: [Estrutura dos blocos principais, grid e hierarquia visual]
- Layout Mobile: [Comportamento responsivo, navegação e densidade de tela]
- Mapeamento dos 4 Estados de Tela:
  · Loading: [Skeleton loader / indicador de carregamento contextual]
  · Erro: [Feedback visual em linha / banner com ação de retry]
  · Vazio (Empty State): [Placeholder visual orientador]
  · Sucesso / Default: [Aparência e comportamento estável]
- Acessibilidade & Usabilidade: [Conformidade com padrões de contraste e navegação por teclado]

OBSERVABILIDADE NO FRONT (Eventos Mapeados no Design)
- [Elemento/CTA 1]: Dispara `event: "[nome_do_evento]"`
- [Elemento/CTA 2]: Dispara `event: "[nome_do_evento]"`
- [Métrica de Permanência]: Critério de leitura/tempo mapeado na jornada

EM ABERTO (Pauta Cirúrgica para os Desenvolvedores)
  Para Frontend:
  - [Viabilidade técnica de componentes complexos ou animações]
  - [Reaproveitamento de componentes existentes do Design System]
  Para Backend / Arquitetura:
  - [Modelagem dos dados necessários para abastecer a tela]
  - [Endpoints, schemas e performance de resposta]
  Para o PO:
  - [Exceções de regra de negócio ainda pendentes]

FIGMA & ENTREGÁVEIS
→ [Link do fluxo no Figma atualizado]
Ajustes que UX/UI fará antes do refinamento completo com os devs:
- [ ] Desenhar variações de estados faltantes
- [ ] Documentar tokens e espaçamentos

INTENSIDADE ACORDADA
- Esqueleto mantido: [Validação de que a proposta visual cabe na fatia mínima da iteração]
══════════════════════════════════════════════════════════════════════════
```

## Regras de aplicação
- Registrado no backlog/board na transição entre a fase de Prototipação e Refinamento Técnico.
- Serve como insumo limpo para a análise assíncrona dos desenvolvedores antes do call de refinamento.
