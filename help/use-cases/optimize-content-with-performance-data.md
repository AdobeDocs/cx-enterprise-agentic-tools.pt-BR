---
title: Otimizar o conteúdo com base nos dados de desempenho
description: Use servidores MCP CJA e AEM juntos para identificar conteúdo com baixo desempenho e atualizá-lo — sem alternar entre ferramentas.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 3%

---


# Otimizar o conteúdo com base nos dados de desempenho

<!-- last-modified: 2026-05-21 -->

![Otimizar conteúdo com base nos dados de desempenho](https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data)

Fechar o loop entre os dados de desempenho do conteúdo e as atualizações de conteúdo normalmente significa alternar entre o Analytics e o CMS. Esta apresentação mostra como conectar o Customer Journey Analytics e o AEM na mesma sessão de IA, para que você possa exibir páginas com baixo desempenho e atualizá-las sem sair da conversa.

| | |
| --- | --- |
| Aplicativos corporativos CX | Customer Journey Analytics, Adobe Experience Manager as a Cloud Service |
| Ferramentas de agilidade | Gateway CX Enterprise MCP, servidor AEM Content MCP |
| Público-alvo | Gerentes de campanha, estrategistas de conteúdo, operações de marketing |
| Pré-requisito | Cliente de IA compatível com MCP, acesso CJA, acesso AEM as a Cloud Service |

Cada etapa mostra um prompt representativo e um exemplo de resposta de IA. Segue-se uma seção **Mais que você pode realizar** para exploração adicional na mesma sessão.

## Antes de começar

>[!BEGINTABS]

>[!TAB Claude.ai]

Conecte ambos os servidores MCP como conectores personalizados. Adicione cada um separadamente.

1. Vá para **Configurações > Integrações** em Claude.ai.
2. Selecione **Adicionar conector personalizado**, insira uma URL de servidor e selecione **Conectar**.
3. Faça logon com a Adobe ID e repita para o segundo servidor.

| Servidor | Endpoint |
| --- | --- |
| Gateway CX Enterprise MCP | `https://cx-enterprise.adobe.io/mcp` |
| Servidor MCP de conteúdo do AEM | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Configuração completa: [documentação dos Conectores personalizados do Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB GPTchat]

Conecte ambos os servidores MCP usando o modo de desenvolvedor ChatGPT (plano Pro, Plus, Business, Enterprise ou Education necessário). Adicione cada servidor separadamente.

1. Habilite o **Modo de Desenvolvedor** em **Configurações de ChatGPT**.
2. Vá para **Configurações > Integrações** e selecione **Adicionar conector personalizado > Servidor MCP remoto**.
3. Insira uma URL de servidor, selecione **Conectar** e entre com sua Adobe ID.
4. Repita o procedimento para o segundo servidor.

| Servidor | Endpoint |
| --- | --- |
| Gateway CX Enterprise MCP | `https://cx-enterprise.adobe.io/mcp` |
| Servidor MCP de conteúdo do AEM | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Configuração completa: [Documentação de MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Outros clientes de IA]

Usando Gemini, Microsoft Copilot, Cursor, Claude Code ou outro ambiente compatível com MCP? Conecte-se a ambos os servidores MCP usando estes pontos finais:

| Servidor | Endpoint |
| --- | --- |
| Gateway CX Enterprise MCP | `https://cx-enterprise.adobe.io/mcp` |
| Servidor MCP de conteúdo do AEM | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Instruções completas de instalação para todos os clientes com suporte: [Conecte-se ao cliente de IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Faça logon com sua Adobe ID quando solicitado e selecione a organização IMS vinculada aos seus ambientes do CJA e do AEM. Escolher a organização errada é a fonte mais comum de erros de autenticação.
>
>Na primeira conexão, o cliente de IA pode solicitar que você selecione uma organização IMS ou especifique uma sandbox. Depois que o contexto é definido, o servidor MCP o utiliza para o restante da sessão.
>
>Algumas ferramentas solicitam sua aprovação antes de serem executadas. Revise a solicitação e aprove ou recuse — nenhuma ação é executada sem sua confirmação.

## Etapa 1: identificar conteúdo com baixo desempenho

Use o gateway do CX Enterprise MCP para classificar páginas por envolvimento e métricas de conversão no Customer Journey Analytics. A meta é obter uma lista clara e priorizada de conteúdo que precise de atenção.

```
Show me the 10 pages with the lowest engagement rate over the last 60 days.
```

+++Ver um exemplo de resposta

Páginas de engajamento mais baixas (22 de março a 21 de maio de 2026):

| Classificação | Página | Taxa de participação | Taxa de rejeição | Média tempo na página |
| --- | --- | --- | --- | --- |
| 1 | /en/products/analytics | 8.2% | 74% | 0:42 |
| 2 | /en/resources/whitepapers | 9.1% | 71% | 0:38 |
| 3 | /pt-BR/solutions/retail | 10.4% | 69% | 0:51 |
| 4 | /en/blog/2025-q4-recap | 11.0% | 68% | 0:44 |
| 5-10 | ... | 12,3-14,1 % | 63-67% | 0:35-1:10 |

A taxa média de engajamento do site é de 34,7%. Essas páginas estão 2 a 4 vezes abaixo da média.

+++

## Etapa 2: revisar o conteúdo no AEM

Sem sair da sessão de IA, obtenha o estado atual dessas páginas do AEM. Entender o que o conteúdo diz é o primeiro passo para saber o que mudar.

```
Show me the current content on the /en/products/analytics page in AEM.
```

+++Ver um exemplo de resposta

**Página:** `/en/products/analytics`
**Última modificação:** 30 de abril de 2026 por T. MacMillan
**Status:** Publicado

**Seção Hero:**
Título: &quot;Decisões orientadas por dados para cada equipe&quot;
Subtítulo: &quot;A Adobe Analytics fornece à sua organização os insights para agir.&quot;
CTA: &quot;Solicitar uma demonstração&quot; → /contact/demo

**Corpo:** 3 blocos de recursos seguidos por uma faixa de logotipo do cliente e um CTA secundário. Nenhum vídeo ou elemento interativo. A página não é atualizada há 21 dias.

**Descrição do Meta:** &quot;Adobe Analytics: relatórios em tempo real e insights de IA para equipes corporativas&quot;.

+++

## Etapa 3: Fazer atualizações direcionadas

Com os dados de desempenho e o conteúdo atual em vista, faça atualizações baseadas no que os dados revelaram.

```
Update the hero headline on the analytics product page to Make faster decisions with AI-powered analytics.
```

+++Ver um exemplo de resposta

**Alteração proposta:**

| Campo | Valor atual | Novo valor |
| --- | --- | --- |
| Título do herói | Decisões orientadas por dados para cada equipe | Tome decisões mais rápidas com análises alimentadas por IA |

Página: `/en/products/analytics`

Confirmar esta alteração? Responder &quot;sim&quot; gravará a atualização na AEM. A página permanecerá publicada em seu estado atual até que você publique novamente de forma explícita.

+++

>[!CAUTION]
>
>Confirme cada alteração de conteúdo quando solicitado. Revise o diferencial completo antes de aprovar atualizações para páginas ativas.

## Etapa 4: validar e publicar

Feche o loop confirmando todas as alterações e promovendo o conteúdo quando estiver satisfeito com as atualizações.

```
Show me a summary of all changes made in this session.
```

+++Ver um exemplo de resposta

**Resumo da sessão — 21 de maio de 2026:**

| Página | Alteração | Status |
| --- | --- | --- |
| /en/products/analytics | Título do herói atualizado | Salvo, não publicado |

1 página atualizada. Pronto para publicar quando confirmado.

**Restantes da sua lista de pouco engajamento:** 9 páginas não foram atualizadas nesta sessão. Deseja continuar com a próxima página ou criar uma inicialização para revisão em lote antes de publicar?

+++

## O que você realizou

Você conectou o Customer Journey Analytics e o AEM em uma única sessão de IA e usou dados de desempenho para informar diretamente as alterações de conteúdo. Ao mudar da métrica para a atualização sem alternar ferramentas, você encurtou o loop de comentários entre o Analytics insight e o conteúdo publicado. Isso é mais importante na escala da campanha, onde dezenas de páginas podem precisar de atenção e os fluxos de trabalho manuais entre ferramentas criam atrasos.

## Mais você pode realizar

Juntos, os servidores MCP da CJA e da AEM oferecem suporte ao ciclo completo, desde a identificação de problemas até as correções de envio. Expanda um cenário abaixo para ver os prompts que você pode tentar na mesma sessão.

+++Encontre o conteúdo que está atrasando seu desempenho

O alto tráfego com baixo engajamento sinaliza um problema de conteúdo, não de tráfego. Esses prompts ajudam a exibir as páginas e os padrões específicos que precisam de atenção antes que o prazo de uma campanha force o problema.

**Solicitações**

```
Show me the 10 pages with the lowest conversion rate this quarter.
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for blog posts versus product pages.
```

```
Find AEM pages that haven't been updated in over 60 days.
```

+++

+++Corrija o que os dados estão informando que você deve corrigir

Depois de saber o que está com baixo desempenho, a próxima etapa é fazer alterações direcionadas. Esses prompts permitem atualizar títulos, CTAs e metadescrições com base nos dados de desempenho revelados.

**Solicitações**

```
Update the CTA on the /en/solutions/retail page to 'See how it works'.
```

```
Add a note to the hero subheadline on the analytics page: Now with AI-powered anomaly detection.
```

```
Update the meta description on all pages in /en/products/ that contain the word 'legacy'.
```

```
Which pages updated in this session still need their CTAs reviewed?
```

+++

+++Melhorias na remessa antes da próxima campanha

As alterações feitas no meio da sessão podem se acumular rapidamente. Esses prompts ajudam a revisar o que está pronto, agrupar atualizações em um lançamento revisável e promover de forma limpa antes que uma campanha entre em vigor.

**Solicitações**

```
Show me all pages updated in this session that are still unpublished.
```

```
Create a launch with all changes from this session for review before publishing.
```

```
Give me a summary of all changes made in this session.
```

```
Promote everything in the current launch to production.
```

+++

## Informações adicionais

| Recurso | O que você encontrará |
| --- | --- |
| [Documentação de MCP do Analytics](https://developer.adobe.com/analytics-mcp/docs/) | Referência da ferramenta e configuração do CJA MCP |
| [Documentação do AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service) | Documentação completa do AEM |
| [Servidor MCP do CJA no Registro de IA](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | Disponibilidade e ferramentas do CJA MCP Server |
| [Servidor MCP de Conteúdo do AEM no Registro de IA](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | Ferramentas e disponibilidade do AEM Content MCP Server |
| [Servidores MCP](../tools/mcp-servers.md) | Conectar um cliente de IA a servidores MCP do Adobe |
