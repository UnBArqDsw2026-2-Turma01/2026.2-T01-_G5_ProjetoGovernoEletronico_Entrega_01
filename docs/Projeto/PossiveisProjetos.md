# Possíveis Projetos

Este documento reúne as propostas de sistemas de **Governo Eletrônico** pesquisadas pelos membros responsáveis pela tarefa, para que a equipe possa comparar as opções e escolher o sistema que será usado como base do projeto **G5_ProjetoGovernoEletronico**.

Cada proposta segue o mesmo modelo: identificação do sistema, justificativa da escolha e a divisão dos fluxos entre as três subequipes, com o respectivo NFR (Requisito Não Funcional) em destaque.


---

## Resumo das Propostas

| # | Responsável | Sistema Proposto | NFRs em destaque |
| -- | -- | -- | -- |
| 1 | Victor Leandro | Carteira Digital de Trânsito | Segurança/Privacidade, Confiabilidade, Usabilidade |
| 2 | Artur Galdino | Fala.BR | Segurança/Privacidade, Desempenho, Usabilidade |
| 3 | Giovani Coelho | Meu SUS Digital | Segurança/Privacidade, Usabilidade, Confiabilidade |

---

## Proposta 1 — Victor Leandro

### Sistema Escolhido

**Carteira Digital de Trânsito**

### Justificativa

É um ecossistema com alta demanda nacional que integra documentos de porte obrigatório e serviços transacionais. Exige forte **Confiabilidade** e **Desempenho** (validação jurídica offline/online e alta disponibilidade) e **Segurança/Privacidade** (acesso a dados biométricos, CNH e restrições veiculares protegidos pela LGPD), além de necessitar de **Usabilidade** simplificada para situações emergenciais de fiscalização no trânsito.

### Divisão dos Fluxos por Subequipe

| Subequipe | Fluxo | NFR em destaque |
| -- | -- | -- |
| SubEquipe_01 | Autenticação Gov.br, Validação Biométrica e Emissão/Validação de CNH Digital | Segurança / Privacidade |
| SubEquipe_02 | Consulta e Gestão de Veículos com Transferência Digital de Propriedade (Venda Digital) | Confiabilidade / Integridade de Dados |
| SubEquipe_03 | Consulta, Adesão ao SNE (Sistema de Notificação Eletrônica) e Pagamento/Parcelamento de Multas com Desconto | Usabilidade / Eficiência |

---

## Proposta 2 — Artur Galdino

### Sistema Escolhido

**Fala.BR**

### Justificativa

(foco em Privacidade) Trata de denúncias, reclamações e pedidos de informação. Isso envolve regras claras de anonimato vs. identificação, pseudonimização de dados do denunciante e proteção de dados sensíveis em anexos.<br>
(foco em Usabilidade) Usuários recorrem à ouvidoria frequentemente sob estresse ou buscando direitos. A clareza no passo a passo, a visibilidade do status do protocolo e a linguagem simples são pontos determinantes e fáceis de mapear e refinar na interface.

### Divisão dos Fluxos por Subequipe

| Subequipe | Fluxo | NFR em destaque |
| -- | -- | -- |
| SubEquipe_01 | Registro de Manifestação/Denúncia com Escolha de Privacidade | Segurança/Privacidade |
| SubEquipe_02 | Acompanhamento de Protocolo e Interação com o Órgão | Desempenho |
| SubEquipe_03 | Gestão de Perfil, Histórico e Anonimização de Conta | Usabilidade |

---

## Proposta 3 — Giovani Coelho

### Sistema Escolhido

**Meu SUS Digital**

### Justificativa

É um cenário perfeito pois lida com dados médicos sensíveis (foco em Privacidade) e precisa ser acessível para toda a população brasileira (foco em Usabilidade).

### Divisão dos Fluxos por Subequipe

| Subequipe | Fluxo | NFR em destaque |
| -- | -- | -- |
| SubEquipe_01 | Autenticação via Gov.br e Termos de Uso | Segurança/Privacidade |
| SubEquipe_02 | Navegação e Busca por serviços de saúde | Usabilidade |
| SubEquipe_03 | Geração e Exportação de certificados, como vacina | Confiabilidade |

---

## Histórico de Versionamento

| Nome do Membro | Contribuição | Data | Commit |
| -- | -- | -- | -- |
| [Victor Leandro](https://github.com/Afrontoso) | Pesquisa da Carteira Digital de Trânsito e divisão de fluxos por subequipe | 22/08/2026 | [79974b8](https://github.com/UnBArqDsw2026-2-Turma01/2026.2-T01-_G5_ProjetoGovernoEletronico_Entrega_01/commit/79974b85fb1146516274a9d206ed7df06293843c) |
| [Victor Leandro](https://github.com/Afrontoso) | Formatação do documento em Markdown e criação do modelo de proposta | 25/08/2026 | [79974b8](https://github.com/UnBArqDsw2026-2-Turma01/2026.2-T01-_G5_ProjetoGovernoEletronico_Entrega_01/commit/79974b85fb1146516274a9d206ed7df06293843c) |
| [Artur Galdino](https://github.com/ArturFGaldino) | Pesquisa da Fala.BR e divisão de fluxos por subequipe | 26/08/2026 | [258ea74](https://github.com/UnBArqDsw2026-2-Turma01/2026.2-T01-_G5_ProjetoGovernoEletronico_Entrega_01/commit/258ea74a6accd1a325df750532ab3bbcfdbf9c98) |
| [Giovani Coelho](https://github.com/Gotc2607) | Adicionando a proposta do Meu SUS Digital, com justificativa e divisão dos fluxos por subequipe | 26/08/2026 | [8a34776](https://github.com/UnBArqDsw2026-2-Turma01/2026.2-T01-_G5_ProjetoGovernoEletronico_Entrega_01/commit/8a347764d88dc67e242c05c46a593a2d09bdbdd0) |
