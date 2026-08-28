# Rich Picture - Foco_01

## Participantes do artefato

| Nome do Membro            |
| ------------------------- |
| Yasmim de Souza Santos    |
| Davi Ursulino de Oliveira |

## Metodologia do Foco_01

O trabalho foi dividido em duas etapas principais: criação e revisão.

Na etapa de criação, com base no fluxo de busca por uma rede de saúde já levantado na fase de Engenharia Reversa (do login via gov.br até a obtenção de rotas no Google Maps), Yasmim de Souza Santos elaborou a primeira versão do rich picture na ferramenta Canva. As 15 interações identificadas foram representadas por meio de setas numeradas, e um usuário idoso foi escolhido como personagem central para evidenciar barreiras de usabilidade associadas a um perfil de baixo letramento digital.

Na etapa de revisão, Davi Ursulino de Oliveira analisou o artefato de forma crítica e propôs a inclusão de um novo balão de preocupação sobre a falta de transparência na solicitação de geolocalização, ajuste que orienta a próxima iteração do artefato.

Essa dinâmica de criação individual seguida de revisão colaborativa assíncrona está registrada, com as respectivas datas, na tabela de contribuições ao final deste documento.

## O que é uma Rich Picture

Rich picture (ou "imagem rica") é uma técnica de representação informal, originada na Soft Systems Methodology (SSM) de Peter Checkland, usada para retratar de forma visual e holística uma situação-problema antes de qualquer tentativa de solução técnica. Diferente de fluxogramas ou diagramas UML, ela não segue uma notação formal: combina desenhos, ícones, setas e balões de fala/pensamento para capturar não só o processo (o que acontece, em que ordem), mas também os atores envolvidos, o ambiente em que atuam e — principalmente — as preocupações, conflitos e percepções subjetivas que cada um tem sobre a situação.

Essa liberdade de notação é proposital: o objetivo não é documentar um sistema com precisão técnica, mas construir um entendimento compartilhado sobre um contexto complexo, incluindo aspectos "soft" (humanos, sociais, emocionais) que dificilmente apareceriam em um diagrama estruturado.

Elementos comuns a uma rich picture:

- **Atores:** bonecos ou ícones de pessoas representando quem participa da situação;
- **Setas:** indicam fluxos, comunicação ou sequência de ações entre os atores e o sistema;
- **Balões de fala/pensamento (nuvens):** expressam preocupações, dúvidas ou sentimentos — os chamados *concerns*;
- **Ícones e desenhos simples:** substituem caixas e formas geométricas padronizadas, tornando o artefato mais próximo de um esboço do que de um diagrama técnico;
- **Ausência de sintaxe fixa:** o mesmo elemento pode ser desenhado de formas diferentes por autores diferentes, desde que o significado fique claro para quem lê.

Neste artefato, a técnica foi usada para representar o fluxo de busca por uma rede de saúde no Meu SUS Digital sob a ótica de um usuário idoso, evidenciando — por meio dos balões de pensamento, os pontos de fricção de usabilidade percebidos em cada etapa, algo que um fluxograma tradicional, focado apenas na sequência de telas, não capturaria. As referências teóricas utilizadas na construção estão detalhadas na seção "Embasamento teórico para criação", ao final deste documento.

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

| Preocupação  | Onde aparece   | Problema de usabilidade evidenciado |
| ----- | --------- | ------ |
| _"Esqueci minha senha do Gov.br, travei aqui de novo"_ | Etapa 3 (login) | Falta de prevenção/recuperação de erro; barreira de autenticação para usuários com baixo letramento digital|
| _"Preciso de ajuda AGORA, por que tem tanto passo antes de eu achar o hospital mais próximo?"_ | Etapa 2 (pós-login)  | Baixa eficiência do fluxo em cenários de urgência; excesso de passos para uma tarefa crítica   |
| _"Não entendo esses ícones, a letra é muito pequena"_   | Etapas 7-8 (seleção de atendimento/localização)  | Falta de reconhecimento visual e legibilidade inadequada para público idoso  |
| _"Por que ele quer saber onde eu estou?"_   | Etapas 8-9 (solicitação/concessão de acesso à localização) | Falta de transparência sobre o motivo da solicitação de dado sensível (geolocalização); gera desconfiança de privacidade em usuários com baixo letramento digital _(adição: Davi Ursulino de Oliveira, 26/08/2026)_ |

#### Elementos gráficos e seu significado

- **SUS Digital / gov.br:** sistemas envolvidos na autenticação e navegação.
- **Ícone de menu (linhas horizontais):** representa o menu principal da plataforma.
- **Hospital:** representando a seção de Rede de Saúde.
- **Ícone "i" (informação):** tela de detalhes do estabelecimento selecionado.
- **Ícones de dente, coração e cruz médica:** tipos de serviços/especialidades disponíveis (ex.: saúde bucal, cardiologia, emergência).
- **Mapa / Google Maps:** integração externa para visualização geográfica e cálculo de rota.

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
| [Yasmim de Souza Santos](https://github.com/eii-yahs) | Adiciona metodologia e contextualização sobre o que é o artefato | 28/08/2026 |
| [Davi Ursulino de Oliveira](https://github.com/DaviUrsulino) | Atualiza a Rich Picture com o balão de preocupação sobre geolocalização proposto na revisão | 28/08/2026 |