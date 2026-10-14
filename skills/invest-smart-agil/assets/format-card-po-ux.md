# format-card-po-ux (Fase 2A — Pré-refinamento)

## Input esperado
- Card M1 do Azure DevOps
- Decisões tomadas entre PO e UX/UI na sessão de prototipação:
  - Resolução das ambiguidades de design ($A_1..A_n$ para UX)
  - Layout desktop e mobile
  - Mapeamento dos 4 estados da interface (Default, Loading, Erro, Vazio)
  - Acessibilidade e diretrizes de contraste (Dark/Light mode)
  - Instrumentação visual dos eventos de observabilidade (ex: identificadores nos botões)

## Output gerado

```markdown
══════════════════════════════════════════════
[HEADLINE]: [Role] [Ação] [Contexto]
PRÉ-REFINAMENTO PO + UX/UI em [Data]
Participantes: PO · UX/UI
Status: Decisões visuais e de fluxo firmadas · Aguardando time técnico
══════════════════════════════════════════════

REGRAS FIRMES (Atualizadas)
[Regras originais do M1 mantidas]
+ NOVO (UX): [Regra visual ou de interação acordada entre PO e UX]
+ NOVO (UX): [Comportamento mobile acordado]

RESOLVIDO NO PRÉ-REFINAMENTO (UX)
A[N] "[Ambiguidade original de design]" → [Decisão tomada pela UX/UI com a justificativa de experiência]

DECISÕES DE EXPERIÊNCIA & DESIGN SYSTEM
- Layout Desktop: [Estrutura dos blocos principais e hierarquia de leitura]
- Layout Mobile: [Comportamento responsivo, padding, navegação adaptada]
- Mapeamento dos 4 Estados:
  · Loading: [Skeleton loader / spinner contextual]
  · Erro: [Feedback visual em linha / banner com ação de retry]
  · Vazio: [Placeholder com mensagem orientadora]
  · Sucesso / Default: [Aparência estável do componente]
- Acessibilidade & Contraste: [Diretrizes WCAG AA / tokens de Dark e Light mode]

OBSERVABILIDADE NO FRONT (Eventos Mapeados no Design)
- [Botão/Elemento X]: aciona evento `event: click_cv_download`
- [Botão/Elemento Y]: aciona evento `event: click_author_contact`
- [Tempo de leitura]: leitor sinaliza leitura completa ao atingir rodapé

EM ABERTO (Pauta Cirúrgica para os Desenvolvedores)
  Para Frontend:
  - [Viabilidade técnica da transição/animação X]
  - [Reaproveitamento de componentes existentes]
  Para Backend / Arquitetura:
  - [Pipeline de dados / parser / contratos Zod e MSW]
  - [Estratégia de SEO / Open Graph para redes sociais]
  Para o PO:
  - [Eventuais exceções de regra ainda em aberto]

FIGMA & ENTREGÁVEIS
→ [Link do fluxo no Figma atualizado]
Ajustes que UX/UI fará antes do refinamento completo com os devs:
- [ ] Desenhar variação mobile do componente X
- [ ] Documentar tokens de espaçamento e tipografia

INTENSIDADE ACORDADA
- Esqueleto mantido: [Validação de que a proposta visual cabe na fatia mínima]
══════════════════════════════════════════════
```

## Regras de aplicação
- Registrado no Azure DevOps na transição entre `Prototyping` e `Refinement`.
- Destrava a análise assíncrona dos desenvolvedores antes do call final.
