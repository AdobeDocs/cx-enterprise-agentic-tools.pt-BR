---
title: Habilidades do agente
description: Fluxos de trabalho e instruções com curadoria da Adobe que orientam os agentes de IA por meio de tarefas do CX Enterprise de forma consistente.
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: da8d1eb1dcfef13af5d24ef1fe22ee9977c4e783
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 1%

---


# Habilidades do agente

<!-- last-modified: 2026-05-19 -->

![Habilidades do agente para o Adobe CX Enterprise](../assets/hero-agent-skills.png)

Habilidades do agente são fluxos de trabalho com curadoria da Adobe que fornecem instruções passo a passo dos agentes de IA para a conclusão confiável das tarefas corporativas do Adobe CX. Cada habilidade do agente codifica a experiência no domínio e as práticas recomendadas para que os agentes produzam resultados consistentes e validados sem precisar improvisar. Habilidades de agente fazem sentido quando você deseja comportamento repetível e guiado em conversas, especialmente para tarefas que de outra forma exigiriam prompts detalhados a cada vez. Eles complementam os servidores MCP e as APIs: as habilidades do agente definem como um agente funciona; os servidores MCP e as APIs fornecem o acesso subjacente.

## Habilidades do agente corporativo Adobe CX

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

## Adicionar habilidades do agente

![Como funcionam as Habilidades dos Agentes](../assets/hero-connect-agent-skills.gif)

Uma habilidade do agente é um conjunto de instruções que informa um agente de IA como concluir uma tarefa usando as ferramentas do agente do Adobe. Quando um agente carrega uma habilidade, ele segue esse fluxo de trabalho em vez de improvisar.

### Instalar habilidades do agente

Habilidades do agente são instaladas com base no cliente de IA que você está usando. Alguns clientes oferecem suporte à instalação direta a partir da linha de comando:

- **Código Claude**: `/plugin install adobe/skills`
- **Ambientes de nós**: `npx skills add adobe/skills`
- **CLI do GitHub**: `gh upskill adobe/skills`

Outros clientes exigem que você baixe e adicione os arquivos de habilidade diretamente ao cliente de IA. Consulte o [LEIAME de habilidades do Adobe no GitHub](https://github.com/adobe/skills#installation) para obter instruções completas de instalação do cliente.

### Encontrar habilidades de agente

Navegue pela lista completa de habilidades disponíveis no [repositório GitHub de Habilidades do Adobe](https://github.com/adobe/skills). Cada habilidade de agente inclui um arquivo `SKILL.md` com orientação detalhada, referências e exemplos.

Depois de instalar ou adicionar o pacote `adobe/skills`, alguns clientes de IA permitem listar todas as habilidades disponíveis diretamente:

- **Código Claude**: `claude /plugin list`
- **Ambientes de nós**: `npx skills list`
- **CLI do GitHub**: `gh upskill list`

## Habilidades do agente em ação

<!--
CARDS

* https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Develop AEM components with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" title="Desenvolver componentes do AEM com IA" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="Desenvolver componentes do AEM com IA"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" title="Desenvolver componentes do AEM com IA">Desenvolver componentes do AEM com IA</a>
                    </p>
                    <p class="is-size-6">Use o código Claude ou o cursor com habilidades de agente para criar andaimes, codificar e refinar componentes do AEM guiados pelas práticas recomendadas da Adobe.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Tente com Habilidades de Agente</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
