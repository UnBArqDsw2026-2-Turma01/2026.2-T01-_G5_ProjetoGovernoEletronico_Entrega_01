# NFR Framework

## Participantes do artefato

| Nome do Membro            |
| ------------------------- |
| Gabriel Mota Oliveira     |
| Yasmim de Souza Santos    |
| Davi Ursulino de Oliveira |

## O que é um NFR (Requisito Não Funcional)

NFR (Non-Functional Requirement, ou Requisito Não Funcional) é um requisito que não descreve uma função específica que o sistema deve executar, mas sim uma qualidade ou restrição sobre _como_ essas funções devem ser realizadas — por exemplo, usabilidade, segurança, desempenho, privacidade ou acessibilidade. Enquanto um requisito funcional responde "o que o sistema faz" (ex.: "o usuário deve conseguir buscar uma unidade de saúde"), um NFR responde "com que qualidade" isso deve acontecer (ex.: "a busca deve ser acessível a usuários com baixo letramento digital").

Chung et al. (2000) argumentam que NFRs raramente podem ser completamente satisfeitos de forma binária (sim/não): eles são, na prática, _softgoals_, sem um critério de satisfação claro e objetivo, cujo cumprimento é sempre uma questão de grau e de compromisso com outros objetivos do sistema. É justamente por isso que o NFR Framework trata a Usabilidade do Meu SUS Digital não como uma caixa a ser marcada, mas como um softgoal a ser refinado, discutido e avaliado ao longo do processo de design, o que motiva o uso do SIG descrito a seguir.

Para mais informações sobre: [Guia NFR Framework](../../../Projeto/GuiaNFR.md)

## O que é um SIG (Softgoal Interdependency Graph)

O SIG (Softgoal Interdependency Graph, ou Grafo de Interdependência de Softgoals) é a notação gráfica proposta pelo NFR Framework (CHUNG et al., 2000) para representar como um softgoal de alto nível se decompõe em softgoals mais específicos, e como decisões de design concretas impactam essa rede de objetivos. Um SIG é composto principalmente por três tipos de elementos:

- **Softgoals**: os próprios requisitos não funcionais, em diferentes níveis de abstração (ex.: Usabilidade → Acessibilidade → Percepção). Representados como nuvens de borda fina.
- **Métodos de Operacionalização**: decisões concretas de design ou implementação que contribuem — positiva ou negativamente — para um ou mais softgoals (ex.: "Autenticação via CPF e senha"). Representados como nuvens de borda grossa.
- **Claims**: argumentos ou justificativas usados para embasar por que determinada contribuição foi avaliada de certa forma, geralmente quando o contexto importa para a interpretação do link. Representados como nuvens de borda tracejada.

Esses elementos são conectados por **links de contribuição** (rotulados com `++`, `+`, `-` ou `--`), que indicam o quanto um nó filho satisfaz ou prejudica o nó pai, e podem opcionalmente receber avaliações finais (`!` crítico, `✓` aceito, `X` rejeitado) que sintetizam o resultado da análise para cada softgoal.

O valor do SIG está em tornar **explícitas e rastreáveis** as decisões de design e seus trade-offs: como o mesmo método pode satisfazer um softgoal enquanto prejudica outro, e como esse raciocínio pode ser revisitado posteriormente — funcionando como um registro do processo de design, e não apenas do seu resultado final.

## SIG de Usabilidade

### Versão 1

**Autoria: Gabriel Mota**

![SIG de Usabilidade na notação do NFR Framework](../assets/subequipe03-fluxos/SIG/SIG_Usabilidade.drawio.svg)

Estrutura inicial do SIG de Usabilidade: o softgoal _Usabilidade_ foi decomposto em _Facilidade de Uso_, _Velocidade de Acesso_ e _Acessibilidade_ (refinada em _Percepção_, _Conteúdo_ e _Navegação_), conectados aos métodos identificados no Meu SUS Digital por meio dos links de contribuição (`++`, `+`, `-`, `--`). Nesta versão, os nós ainda não têm avaliação final (`!`, `✓` ou `X`) — a análise mostra apenas o sentido de cada contribuição, sem indicar quais softgoals foram aceitos ou rejeitados.

### Versão 2

**Autoria: Yasmim de Souza**

![SIG de Usabilidade na notação do NFR Framework - versão 2](../assets/subequipe03-fluxos/SIG/SIG_Usabilidade_V2.drawio.svg)

A estrutura de nós e links da Versão 1 foi mantida, e os símbolos de avaliação final foram adicionados a cada softgoal. *Facilidade de Uso* e *Percepção* receberam `✓` (aceito), sustentados por métodos com contribuição fortemente positiva (*Navegação Intuitiva* e *Alto contraste*). *Acessibilidade*, *Conteúdo* e *Navegação* receberam `X` (rejeitado), devido às lacunas de acessibilidade do sistema (ausência de libras, ausência de text-to-speech e navegação por teclado parcial, todas `--`). *Velocidade de Acesso* recebeu `!` (crítico) por um trade-off interno: a contribuição positiva de *Autenticação rápida* (`+`) não compensa a negativa de *Carregamento lento* (`-`). O softgoal raiz *Usabilidade* também recebeu `!`, propagando o resultado misto dos três ramos filhos (um aceito, um crítico, um rejeitado).

> **Nota de revisão** _(Davi Ursulino de Oliveira, 28/08/2026)_: a avaliação `+` de *Autenticação rápida* foi checada cruzando com o Rich Picture do Foco_01 — ver a seção "Rastreabilidade com o Foco_01", abaixo, e a "Versão 3" para as correções aplicadas a partir dessa análise.

Arquivo editável: [SIG_Usabilidade.drawio](https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=SIG_Usabilidade&dark=0#R%3Cmxfile%3E%3Cdiagram%20name%3D%22P%C3%A1gina-1%22%20id%3D%22czpdueMdJo24robT8H2u%22%3E5Vtbc5s4FP41PDqDENdH22l2O9PtpJPJbvMog2yrlREVcmLvr18Bwlx8iR0jyDYvDjqII%2Bk79wMx4HS1%2BYOjZPkXizA1LDPaGPDWsCxgQyj%2FZJRtQfGBVRAWnERqUkV4IP9iRTQVdU0inDYmCsaoIEmTGLI4xqFo0BDn7KU5bc5oc9UELfAe4SFEdJ%2F6D4nEUp3C8ir6n5gsluXKwA2KOytUTlYnSZcoYi81EvxkwClnTBRXq80U0wy8Epfiubsjd3cb4zgW5zwg%2BK%2FH%2B2%2Brr09P7Ntnd47Npx%2BzkVNwwdEeChVbRUrZmof4BK9yntiW4HG2jiOcrW8acMK4WLIFixH9wlgiiUASf2AhtkrsaC2YJC3Fiqq7OI7GmRDlMGYxLih3hFLFUikE4gssTuzM2sEt9RSzFRZ8K5%2FjmCJBnpsnR0phFrt5FabyQsF6AcTuh4AYDgmx%2FyEg9oaE%2BASiFVKSj%2FTL2QGls0syYkjZWrKdvCyJwA8JyqF%2FkaGiiVDB6RnRteJkWC6Vy0wi8iwvF9nlY4pmhJIIRbi8K09Sm6CYYC7wprbDfcSWDYet3PNL5d2Bq2iKDSxdeOeoWv2ieofCHYJm%2FvOYsrfBZr0OW4msivzA14UitC%2Bw%2F97t%2BoBWz5ncVX0v7q81K2%2BM0ny9sZwAzWST8ynvl6o%2BqllAwawygSs8hHr0npF8f6X6%2B%2BDGtGFgB7brmjbwG2KFpncTmLbvubbn2MC0nSb%2FwuEqlvX0pL2KDeUqAQws24XQ9d3GKjawbgCwgWd6luNBF8DmKoXz3FslV6cdEldoWJdBHL7bCAMdfSprWBM9Snud6xg8rP2NKQvrPtlFq4xNPEuTAr6DoW6PzzjEaebMu4uMZ7j4XWQsfXygy8eDS3z8qzle0L0JptK6RMsIc1rNDF8zU4pmmE5Q%2BHORb2fKKOO1uRsivmczbxxHDZ%2FyYVAObzflQtlgWxvcY06kIDC%2FzCEA0EMMa%2FoC83hs6y%2FkBW5Tr12npddHolpX8cbqsqLx3m28AYOWNFbwMUD2Bw2w5scAORgSZO84pDqymDzVIFUxrim58P3ekgu93Y1UcPZz1z52zkwMD4XHGD3jBTKm0Bh7%2BS9kJxLGI9HzdB55aNlEpiHSCHBIUcS0LIB4SBC9kLWuvoXVympdW1vnwuoyqx3APR7JWCM8R2taSen1ylNjoplXnub7rD9Bz677gD3K0iDESdun9Glwu%2By6bPaY2vqtsEt78%2F%2B%2F9lZKRVNhd6KIGzDf77SFMIDwz5WtNSjKyqOpF%2FJoVsJj7oN9Ukx1%2Fycl9iXT%2FCZeiJJFnDlDyTDrbEwy30RCRMfqxopEUcZjwrHUW7UVM09oZOGen9yZGM7t%2BYZ1ScqmzYSucs4HtUA9Yt5A0Gq8jy7unXit54MmAzafp1hL06Q0yb5i6VQKBWcRczKO9L1Fa1dB%2BoJjKam%2B8Pt6qJjRldMDq7cc44CjG7yYHK9THMsSy7jqHYOUihgJNkoTjMNlz1niXk9WW1VmWb%2BvBDmK1i2TM%2FHqzfwomXGJf7%2Ba4Ju91eeDN4bGVLAim5KiS4W%2BbpsT9Aaq3peuZ4A6RZzL0LOSy%2B9q3Rnf6XRB1oSzZbcCEdCGszM0zgfdmJCbkUn6uU3M0%2F6H5wxAQiLUsxOy2wmFPjnq7RG9TY4Hk7c3CvFzLNZE1iR9ixD0JsEuX%2BdCLW1eecz6twXZuP5xQTauvi7IR9v6qP19QZcfbv9OXWE5rL74Lwrf6v8m4Kf%2FAA%3D%3D%3C%2Fdiagram%3E%3C%2Fmxfile%3E)

### Versão 3
**Autoria: Davi Ursulino de Oliveira**

![SIG de Usabilidade na notação do NFR Framework - versão 3](../assets/subequipe03-fluxos/SIG/SIG_Usabilidade_V3.drawio.png)

A partir da tabela de rastreabilidade acima (ver "Rastreabilidade com o Foco_01"), esta versão fecha duas das lacunas identificadas entre o SIG e as preocupações reais do usuário levantadas na Rich Picture:

- **Nova folha em *Facilidade de Uso*:** *Ícones pequenos / pouco reconhecíveis* (`--`), correspondendo à preocupação *"Não entendo esses ícones, a letra é muito pequena"*. Como *Facilidade de Uso* passou a ter um filho negativo além do positivo (*Navegação Intuitiva*, `++`), sua avaliação final foi corrigida de `✓` (aceito) para `!` (crítico) — mantendo a mesma coerência de propagação já aplicada a *Velocidade de Acesso*.
- **Novo softgoal *Privacidade*:** adicionado como quarto filho direto de *Usabilidade*, com a folha *Solicitação de geolocalização sem explicação* (`--`), correspondendo à preocupação *"Por que ele quer saber onde eu estou?"*. Recebeu avaliação `X` (rejeitado), já que nenhum método de operacionalização no sistema atual mitiga essa falta de transparência.

As duas preocupações restantes da tabela de rastreabilidade (fluxo de recuperação de senha e número de etapas até o resultado) não foram incorporadas nesta versão e seguem como pendência para uma iteração futura.

Arquivo editável: [SIG_Usabilidade_V3.drawio](https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=SIG_Usabilidade_V3&dark=0#R%3Cmxfile%3E%3Cdiagram%20name%3D%22Pagina-1%22%20id%3D%22czpdueMdJo24robT8H2u%22%3E7Vxbd9o4EP41PMKRLF%2FwI5DS7dlum25Ot82jsAWoMZZrC0L661cyMtjG3BLAgpDTk6KxMhL6Ps2MRrIaqDeZf4xxNP6H%2BSRoGMCfN9BdwzAgdJH4T0peFpI2NBeCUUx9VWkleKB%2FiBICJZ1SnySFipyxgNOoKPRYGBKPF2Q4jtlzsdqQBcVWIzwia4IHDwfr0h%2FU52MldQFYPfiL0NFYNb18MMFZZSVIxthnzzkR%2BtAAnYb8XPyHejFjfOPjrNJk3iOBHOxsHFU7DaN%2F%2BN8uv2ZMQv52dTz%2B%2Ff3%2B2%2BTL4yP79skeEvD4a9C0FgqJvzbiq0aVKGHT2CNbdGX1%2BEsGVMymoU9k%2B6JHXRbzMRuxEAefGYuEEArhL8L5i6IYnnImRGM%2BCdRTEvodSRhRDFlIFpI%2BDQKlUpEPxyPCt%2FTM2AZtedg%2BEjYhPH4R5ZgEmNNZcWiwYu9oWW9fSEQdhcpxwLPfBXjoOsFrvwvwnOsEbwtWKwyEHuER5dAJNxNJoRewqVDbfR5TTh4inIL6LJx0cewXmmY4mCpNDcMORDNdn87Ex5H8%2BD3BAxpQH%2Fskeyq%2BZK6CUkJiTua5Hr4Ci3HOlcIsBnjOOV5byVQ7VlZHhRdLt6UPfsZ58etjb4kVSH99T9iJADJ2A2SAIkAm0A4gZB5gHs9u9iqm5pCJXuX7Yv%2BesuxBM0nbk8OCQDRP9WTPs%2FnazE3jhbLVPD6lAd1H96qFe0bT75lNdQe2gIlc0zVtG5iwXeCVZTgtF5htxzYdy4TALPZi4daUxv2Itqs7CInuuMg1TBshu20XumMjowWhCR3giI4juzQoC1%2F2iu4o9i8H%2F%2Bxz5ZhxINI3DrRON%2FkaRrem6VeTea09fvmPBMzLu0QbT6SacJBEC2AqY5o1PR2PJNKXnjEEMg4PgUyonYeF5jEXIO7xzUYiLAIvGY5UljMdu0xLgAck6GLvaZR2p8cCFufqzin%2FKWu2LEsVH9OimxXv5llDsvCSK9yTmAoESXyYEYPwDBFE0X6BzZHF5QUcEFrFmdV2wJGiirrduHHMjICjrRuHV5oSMNz3AV%2F7SiMi8D7gc68TPue8AW0addJVAq6uOBMCR%2F9A87TJ0oTH7Gm5D2jtufyoCpVCPCMj3OihRsdJfyO2ZVmyIZLavlqpajYSIamYucQLsM9O0gCOPYqDA1XXRmmztHZq2%2FplJ41jrp1q8BYb1kU%2BGeJpwA%2FIycAT52TAe8vMQKf21IxY2nokKttBrYxE2yzaCFvDLSZ0TBvRvlwbkUFzopQHaL4r%2B2CYF06rfVlzpWd2DKdwNg4PsoEH6zBuJUDeGwgufJaztYgEDugolK5BKJR5yq601NTDQUc9mFDflzq6MRFzTXUFpCEpDXk6ZFa3Yd3tbwwOCbpPNu1P66oq%2BaV0ghaCpU3H5qkyoU6pGbfYDhsOE3JhGdDMHJ0r9ukJ2hAZ4XQ7PtNoEa9hNJPR61zQfKlai9cGEIL6h5tAwyxLZ5qQ0KP4bVu8Am%2Fe5KyZRIR4Y%2B3yFWs7UvrlKwzjeskRY39ashOATF6tL6CDWACnGclcV%2F%2BcWO1p3k7A2SKyFqRIeI1peaetP1yobrh6OI6Fj5%2BI5pf5pUG8nIcLcV0Imqjk8ZF%2BCFpaGnUuOiMWmftuo2y3xnGqAEbUx7qZZBvqzxBHQ4Z8OWiXbTs9PoV8SsViXDtylE%2FY60iOYx43QifZwxLjkz%2BeJ8v583myvDqgl5Ze8qXyEb1jvkx42%2FJ6FROHX4nhfer%2B%2BPrx71%2FTh6eHfu%2F%2B3%2F1expGLwCI%2FqqzTwiSVjnkOBcQl0QGp0QKN3wy9gTZCD7eAfnwrhtaNWNmGlda1yLZ0Yw66MUdH5lilfCZ0gW7MsW7M0ZI5pYUz0o859j7MyaBNd%2BXuWSKCVCYhHjDO2aQCe87KwbWKxSfzkbzEozXACfVa4m%2BeJJWSaHGvxpDOJU92c7AhBj%2F9qSbUKdCuCpOdYlarvMgG2qG9145UhhWdpBeX5GGsxnknPTZstwoUh%2BmPqJI21smIAKpYofpzN%2BZc3szSkQNo9KnHwqTlUyyINUlaodwl7OMkITxRVqCJn0kiRl4UxZft%2F2wls1GmbtWpFdFqJJRVysWjdsuxdDch7o1U%2BpDKaNnOLkMFYbtsqYxWlkHVh1cQ3Ih1SdYKuVaJVWdYYR3GMx%2FPaDMmM0qem1qe4%2B%2BhRvtOcIQksmvk95SELFGDtW8aMWJTj6V5EqFoTLw0LXk3I1S7fUCtdiXy3DA0up1jLaO5M31prKf%2BKoh%2FO8D6BoKc%2BcaB%2B5jOsFf321m2pdPbWXk4zIuer3D7fEVXNXOsW1B3SUGdk734ocX6M08kW8P47YEF1KO8vB8MNt9qt6ZCjGfABJPpH7zXO0trChJ5XAyQeRRUnFs4X%2FhnVuXLyg7FtDQNAJ1LcSgVQckmP2Lf4r4yL1L5hquQs9cHVpdOow%2F%2FAw%3D%3D%3C%2Fdiagram%3E%3C%2Fmxfile%3E)

## Legenda do SIG

| Categoria                                    | Símbolo / Elemento Visual | Texto Original                | Tradução (Português)                      |
| :------------------------------------------- | :------------------------ | :---------------------------- | :---------------------------------------- |
| **Softgoals**                                | Nuvem com borda fina      | NFR Softgoal                  | Softgoal de NFR (Requisito Não-Funcional) |
|                                              | Nuvem com borda grossa    | Operationalizing Method       | Método de Operacionalização               |
|                                              | Nuvem com borda tracejada | Claim                         | Argumento (ou Afirmação)                  |
|                                              | `!`                       | Critical                      | Crítico                                   |
|                                              | `✓`                       | Accepted                      | Aceito                                    |
|                                              | `X`                       | Rejected                      | Rejeitado                                 |
| **Interdependência** <br>_(Interdependency)_ | Seta com linha contínua   | Implicity                     | Implícito                                 |
|                                              | Seta com linha tracejada  | Explicity                     | Explícito                                 |
|                                              | `++`                      | Strongly positive satisficing | Satisfação fortemente positiva            |
|                                              | `+`                       | Positive satisficing          | Satisfação positiva                       |
|                                              | `-`                       | Negative satisficing          | Satisfação negativa                       |
|                                              | `--`                      | Strongly Negative satisficing | Satisfação fortemente negativa            |

## Leitura do SIG

O SIG de Usabilidade construído para o Meu SUS Digital decompõe o softgoal de topo em três softgoals de segundo nível, Facilidade de Uso, Velocidade de Acesso e Acessibilidade, sendo o último refinado ainda em Percepção, Conteúdo e Navegação. Essa decomposição aproxima-se dos princípios POUR (Perceivable, Operable, Understandable, Robust) usados pela WCAG para estruturar requisitos de acessibilidade.

| Softgoal pai         | Softgoal/Método filho          | Contribuição | Tipo de nó (nuvem)          |
| -------------------- | ------------------------------ | :----------: | --------------------------- |
| Facilidade de Uso    | Navegação Intuitiva            |     `++`     | Método de Operacionalização |
| Velocidade de Acesso | Carregamento lento             |     `-`      | Método de Operacionalização |
| Velocidade de Acesso | Autenticação rápida            |     `+`      | Método de Operacionalização |
| Acessibilidade       | Percepção                      |      —       | Softgoal                    |
| Acessibilidade       | Conteúdo                       |      —       | Softgoal                    |
| Acessibilidade       | Navegação                      |      —       | Softgoal                    |
| Percepção            | Alto contraste                 |     `++`     | Método de Operacionalização |
| Conteúdo             | Ausência de tradução em libras |     `--`     | Método de Operacionalização |
| Conteúdo             | Ausência de text-to-speech     |     `--`     | Método de Operacionalização |
| Navegação            | Navegação por teclado parcial  |     `--`     | Método de Operacionalização |
| Facilidade de Uso    | Ícones pequenos / pouco reconhecíveis | `--` | Método de Operacionalização (v3) |
| Usabilidade          | Privacidade                    |      —       | Softgoal (v3)                |
| Privacidade          | Solicitação de geolocalização sem explicação | `--` | Método de Operacionalização (v3) |

O ramo de Velocidade de Acesso é o único que apresenta explicitamente um trade-off dentro do mesmo softgoal (um método com contribuição negativa e outro com contribuição positiva), evidenciando que nem toda decisão de otimização de desempenho converge no mesmo sentido.

## Rastreabilidade com o Foco_01

Seguindo a proposta de pré-rastreabilidade baseada em interação social de Serrano e Leite (2011), é possível comparar as preocupações de usabilidade levantadas na Rich Picture (Foco_01) com os nós do SIG para verificar em que medida cada uma delas já está representada na análise formal de requisitos não funcionais.

| Preocupação (Foco_01)                                                                           | Representada no SIG?                                                                 |
| ------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| _"Esqueci minha senha do Gov.br, travei aqui de novo"_                                            | Não. Existe apenas "Autenticação rápida" (`+`), sem nenhum nó relativo a recuperação de senha ou prevenção/tratamento de erro. |
| _"Preciso de ajuda AGORA, por que tem tanto passo antes de eu achar o hospital mais próximo?"_    | Parcialmente. "Velocidade de Acesso" cobre desempenho técnico (carregamento), mas não o número de etapas do fluxo de navegação até o resultado. |
| _"Não entendo esses ícones, a letra é muito pequena"_                                             | Parcialmente. "Facilidade de Uso" possui apenas a folha positiva "Navegação Intuitiva", sem um contraponto negativo sobre legibilidade ou reconhecimento de ícones. |
| _"Por que ele quer saber onde eu estou?"_                                                         | Não. Não há softgoal de Privacidade ou Transparência em nenhum ramo do SIG. |

Das quatro preocupações identificadas na Rich Picture, apenas uma encontra correspondência (ainda que parcial) no SIG atual. Isso indica duas frentes de evolução para a próxima iteração do artefato:

1. Adicionar folhas negativas em Facilidade de Uso (ex.: "Ícones pequenos/pouco reconhecíveis" `--`) e em um softgoal ainda não representado, relacionado à prevenção de erros de autenticação.
2. Introduzir um softgoal de Privacidade (possivelmente como filho direto de Usabilidade, ou combinado a Acessibilidade) para abrigar a preocupação sobre a solicitação de geolocalização, hoje presente apenas na Rich Picture.

Essa comparação materializa, na prática, a rastreabilidade entre o modelo informal (Foco_01) e o modelo formal de NFR, permitindo verificar se decisões de design capturadas de forma qualitativa no rich picture estão sendo de fato consideradas na análise estruturada de requisitos não funcionais.

## Embasamento teórico para criação:

1. CHUNG, Lawrence; NIXON, Brian A.; YU, Eric; MYLOPOULOS, John. Non-Functional Requirements in Software Engineering. Boston: Kluwer Academic Publishers, 2000. DOI: 10.1007/978-1-4615-5269-7.
2. SERRANO, Maurício; LEITE, Julio Cesar Sampaio do Prado. A social interaction based pre-traceability for i* models. In: INTERNATIONAL I* WORKSHOP, 5., 2011. CEUR Proceedings of the 5th International i* Workshop (iStar 2011). [S. l.]: CEUR-WS, 2011. p. 132-137. (Base teórica para a seção "Rastreabilidade com o Foco_01".)

---

| Nome do Membro                                        | Contribuição                                                                                                                      | Data       |
| ----------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| [Gustavo Fornaciari](https://github.com/GUGOFO)       | Criação do Repositorio                                                                                                            | 17/08/2026 |
| [Gabriel Mota Oliveira](https://github.com/Gabro-MO)  | adição do SIG de usabilidade, juntamente com a legenda da notação do NFR Framework (Foco_01)                                      | 26/08/2026 |
| [Gabriel Mota Oliveira](https://github.com/Gabro-MO)  | Adição do embasamento teórico e justificativa para o SIG, e comentarios extras (Foco_01)                                          | 27/08/2026 |
| [Yasmim de Souza Santos](https://github.com/eii-yahs) | Criação do arquivo separado para o artefato produzido                                                                             | 28/08/2026 |
| [Yasmim de Souza Santos](https://github.com/eii-yahs) | Adição da Versão 2 do SIG de Usabilidade, das seções conceituais "O que é um NFR" e "O que é um SIG", e da seção "Leitura do SIG" | 28/08/2026 |
| [Gabriel Mota Oliveira](https://github.com/Gabro-MO)  | Adição do link para guia NFR e correção textual (Foco_01)                                                                         | 28/08/2026 |
| [Davi Ursulino de Oliveira](https://github.com/DaviUrsulino) | Revisão do SIG: correção da justificativa de avaliação de "Velocidade de Acesso" e nota cruzando a avaliação de "Autenticação rápida" com o achado da Rich Picture | 28/08/2026 |
| [Davi Ursulino de Oliveira](https://github.com/DaviUrsulino) | Criação da Versão 3 do SIG: nova folha "Ícones pequenos/pouco reconhecíveis" e novo softgoal "Privacidade", a partir da tabela de rastreabilidade com o Foco_01 | 28/08/2026 |
