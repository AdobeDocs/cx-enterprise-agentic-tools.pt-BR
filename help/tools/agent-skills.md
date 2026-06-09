---
title: Habilidades do agente
description: Fluxos de trabalho e instruções com curadoria da Adobe que orientam os agentes de IA por meio de tarefas do CX Enterprise de forma consistente.
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: 9a3b90f5f1238e780a0f40b082623cd8da0e71a5
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 3%

---


# Habilidades do agente

<!-- last-modified: 2026-05-19 -->

![Habilidades do agente para o Adobe CX Enterprise](../assets/hero-agent-skills.png)

Habilidades do agente são fluxos de trabalho com curadoria da Adobe que fornecem instruções passo a passo dos agentes de IA para a conclusão confiável das tarefas corporativas do Adobe CX. Cada habilidade do agente codifica a experiência no domínio e as práticas recomendadas para que os agentes produzam resultados consistentes e validados sem precisar improvisar. Habilidades de agente fazem sentido quando você deseja comportamento repetível e guiado em conversas, especialmente para tarefas que de outra forma exigiriam prompts detalhados a cada vez. Eles complementam os servidores MCP e as APIs: as habilidades do agente definem como um agente funciona; os servidores MCP e as APIs fornecem o acesso subjacente.

## Habilidades dos agentes corporativos do Adobe CX

Selecione uma área de recurso abaixo para explorar habilidades para esse fluxo de trabalho.

>[!BEGINTABS]

>[!TAB Adobe Experience Manager]

Habilidades do agente para desenvolvimento, conteúdo, design e gerenciamento de projetos do Experience Manager em AEM as a Cloud Service, Edge Delivery Services e AEM 6.5 LTS.

[Exibir habilidades do agente](https://github.com/adobe/skills/tree/main/plugins/aem)

>[!TAB Adobe Analytics]

Habilidades do agente para monitoramento de KPI, análise do funnel e workflows de relatórios executivos no Adobe Analytics.

[Exibir habilidades do agente](https://github.com/adobe/skills/tree/main/plugins/adobe-analytics)

>[!TAB Customer Journey Analytics]

Habilidades do agente para comparação de desempenho, análise de dimensão e criação de espaço de trabalho no Customer Journey Analytics.

[Exibir habilidades do agente](https://github.com/adobe/skills/tree/main/plugins/adobe-cja)

>[!TAB Adobe App Builder]

Habilidades do agente para andaimes, testes e implantação de aplicativos personalizados com o Adobe App Builder.

[Exibir habilidades do agente](https://github.com/adobe/skills/tree/main/plugins/app-builder)

>[!TAB Creative Cloud]

Habilidades do agente para edição de fotos em lote, design a partir de modelos, edição de vídeo e variantes de redes sociais com o Creative Cloud.

[Exibir habilidades do agente](https://github.com/adobe/skills/tree/main/plugins/creative-cloud)

>[!ENDTABS]

## Como as habilidades do agente funcionam

![Como funcionam as Habilidades dos Agentes](../assets/hero-connect-agent-skills.gif)

Uma habilidade do agente é um conjunto de instruções que informa um agente de IA como concluir uma tarefa usando as ferramentas do agente do Adobe. Quando um agente carrega uma habilidade, ele segue esse fluxo de trabalho em vez de improvisar.

- Os agentes concluem as tarefas da mesma forma a cada vez
- A experiência em domínios é codificada uma vez e reutilizada em conversas
- As habilidades podem agrupar várias ferramentas e ações de agentes em um único fluxo de trabalho

## Introdução

Habilidades do agente são instaladas com base no cliente de IA que você está usando. Alguns clientes oferecem suporte à instalação direta a partir da linha de comando:

- **Código Claude**: `/plugin install adobe/skills`
- **Ambientes de nós**: `npx skills add adobe/skills`
- **CLI do GitHub**: `gh upskill adobe/skills`

Outros clientes exigem que você baixe e adicione os arquivos de habilidade diretamente ao cliente de IA. Consulte o [LEIAME de habilidades do Adobe no GitHub](https://github.com/adobe/skills#installation) para obter instruções completas de instalação do cliente.

### Encontrar habilidades de agentes

Navegue pela lista completa de habilidades disponíveis no [repositório GitHub de Habilidades do Adobe](https://github.com/adobe/skills). Cada habilidade de agente inclui um arquivo `SKILL.md` com orientação detalhada, referências e exemplos.

Depois de instalar ou adicionar o pacote `adobe/skills`, alguns clientes de IA permitem listar todas as habilidades disponíveis diretamente:

- **Código Claude**: `claude /plugin list`
- **Ambientes de nós**: `npx skills list`
- **CLI do GitHub**: `gh upskill list`

## Habilidades do agente versus servidores MCP versus APIs para construtores

| | Habilidades do agente | Servidores MCP | APIs para construtores |
| --- | --- | --- | --- |
| Finalidade | Fluxos de trabalho guiados e práticas recomendadas | Acesso aos dados e ao fluxo de trabalho do Adobe | Integração direta do sistema |
| Codifica a experiência do domínio | Sim | Não | Não |
| Requer codificação | Não | Não | Sim |
| Melhor para | Tarefas guiadas e repetíveis | Consultas de dados e ações de fluxo de trabalho | Desenvolvimento de aplicativos personalizados |
