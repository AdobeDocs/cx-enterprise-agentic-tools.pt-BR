---
title: Entenda seus públicos-alvo e onde eles são ativados
description: Use o gateway do CX Enterprise MCP para monitorar o status de ativação do público-alvo, verificar a integridade do destino e exibir problemas antes que eles afetem suas campanhas.
index: false
source-git-commit: 14488b494c454ce6d1207e2d21024749d93db669
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 2%

---


# Entenda seus públicos-alvo e onde eles são ativados

<!-- last-modified: 2026-06-04 -->

![Consultar públicos-alvo com linguagem natural](https://placehold.co/1600x900?text=Query+Audiences)

Entender quais públicos-alvo são ativados, onde estão fluindo e se os destinos estão íntegros geralmente significa abrir o Real-Time CDP e navegar por várias telas. Esta apresentação mostra como obter as mesmas respostas por meio de um cliente de IA, usando o servidor MCP do RTCDP para exibir a configuração de destino, o status de ativação e a integridade do fluxo de dados por meio de perguntas em linguagem simples.

| | |
| --- | --- |
| Aplicativos corporativos CX | Real-Time Customer Data Platform (Real-Time CDP) |
| Ferramentas de agilidade | Gateway CX Enterprise MCP |
| Público-alvo | Profissionais de marketing, analistas, operadores |
| Pré-requisito | Cliente de IA compatível com MCP, acesso ao Real-Time CDP |

Cada etapa mostra um prompt representativo e um exemplo de resposta de IA. Segue-se uma seção **Mais que você pode realizar** para exploração adicional na mesma sessão.

## Antes de começar

>[!BEGINTABS]

>[!TAB Claude.ai]

Conecte o gateway do CX Enterprise MCP como um conector personalizado para acessar as ferramentas do Real-Time CDP.

1. Vá para **Configurações > Integrações** em Claude.ai.
2. Selecione **Adicionar conector personalizado** e insira a URL do servidor: `https://cx-enterprise.adobe.io/mcp`
3. Selecione **Conectar** e entre com sua Adobe ID.

Configuração completa: [documentação dos Conectores personalizados do Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB GPTchat]

Conecte o gateway do CX Enterprise MCP usando o modo de desenvolvedor ChatGPT (plano Pro, Plus, Business, Enterprise ou Education necessário).

1. Habilite o **Modo de Desenvolvedor** em **Configurações de ChatGPT**.
2. Vá para **Configurações > Integrações** e selecione **Adicionar conector personalizado > Servidor MCP remoto**.
3. Digite a URL do servidor: `https://cx-enterprise.adobe.io/mcp`
4. Selecione **Conectar** e entre com sua Adobe ID.

Configuração completa: [Documentação de MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Outros clientes de IA]

Usando Gemini, Microsoft Copilot, Cursor, Claude Code ou outro ambiente compatível com MCP? Conecte-se ao gateway do CX Enterprise MCP usando este endpoint:

```
https://cx-enterprise.adobe.io/mcp
```

Instruções completas de instalação para todos os clientes com suporte: [Conecte-se ao cliente de IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Faça logon com sua Adobe ID quando solicitado e selecione a organização IMS vinculada à sua instância do Real-Time CDP. Escolher a organização errada é a fonte mais comum de erros de autenticação.

## Etapa 1: Descubra seus públicos-alvo e o que eles representam

Comece solicitando um inventário dos públicos-alvo disponíveis e dos comportamentos dos clientes que eles capturam. Isso oferece o cenário completo antes de analisar qualquer segmento específico.

```
What audiences are currently available and what customer behaviors do they represent?
```

+++Ver um exemplo de resposta

![Listagem de clientes de IA disponíveis e os comportamentos dos clientes que eles representam](../assets/use-cases/query-audiences/query-audiences-step1-audience-list.png)

+++


## Etapa 2: identificar os segmentos mais valiosos

Com o público-alvo no modo de exibição, pergunte quais segmentos são maiores e o que os torna estrategicamente valiosos.

```
Which audiences are the largest and what makes them valuable?
```

+++Ver um exemplo de resposta

![Cliente de IA identificando os maiores públicos e explicando o que os torna valiosos](../assets/use-cases/query-audiences/query-audiences-step2.gif)

+++


## Etapa 3: revisar a ativação e os destinos

Pergunte para onde seus públicos-alvo estão fluindo e quais destinos eles estão ativados.

```
Where are our audiences currently being activated and to which destinations?
```

+++Ver um exemplo de resposta

![Cliente de IA mostrando o status de ativação de público-alvo e o mapeamento de destino](../assets/use-cases/query-audiences/query-audiences-step3.gif)

+++


## Etapa 4: obter recomendações estratégicas

As ferramentas RTCDP do gateway do CX Enterprise MCP são somente leitura — elas exibem o status de ativação, a integridade do destino e os dados de fluxo de dados, mas não modificam a configuração. Depois de identificar um problema, a correção acontece no aplicativo.

```
If you were our audience strategist, what would you prioritize next and why?
```

+++Ver um exemplo de resposta

![Cliente de IA dando recomendações de estratégia de público-alvo priorizado](../assets/use-cases/query-audiences/query-audiences-step4.gif)

+++


>[!NOTE]
>
>As ferramentas do RTCDP do gateway do CX Enterprise MCP exibem os dados de destino e de ativação, mas não podem modificar a configuração de destino, as definições de segmento ou as configurações de fluxo de dados. As etapas de correção ocorrem no aplicativo Real-Time CDP.

## O que você realizou

Você conectou um cliente de IA à Real-Time CDP e criou uma imagem estratégica do seu portfólio de público-alvo em quatro prompts. Você mapeou os públicos-alvo disponíveis para os comportamentos dos clientes que eles capturam, identificou os segmentos maiores e mais valiosos, confirmou para onde cada público-alvo está fluindo e para quais destinos e recebeu recomendações priorizadas na próxima ativação. Isso substitui a navegação em várias telas do Real-Time CDP por uma conversa direta e estratégica.

## Mais você pode realizar

As ferramentas do Real-Time CDP do gateway do CX Enterprise MCP oferecem suporte a uma ampla variedade de consultas de público-alvo e ativação. Expanda um cenário abaixo para ver os prompts que você pode tentar na mesma sessão.

+++Saber exatamente o que está fluindo para onde antes de uma campanha enviar

As falhas de ativação são silenciosas. Os públicos param de fluir sem aviso e as campanhas são enviadas para listas desatualizadas. Esses prompts fornecem uma imagem clara de quais segmentos estão atingindo quais destinos e quando.

**Solicitações**

```
Which audiences are activated to Google Ads?
```

```
Show me the activation history for the [audience name] audience.
```

```
What is the last refresh time for the [audience name] audience?
```

+++

+++Problemas de ativação de captura antes que afetem uma campanha

Um destino que perdeu uma execução ou um segmento sem um destino ativo significa que sua campanha pode estar atingindo menos pessoas do que o esperado. Esses prompts destacam essas lacunas de forma proativa.

**Solicitações**

```
Are there any audiences with no active destinations?
```

```
Are any destination dataflows showing errors right now?
```

```
Which audiences have not been updated in the last 30 days?
```

+++

+++Auditoria e compreensão do cenário de público-alvo

Quando os tamanhos do público-alvo mudam ou novos segmentos são criados, ter um inventário claro ajuda a planejar e evitar a ativação da lista errada. Esses prompts fornecem essa visibilidade sob demanda.

**Solicitações**

```
How many profiles are in the [segment name] segment?
```

```
Show me all audiences created in the last 30 days.
```

```
Which audience has grown the most in the last 60 days?
```

```
How many total profiles are in my Real-Time CDP instance?
```

+++

+++Entender a identidade e a qualidade dos dados

Os namespaces de identidade e as políticas de mesclagem afetam diretamente quais perfis são incluídos em um público-alvo e como eles são resolvidos. Esses prompts exibem detalhes de configuração que podem explicar tamanhos inesperados de público-alvo ou sobreposições de perfil.

**Solicitações**

```
What identity namespaces are configured and which are most commonly used?
```

```
What merge policies are defined and which audiences use each one?
```

```
Are there any audiences using a non-default merge policy that could cause profile overlap?
```

+++


## Informações adicionais

| Recurso | O que você encontrará |
| --- | --- |
| [Documentação do Real-Time CDP MCP](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) | Referência da ferramenta e configuração do servidor MCP |
| [Registro do Adobe AI](https://developer.adobe.com/ai-registry/?type=mcp) | Metadados e disponibilidade do servidor MCP |
| [Documentação do Real-Time CDP](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/home) | Documentação completa do aplicativo do Real-Time CDP |
| [Documentação de destinos do AEP](https://experienceleague.adobe.com/pt-br/docs/experience-platform/destinations/home) | Referência completa de destinos |
