# load-project-context (MCP Knowledge Base & Codebase Inspector)

## Quando acionar
- Flag `--with-docs` está ativa no chat.
- Papel atual é de Engenharia (Frontend, Backend, Mobile, Fullstack, DevOps).
- Fase em curso é Refinamento (antes de responder cada pendência técnica) ou Planning (antes de gerar as tasks).

## Quando NÃO acionar
- Flag ausente ou `--no-docs` em vigor.
- Papel é PO ou UX/UI.
- Pendência é puramente de negócio/estratégia sem implicação técnica.

---

## 🏛️ Fonte Única da Verdade (SSoT): Knowledge Base via MCP

A **Wiki do projeto (Knowledge Base)** é a autoridade canônica para todas as decisões técnicas, arquiteturais, convenções e tecnologias homologadas.

Quando `--with-docs` é ativado, o agente segue este protocolo estrito de 2 camadas:

```
[Chat com Flag --with-docs]
            ↓
  1. Consulta à Wiki via MCP (SSoT) ➔ Lê stack, padrões e contratos homologados
            ↓
  2. Inspeção do Código Local       ➔ Localiza implementações reais (arquivo:linha)
            ↓
  Output Estruturado com Rastreabilidade Dupla (Wiki + Código)
```

### Protocolo de Execução

1. **Camada 1 — Consulta à Knowledge Base (Via MCP):**
   * Acessa a Wiki do projeto utilizando as ferramentas MCP disponíveis (ex: `call_mcp_tool(ServerName="azure-devops", ToolName="wiki", Arguments={"action": "get_page_content", "path": "..."})`).
   * Consulta primeiro o catálogo semântico (ex: `/knowledge/index` ou índice da wiki) para identificar as páginas pertinentes da categoria de engenharia e arquitetura (ex: `wiki/engineering/stack-tecnica`, `wiki/engineering/arquitetura-*`, `wiki/engineering/fluxo-do-board`).
   * Extrai da Wiki as diretrizes oficiais: bibliotecas homologadas, padrões de contratos/schemas, convenções de teste e regras inegociáveis.

2. **Camada 2 — Cruzamento com o Repositório Local:**
   * A partir do que a Wiki prescreve como verdade, inspeciona pontualmente o repositório para localizar onde esse padrão já está implementado.
   * Busca schemas, módulos, componentes ou utilitários existentes relacionados à pendência.
   * Registra a citação exata `caminho/arquivo.ext:linha`.

---

## Output entregue ao Dev no chat

Antes da discussão de cada pendência técnica (no Refinamento) ou antes da geração das tasks (no Planning):

```markdown
📎 Contexto da Knowledge Base (SSoT) & Projeto para [pendência | escopo da task]:

· Fonte da Verdade (Wiki via MCP):
  - Diretriz oficial: [Regra/tecnologia homologada] — `wiki/engineering/[pagina-na-wiki]`
  - Padrão arquitetural: [Convenção mandatória registrada na base de conhecimento]

· Implementação no Repositório:
  - Já existe no código: [Componente, schema ou service encontrado] — `caminho/arquivo.ext:linha`
  - Lacuna real: [O que NÃO existe e precisa ser implementado agora]

· Sugestão para Revisão:
  - [Proposta técnica alinhada com a Wiki, marcada expressamente como sugestão]

Faz sentido seguir por esta diretriz da Wiki ou há necessidade de evolução de arquitetura?
```

---

## Integração no Planning (Tasks SMART)

Quando `--with-docs` está ativo durante o `plan-dev`, as tasks técnicas SMART incorporam a rastreabilidade da Wiki e do código:

* **S (Specific):** Cita a página da Wiki que dita o padrão e o `arquivo:linha` onde a task atua.
* **M (Measurable):** Utiliza as ferramentas de testes e validação prescritas na página de stack técnica da Wiki.
* **Bloco Final de Reúso:**
  ```markdown
  REÚSO IDENTIFICADO:
  • [Padrão arquitetural] — SSoT: `wiki/engineering/[nome-da-pagina]`
  • [Schema/Componente reutilizado] — Código: `caminho/arquivo.ext:linha`
  ```

---

## Regras Críticas

- **A Wiki prevalece sobre achismos:** Se houver conflito entre uma sugestão genérica e o que está registrado na Knowledge Base via MCP, a diretriz da Wiki é a fonte canônica.
- **Rastreabilidade obrigatória:** Nunca afirmar que uma tecnologia é o padrão do projeto sem citar a página da Wiki (`wiki/...`) ou o arquivo de código (`arquivo:linha`).
- **Read-only estrito:** Este atom apenas consulta a Wiki e o código via MCP/leitura, nunca edita documentos sem instrução expressa.
- **Transparência em lacunas:** Se a Wiki ainda não possuir diretriz para a tecnologia demandada, o agente deve alertar:
  > *"Não há diretriz oficial para essa tecnologia na Knowledge Base (Wiki). Recomendo decidirmos com o time e posteriormente documentar na Wiki."*
