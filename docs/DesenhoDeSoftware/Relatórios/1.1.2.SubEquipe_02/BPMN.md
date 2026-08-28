# BPMN

Nesta seção, apresenta-se a versão finalizada do **BPMN (Business Process Model and Notation)**, que ilustra o contexto, atores, sistemas envolvidos, fluxos de informação e principais preocupações do sistema.


Image Aqui


### Legenda e Tipos de Elementos do SIG

- **Softgoals de Requisito (Nuvem de Borda Fina):** Objetivos de qualidade (ex.: *Usabilidade*, *Segurança*, *Desempenho*).
- **Operacionalizações (Nuvem de Borda Grossa):** Soluções técnicas e escolhas de arquitetura (ex.: *Autenticação Gov.br*, *Criptografia TLS*, *Mascaramento de Dados*).
- **Claims (Nuvem Tracejada):** Justificativas e argumentos de projeto.
- **Tipos de Contribuição:**
  - **`++` (Make):** Satisfaz fortemente o softgoal.
  - **`+` (Help):** Contribuição positiva parcial.
  - **`-` (Hurt):** Prejudica parcialmente o softgoal.
  - **`--` (Break):** Compromete severamente o softgoal.

---


### Participantes
| Nome do Membro |
| :--- |
| [Victor Leandro](https://github.com/Afrontoso) |

### Metodologia
Fale sua Metodologia

### Processo de Engenharia Reversa Aplicado

A Engenharia Reversa foi aplicada sob uma perspectiva comportamental (caixa-preta). Simulamos um login real no aplicativo Meu SUS Digital usando uma conta Gov.br, interceptando visualmente as etapas (redirecionamentos de navegador) e analisando o padrão arquitetural esperado para esse tipo de integração, que é o OAuth 2.0 com PKCE (Proof Key for Code Exchange).

Os achados revelaram que o Frontend do Meu SUS Digital interage com o Gov.br gerando códigos de desafio (Code Verifier e Challenge), enviando-os no Backchannel, recebendo os Tokens e validando as assinaturas (JWKS) antes de permitir o acesso seguro ao painel do Cidadão.

### Modelagem BPMN
O modelo gerado detalha o fluxo de Autenticação entre o Cidadão, o Frontend (Meu SUS Digital) e o provedor Gov.br.

## Histórico de Versionamento

### Versão 1.0 (v1)

Imagem V1 aqui

#### Quem fez a versão
- [Victor Leandro](https://github.com/Afrontoso)

#### O que mudou da versão anterior
- Estruturação do Foco 2: Engenharia Reversa e BPMN do fluxo de login (Gov.br).
- Adição de fundamentação teórica e referências bibliográficas (OAuth 2.0, OWASP, Gov.br) ao Foco 2.
- Inclusão da tabela de detalhamento do fluxo de autenticação.

### Versão 2.0 (v2)

Imagem V2 aqui

#### Quem fez a versão
- [Victor Leandro](https://github.com/Afrontoso)

#### O que mudou da versão anterior
- Estruturação do Foco 2: Engenharia Reversa e BPMN do fluxo de login (Gov.br).
- Adição de fundamentação teórica e referências bibliográficas (OAuth 2.0, OWASP, Gov.br) ao Foco 2.
- Inclusão da tabela de detalhamento do fluxo de autenticação.

---

| Nome do Membro | Contribuição | Data |
| :--- | :--- | :--- |
| [Victor Leandro](https://github.com/Afrontoso) | Primeira versao do BPMN | 27/08/2026 |
