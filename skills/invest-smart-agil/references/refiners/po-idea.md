# po-idea (Universal Refiner)

## Quando acionar
- PO apresenta uma ideia bruta, nova demanda ou problema de negócio.
- Primeira interação de uma nova funcionalidade no chat.
- Fase detectada: PHASE_CREATE.

## Sequência de extração (Uma pergunta por vez)

### Dimensão 1 — Valor & Dor
**Objetivo:** Entender quem é o usuário ou persona afetada, qual a dor real e a consequência de não resolver.
* Pergunta inicial:
  > *"Me conta mais sobre o problema. Quem é o usuário, cliente ou perfil afetado hoje, e o que acontece de ruim se não resolvermos isso?"*
* Se a resposta for vaga ("o cliente quer X"):
  > *"E se não fizermos isso agora, qual é o impacto concreto — perda de receita, ineficiência operacional, risco de reputação ou retrabalho?"*
* *Critério de suficiência:* Persona/perfil identificado + dor concreta + consequência nomeada.

### Dimensão 2 — Negócio & Regras Firmes
**Objetivo:** Separar o que é mandatório e inegociável do que ainda pode ser moldado pelo time.
* Pergunta inicial:
  > *"O que você já sabe com certeza absoluta que precisa acontecer — alguma regra de negócio, restrição legal ou diretriz inegociável?"*
* Se misturar regras com ideias de interface:
  > *"Isso é uma regra mandatória de negócio ou é uma sugestão de como a tela pode resolver que ainda podemos ajustar no refinamento?"*
* *Critério de suficiência:* Pelo menos uma regra firme separada de suposições.

### Dimensão 3 — Esqueleto vs. Intensificação (Tamanho / Small)
**Objetivo:** Identificar a menor fatia vertical que entrega valor real verificável (MVP da história).
* Pergunta inicial:
  > *"Se tivéssemos que colocar no ar apenas uma fatia mínima nesta iteração para validar o valor com o usuário, qual seria? O que deixamos explicitamente para as próximas intensificações?"*
* Se o PO disser que "tudo é prioridade":
  > *"Se você tivesse apenas alguns dias de time para entregar valor real, qual parte o usuário sentiria mais falta se não existisse?"*
* *Critério de suficiência:* Descrição clara do esqueleto isolada das intensificações futuras.

### Dimensão 4 — Observabilidade & Sinais de Sucesso
**Objetivo:** Garantir que o valor prometido possa ser medido no mundo real após a publicação.
* Pergunta inicial:
  > *"Após a funcionalidade estar em produção, como saberemos que a dor foi resolvida? Que métricas ou eventos observáveis (ex: adoção, tempo de conclusão, conversão nos CTAs, taxa de erros) indicarão o sucesso?"*
* *Critério de suficiência:* Pelo menos um sinal de adoção/engajamento e uma métrica ou evento de conversão/sucesso.

### Dimensão 5 — Dependências & Acoplamento (Independência)
**Objetivo:** Identificar bloqueios externos e garantir que a história possa ser desenvolvida com autonomia.
* Pergunta inicial:
  > *"Essa funcionalidade depende de algo que ainda não existe no sistema (APIs externas, telas prévias, serviços de terceiros), ou pode ser desenvolvida de forma independente?"*
* Se houver dependência:
  > *"Essa dependência é um bloqueio total ou tem contorno viável (como mocks de dados, contratos prévios ou desenvolvimento em paralelo)?"*
* *Critério de suficiência:* Dependências identificadas e tipadas (bloqueio total ou contornável).

### Dimensão 6 — Testabilidade (Confirmação)
**Objetivo:** Garantir que o time saberá exatamente quando a entrega está pronta.
* Pergunta inicial:
  > *"Como saberemos na prática que a entrega está funcionando? Consegue me descrever 2 cenários concretos no formato: 'Quando o usuário faz X, então o sistema responde Y'?"*
* *Critério de suficiência:* Mínimo de 2 cenários de teste claros e verificáveis.

---

## Encerramento da entrevista
Quando os critérios de suficiência das dimensões forem atingidos, emitir:
> *"Tenho o suficiente para estruturar o card inicial. Vou formatar agora — revise e confirme se capturei a visão com fidelidade."*

Acionar internamente `check-invest` e `format-card-m1`.
