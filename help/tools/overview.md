---
title: Ferramentas de agente
description: Compare servidores MCP, habilidades do agente e APIs para construtores e escolha a ferramenta de agente certa para seus fluxos de trabalho do Adobe CX Enterprise.
index: false
source-git-commit: bb341fa02a8e1e8b3efbf832359846c94441df88
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---


# Ferramentas de agente

<!-- last-modified: 2026-06-08 -->

Nem todas as ferramentas de agilidade atendem à mesma necessidade. Explore o que cada um faz, quando usá-lo e como começar a usá-lo para que você possa escolher o ponto de partida certo para a sua situação.

<!--
CARDS

* mcp-servers.md
  {title = MCP Servers}
  {description = Connect any compatible AI client to Adobe CX Enterprise data and workflows. No coding required.}
  {cta = Explore MCP Servers}
  {image = ../assets/mcp-servers-card.png}

* agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflow instructions that guide agents through CX Enterprise tasks consistently.}
  {cta = Explore Agent Skills}
  {image = ../assets/agent-skills-card.png}

* apis.md
  {title = APIs for Builders}
  {description = Build custom applications and integrations using the same APIs that power Adobe products.}
  {cta = Explore APIs for Builders}
  {image = ../assets/apis-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="mcp-servers.md" title="Servidores MCP" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-servers-card.png" alt="Servidores MCP"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="mcp-servers.md" target="_blank" rel="referrer" title="Servidores MCP">Servidores MCP</a>
                    </p>
                    <p class="is-size-6">Conecte qualquer cliente de IA compatível aos dados e workflows do Adobe CX Enterprise. Nenhum código necessário.</p>
                </div>
                <a href="mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Explorar Servidores MCP</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="agent-skills.md" title="Habilidades do agente" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="Habilidades do agente"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="agent-skills.md" target="_blank" rel="referrer" title="Habilidades do agente">Habilidades do agente</a>
                    </p>
                    <p class="is-size-6">Instruções de fluxo de trabalho com curadoria da Adobe que orientam os agentes pelas tarefas do CX Enterprise de forma consistente.</p>
                </div>
                <a href="agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Explorar habilidades do agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="apis.md" title="APIs para construtores" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-card.png" alt="APIs para construtores"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="apis.md" target="_blank" rel="referrer" title="APIs para construtores">APIs para Construtores</a>
                    </p>
                    <p class="is-size-6">Crie aplicativos e integrações personalizados usando as mesmas APIs que alimentam os produtos da Adobe.</p>
                </div>
                <a href="apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Explorar APIs para Construtores</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## Comparar ferramentas de agilidade

| | Servidores MCP | Habilidades do agente | APIs para construtores |
| --- | --- | --- | --- |
| Melhor para | Usuários do aplicativo corporativo CX | Usuários e desenvolvedores do aplicativo corporativo CX | Desenvolvedores |
| Requer codificação | Não | Não | Sim |
| Configurar tempo | Minutes | Minutes | Horas a dias |
| O que você ganha | Acesso aos aplicativos do CX Enterprise pelos clientes de IA | Fluxos de trabalho guiados e repetíveis | Controle programático completo |

## Não tem certeza de onde começar?

- Para usar a IA para interagir com os aplicativos CX Enterprise (executando ações, consultando dados e permitindo que a IA descubra o que fazer em seguida por meio de uma conversa natural), os [Servidores MCP](mcp-servers.md) são o ponto de partida mais flexível.
- Para que os agentes sigam consistentemente as práticas recomendadas da Adobe para fluxos de trabalho do CX Enterprise sem improvisar, as [Habilidades do agente](agent-skills.md) codificam esse conhecimento de domínio em instruções reutilizáveis.
- Para criar um aplicativo focado que simplifique ou automatize um fluxo de trabalho específico do CX Enterprise para seus usuários, as [APIs para construtores](apis.md) oferecem a você controle direto e programável sobre exatamente o que acontece.

>[!BEGINTABS]

>[!TAB Servidores MCP]

Pense nos servidores MCP como um cabo ativo entre seu cliente de IA e os aplicativos CX Enterprise. Conecte-se uma vez e sua IA pode consultar campanhas, extrair públicos, verificar o status da jornada e muito mais, tudo em linguagem simples, sem a necessidade de código.

**Usar servidores MCP quando:**

- Você deseja integrar a IA diretamente aos fluxos de trabalho do CX Enterprise
- Você deseja dados do CX Enterprise dentro do cliente de IA que você já usa
- Você está fazendo análise exploratória ou recuperação de dados ad hoc
- Você deseja resultados rápidos, sem gerar um projeto

[Explorar servidores MCP](mcp-servers.md)

>[!TAB Habilidades do agente]

As Habilidades do agente são a experiência de domínio da Adobe, codificadas como instruções que seu agente pode seguir. Em vez de esperar que seu agente descubra as etapas certas, uma habilidade informa exatamente o que fazer — de modo confiável, repetitivo e já ajustado para os fluxos de trabalho do CX Enterprise.

**Usar Habilidades do Agente quando:**

- Você deseja seguir as práticas recomendadas da Adobe ao realizar trabalhos em aplicativos CX Enterprise por meio de clientes AI
- Você deseja que a mesma tarefa seja feita da mesma maneira todas as vezes
- Você está executando conteúdo repetível ou fluxos de trabalho de produção de mídia

[Explorar habilidades do agente](agent-skills.md)

>[!TAB APIs para Construtores]

As APIs são os blocos fundamentais. Eles fornecem aos desenvolvedores acesso direto e programático aos dados e operações do Adobe, usando as mesmas APIs que alimentam os próprios produtos da Adobe. Use-as para criar experiências personalizadas focadas que simplificam fluxos de trabalho empresariais específicos com as medidas de proteção de que sua organização precisa.

**Usar APIs quando:**

- Você está criando um aplicativo personalizado ou uma integração para um caso de uso de negócios específico
- Você precisa otimizar ou automatizar um fluxo de trabalho com medidas de proteção e controles específicos
- Você está usando o código Claude ou o cursor para gerar um aplicativo completo
- Você precisa integrar os dados do CX Enterprise a outro sistema

[Explorar APIs para construtores](apis.md)

>[!ENDTABS]

## Usá-los juntos

Essas ferramentas foram projetadas para funcionar em conjunto — e combiná-las é onde você obtém o máximo do Adobe AI. Habilidades do agente podem orientar como um cliente de IA usa servidores MCP, mantendo os agentes no caminho certo para os workflows do CX Enterprise. As habilidades também podem informar como e quando chamar APIs, adicionando medidas de proteção de práticas recomendadas do Adobe a automações personalizadas. Você não precisa escolher apenas um.
