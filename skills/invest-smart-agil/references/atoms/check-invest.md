# check-invest (Validação Silenciosa)

## Input esperado
- Card M1 ou M2 completo
- Contexto do chat

## Output gerado
Resultado **silencioso** se tudo estiver em conformidade. Só gera mensagem se detectar problema.

### Critérios Silenciosos de Qualidade (INVEST + O)

| Critério | O que verificar | Severidade |
| :--- | :--- | :--- |
| **Independente** | Pode ser desenvolvida sem travar outras features? Contorno viável? | ⚠️ Aviso |
| **Negociável** | Prescreve o "quê" e não o "como"? Figma como referência e não spec rígida? | ⚠️ Aviso |
| **Valioso** | Resolve a dor de uma persona real (Carlos, Mariana ou Matheus)? Entrega valor externo? | ⛔ Bloqueio se não houver valor externo |
| **Estimável** | O time consegue entender o escopo sem depender de adivinhação? | ⚠️ Aviso |
| **Small (Esqueleto)** | Menor entrega com valor real bem delimitada? Cabe em poucos dias? | ⚠️ Aviso |
| **Testável** | Cenários claros sem termos vagos ("fácil", "bonito", "intuitivo")? | ⛔ Bloqueio se CA inviável |
| **Observável** | Possui sinais de sucesso/métricas para saber se a dor foi resolvida pós-launch? | ⚠️ Aviso se faltar observabilidade |

### Regras de aplicação
- Executar em segundo plano sem narrar ("estou conferindo o INVEST...").
- Bloqueio total apenas se faltar valor externo real ou se os testes forem puramente subjetivos.
- Aviso amigável se faltar a seção de Observabilidade, sugerindo adicionar eventos/sinais.
