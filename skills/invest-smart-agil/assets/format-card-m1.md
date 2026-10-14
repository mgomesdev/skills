# format-card-m1 (Estrutura INVEST — Bill Wake)

## Input esperado
Output estruturado do `refiner-po-idea`:
- Headline (Role + Ação + Contexto)
- [V] Valuable: Por quê, personas, valor, observabilidade (HEART)
- [I] Independent: Dependências e autonomia
- [N] Negotiable: Figma, perguntas abertas, ambiguidades
- [E] Estimable: Regras firmes que delimitam escopo
- [S] Small: Esqueleto (MVP vertical) vs. intensificações
- [T] Testable: Cenários de confirmação (Dado/Quando/Então)

## Output gerado

```markdown
══════════════════════════════════════════════════════════════════════════
[HEADLINE]: [Role/Persona] [Ação] [Contexto]
Ex: Matheus publica artigos técnicos em blog próprio para posicionar a marca The Agentic Curator e atrair decisores
══════════════════════════════════════════════════════════════════════════

[V] VALIOSO (Valuable)
--------------------------------------------------------------------------
• Por quê:
  [Dor que resolve · Para quem · Consequência se não resolver]
• Dores por Persona:
  - [Persona 1 (ex: Matheus)]: [Dor específica]
  - [Persona 2 (ex: Carlos Líder Técnico)]: [Dor específica]
  - [Persona 3 (ex: Mariana Recrutadora)]: [Dor específica]
• Classificação de Valor:
  [ ] Receita  [ ] Custo  [ ] Serviço  [ ] Regulação  [ ] Reputação  [ ] Opção  [ ] Informação
• Observabilidade & Métricas de Sucesso (HEART):
  - Adoção: [Volume de acessos / novos visitantes / canais de origem]
  - Engajamento: [Tempo de permanência / scroll depth / interação real]
  - Sucesso de Conversão: [Taxa de cliques nos CTAs de contato/CV / downloads]
  - Acessibilidade: [Distribuição de uso Dark vs. Light mode]

[I] INDEPENDENTE (Independent)
--------------------------------------------------------------------------
• Dependências & Acoplamento:
  - Design: [Dependência de protótipo no Figma — Bloqueante ou Contornável]
  - Infra/Serviços: [Dependência externa — Bloqueante ou Contornável]
• Autonomia de Entrega:
  [Declaração de como esta história entrega uma fatia vertical completa de forma desacoplada]

[N] NEGOCIÁVEL (Negotiable)
--------------------------------------------------------------------------
• Figma & Experiência:
  → Protótipo de referência: [Link do Figma] (Layout maleável a trade-offs de engenharia)
• Em Aberto (Para discussão no Refinamento):
  - UX/UI: [Questões visuais, fluxos e componentes]
  - Frontend: [Viabilidade técnica, estados e transições]
  - Backend/Arquitetura: [Contratos de dados, schemas e performance]
  - PO: [Trade-offs de negócio e exceções]
• Ambiguidades com Dono:
  A1 — [Descrição da incerteza] — para: [Papel responsável por decidir]
  A2 — [Descrição da incerteza] — para: [Papel responsável por decidir]

[E] ESTIMÁVEL (Estimable)
--------------------------------------------------------------------------
• Regras Firmes (O que delimita o escopo e viabiliza a estimativa técnica sem adivinhação):
  - [Regra inegociável 1]
  - [Regra inegociável 2]
  - [Restrição de domínio ou arquitetura mandatória]

[S] SMALL / PEQUENO (Small)
--------------------------------------------------------------------------
• Esqueleto (MVP - Menor entrega com valor real vertical):
  - [Item essencial da fatia mínima navegável]
  - [Item essencial de integração/dados]
  - [Telemetria básica de observabilidade]
• Próximas Intensificações (Fora desta iteração):
  - [Funcionalidade avançada 1]
  - [Funcionalidade avançada 2]

[T] TESTÁVEL (Testable)
--------------------------------------------------------------------------
• Cenários de Confirmação:
  1. Dado que [contexto inicial], quando [ação principal], então [resultado observável esperado].
  2. Dado que [contexto], quando [ação alternativa ou exceção], então [comportamento do sistema].
  3. Dado que [contexto de acessibilidade ou tema], quando [ação], então [resultado verificável].
══════════════════════════════════════════════════════════════════════════
```

## Regras de aplicação
- Os blocos [V], [I], [N], [E], [S], [T] são canônicos e obrigatórios.
- Seção [V] obrigatoriamente contém o bloco de Observabilidade (HEART).
- Seção [N] reforça que o Figma é referência viva de experiência, não especificação fechada.
- Seção [S] delimita com rigor a fronteira entre Esqueleto (entra agora) e Intensificações (fica depois).
