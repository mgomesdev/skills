# check-invest (Validação Universal INVEST)

## Input esperado
- Card M1 ou M2 completo
- Contexto da feature e do chat

## Output gerado
Resultado **silencioso** se a história estiver em conformidade. Só gera mensagem se detectar problema.

### Critérios Silenciosos de Qualidade (INVEST + O de Bill Wake)

| Critério | O que verificar | Severidade se falhar |
| :--- | :--- | :--- |
| **[I] Independente** | Pode ser desenvolvida e entregue sem acoplamento rígido a outras histórias? Dependências têm contorno definido? | ⚠️ Aviso |
| **[N] Negociável** | O card prescreve o "quê" e não o "como"? Figma é tratado como referência viva e não contrato engessado? | ⚠️ Aviso |
| **[V] Valioso** | Resolve a dor de um usuário, cliente ou stakeholder real? Entrega fatia vertical com valor perceptível? | ⛔ Bloqueio se não houver valor externo |
| **[E] Estimável** | O time técnico tem clareza suficiente de domínio e regras firmes para estimar sem adivinhação? | ⚠️ Aviso + sugerir Spike |
| **[S] Small (Pequeno)** | É uma fatia mínima (esqueleto) que cabe em poucos dias? Escopos futuros estão claramente separados? | ⚠️ Aviso |
| **[T] Testável** | Os cenários possuem comportamento esperado verificável? Isento de palavras subjetivas e vagas? | ⛔ Bloqueio se CA for inviável |
| **[O] Observável** | Possui indicadores ou telemetria para medir se a dor foi resolvida no mundo real pós-lançamento? | ⚠️ Aviso se faltar observabilidade |

### Palavras-gatilho que violam Testabilidade (Sinalizar e pedir reformulação)
"rápido", "fácil", "intuitivo", "apropriado", "melhor", "correto", "agradável", "qualquer", "todas as combinações", "natural".

### Regras de aplicação
- Executar silenciosamente em segundo plano — não narrar o processo interno.
- Bloqueio total emitido apenas para falta de valor real ou cenários de teste inviáveis.
- Mensagens de aviso devem conter sempre: **Critério**, **Impacto potencial** e **Ação corretiva sugerida**.
