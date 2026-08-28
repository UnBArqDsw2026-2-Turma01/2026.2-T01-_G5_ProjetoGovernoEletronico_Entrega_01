# Requisitos Não-Funcionais em Desenvolvimento de Software

Os requisitos não-funcionais (NFR) definem como o sistema deve operar, afetando diretamente a qualidade, experiência do usuário e a escolha de arquitetura. Uma boa engenharia de requisitos assegura metas de qualidade mensuráveis, evitando retrabalho caro e riscos como penalidades de LGPD por falta de conformidade.

O NFR Framework propõe tratar os RNFs como "softgoals" que guiam o design, priorizando atributos como segurança, usabilidade e escalabilidade desde o início. A seguir será apresentado definições, categorias comuns com exemplos práticos, métodos e métricas de medição, técnicas de elicitação/priorização, templates de especificação e um passo a passo.

## Definição e Princípios do NFR Framework

Requisitos não-funcionais são atributos de qualidade que definem como o software executa suas funções, velocidade, confiabilidade, segurança, etc., não apenas o que faz. Ao contrário dos requisitos funcionais, os RNFs determinam critérios de aceitação e limitações do sistema. Por exemplo, "processar login" é funcional, enquanto "tempo de resposta ≤ 200ms", e "99,9% de disponibilidade" são RNFs.

O NFR Framework, incentiva a priorização precoce desses requisitos, representando-os como softgoals na arquitetura. Isso significa documentar RNFs objetivamente usando métricas e limites claros, e inseri-los no processo de design desde o início. Princípios importantes incluem:

- **Mensurabilidade:** RNFs devem ser quantificáveis e testáveis (ex.: latência, MTTR, índices de falhas).
- **Transparência:** Envolva stakeholders relevantes para validar e negociar metas (NIST, IREB, ISO/IEC 25010).
- **Trade-offs:** Reconheça que RNFs podem conflitar (e.g. mais segurança pode degradar performance) e busque compromissos e análises de risco.

## Categorias Comuns de NFR

- **Segurança:** Capacidade de proteger dados e recursos contra acessos e ataques não autorizados. Ex.: "Todos os dados sensíveis devem ser armazenados criptografados e o sistema deve resistir a cenários de ataques OWASP Top10"\*.
- **Desempenho:** Velocidade e eficiência na resposta e processamento de dados. Ex.: "Tempo de resposta máximo de 500ms em 95% das requisições" ou "suporta mais de 100 transações por segundo".
- **Disponibilidade:** Percentual de tempo em que o sistema deve estar operacional. Ex.: "Sistema disponível 99,9% do tempo mensurado por monitoramento".
- **Escalabilidade:** Capacidade de manter desempenho ao aumentar carga de usuários ou dados. Ex.: "Suportar crescimento de usuários ativos de 50% sem degradar latência ou uso de arquiteturas elásticas (auto-escalamento)".
- **Manutenibilidade:** Facilidade de modificar, corrigir ou evoluir o sistema. Ex.: "Arquitetura modular com baixo acoplamento e cobertura de testes $\ge80\%$". Subcaracterísticas incluem modularidade, testabilidade e reusabilidade.
- **Usabilidade:** Facilidade de aprendizado, eficiência e satisfação do usuário. Ex.: "Sistema deve obter $SUS\ge80$ e máxima de 2 erros por tarefa em testes de usabilidade". Engloba interface intuitiva, feedback claros e acessibilidade.
- **Compatibilidade/Portabilidade:** Capacidade de operar em diferentes ambientes ou integrar-se a outros sistemas. Ex.: "Suporta Windows, Linux e integração via API REST com sistemas externos". ISO/IEC 25010 define sub-itens como interoperabilidade e coexistência.
- **Conformidade:** Adequação a leis, normas e padrões como. ISO, LGPD/GDPR, PCI. Ex.: "Atender os controles da LGPD para dados pessoais, com auditoria trimestral"\*.
- **Internacionalização/Localização:** Suporte a múltiplos idiomas, formatos de data/moeda e cultura. Ex.: "Interface disponível em Português e Inglês, com formatos regionais configuráveis".
- **Observabilidade/Monitoramento:** Possibilidade de coletar métricas, logs e rastros para entender o estado interno do sistema. Ex.: "Implementar logs estruturados, métricas de desempenho (CPU, memória) e tracing distribuído para cada serviço".

## Métricas e Métodos de Medição por Categoria

Cada atributo de NFR deve ser traduzido em metas numéricas e validadas por testes/monitoramento. Exemplos de métricas incluem:

- **Desempenho:** Latência média/percentil (ms), throughput $(req/s)$, tempo CPU, SLAs/SLOs. Medições via teste de carga e estresse, benchmarking e profilers.
- **Disponibilidade e Confiabilidade:** Uptime (%) em períodos, MTBF, MTTR. Instrumenta-se monitoração em produção (ex. Ping/HTTP checks), calculam-se métricas como disponibilidade = MTTF/(MTTF+MTTR).
  - **MTBF (Mean Time Between Failures):** Tempo Médio Entre Falhas é o tempo médio entre falhas sucessivas, geralmente usado para sistemas reparáveis. Ex.: Imagine um servidor que funciona 500 h então falha e demora 2 h para reparar, então funciona por mais 700 h e falha novamente, então $MTBF=600$ h.
  - **MTTF (Mean Time To Failure):** Tempo Médio Até a Falha é o tempo médio que um sistema funciona até ocorrer uma falha. Ex.: se um sistema funciona, em média, 1.000 horas antes de falhar então $MTTF=1.000$ h.
  - **MTTR (Mean Time To Repair/Recover):** Tempo Médio Para Reparo/Recuperação é o tempo médio necessário para corrigir a falha e colocar o sistema novamente em funcionamento. Ex.: se, após uma falha, são necessárias 2 horas para recuperar o sistema então MTTR $=2$ h.
- **Escalabilidade:** Índice de usuários suportados antes de queda de desempenho, testes de stress e load testing variando carga. Métricas: fator de escala (ex. 2x usuários mantém <5% de aumento na latência) e métrica de elasticidade.
- **Segurança:** Número de vulnerabilidades identificadas (ferramentas de análise estática/dinâmica), cobertura de criptografia, incidentes por período, tempo de resposta a incidentes (MTTD/MTTR de segurança). Testes: pentests, varredura OWASP, revisão de código focada em segurança.
- **Usabilidade:** Índices de satisfação (SUS, NPS, avaliações), tempo médio para completar tarefas, taxa de erro do usuário, métricas de engajamento (bounce rate, tempo na página). Métodos: testes de usabilidade, protótipos com usuários reais, análises UX quantitativas.
- **Manutenibilidade:** Métricas estáticas de código (complexidade ciclomática, acoplamento), cobertura de testes $(ex.\ge80\%)$, tempo médio para implementar mudanças (Lead time). Métricas de defeitos pós-release. Ferramentas: análise estática de código, code coverage, testes automatizados.
- **Compatibilidade:** Percentual de casos de uso cobertos em ambientes suportados, testes de interoperabilidade. Por exemplo, tempo de integração (hours) para plataformas diferentes. Usa-se testes de conformidade (casos de teste executados em diferentes SOs e browsers).
- **Conformidade:** Checklist de requisitos legais atendidos, relatórios de auditoria, número de não-conformidades. Validações via auditorias internas/externas e planos de remediação.
- **Internacionalização:** Cobertura de idiomas suportados, teste de formatos regionais (datas, moedas), localização de mensagens. Usa-se revisão linguística e testes exploratórios em diferentes localidades.
- **Observabilidade:** Percentual de componentes com logs métricos configurados, cobertura de métricas (latência, erros, uso de recursos) e tempo médio de detecção de falhas (MTTD).

## Técnicas de Elicitação, Priorização e Trade-offs

- **QFD (Quality Function Deployment):** Mapeia necessidades do usuário/negócio em requisitos de qualidade, usando matriz "Casa da Qualidade" para relacionar atributos (ex.: "facilidade de uso" vs. "tempo de resposta") e balancear trade-offs.
- **ATAM (Architecture Tradeoff Analysis Method):** Técnica de análise arquitetural para avaliar como design alternativo atende RNFs conflitantes. Identifica objetivos de negócio, expõe trade-offs e riscos de arquitetura. (Ex.: ATAM ajuda a escolher entre autenticação leve ou forte, avaliando impacto na latência.).
- **FURPS+:** Modelo de classificação de atributos (Funcionalidade, Usabilidade, Confiabilidade, Performance, Suportabilidade). Funciona como checklist: por exemplo, em Suportabilidade consideram-se manutenibilidade, compatibilidade, testabilidade, etc. Auxilia a não esquecer categorias ao listar RNFs.
- **MOSCOW:** Priorização ágil (Must/Should/Could/Won't). Ajuda a definir quais RNFs são essenciais na entrega (Must), desejáveis (Should) ou adiáveis (Could).
- **Análise de Risco:** Classifica RNFs pela criticidade para o negócio. Típicos critérios: impacto financeiro, segurança/regulatório, experiência do usuário.

## Passo a Passo

1. **Planejamento de RNFs:** Envolver product owner e equipe: levantar RNFs iniciais via entrevistas com stakeholders e análise de documentações. Priorizar em MoSCoW ou matriz de valor/risco.
2. **Documentação e Especificação:** Refinar e documentar RNFs em histórias ou no método relativo à abordagem do projeto. Incluir critérios de aceitação claros. Vincular a Definition of Done e Ready, e checklist de qualidade.
3. **Implementação de Medições e Testes Iniciais:** Configurar pipelines de CI/CD para rodar testes não-funcionais automatizados.
4. **Validação e Ajustes:** Realizar testes de carga/segurança/usabilidade nas features implementadas, coletar dados. Ajustar requisitos conforme resultados. Por exemplo, se a latência média excedeu o alvo, otimizar ou re-priorizar soluções arquiteturais. Incluir demonstração das RNFs na review.
5. **Revisão Contínua e Entrega:** A cada sprint subsequente, revisitar RNFs: atualizar o backlog, acrescentar novos se necessário. Garantir que a aceitação dependa de atendimento a RNF. Integre testes não-funcionais no pipeline e revise as prioridades para futuras sprints.

## Ferramentas Recomendadas

- **Ferramentas:** Ferramentas de gestão de requisitos (Atlassian Jira/Confluence, IBM DOORS), plataformas de CI/CD (GitLab, Jenkins) integrando testes NFR, APM e monitoramento (NewRelic, Prometheus+Grafana), ferramentas de teste não-funcional (JMeter/Gatling, OWASP ZAP, Selenium para usabilidade automatizada), análise estática (SonarQube). Frameworks de arquitetura (C4, UML) para modelar NFR via softgoals/SIG.

## Bibliografia

- **Normas e Padrões:** ISO/IEC 25010 (modelo de qualidade de software com categorias de RNF); IEEE 830/ISO/IEC 29148 (especificação de requisitos); normas específicas (ISO 27001 para segurança, PCI DSS, LGPD/GDPR). Documentos do NFR Framework (Chung et al., 2000) e extensões.
- **Papers e Referências:** "Non-Functional Requirements in Software Engineering" (Chung et al., 2000), base conceitual do NFR Framework; artigos de DevMedia e SoftDesign sobre RNF no contexto de arquitetura; Whitepapers sobre QA e métricas (Visure Solutions). Blogs técnicos especializados em requisitos (e.g. Sofist sobre ISO 25010, Visure sobre gestão de NFR).

---

## Histórico de Versionamento

| Nome do Membro                              | Contribuição                     | Data       |
| ------------------------------------------- | -------------------------------- | ---------- |
| [Gabriel Mota](https://github.com/Gabro-MO) | Criação do Guia do NFR Framework | 23/08/2026 |
