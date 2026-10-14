# task-smart (Universal SMART Task — Bill Wake)

## Input esperado
- Papel ou Especialidade técnica (Frontend, Backend, Mobile, DevOps, QA, etc.)
- Nome descritivo da tarefa
- Escopo técnico e fronteira de atuação
- Definição de Pronto verificável
- Pré-requisitos e dependências
- Critérios de Aceitação (CAs) da história que esta task viabiliza
- Estimativa de duração e limite de alerta

## Output gerado

```markdown
### TASK [N] [ESPECIALIDADE]: [Nome Descritivo da Task]

- [ ] **S — Specific (Específico):**
      [Escopo técnico concreto e delimitado — o que exatamente será feito,
      em quais arquivos/módulos, com quais entradas e saídas esperadas,
      sem sobreposição de fronteiras com outras tarefas]

- [ ] **M — Measurable (Mensurável — Definição de Pronto):**
      - [ ] Funcionalidade entrega com fidelidade o comportamento descrito em S
      - [ ] Testes automatizados verdes cobrindo o escopo (unitários, integração, E2E ou contrato conforme aplicável)
      - [ ] Linters, formatadores e verificação estática de tipos 100% aprovados
      - [ ] Code review do time aprovado com padrões do projeto

- [ ] **A — Achievable (Atingível):**
      [Pré-requisitos imediatos · dependência de outras tasks técnicas ·
      a quem recorrer caso surja um bloqueador de arquitetura ou regra]

- [ ] **R — Relevant (Relevante):**
      Viabiliza [CA1, CA2, ...] (declaração explícita de quais CAs da história esta task viabiliza)

- [ ] **T — Time-bound (Temporal / Estimativa):**
      ~[estimativa de esforço em horas ou dias] · Alerta de bloqueio se passar de [limite máximo]
```

---

## Bloco de Cobertura (Obrigatório ao final do conjunto de tasks)

Após a geração de todas as tasks técnicas da história, fechar obrigatoriamente com o relatório de cobertura:

```markdown
COBERTURA DOS CRITÉRIOS DE ACEITAÇÃO:
✅ CA1 — Viabilizado por: Task [X] + Task [Y]
✅ CA2 — Viabilizado por: Task [Z]
⚠️ CA[N] — Não coberto [especificar o que falta antes de iniciar o desenvolvimento]
```

## Regras de aplicação
- **S:** O escopo deve ser específico o bastante para não colidir com o trabalho de outro desenvolvedor.
- **M:** Deve conter critérios objetivos de aprovação automatizada (testes e checagens estáticas).
- **A:** Dependências técnicas entre tarefas devem ser declaradas expressamente.
- **R:** Toda task técnica deve viabilizar ao menos um Critério de Aceitação da história.
- **T:** Estimativas em tempo real (horas ou poucos dias), nunca em pontos abstratos.
