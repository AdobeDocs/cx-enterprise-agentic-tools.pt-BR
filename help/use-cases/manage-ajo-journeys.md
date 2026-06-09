---
title: Identifique problemas de jornada antes que afetem os clientes
description: Use o CX Enterprise MCP para monitorar jornadas ativas do AJO, revisar a configuração da campanha e exibir problemas operacionais antes que eles atinjam seu público-alvo.
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: 6a2b8b54eb9fe040f5f9defa9e6681e46a5e65cf
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 2%

---


# Identifique problemas de jornada antes que afetem os clientes
<!-- last-modified: 2026-06-08 -->

![Cliente de IA que resume a campanha e a estratégia de jornada com um resumo executivo](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png)

Obter uma visão clara de quais jornadas estão ativas, quais condições as impulsionam e como as campanhas são configuradas normalmente significa abrir o Adobe Journey Optimizer e navegar em sua interface. Esta apresentação mostra como obter a mesma visibilidade por meio de um cliente de IA, usando o CX Enterprise MCP para consultar dados de jornada e campanha do AJO por meio de perguntas em linguagem simples.

| Detalhes do cenário | |
| --- | --- |
| Aplicativos corporativos CX | [Adobe Journey Optimizer (AJO)](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home) |
| Ferramentas de agilidade | [CX Enterprise MCP](../tools/mcp-servers.md#cx-enterprise-mcp-servers) |
| Público-alvo | Gerentes de campanha, profissionais de marketing |
| Pré-requisito | Cliente de IA compatível com MCP, acesso ao AJO |

Cada etapa mostra um prompt representativo e um exemplo de resposta de IA. Segue-se uma seção **Mais que você pode realizar** para exploração adicional na mesma sessão.


## Antes de começar

>[!BEGINTABS]

>[!TAB Claude.ai]

Conecte o CX Enterprise MCP como um conector personalizado para acessar as ferramentas do Adobe Journey Optimizer.

1. Vá para **Configurações > Integrações** em Claude.ai.
2. Selecione **Adicionar conector personalizado** e insira a URL do servidor: `https://cx-enterprise.adobe.io/mcp`
3. Selecione **Conectar** e entre com sua Adobe ID.

Configuração completa: [documentação dos Conectores personalizados do Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB GPTchat]

Conecte o CX Enterprise MCP usando o modo de desenvolvedor ChatGPT (plano Pro, Plus, Business, Enterprise ou Education necessário).

1. Habilite o **Modo de Desenvolvedor** em **Configurações de ChatGPT**.
2. Vá para **Configurações > Integrações** e selecione **Adicionar conector personalizado > Servidor MCP remoto**.
3. Digite a URL do servidor: `https://cx-enterprise.adobe.io/mcp`
4. Selecione **Conectar** e entre com sua Adobe ID.

Configuração completa: [Documentação de MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Outros clientes de IA]

Usando Gemini, Microsoft Copilot, Cursor, Claude Code ou outro ambiente compatível com MCP? Conecte-se ao CX Enterprise MCP usando este endpoint:

```
https://cx-enterprise.adobe.io/mcp
```

Instruções completas de instalação para todos os clientes com suporte: [Conecte-se ao cliente de IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Faça logon com sua Adobe ID quando solicitado e selecione a organização IMS vinculada ao seu ambiente AJO. Escolher a organização errada é a fonte mais comum de erros de autenticação.
>
>Na primeira conexão, o cliente de IA pode solicitar que você selecione uma organização IMS ou especifique uma sandbox. Depois que o contexto é definido, o servidor MCP o utiliza para o restante da sessão.
>
>Algumas ferramentas solicitam sua aprovação antes de serem executadas. Revise a solicitação e aprove ou recuse. Nenhuma ação é executada sem a sua confirmação.


## Etapa 1: Descubra jornadas ativas e sua finalidade

Comece solicitando um inventário das jornadas ativas e os objetivos de negócios por trás delas. Isso dá a você o quadro completo antes de mergulhar em qualquer jornada específica.

```
What customer journeys are currently available and what business objectives do they support?
```

+++Ver um exemplo de resposta

![Lista de clientes de IA disponíveis para jornadas e seus objetivos comerciais](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step1.gif)

+++



## Etapa 2: analisar as etapas de uma jornada e a experiência do cliente

Com a lista de jornadas na exibição, peça ao cliente de IA para percorrer as etapas de uma jornada específica e explicar o que o cliente experimenta em cada estágio.

```
Walk me through the [journey name] journey and explain the customer experience.
```

+++Ver um exemplo de resposta

![Cliente de IA apresentando as etapas de jornada e a experiência do cliente Bem-vindo(a)](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step2-welcome-journey.png)

+++


>[!NOTE]
>
>Substitua `[journey name]` com o nome de uma jornada dos resultados da etapa 1.


## Etapa 3: revisar campanhas, públicos e objetivos

Mudança de jornadas para campanhas. Solicite um resumo de quais campanhas estão ativas, quem elas direcionam e quais resultados elas foram projetadas para impulsionar.

```
Show me our campaigns, the audiences they target, and the outcomes they're designed to drive.
```

+++Ver um exemplo de resposta

![Campanhas ativas da lista de clientes de IA com seu direcionamento de público-alvo e resultados pretendidos](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step3.gif)

+++



## Etapa 4: entender como as campanhas e o jornada se conectam

Peça ao cliente de IA para conectar os pontos entre campanhas e jornadas e explicar como elas trabalham juntas em direção a metas de engajamento compartilhado.

```
How do our campaigns and journeys work together to improve customer engagement?
```

+++Ver um exemplo de resposta

![Cliente de IA explicando a relação entre campanhas e jornadas](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step4-connection.png)

+++



## Etapa 5: Obtenha recomendações priorizadas

Peça recomendações priorizadas sobre no que focar a seguir, enquadradas pela perspectiva de um gerenciador de marketing do ciclo de vida. Isso revela as lacunas e oportunidades mais impactantes de tudo o que foi revisado na sessão.

```
If you were our lifecycle marketing manager, what would you prioritize next and why?
```

+++Ver um exemplo de resposta

![Cliente de IA dando recomendações de marketing de ciclo de vida priorizadas](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5.gif)

+++


>[!NOTE]
>
>O AJO MCP Server exibe informações de jornada e campanha, mas não pode modificar jornadas, campanhas ou conteúdo. Para implementar as recomendações, acesse o aplicativo do AJO diretamente ou conecte o AEM Content MCP Server para alterações de conteúdo na mesma sessão.


## O que você realizou

Você conectou um cliente de IA à Adobe Journey Optimizer e criou uma imagem completa do seu portfólio do jornada e da campanha por meio de cinco prompts. Você inventariou jornadas ativas e seus objetivos de negócios, revisou a experiência passo a passo do cliente para uma jornada específica, mapeou campanhas ativas para seus públicos e resultados pretendidos, entendeu como campanhas e jornadas funcionam juntas e recebeu recomendações priorizadas sobre onde se concentrar em seguida. Isso proporciona visibilidade estratégica ao marketing de ciclo de vida e aos gerentes de campanha sem precisar abrir a interface do AJO.


## Mais você pode realizar

O CX Enterprise MCP pode exibir uma grande variedade de jornadas e detalhes de campanhas do AJO. Expanda um cenário abaixo para ver os prompts que você pode tentar na mesma sessão.

+++Saiba o que há de novo antes de fazer uma mudança

Fazer alterações em uma jornada sem saber o que mais está sendo executado é arriscado. Esses prompts fornecem um inventário atual do que está ativo, o que foi modificado recentemente e como as campanhas são configuradas.

**Solicitações**

```
Show me all journeys modified in the last 7 days.
```

```
Show me all journeys that use SMS as a channel.
```

```
Which campaigns are scheduled to end this week?
```

```
What loyalty challenges are currently active?
```

+++

+++Acessar os detalhes de uma jornada específica

Quando você precisa revisar, aprovar ou entregar uma jornada, ter a lógica completa à sua frente sem abrir o AJO economiza tempo. Isso avisa as condições de superfície, as programações e as regras de segmento sob demanda.

**Solicitações**

```
What is the entry condition for the [journey name] journey?
```

```
What are the exit conditions and timeout rules for the [journey name] journey?
```

```
What messages and wait conditions are in the [journey name] journey?
```

```
Which segment does the [journey name] journey target?
```

+++

+++Acessar os detalhes de uma campanha específica

Quando é necessário revisar a configuração completa de uma campanha antes de aprovar, entregar ou fazer alterações, esses prompts exibem regras de público-alvo, configurações de canal e detalhes de agendamento sem abrir o AJO.

**Solicitações**

```
Walk me through the full configuration of the [campaign name] campaign.
```

```
What audience does the [campaign name] campaign target and how large is that segment?
```

```
What frequency cap and send schedule apply to the [campaign name] campaign?
```

```
Are any campaigns targeting overlapping audiences?
```

```
What channel configurations are set up in our AJO environment?
```

+++



## Informações adicionais

| Recurso | O que você encontrará |
| --- | --- |
| [Servidor MCP do AJO no Registro de IA](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server){target="_blank"} | Disponibilidade e ferramentas do AJO MCP Server |
| [Documentação do AJO](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home){target="_blank"} | Documentação completa do aplicativo do AJO |
