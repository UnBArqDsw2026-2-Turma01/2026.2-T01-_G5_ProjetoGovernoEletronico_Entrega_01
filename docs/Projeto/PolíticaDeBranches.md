# Política de Branches

## 1. Branches Principais

- **main**: Representa o código oficial e estável do projeto. Todo o código nesta branch deve estar pronto para uso ou implantação. Commits diretos são bloqueados; as alterações devem ser integradas via Pull Request.
- **developer**: Atua como a branch de integração. Centraliza as novas funcionalidades, testes e correções antes de serem promovidas para a main.

## 2. Padrão de Nomenclatura das Branches

As ramificações devem ter nomes descritivos que indiquem claramente o propósito da alteração. É recomendado o uso dos seguintes prefixos padronizados:

| Prefixo | Propósito | Exemplo |
|---|---|---|
| `feature/` | Desenvolvimento de novas partes do projeto. | `feature/exportacao-relatorios` |
| `bugfix/` | Correção de erros e falhas no código. | `bugfix/erro-login-usuario` |
| `docs/` | Adições ou modificações exclusivas na documentação. | `docs/atualiza-readme` |

## 3. Fluxo de Integração e Pull Requests (PRs)

- **Sincronização Base**: Atualize seu repositório local e sempre crie sua branch de trabalho a partir da branch principal de integração (como a `developer`).
- **Desenvolvimento**: Realize commits lógicos e atômicos durante o trabalho.
- **Abertura do PR**:
  - Descreva claramente o objetivo das alterações.
  - Referencie o problema ou chamado que motivou a mudança.
- **Revisão de Código (Code Review)**: Sempre que possível, o PR deve ser revisado por pelo menos um colega para garantir a qualidade do código e minimizar riscos de falhas.

## 4. Práticas Gerais de Boa Convivência

- **Integração Frequente e Branches Curtas**: Mantenha o escopo das alterações o menor possível. Entregas menores facilitam a revisão de código e evitam conflitos complexos no momento de integrar os arquivos.
- **Limpeza do Repositório**: Delete a branch logo após o Pull Request ter sido mesclado com sucesso.
