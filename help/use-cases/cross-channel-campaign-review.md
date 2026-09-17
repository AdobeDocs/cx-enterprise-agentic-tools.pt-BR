---
title: Executar uma revisão de campanha entre canais
description: Obtenha uma visualização unificada da integridade da campanha do AJO, CJA e Real-Time CDP em jornadas, públicos-alvo e desempenho em uma única sessão de IA.
last-substantial-update: 2026-09-16
source-git-commit: a70eede6e0efe0d1dbdc00c5d9de5aeb3b5d75de
workflow-type: tm+mt
source-wordcount: '1564'
ht-degree: 6%
---

# Executar uma revisão de campanha entre canais

<!-- last-modified: 2026-05-21 -->

![Executar uma Análise de Campanha entre Canais](https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review){zoomable="yes"}

*Selecione para aplicar zoom.*

Uma imagem completa da integridade da campanha requer dados de vários sistemas: jornadas ativas do AJO, status de ativação de público-alvo do Real-Time CDP e métricas de desempenho do CJA. Esta apresentação mostra como reunir os três em uma única sessão de IA, para que você possa mudar do status da jornada para a integridade do público-alvo para as tendências de desempenho em uma conversa em vez de três ferramentas separadas.

| Detalhes do cenário | |
| --- | --- |
| Aplicativos corporativos CX | [Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home), [Customer Journey Analytics](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-overview/cja-overview), [Real-Time CDP](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/home) |
| Ferramentas agênticas | [CX Enterprise Coworker](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-coworker/content/home) ou [Adobe Journey Optimizer](../tools/mcp-servers.md), [Customer Journey Analytics](../tools/mcp-servers.md) e [Real-Time CDP](../tools/mcp-servers.md) Servidores MCP |
| Público-alvo | Gerentes de campanha, operações de marketing |
| Pré-requisito | Cliente de IA compatível com MCP, acesso ao AJO, CJA e Real-Time CDP |

Cada etapa mostra um prompt representativo e um exemplo de resposta de IA. Segue-se uma seção **Mais que você pode realizar** para exploração adicional na mesma sessão.

## Antes de começar

>[!BEGINTABS]

>[!TAB CX Enterprise Coworker]

O CX Enterprise Coworker se conecta ao AJO, CJA e Real-Time CDP em um só local, sem a necessidade de configuração do servidor ou do cliente de IA. [Experimente o CX Enterprise Coworker](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-coworker/content/home)

Se você preferir conectar seu próprio cliente de IA diretamente, conecte todos os três servidores MCP usando as guias abaixo. O Real-Time CDP MCP Server está em versão beta pública e requer que sua organização seja reconhecida.

>[!TAB Claude.ai]

Conecte todos os três servidores MCP como conectores personalizados. Adicione cada um separadamente.

1. Vá para **Configurações > Integrações** em Claude.ai.
2. Selecione **Adicionar conector personalizado**, insira uma URL de servidor e selecione **Conectar**.
3. Faça logon com sua Adobe ID e repita o procedimento para os servidores restantes.

| Servidor | Endpoint |
| --- | --- |
| Adobe Journey Optimizer MCP Server | `https://ajo-mcp.adobe.io/mcp` |
| Customer Journey Analytics MCP Server | `https://cja-mcp.adobe.io/mcp` |
| Real-Time CDP MCP Server | `https://rtcdp-mcp.adobe.io/mcp` |

Configuração completa: [documentação dos Conectores personalizados do Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB GPTchat]

Conecte todos os três servidores MCP usando o modo de desenvolvedor ChatGPT (plano Pro, Plus, Business, Enterprise ou Education necessário). Adicione cada servidor separadamente.

1. Habilite o **Modo de Desenvolvedor** em **Configurações de ChatGPT**.
2. Vá para **Configurações > Integrações** e selecione **Adicionar conector personalizado > Servidor MCP remoto**.
3. Insira uma URL de servidor, selecione **Conectar** e entre com sua Adobe ID.
4. Repita o procedimento para os servidores restantes.

| Servidor | Endpoint |
| --- | --- |
| Adobe Journey Optimizer MCP Server | `https://ajo-mcp.adobe.io/mcp` |
| Customer Journey Analytics MCP Server | `https://cja-mcp.adobe.io/mcp` |
| Real-Time CDP MCP Server | `https://rtcdp-mcp.adobe.io/mcp` |

Configuração completa: [Documentação de MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Outros clientes de IA]

Usando Gemini, Microsoft Copilot, Cursor, Claude Code ou outro ambiente compatível com MCP? Conecte-se aos três servidores MCP usando estes endpoints:

| Servidor | Endpoint |
| --- | --- |
| Adobe Journey Optimizer MCP Server | `https://ajo-mcp.adobe.io/mcp` |
| Customer Journey Analytics MCP Server | `https://cja-mcp.adobe.io/mcp` |
| Real-Time CDP MCP Server | `https://rtcdp-mcp.adobe.io/mcp` |

Instruções completas de instalação para todos os clientes com suporte: [Conecte-se ao cliente de IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Faça logon com a Adobe ID quando solicitado e selecione a organização IMS vinculada aos ambientes da AJO, CJA e Real-Time CDP. Escolher a organização errada é a fonte mais comum de erros de autenticação.
>
>Na primeira conexão, o cliente de IA pode solicitar que você selecione uma organização IMS ou especifique uma sandbox. Depois que o contexto é definido, o servidor MCP o utiliza para o restante da sessão.
>
>Algumas ferramentas solicitam sua aprovação antes de serem executadas. Revise a solicitação e aprove ou recuse. Nenhuma ação é executada sem a sua confirmação.

## Etapa 1: revisar jornadas e campanhas ativas

Comece com o AJO para estabelecer o que está em execução no momento. Saber quais jornadas estão ativas e foram modificadas recentemente fornece a base para o restante da revisão.

```
What journeys are currently active in AJO?
```

+++Ver um exemplo de resposta

Foram encontradas 8 jornadas ativas em sua organização da AJO:

| Jornada | Canal(s) | Última modificação |
| --- | --- | --- |
| Série de Boas-vindas: Novos Membros | Email, Push | 18 de maio de 2026 |
| Acompanhamento Pós-Compra | Email, SMS | 14 de maio de 2026 |
| Reengajamento de fidelidade | Email | 20 de maio de 2026 |
| Carrinho abandonado: 24 horas | Email, SMS | 10 de maio de 2026 |
| Promoção da primavera | Email, Push | 19 de maio de 2026 |
| Win-Back: 90 Dias Inativos | Email | 28 de abril de 2026 |
| Recompensa de Aniversário | Email | 15 de abril de 2026 |
| Reengajamento: Recusa por push | SMS | 12 de maio de 2026 |

3 jornadas foram modificadas nos últimos 7 dias. Você quer detalhes sobre qualquer um desses?

+++


## Etapa 2: verificar o status de ativação do público

Com as jornadas em exibição, verifique se os públicos-alvo que alimentam essas campanhas estão fluindo corretamente para os destinos.

```
Show me the activation status for the high-value loyalty segment.
```

+++Ver um exemplo de resposta

**Segmento de Fidelidade de Alto Valor**: status de ativação entre destinos:

| Destino | Status | Última execução bem-sucedida | Tamanho do público-alvo |
| --- | --- | --- | --- |
| Google Ads | Ativo | 21 de maio de 2026 02:14 AM | 48,320 |
| Anúncios do Meta | Ativo | 21 de maio de 2026 01:58 AM | 48,295 |
| Salesforce Marketing Cloud | Ativo | 20 de maio de 2026, 23h30 | 47,940 |
| Adobe Target | Ativo | 21 de maio de 2026, 00:00 | 48,320 |

Nenhum erro de fluxo de dados detectado. Todas as ativações foram concluídas nas últimas 3 horas.

+++


## Etapa 3: Extrair métricas de desempenho do CJA

Com o contexto de jornada e público-alvo estabelecido, use o CJA para avaliar como essas campanhas estão se convertendo e onde o engajamento cai.

```
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
```

+++Ver um exemplo de resposta

**Campanha de reengajamento de fidelidade**: 21 de abril a 21 de maio de 2026:

| Canal | Envios | CTR | Conversões | Conv Taxa |
| --- | --- | --- | --- | --- |
| Email | 48,320 | 8.4% | 1,973 | 4.1% |
| Push | 31,200 | 12.1% | 987 | 3.2% |

Taxa de conversão combinada: 3,8%. O CTR de email está 1,2% acima do período anterior de 30 dias. As conversões por push são simples.

+++


## Etapa 4: sintetizar um resumo de integridade da campanha

Peça ao seu cliente de IA para reunir a imagem em todas as três fontes e destacar tudo o que precise de atenção.

```
Give me a summary of our campaign health: what is running, which audiences are activated, and how performance looks against last month.
```

+++Ver um exemplo de resposta

Este é o resumo atual da integridade da campanha no AJO, Real-Time CDP e CJA:

**jornadas ativas:** 8 ao vivo, 3 modificadas esta semana. A jornada de reengajamento de fidelidade é a atualizada mais recentemente.

**Ativação de público-alvo:** Todos os segmentos fluem corretamente para 4 destinos. Nenhum erro de fluxo de dados detectado.

**Desempenho:** a CTR de email está ativa em campanhas de fidelidade. A conversão de push é simples. Nenhum canal está em declínio significativo.

**Sinalizadores para atenção:**

- A jornada Win-Back (90 dias inativa) foi modificada pela última vez há 23 dias e não foi revisada recentemente.
- A taxa de conversão por push permaneceu inalterada por 3 períodos consecutivos, valendo a pena revisar as mensagens ou o tempo.

Nenhum problema crítico detectado. Dois itens acima garantem revisão antes do próximo lançamento da campanha.

+++


É nesse ponto que a abordagem de vários servidores compensa: os motivos de seu cliente de IA abrangem a configuração da jornada, o status do público-alvo e os dados de desempenho em uma única conversa.

## Etapa 5: executar ação sobre o que você encontrou

A revisão trouxe à tona dois itens. Peça ao cliente de IA para ajudá-lo a priorizar e direcionar cada um.

```
For each flag you identified, what should I do and where should I go to do it?
```

+++Ver um exemplo de resposta

Este é um plano de ação priorizado para os dois sinalizadores:

**1. Jornada Win-Back — examine as condições de reentrada (AJO MCP e, em seguida, o aplicativo AJO, se necessário)**

A jornada do Win-Back não foi modificada em 23 dias. Peça-me para percorrer suas condições de reentrada atuais e a lógica de saída. Se as condições parecerem obsoletas ou incorretas, as alterações estruturais no fluxo de jornada exigirão a abertura do AJO. As atualizações de limite de frequência e público-alvo podem ser feitas aqui.

**2. Forçar conversão simples por 3 períodos — atualizar mensagens ou testar uma variante**

A conversão simples geralmente sinaliza fadiga da mensagem ou uma incompatibilidade entre a oferta e o público-alvo. Dois caminhos:

- **Atualizar conteúdo de push agora (AEM MCP):** Se as notificações de push estiverem vinculadas a uma página de aterrissagem, adicione o Servidor MCP de Conteúdo do AEM e atualize a cópia da página ou o CTA sem alternar as ferramentas.
- **Execute um teste A/B por push (aplicativo AJO):** Crie uma variante no nível da campanha com mensagens diferentes para isolar se ela é conteúdo ou direcionamento. Isso requer ir diretamente para o AJO.

Com o que você gostaria de começar?

+++


## O que você realizou

Você executou uma revisão de integridade da campanha entre canais conectando o AJO, o Real-Time CDP e o CJA a uma única sessão de IA. Em vez de abrir três aplicativos e montar uma imagem manualmente, você percorreu o status da jornada, a ativação do público-alvo e os dados de desempenho em uma conversa. O resumo sintetizado fornece aos gerentes de campanha um caminho mais rápido para identificar o que está funcionando, o que precisa de ajuste e onde se concentrar em seguida.

## Mais você pode realizar

Com o AJO, o CJA e o Real-Time CDP conectados na mesma sessão, você pode ir muito além da apresentação. Expanda um cenário abaixo para ver os prompts que você pode tentar.

+++Saiba exatamente o que está sendo executado antes de iniciar algo novo

A sobreposição de jornadas, campanhas modificadas recentemente e canais que você não analisou pode afetar um novo lançamento. Esses prompts fornecem uma imagem clara do estado atual antes de você adicionar algo.

**Solicitações**

```
Which journey has the most active profiles right now?
```

```
Show me all journeys modified in the last 7 days.
```

```
Which campaigns are scheduled to end this week?
```

```
Are any journeys targeting the same segment as the campaign I'm about to launch?
```

+++

+++Verifique se os públicos-alvo estão atingindo os destinos certos

Problemas de ativação são silenciosos — um segmento para de fluir e sua campanha envia para uma lista menor sem nenhum aviso. Esses prompts exibem lacunas e erros antes de afetarem os resultados.

**Solicitações**

```
Which audiences have grown the most in the last 30 days?
```

```
Are there any dataflow errors across my active destinations?
```

```
How many records were exported to each destination in the last 7 days?
```

```
Are there any audiences with no active destinations?
```

+++

+++Entenda o que está funcionando e onde se concentrar em seguida

As tendências de desempenho em todos os canais informam onde investir e o que obter. Esses prompts ajudam a identificar o que está impulsionando os resultados e para onde a atenção do próximo trimestre deve ir.

**Solicitações**

```
Show me email performance trends for the last 90 days.
```

```
Which campaigns are underperforming against their conversion targets?
```

```
What is the average revenue per conversion this month compared to last month?
```

```
Which channel has the highest conversion rate across all active campaigns?
```

+++


## Informações adicionais

| Recurso | O que você encontrará |
| --- | --- |
| [Documentação do AJO](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home){target="_blank"} | Documentação completa do aplicativo do AJO |
| [Servidor MCP do AJO no Registro de IA](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server){target="_blank"} | Disponibilidade e ferramentas do AJO MCP Server |
| [Servidor MCP do CJA no Registro de IA](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp){target="_blank"} | Disponibilidade e ferramentas do CJA MCP Server |
