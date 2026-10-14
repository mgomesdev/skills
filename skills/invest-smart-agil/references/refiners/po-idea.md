# po-idea (Personal Branding Edition)

## Quando acionar
- PO apresenta ideia bruta, demanda ou problema de produto.
- Ausência de card estruturado no histórico do chat.
- Fase detectada: PHASE_CREATE.

## Sequência de extração (Uma pergunta por vez)

### Dimensão 1 — Valor & Dor
**Objetivo:** Entender quem sofre a dor (Carlos, Mariana ou Matheus), qual o problema e a consequência real se não resolver.
* Pergunta: *"Me conta mais sobre o problema. Quem está sendo prejudicado hoje e o que acontece de ruim por causa disso?"*
* *Critério de suficiência:* Persona identificada + dor concreta + consequência nomeada.

### Dimensão 2 — Negócio & Regras Firmes
**Objetivo:** Separar o que é inegociável do que ainda pode ser moldado.
* Pergunta: *"O que você já sabe com certeza absoluta que tem que acontecer — alguma regra ou restrição inegociável da marca ou do produto?"*
* *Critério de suficiência:* Pelo menos uma regra mandatória isolada de suposições.

### Dimensão 3 — Esqueleto vs. Intensificação
**Objetivo:** Identificar a menor entrega vertical que já resolve a dor (MVP).
* Pergunta: *"Se pudéssemos colocar no ar apenas uma fatia mínima esta semana para validar o valor com o usuário, qual seria? O que deixamos para as próximas intensificações?"*
* *Critério de suficiência:* Descrição clara do esqueleto separada das ideias futuras.

### Dimensão 4 — Observabilidade & Sinais de Sucesso
**Objetivo:** Garantir que a feature possa ser medida no mundo real para confirmar se resolveu a dor.
* Pergunta: *"Após a publicação, como saberemos que as dores foram realmente resolvidas? Que sinais ou métricas observáveis (ex: visitas, conversão em cliques no CV/contato, tempo de leitura) nos dirão que funcionou?"*
* *Critério de suficiência:* Pelo menos um sinal de engajamento/adoção e um evento de conversão/sucesso.

### Dimensão 5 — Dependências
**Objetivo:** Identificar bloqueios externos ou precedências.
* Pergunta: *"Essa funcionalidade depende de algo que ainda não existe (design no Figma, infra, domínio), ou pode ser desenvolvida de forma independente?"*
* *Critério de suficiência:* Dependências tipadas (bloqueio total ou contornável).

### Dimensão 6 — Testabilidade
**Objetivo:** Garantir que o time saberá quando está pronto através de cenários verificáveis.
* Pergunta: *"Como o usuário experimenta isso na prática? Consegue me descrever 2 cenários concretos no formato: 'Quando o visitante faz X, ele vê Y'?"*
* *Critério de suficiência:* Mínimo de 2 cenários de teste claros.

---

## Encerramento da entrevista
Atingidos os critérios das dimensões, emitir:
> *"Tenho as informações necessárias para estruturar o card inicial. Vou formatar agora — revise se capturei fielmente sua visão."*
E acionar internamente `check-invest` e `format-card-m1`.
