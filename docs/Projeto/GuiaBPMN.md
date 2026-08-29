# Guia BPMN Geral

Este documento apresenta uma introdução à notação **BPMN (Business Process Model and Notation)** e orientações sobre a escolha e utilização de ferramentas de modelagem para o projeto.

## Introdução à Notação BPMN

A **BPMN (Business Process Model and Notation)** é um padrão internacional para modelagem e diagramação visual de processos de negócio. No contexto de Desenho de Software (DSW), ela é utilizada para documentar os fluxos de trabalho e a jornada do usuário recuperados durante a Engenharia Reversa, auxiliando na tradução de processos em visões arquiteturais do sistema.

### Principais Elementos

- **Piscinas (Pools) e Raias (Lanes):** Utilizadas para delimitar papéis, atores e diferentes subpartes da organização/sistema.
- **Atividades / Tarefas:** Representam o trabalho ou ações executadas dentro do fluxo.
- **Eventos:** Indicam o **Início**, estados **Intermediários** e o **Fim** de um processo.
- **Conectores de Fluxo:** Linhas e setas que indicam a ordem de execução das atividades.
- **Gateways:** Pontos de decisão e controle do fluxo (ex.: Exclusivo, Inclusivo e Paralelo).

---

## Ferramentas Recomendadas

Com o objetivo de garantir flexibilidade entre diferentes sistemas operacionais, ferramentas gratuitas e facilidade de aprendizado sem necessidade de instalações locais, foram analisadas múltiplas ferramentas do mercado. As opções recomendadas para a equipe são o **HEFLO** e o **Draw.io**.

### 1. HEFLO 

Excelente para a criação de fluxos formais em notação BPMN 2.0, oferecendo elementos coloridos e uma interface agradável e intuitiva.

- **Acesso:** [HEFLO App](https://app.heflo.com/)

#### Passo a Passo de Uso no HEFLO:
1. Acesse a plataforma e crie sua conta.
2. Crie um novo diagrama clicando no ícone de **"+"** na barra superior da área de trabalho.
3. Para adicionar elementos ao fluxo, selecione o ícone na barra lateral e arraste-o para a área de trabalho.
4. Para conectar elementos com setas, clique na seta ao lado do elemento origem e arraste o cursor até o elemento destino.
5. Para delimitar papéis e responsabilidades, utilize os ícones de **Piscina** e **Raia** disponíveis na barra lateral.

---

### 2. Draw.io

Excelente para diagramações rápidas, rascunhos e colaboração visual contínua. Oferece uma ampla variedade de elementos, setas e ícones gerais.

- **Acesso:** [Draw.io](https://app.diagrams.net/)

#### Passo a Passo de Uso no Draw.io:
1. Acesse o site para abrir diretamente a área de trabalho.
2. No menu lateral esquerdo, clique em **"+ Mais Formas"**.
3. Selecione a opção **BPMN 2.0** e clique em **Aplicar** para habilitar o pacote completo de símbolos BPMN.
4. Utilize o conjunto de elementos de **BPMN 2.0 General** e **BPMN 2.0 Tasks**, incluindo as estruturas de **Pool** (Piscina) e **Lane** (Raia).

---

## Outras Opções Analisadas

### Bizagi Modeler
É a solução mais difundida no mercado corporativo. No entanto, seu instalador desktop é restrito ao sistema operacional **Windows**, o que gera limitações para membros da equipe que utilizam outros sistemas. Fica disponível como recomendação de uso individual para quem possui sistema Windows.
- **Acesso:** [Bizagi Modeler](https://www.bizagi.com/)

### BPMN.io
Editor 100% web que executa diretamente no navegador. É simples, rápido e possui excelente aderência à notação BPMN para diagramas de processos. No entanto, apresenta limitações quanto à variedade de elementos, ícones, setas e opções de customização visual.
- **Acesso:** [BPMN.io](https://bpmn.io/)

---

## Histórico de Versionamento

| Nome do Membro | Contribuição | Data | Commit |
| -- | -- | -- | -- |
| [Nicole Jovita](https://github.com/nicolejovita) | Criação do Guia de Modelador BPMN e Notações | 26/08/2026 | [9ec435e](https://github.com/UnBArqDsw2026-2-Turma01/2026.2-T01-_G5_ProjetoGovernoEletronico_Entrega_01/commit/9ec435e373a7dbd1bb1d390c2e473046d31c4442) |