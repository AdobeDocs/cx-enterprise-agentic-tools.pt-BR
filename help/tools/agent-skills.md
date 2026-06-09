---
title: Habilidades do agente
description: Fluxos de trabalho e instruções com curadoria da Adobe que orientam os agentes de IA por meio de tarefas do CX Enterprise de forma consistente.
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: 1681b6de9d0459ed9d5420f77048778712cd0004
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 6%

---


# Habilidades do agente

<!-- last-modified: 2026-05-19 -->

![Habilidades do agente para o Adobe CX Enterprise](../assets/hero-agent-skills.png)

Habilidades do agente são fluxos de trabalho com curadoria da Adobe que fornecem instruções passo a passo dos agentes de IA para a conclusão confiável das tarefas corporativas do Adobe CX. Cada habilidade do agente codifica a experiência no domínio e as práticas recomendadas para que os agentes produzam resultados consistentes e validados sem precisar improvisar. Habilidades de agente fazem sentido quando você deseja comportamento repetível e guiado em conversas, especialmente para tarefas que de outra forma exigiriam prompts detalhados a cada vez. Eles complementam os servidores MCP e as APIs: as habilidades do agente definem como um agente funciona; os servidores MCP e as APIs fornecem o acesso subjacente.

Todas as Habilidades do Agente são mantidas no [repositório GitHub de Habilidades da Adobe](https://github.com/adobe/skills), que é a fonte primária para a documentação, instalação e detalhes de implementação das Habilidades do Agente.

## Habilidades dos agentes corporativos do Adobe CX

Todas as Habilidades do Agente são mantidas no [repositório GitHub de Habilidades do Adobe](https://github.com/adobe/skills). Selecione uma área de recurso abaixo para explorar habilidades para esse fluxo de trabalho.

<!--
CARDS

* https://github.com/adobe/skills/tree/main/plugins/aem
  {title = Adobe Experience Manager}
  {description = Agent Skills for Experience Manager development, content, design, and project management across AEM as a Cloud Service, Edge Delivery Services, and AEM 6.5 LTS.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-aem-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-analytics
  {title = Adobe Analytics}
  {description = Agent Skills for KPI monitoring, funnel analysis, and executive reporting workflows in Adobe Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-analytics-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-cja
  {title = Customer Journey Analytics}
  {description = Agent Skills for performance comparison, dimension analysis, and workspace authoring in Customer Journey Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cja-card.png}

* https://github.com/adobe/skills/tree/main/plugins/app-builder
  {title = Adobe App Builder}
  {description = Agent Skills for scaffolding, testing, and deploying custom applications with Adobe App Builder.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cxenterprise-card.png}

* https://github.com/adobe/skills/tree/main/plugins/creative-cloud
  {title = Creative Cloud}
  {description = Agent Skills for batch photo editing, design from templates, video editing, and social media variants with Creative Cloud.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-creative-cloud.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Manager">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/aem" title="Adobe Experience Manager" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-aem-card.png" alt="Adobe Experience Manager"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/aem" target="_blank" rel="referrer" title="Adobe Experience Manager">Adobe Experience Manager</a>
                    </p>
                    <p class="is-size-6">Habilidades do agente para desenvolvimento, conteúdo, design e gerenciamento de projetos do Experience Manager em AEM as a Cloud Service, Edge Delivery Services e AEM 6.5 LTS.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/aem" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Exibir habilidades do agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-analytics" title="Adobe Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-analytics-card.png" alt="Adobe Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-analytics" target="_blank" rel="referrer" title="Adobe Analytics">Adobe Analytics</a>
                    </p>
                    <p class="is-size-6">Habilidades do agente para monitoramento de KPI, análise do funnel e workflows de relatórios executivos no Adobe Analytics.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-analytics" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Exibir habilidades do agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Customer Journey Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-cja" title="Customer Journey Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-cja-card.png" alt="Customer Journey Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-cja" target="_blank" rel="referrer" title="Customer Journey Analytics">Customer Journey Analytics</a>
                    </p>
                    <p class="is-size-6">Habilidades do agente para comparação de desempenho, análise de dimensão e criação de espaço de trabalho no Customer Journey Analytics.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-cja" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Exibir habilidades do agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe App Builder">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/app-builder" title="Adobe App Builder" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-cxenterprise-card.png" alt="Adobe App Builder"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/app-builder" target="_blank" rel="referrer" title="Adobe App Builder">Adobe App Builder</a>
                    </p>
                    <p class="is-size-6">Habilidades do agente para andaimes, testes e implantação de aplicativos personalizados com o Adobe App Builder.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/app-builder" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Exibir habilidades do agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Creative Cloud">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/creative-cloud" title="Creative Cloud" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-creative-cloud.png" alt="Creative Cloud"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/creative-cloud" target="_blank" rel="referrer" title="Creative Cloud">Creative Cloud</a>
                    </p>
                    <p class="is-size-6">Habilidades do agente para edição de fotos em lote, design a partir de modelos, edição de vídeo e variantes de redes sociais com o Creative Cloud.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/creative-cloud" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Exibir habilidades do agente</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


Para obter detalhes completos sobre as habilidades, métodos de instalação e código-fonte, consulte o [repositório do GitHub de Habilidades do Adobe](https://github.com/adobe/skills).

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
