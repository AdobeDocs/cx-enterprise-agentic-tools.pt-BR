---
title: Entenda seus públicos-alvo e onde eles são ativados
description: Use o Real-Time CDP MCP Server para monitorar o status de ativação do público-alvo, verificar a integridade do destino e exibir problemas antes que eles afetem suas campanhas.
last-substantial-update: 2026-09-16
source-git-commit: a70eede6e0efe0d1dbdc00c5d9de5aeb3b5d75de
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 4%
---

# Entenda seus públicos-alvo e onde eles são ativados

<!-- last-modified: 2026-06-04 -->

![Cliente de IA que fornece uma estratégia de público-alvo priorizada com recomendações de ativação](../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png){zoomable="yes"}

*Selecione para aplicar zoom.*

Saber quais públicos-alvo estão ativos, onde eles estão fluindo e se os destinos estão íntegros é essencial antes do lançamento de uma campanha ou quando o desempenho é baixo. Esta apresentação mostra como obter uma imagem de ativação completa por meio de um cliente de IA, usando o servidor MCP do Real-Time CDP para exibir o status do público-alvo e a integridade do destino em segundos, sem abrir o Real-Time CDP.

>[!NOTE]
>
>O Real-Time CDP MCP Server está em versão beta pública e requer que sua organização seja reconhecida para acesso.

| Detalhes do cenário | |
| --- | --- |
| Aplicativos corporativos CX | [Real-Time Customer Data Platform (Real-Time CDP)](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/home) |
| Ferramentas agênticas | [CX Enterprise Coworker](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-coworker/content/home) ou [Real-Time CDP MCP Server](../tools/mcp-servers.md) |
| Público-alvo | Profissionais de marketing, analistas, operadores |
| Pré-requisito | Cliente de IA compatível com MCP, acesso ao Real-Time CDP |

Cada etapa mostra um prompt representativo e um exemplo de resposta de IA. Segue-se uma seção **Mais que você pode realizar** para exploração adicional na mesma sessão.

## Antes de começar

>[!BEGINTABS]

>[!TAB CX Enterprise Coworker]

A maneira mais rápida de obter essa imagem de ativação é o CX Enterprise Coworker, que não requer nenhuma configuração do servidor ou do cliente de IA. [Experimente o CX Enterprise Coworker](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-coworker/content/home)

Se você preferir conectar seu próprio cliente de IA diretamente ao Real-Time CDP, consulte as guias abaixo. O Real-Time CDP MCP Server está em versão beta pública e requer que sua organização seja reconhecida.

>[!TAB Claude.ai]

Conecte o Real-Time CDP MCP Server como um conector personalizado.

1. Vá para **Configurações > Integrações** em Claude.ai.
2. Selecione **Adicionar conector personalizado** e insira a URL do servidor: `https://rtcdp-mcp.adobe.io/mcp`
3. Selecione **Conectar** e entre com sua Adobe ID.

Configuração completa: [documentação dos Conectores personalizados do Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB GPTchat]

Conecte o Real-Time CDP MCP Server usando o modo de desenvolvedor ChatGPT (plano Pro, Plus, Business, Enterprise ou Education necessário).

1. Habilite o **Modo de Desenvolvedor** em **Configurações de ChatGPT**.
2. Vá para **Configurações > Integrações** e selecione **Adicionar conector personalizado > Servidor MCP remoto**.
3. Digite a URL do servidor: `https://rtcdp-mcp.adobe.io/mcp`
4. Selecione **Conectar** e entre com sua Adobe ID.

Configuração completa: [Documentação de MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Outros clientes de IA]

Usando Gemini, Microsoft Copilot, Cursor, Claude Code ou outro ambiente compatível com MCP? Conecte-se ao Servidor MCP do Real-Time CDP usando este endpoint:

```
https://rtcdp-mcp.adobe.io/mcp
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

![Listagem de clientes de IA disponíveis e os comportamentos dos clientes que eles representam](../assets/use-cases/query-audiences/query-audiences-step1-audience-list.png){zoomable="yes"}

*Selecione para aplicar zoom.*

+++


## Etapa 2: identificar os segmentos mais valiosos

Com o público-alvo no modo de exibição, pergunte quais segmentos são maiores e o que os torna estrategicamente valiosos.

```
Which audiences are the largest and what makes them valuable?
```

+++Ver um exemplo de resposta

![Cliente de IA identificando os maiores públicos e explicando o que os torna valiosos](../assets/use-cases/query-audiences/query-audiences-step2.gif){zoomable="yes"}

*Selecione para aplicar zoom.*

+++


## Etapa 3: revisar a ativação e os destinos

Pergunte para onde seus públicos-alvo estão fluindo e quais destinos eles estão ativados.

```
Where are our audiences currently being activated and to which destinations?
```

+++Ver um exemplo de resposta

![Cliente de IA mostrando o status de ativação de público-alvo e o mapeamento de destino](../assets/use-cases/query-audiences/query-audiences-step3.gif){zoomable="yes"}

*Selecione para aplicar zoom.*

+++


## Etapa 4: obter recomendações estratégicas

As ferramentas do Real-Time CDP MCP Server são somente leitura — elas exibem o status de ativação, a integridade de destino e os dados de fluxo de dados, mas não modificam a configuração. Depois de identificar um problema, a correção acontece no aplicativo.

```
If you were our audience strategist, what would you prioritize next and why?
```

+++Ver um exemplo de resposta

![Cliente de IA dando recomendações de estratégia de público-alvo priorizado](../assets/use-cases/query-audiences/query-audiences-step4.gif){zoomable="yes"}

*Selecione para aplicar zoom.*

+++


>[!NOTE]
>
>As ferramentas do Servidor MCP do Real-Time CDP exibem os dados de destino e de ativação, mas não podem modificar a configuração de destino, as definições de segmento ou as configurações de fluxo de dados. As etapas de correção ocorrem no aplicativo Real-Time CDP.

## O que você realizou

Você conectou um cliente de IA à Real-Time CDP e criou uma imagem estratégica do seu portfólio de público-alvo em quatro prompts. Você mapeou os públicos-alvo disponíveis para os comportamentos dos clientes que eles capturam, identificou os segmentos maiores e mais valiosos, confirmou para onde cada público-alvo está fluindo e para quais destinos e recebeu recomendações priorizadas na próxima ativação. Isso substitui a navegação em várias telas do Real-Time CDP por uma conversa direta e estratégica.

## Mais você pode realizar

O Real-Time CDP MCP Server é compatível com uma ampla variedade de consultas de público-alvo e ativação. Expanda um cenário abaixo para ver os prompts que você pode tentar na mesma sessão.

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
| [Registro do Adobe AI](https://developer.adobe.com/ai-registry/?type=mcp){target="_blank"} | Conectores gerenciados e detalhes do servidor para servidores Adobe MCP selecionados |
| [Documentação do Real-Time CDP](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/home){target="_blank"} | Documentação completa do aplicativo do Real-Time CDP |
