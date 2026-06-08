---
title: Servidores MCP
description: Conecte qualquer cliente de IA compatível com MCP aos workflows corporativos do Adobe CX usando os servidores do Protocolo de contexto de modelo.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 2%

---


# Servidores MCP

<!-- last-modified: 2026-05-19 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Os servidores MCP corporativos do Adobe CX fornecem a qualquer cliente de IA compatível acesso direto e controlado a dados e workflows da Adobe. Conecte-se uma vez e poderá consultar o desempenho da campanha, ativar públicos, revisar jornadas, gerenciar conteúdo e muito mais, tudo em linguagem simples, sem sair do ambiente de IA. Como os servidores MCP ficam entre o cliente de IA e os sistemas subjacentes da Adobe, você obtém flexibilidade de linguagem natural enquanto os controles de acesso e a governança de dados de sua organização permanecem em vigor.

Os servidores MCP da Adobe seguem o padrão aberto Protocolo de Contexto de Modelo. Qualquer cliente de IA compatível com MCP se conecta a qualquer servidor MCP do Adobe.

## Gateway CX Enterprise MCP

![O CX Enterprise MCP Gateway conecta seu cliente de IA a ferramentas MCP em todo o Adobe CX Enterprise Suite](../assets/mcp-gateway-hero.gif)

**Um ponto de extremidade. Cada servidor MCP Adobe CX Enterprise.**

O CX Enterprise Gateway roteia seu cliente de IA para ferramentas no Analytics, Campaigns, Content and Data — sem uma conexão separada para cada aplicativo. Conecte-se uma vez e o gateway mostre apenas as ferramentas para as quais sua organização está licenciada, com base nos direitos da Adobe.

>[!BEGINTABS]

>[!TAB Aplicativos da CX Enterprise]

As ferramentas de cada aplicativo estão disponíveis com base nas licenças da Adobe de sua organização.

| Aplicativo | O que você pode fazer |
| --- | --- |
| Adobe Journey Optimizer | [Revisar jornadas, campanhas e configurações de canal](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) |
| Customer Journey Analytics | [Relatórios de consulta, exibições de dados de descoberta, espaços de trabalho do autor](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) |
| Real-Time CDP | [Verificar destinos, status de ativação e integridade do fluxo de dados](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) (beta fechado) |

>[!TAB Conectar]

Use o endpoint do CX Enterprise Gateway onde quer que você use um endpoint de MCP específico do aplicativo.

```
https://cx-enterprise.adobe.io/mcp
```

>[!NOTE]
>Para o AEM, use o endpoint direto do AEM — O AEM não é roteado pelo gateway do CX Enterprise MCP.

Faça logon com a Adobe ID quando solicitado e selecione a organização IMS vinculada aos aplicativos da Adobe. Escolher a organização errada é a fonte mais comum de ferramentas ausentes ou erros de autenticação.

Para obter instruções completas de configuração, consulte [Conectar-se ao cliente de IA](#connect-to-your-ai-client) abaixo.

>[!ENDTABS]

## Servidores MCP corporativos Adobe CX

Os servidores listados abaixo se conectam diretamente e não são roteados pelo gateway do CX Enterprise MCP. Para obter acesso ao AJO, Customer Journey Analytics e Real-Time CDP, use o [CX Enterprise MCP Gateway](#cx-enterprise-mcp-gateway) acima.

<!--
CARDS

* #cx-enterprise-mcp-gateway
  {title = CX Enterprise MCP Gateway}
  {description = One connection to AJO, CJA, and Real-Time CDP tools. The gateway surfaces only the tools your organization is licensed for.}
  {cta = Connect}
  {image = ../assets/mcp-cxenterprise-card.png}

* https://developer.adobe.com/analytics-mcp/docs/aa/
  {title = Adobe Analytics}
  {description = Tools for report suite discovery, dimension and metric analysis, segment authoring, and workspace creation in Adobe Analytics.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-analytics-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content}
  {description = Tools for managing pages, content fragments, assets, and launches in Adobe Experience Manager as a Cloud Service using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content (Read-Only)}
  {description = Tools for discovering and querying pages, content fragments, and launches in AEM as a Cloud Service. No write access.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager
  {title = AEM Cloud Manager}
  {description = Tools for managing Cloud Manager programs, environments, pipelines, and repositories from your IDE using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

-->

### Endpoints do servidor MCP

| Servidor | Endpoint | Ferramentas |
| --- | --- | --- |
| [Gateway CX Enterprise MCP](#cx-enterprise-mcp-gateway) | `https://cx-enterprise.adobe.io/mcp` | · [Ferramentas do Adobe Journey Optimizer](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server)<br>· [Ferramentas do Customer Journey Analytics](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp)<br>· [Ferramentas do Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) |
| [Adobe Analytics](https://developer.adobe.com/analytics-mcp/docs/aa/) | `https://aa-mcp.adobe.io/mcp` | [Exibir ferramentas](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | [Exibir ferramentas](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [Conteúdo do AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | [Exibir ferramentas](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [Conteúdo Do AEM (Somente Leitura)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | [Exibir ferramentas](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |

## Conectar ao cliente de IA

Todos os servidores MCP do Adobe usam OAuth com o Adobe Identity Management Service (IMS). Selecione a organização IMS correta quando solicitado. Escolher o errado é a fonte mais comum de erros de autenticação.

Antes de configurar manualmente, verifique o [Registro do Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) para obter um conector gerenciado para o cliente de IA e o aplicativo Adobe. Os conectores gerenciados manipulam a autenticação automaticamente. Se um conector estiver disponível para seu cliente e aplicativo, use-o em vez das etapas manuais abaixo.

![Um agente de IA se conectando a um servidor MCP do Adobe](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB Claude.ai]

### ![Recomendado](../assets/badge-recommended.svg) Usar um conector gerenciado

Vá para o [Registro do Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) e pesquise seu aplicativo do Adobe. Se um conector Claude estiver listado (por exemplo, o [conector Adobe Experience Manager](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), siga as instruções de configuração em vez das etapas abaixo.

### Conectar usando um conector personalizado

O Claude.ai oferece suporte a servidores MCP remotos por meio dos Conectores personalizados nas configurações da conta.

1. Vá para **Configurações > Integrações**.
2. Clique em **Adicionar conector personalizado**.
3. Digite `https://cx-enterprise.adobe.io/mcp` como a URL e um nome para exibição, como `Adobe CX Enterprise`.
4. Clique em **Conectar** e entre com sua Adobe ID. Selecione a organização IMS correta.

Configuração completa: [documentação dos Conectores personalizados do Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Código Claude]

### Uso da CLI

Execute `claude mcp add` para registrar o Gateway CX Enterprise MCP. Uma conexão fornece acesso às ferramentas do AJO, CJA e Real-Time CDP com base nas licenças de sua organização.

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### Editar seu arquivo de configurações

Adicionar o servidor a `~/.claude.json` (global) ou `.mcp.json` na raiz do projeto (nível de projeto):

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Os servidores MCP do Adobe usam OAuth. O Claude Code solicita a autenticação com o Adobe ID na primeira vez que você chama uma ferramenta. Selecione a organização IMS correta quando solicitado.

Configuração completa: [documentação MCP do Claude Code](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Cursor]

Adicione o Gateway CX Enterprise MCP ao arquivo de configuração Cursor `mcp.json` e conecte-se por meio de **Configurações > MCP**.

- **Global (todos os projetos):** `~/.cursor/mcp.json`
- **Nível do projeto:** `.cursor/mcp.json` na raiz do projeto

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Uma entrada de gateway fornece acesso ao AJO, CJA e Real-Time CDP com base nas licenças de sua organização.

Depois de adicionados, os servidores MCP aparecem em **Servidores MCP instalados** nas Configurações do Cursor. Selecione **Conectar** ao lado de qualquer servidor que mostre que **Precisa de autenticação** e entre com sua Adobe ID. Selecione a organização IMS que tem acesso ao aplicativo.

![Configuração do servidor MCP do cursor mostrando os servidores MCP Adobe instalados e mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

Configuração completa: [Documentação de MCP do cursor](https://cursor.com/docs/mcp)

>[!TAB GPTchat]

### ![Recomendado](../assets/badge-recommended.svg) Usar um conector gerenciado

Vá para o [Registro do Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) e pesquise seu aplicativo do Adobe. Se um conector de ChatGPT estiver listado, siga as instruções de configuração em vez das etapas abaixo.

### Conectar usando um servidor MCP remoto

O ChatGPT dá suporte a servidores MCP remotos por meio do [Modo de Desenvolvedor](https://developers.openai.com/api/docs/guides/developer-mode), disponível nos planos Pro, Plus, Business, Enterprise e Education.

1. Habilite o Modo de Desenvolvedor em **Configurações de ChatGPT**.
2. Vá para **Configurações > Integrações**.
3. Clique em **Adicionar conector personalizado** e escolha **Servidor MCP remoto**.
4. Digite `https://cx-enterprise.adobe.io/mcp` como a URL e `Adobe CX Enterprise` como o nome.
5. Defina a autenticação como **OAuth**.
6. Clique em **Conectar** e entre com sua Adobe ID. Selecione a organização IMS correta.

Configuração completa: [Documentação de MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB CLI do OpenAI Codex]

A CLI do OpenAI Codex oferece suporte a servidores MCP remotos por meio da configuração TOML.

**Locais do arquivo de configuração:**

- **Nível de usuário (todos os projetos):** `~/.codex/config.toml`
- **Com escopo de projeto:** `.codex/config.toml` na raiz do projeto

Adicione o gateway do CX Enterprise MCP:

```toml
[mcp_servers.adobe-cx-enterprise]
url = "https://cx-enterprise.adobe.io/mcp"
enabled = true
```

Os servidores MCP do Adobe usam OAuth. O Codex CLI lida com o fluxo do OAuth automaticamente no primeiro uso. Selecione a organização IMS correta quando solicitado.

Configuração completa: [Documentação de MCP do OpenAI Codex CLI](https://developers.openai.com/codex/mcp)

>[!TAB Copilot Studio]

O Microsoft Copilot Studio se conecta a servidores MCP remotos usando o Assistente de integração de MCP, que cria automaticamente um conector personalizado da Plataforma de energia.

1. Abra o agente no Copilot Studio.
2. Vá para a página **Ferramentas**.
3. Selecione **Adicionar uma ferramenta > Nova ferramenta > Protocolo de Contexto de Modelo**.
4. No Assistente de integração do MCP, digite:
   - **Nome do servidor:** `Adobe CX Enterprise`
   - **URL do Servidor:** `https://cx-enterprise.adobe.io/mcp`
5. Defina a autenticação como **OAuth 2.0** e configure com sua autorização do Adobe IMS e URLs de token.
6. Selecione **Criar** e **Adicionar ao agente**.

>[!NOTE]
>
>As conexões de servidor MCP no Copilot Studio passam pela Power Platform. As políticas de prevenção de perda de dados (DLP) de sua organização se aplicam.

Configuração completa: [Documentação do Copilot Studio MCP](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## Solução de problemas

+++Alternar organizações da Adobe

Se o usuário do Adobe pertencer a várias organizações IMS e você estiver vendo ferramentas ou dados para a organização errada, desconecte o servidor MCP, saia da sessão do Adobe no navegador e reconecte. Você será solicitado a escolher uma organização durante o logon.

Um servidor Adobe CX Enterprise MCP só pode ser autenticado em uma organização IMS por vez, mesmo se a conta de usuário tiver acesso a mais de uma.

+++

+++Especificação de uma sandbox, conjunto de relatórios, ambiente ou outro recurso de sessão

Alguns servidores Adobe CX Enterprise MCP exigem que você especifique um recurso antes que eles possam retornar resultados. Dependendo do aplicativo, pode ser uma sandbox, um programa, um ambiente, um conjunto de relatórios ou uma visualização de dados.

Se não tiver certeza de quais recursos você tem acesso, pergunte ao cliente da IA. Por exemplo: &quot;Listar as sandboxes disponíveis&quot; ou &quot;A quais conjuntos de relatórios tenho acesso?&quot; Os servidores MCP Adobe CX Enterprise geralmente podem retornar uma lista completa de recursos disponíveis para o usuário.

Depois que um recurso de sessão é definido, você pode alterná-lo a qualquer momento, informando ao cliente de IA qual usar.

+++

+++Erros de permissões e acesso

Os clientes de IA agem em nome da sua conta de usuário do Adobe usando OAuth. As mesmas permissões e controles de acesso que se aplicam quando você faz logon em um aplicativo do Adobe se aplicam quando você usa um servidor MCP.

Se uma ação falhar ou não retornar resultados, verifique se o usuário tem as permissões necessárias no Adobe Admin Console e no aplicativo CX Enterprise relevante. Entre em contato com o administrador do sistema da Adobe se precisar ajustar o acesso.

+++

+++Reautenticação após uma sessão perdida

Os servidores MCP Adobe CX Enterprise usam o OAuth para autenticar sua conta de usuário do Adobe. Se o estado de autenticação for perdido, nenhuma outra chamada de ferramenta será bem-sucedida até que você faça a autenticação novamente.

Para autenticar novamente: abra a configuração do servidor MCP do cliente de IA, selecione a entrada do servidor Adobe CX Enterprise MCP e reconecte. Você será solicitado a fazer logon com sua Adobe ID novamente.

+++

## Ferramentas de agente em ação

Consulte servidores MCP corporativos Adobe CX aplicados a fluxos de trabalho de negócios reais.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine the CX Enterprise MCP Gateway and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use the CX Enterprise MCP Gateway for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->
