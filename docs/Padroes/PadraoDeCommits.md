# Padrão de Commits

Este documento define as regras de padronização de commits adotadas pelo grupo (G5 - Projeto Governo Eletrônico), explicando como as mensagens devem ser estruturadas para manter o histórico do repositório limpo, rastreável e fácil de entender.

## Padrão adotado: Conventional Commits

Utilizamos o padrão [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/), amplamente usado no mercado. A estrutura da mensagem é:

```

<tipo>(<escopo opcional>): <descrição curta>

<corpo opcional, explicando o quê e o porquê>

<rodapé opcional, ex: referência a issue>
```

### Exemplo

```
feat(login): adicionar validação de CPF no formulário de acesso

Impede o envio do formulário quando o CPF informado é inválido,
seguindo o requisito de usabilidade RF-03.

Refs: #12
```

## Tipos de commit

| Tipo | Quando usar |
| --- | --- |
| `feat` | Nova funcionalidade para o usuário |
| `fix` | Correção de bug |
| `docs` | Alteração apenas em documentação (README, Wiki, GitPages) |
| `style` | Formatação, indentação, ponto e vírgula etc. (sem mudança de lógica) |
| `refactor` | Alteração de código que não corrige bug nem adiciona funcionalidade |
| `test` | Criação ou ajuste de testes |
| `chore` | Tarefas de manutenção (configuração, dependências, build) |
| `perf` | Melhoria de performance |

## Regras para a mensagem

1. **Descrição curta no imperativo**: escreva como uma ordem/ação ("adicionar", "corrigir", "remover"), não no gerúndio ou passado ("adicionando", "adicionou").
2. **Até ~72 caracteres** na primeira linha.
3. **Sem ponto final** na descrição curta.
4. **Escopo entre parênteses** (opcional) indica a parte do projeto afetada (ex: `login`, `docs`, `bpmn`, `sig`).
5. **Corpo explica o "porquê"**, não o "o quê" (o diff já mostra o que mudou).
6. **Um commit, uma responsabilidade**: evite misturar mudanças não relacionadas no mesmo commit.
7. **Referencie issues/artefatos** quando aplicável (ex: `Refs: #12`, ou link para o artefato no Miro/Figma).

## Por que isso importa para a disciplina

O módulo de Desenho de Software exige rastreabilidade clara entre membros, contribuições e artefatos (ver [1.2. Participações](/docs/Base/1.2.ParticipacoesBase.md)). Um histórico de commits padronizado permite:

- Identificar rapidamente quem fez o quê e por quê;
- Servir como comprobatório de participação individual;
- Facilitar a montagem do relatório e da apresentação para a professora.
