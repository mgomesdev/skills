# load-project-context (Universal Codebase Inspector)

## Quando acionar
- Flag `--with-docs` está ativa no chat.
- Papel atual é de Engenharia (Frontend, Backend, Mobile, Fullstack).
- Fase em curso é Refinamento (antes de responder cada pendência técnica) ou Planning (antes de gerar as tasks).

## Quando NÃO acionar
- Flag ausente ou `--no-docs` em vigor.
- Papel é PO ou UX/UI.
- Pendência é puramente de negócio/estratégia sem implicação técnica.

## Estratégia de inspeção agnóstica de repositório

1. **Descoberta do Padrão do Repositório:**
   - Detectar a estrutura do projeto ativo (monorepo com `apps/` e `packages/`, repositório único, backend isolado, etc.).
   - Localizar os arquivos canônicos de definição de dados e contratos (ex: schemas, interfaces, DTOs, modelos ORM).
   - Localizar a biblioteca de componentes e design system do projeto (se frontend).
2. **Busca Cirúrgica e Pontual:**
   - Extrair palavras-chave da headline e da pendência técnica (domínio + verbo + entidade).
   - Fazer busca rápida dirigida por termos-chave nos módulos correspondentes.
   - Limite estrito: no máximo 2 tentativas de busca por pendência para economizar tokens e tempo.
3. **Citação Verificável:**
   - Sempre citar `arquivo:linha` ao afirmar que algo "já existe" no código.

## Output entregue ao Dev no chat

Antes da pergunta da pendência (no Refinamento) ou da geração da task (no Planning):

```
📎 Contexto do projeto para [pendência | escopo da task]:

· Já existe: [achado em linguagem direta] — `caminho/arquivo.ext:linha`
· Convenção aplicável: [padrão detectado no repo] — `docs/...` ou `exemplo:linha`
· Lacuna real: [o que NÃO existe no código e precisa ser decidido agora]
· Sugestão para revisar: [proposta técnica concreta marcada como sugestão]

Faz sentido seguir por aqui ou prefere outro caminho?
```

## Regras críticas
- **Nunca decidir pelo desenvolvedor.** O agente traz fatos e evidências do código, mas o dev tem a palavra final.
- **Se não encontrar nada relevante, declarar com transparência:** *"Não localizei referências prévias no código para esta pendência — vamos decidir pelo card e pelo diálogo com o time."*
- **Read-only estrito:** Este atom apenas inspeciona, nunca altera arquivos no repositório.
