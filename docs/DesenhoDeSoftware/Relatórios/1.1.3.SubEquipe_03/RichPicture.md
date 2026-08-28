# Rich Picture - Foco_01

## Participantes do artefato

| Nome do Membro            |
| ------------------------- |
| Yasmim de Souza Santos    |
| Davi Ursulino de Oliveira |

## Metodologia do Foco_01

Espaço para contar um pouco sobre como ocorreu o trabalho em equipe. Vídeos ajudam aqui.

## Rich Picture

![Rich Picture do fluxo do login até a localização de um local da rede de saúde - versão 1](../assets/subequipe03-fluxos/rich-picture/rich-picture-usabilidade.png)

Arquivo editável: [Rich Picture Usabilidade](https://canva.link/5nzidpjb7mkkt9k)

### Legenda da Rich Picture: Fluxo de Busca de Rede Credenciada no Meu SUS Digital

#### Convenção geral:

- **Setas numeradas (1-15):** sequência cronológica de interações entre o usuário e o sistema, do login até a obtenção da rota até o atendimento.
- **Balões de fala (nuvens):** preocupações de usabilidade (concerns) expressas pelo usuário em cada etapa do fluxo.
- **Personagem central:** usuário idoso, escolhido propositalmente para evidenciar barreiras de usabilidade em um perfil de baixo letramento digital.

#### Sequência de interações

| Nº  | Ação                                        | Descrição                                                                               |
| --- | ------------------------------------------- | --------------------------------------------------------------------------------------- |
| 1   | Acessa o site                               | Usuário entra na plataforma Meu SUS Digital                                             |
| 2   | Redireciona autenticação                    | Sistema encaminha o usuário para o login via gov.br                                     |
| 3   | Solicita CPF e senha                        | gov.br pede as credenciais                                                              |
| 4   | Informa CPF e Senha                         | Usuário preenche os dados de login                                                      |
| 5   | Acessa o menu principal                     | Usuário retorna à plataforma já autenticado                                             |
| 6   | Acessa redes de saúde                       | Usuário navega até a seção de busca de estabelecimentos                                 |
| 7   | Seleciona o tipo de atendimento             | Usuário escolhe a categoria de necessidade (emergência, maternidade, especialista etc.) |
| 8   | Solicita acesso à localização               | Sistema pede permissão de geolocalização                                                |
| 9   | Permite acesso à localização ou fornece ela | Usuário autoriza o uso do GPS ou digita o endereço manualmente                          |
| 10  | Visualiza os resultados                     | Lista de estabelecimentos compatíveis é exibida                                         |
| 11  | Pede para consultar detalhes                | Usuário solicita mais informações sobre um resultado                                    |
| 12  | Visualiza os tipos de serviços              | Detalhamento das especialidades/serviços oferecidos pelo estabelecimento                |
| 13  | Pede para ver no mapa                       | Usuário solicita visualização geográfica do local                                       |
| 14  | Redireciona para o Google Maps              | Sistema integra com aplicativo externo de mapas                                         |
| 15  | Fornece rotas para o local escolhido        | Google Maps entrega o trajeto até o estabelecimento                                     |

#### Preocupações de usabilidade (balões de pensamento)

| Preocupação                                                                                    | Onde aparece                                               | Problema de usabilidade evidenciado                                                                                                                                                                                 |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _"Esqueci minha senha do Gov.br, travei aqui de novo"_                                         | Etapa 3 (login)                                            | Falta de prevenção/recuperação de erro; barreira de autenticação para usuários com baixo letramento digital                                                                                                         |
| _"Preciso de ajuda AGORA, por que tem tanto passo antes de eu achar o hospital mais próximo?"_ | Etapa 2 (pós-login)                                        | Baixa eficiência do fluxo em cenários de urgência; excesso de passos para uma tarefa crítica                                                                                                                        |
| _"Não entendo esses ícones, a letra é muito pequena"_                                          | Etapas 7-8 (seleção de atendimento/localização)            | Falta de reconhecimento visual e legibilidade inadequada para público idoso                                                                                                                                         |
| _"Por que ele quer saber onde eu estou?"_                                                      | Etapas 8-9 (solicitação/concessão de acesso à localização) | Falta de transparência sobre o motivo da solicitação de dado sensível (geolocalização); gera desconfiança de privacidade em usuários com baixo letramento digital _(adição: Davi Ursulino de Oliveira, 26/08/2026)_ |

#### Elementos gráficos e seu significado

- **SUS Digital / gov.br:** sistemas envolvidos na autenticação e navegação.
- **Ícone de menu (linhas horizontais):** representa o menu principal da plataforma.
- **Hospital:** representando a seção de Rede de Saúde.
- **Ícone "i" (informação):** tela de detalhes do estabelecimento selecionado.
- **Ícones de dente, coração e cruz médica:** tipos de serviços/especialidades disponíveis (ex.: saúde bucal, cardiologia, emergência).
- **Mapa / Google Maps:** integração externa para visualização geográfica e cálculo de rota.

> **Nota de revisão** _(adição: Davi Ursulino de Oliveira, 26/08/2026)_: os elementos das etapas 7-11 (janela cinza com "Option 1/2/3 + OK") representam de forma genérica as telas de seleção de categoria e resultados, mas não correspondem literalmente à interface real do Meu SUS Digital, que exibe uma grade de ícones por categoria (Hospital, Maternidade, Unidade Básica de Saúde etc., ver prints em `assets/subequipe03-fluxos/fluxo-rede-de-saude/`). Sugestão para uma próxima versão: substituir esses elementos genéricos pelos ícones reais do sistema, aumentando a fidelidade do artefato com o que foi encontrado na Engenharia Reversa.

### Embasamento teórico para criação:

1. DE MONTFORT UNIVERSITY. CTEC2402 Software Development Project: introducing rich pictures. Leicester: De Montfort University.
2. MONK, Andrew; HOWARD, Steve. The rich picture: a tool for reasoning about work context. Interactions, New York, v. 5, n. 2, p. 21-30, mar./abr. 1998.
3. SERRANO, Maurício; LEITE, Julio Cesar Sampaio do Prado. A social interaction based pre-traceability for i* models. In: INTERNATIONAL I* WORKSHOP, 5., 2011. CEUR Proceedings of the 5th International i\* Workshop (iStar 2011). [S. l.]: CEUR-WS, 2011. p. 132-137.

---

| Nome do Membro  | Contribuição   | Data  |
| ---- | ------ | ----- |
| [Gustavo Fornaciari](https://github.com/GUGOFO)  | Criação do Repositorio   | 17/08/2026 |
| [Yasmim de Souza Santos](https://github.com/eii-yahs) | Criação da Rich Picture (Foco_01) | 26/08/2026 |
| [Davi Ursulino de Oliveira](https://github.com/DaviUrsulino) | Revisão da Rich Picture (Foco_01): balão de preocupação sobre geolocalização e nota de fidelidade dos ícones de tela                                                  | 27/08/2026 |
| [Yasmim de Souza Santos](https://github.com/eii-yahs) | Criação do arquivo separado para o artefato produzido | 28/08/2026 |
