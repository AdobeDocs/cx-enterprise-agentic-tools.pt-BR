---
title: Ferramentas de agente
description: Compare servidores MCP, habilidades do agente e APIs para construtores e escolha a ferramenta de agente certa para seus fluxos de trabalho do Adobe CX Enterprise.
index: false
source-git-commit: 3c29bfeeef3d2cb523724db02448aaa77cdf8900
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 1%

---


# Ferramentas de agente

<!-- last-modified: 2026-05-08 -->

Nem toda abordagem de usinagem de agilidade atende à mesma necessidade. Os servidores MCP fornecem acesso imediato e em linguagem natural aos dados do Adobe de qualquer cliente de IA compatível, sem a necessidade de codificação. As Habilidades do agente codificam a experiência de domínio da Adobe em fluxos de trabalho de agente repetíveis, de modo que as tarefas sejam executadas de forma consistente sempre que necessário. As APIs fornecem aos desenvolvedores controle programático total para criar aplicativos e integrações personalizados. Esta página explica as compensações para que você possa escolher o ponto de partida certo para sua situação.

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
| Melhor para | Usuários clientes de IA | Todos os usuários | Desenvolvedores |
| Requer codificação | Não | Não | Sim |
| Configurar tempo | Minutes | Minutes | Horas a dias |
| O que você ganha | Acesso ao Adobe por meio da ferramenta de IA | Fluxos de trabalho guiados e repetíveis | Controle programático completo |
| Cliente de IA necessário | Sim | Sim | Opcional |

## Não tem certeza de onde começar?

- Para usar a IA para interagir com os aplicativos corporativos do Adobe CX (executando ações, consultando dados e permitindo que a IA descubra o que fazer em seguida por meio de uma conversa natural), os [Servidores MCP](mcp-servers.md) são o ponto de partida mais flexível.
- Para que os agentes sigam consistentemente os fluxos de trabalho nativos do Adobe sem improvisar, as [Habilidades do agente](agent-skills.md) codificam esse conhecimento de domínio em instruções reutilizáveis.
- Para criar um aplicativo focado que simplifique ou automatize um fluxo de trabalho específico do Adobe para seus usuários, as [APIs para Construtores](apis.md) oferecem controle direto e programável sobre exatamente o que acontece.

>[!BEGINTABS]

>[!TAB Servidores MCP]

Pense nos servidores MCP como uma conexão ativa entre sua ferramenta de IA e o Adobe. Conecte uma vez e sua IA pode consultar campanhas, extrair públicos, verificar o status da jornada e muito mais. Tudo em linguagem simples, nenhum código é necessário.

**Usar servidores MCP quando:**

- Você deseja dados do Adobe dentro da ferramenta de IA já usada
- Você está fazendo análise exploratória ou recuperação de dados ad hoc
- Você deseja resultados rápidos, sem gerar um projeto

**Experimente:** peça a Claude para resumir suas jornadas ativas. Extrair tamanhos de público-alvo do Real-Time CDP do ChatGPT. Revise as métricas de campanha do CJA sem abrir um painel.

[Explorar servidores MCP](mcp-servers.md)

>[!TAB Habilidades do agente]

As Habilidades do agente são a experiência de domínio da Adobe, codificadas como instruções que seu agente pode seguir. Em vez de esperar que seu agente descubra os passos certos, uma habilidade diz a ele exatamente o que fazer. Confiável, repetível e já ajustado para workflows do Adobe.

**Usar Habilidades do Agente quando:**

- Você deseja que a mesma tarefa seja feita da mesma maneira todas as vezes
- Você está executando conteúdo repetível ou fluxos de trabalho de produção de mídia
- Você quer um agente que conheça a Adobe sem que você precise explicá-la

**Experimente:** Edite em lote um conjunto de fotos para parecer coeso. Gere variantes sociais prontas para plataforma a partir de um ativo de origem. Crie a partir de um modelo do Adobe Express em alguns prompts.

[Explorar habilidades do agente](agent-skills.md)

>[!TAB APIs para Construtores]

As APIs são os blocos fundamentais. Eles fornecem aos desenvolvedores acesso direto e programático aos dados e operações do Adobe, usando as mesmas APIs que alimentam os próprios produtos da Adobe. Use-as para criar algo que seja executado em seu cronograma, seus termos, sua pilha.

**Usar APIs quando:**

- Você está criando um aplicativo ou painel personalizado
- É necessário integrar os dados do Adobe em outro sistema
- Você está usando o código Claude ou o cursor para gerar um aplicativo completo
- Você precisa de controle total de criação, atualização ou exclusão

**Experimente:** Crie um painel de campanha personalizado. Automatizar um pipeline de dados. Gere um aplicativo com Claude Code que lê e grava no Adobe Experience Platform.

[Explorar APIs para construtores](apis.md)

>[!ENDTABS]

## Usá-los juntos

Servidores MCP, habilidades do agente e APIs são complementares. Muitos workflows combinam os três:

- Uma habilidade do agente define o fluxo de trabalho e orienta o agente
- Os servidores MCP fornecem ao agente acesso de leitura aos dados do Adobe no meio do fluxo de trabalho
- As APIs lidam com ações que exigem gravações diretas do sistema ou lógica personalizada do aplicativo
