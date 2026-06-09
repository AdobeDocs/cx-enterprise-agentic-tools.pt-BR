---
title: Servidores MCP
description: Conecte qualquer cliente de IA compatível com MCP aos workflows corporativos do Adobe CX usando os servidores do Protocolo de contexto de modelo.
index: false
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: a580957c41e750578b03688bb7ef980103a97781
workflow-type: tm+mt
source-wordcount: '1965'
ht-degree: 3%

---


# Servidores MCP

<!-- last-modified: 2026-06-09 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491327/?captions=por_br&learn=on&enablevpops)

Os servidores MCP corporativos do Adobe CX fornecem a qualquer cliente de IA compatível acesso direto e controlado a dados e workflows da Adobe. Conecte-se uma vez e poderá consultar o desempenho da campanha, ativar públicos, revisar jornadas, gerenciar conteúdo e muito mais, tudo em linguagem simples, sem sair do ambiente de IA. Como os servidores MCP ficam entre o cliente de IA e os sistemas subjacentes da Adobe, você obtém flexibilidade de linguagem natural enquanto os controles de acesso e a governança de dados de sua organização permanecem em vigor.

Os servidores MCP do Adobe seguem o padrão [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro) aberto. Qualquer cliente de IA compatível com MCP se conecta a qualquer servidor MCP do Adobe.

## Servidores CX Enterprise MCP

![O CX Enterprise MCP conecta seu cliente de IA a ferramentas em todo o Adobe CX Enterprise Suite](../assets/mcp-gateway-hero.gif)

Selecione um aplicativo para exibir o endpoint e os recursos.

>[!BEGINTABS]

>[!TAB CX Enterprise MCP]

**Um ponto de extremidade. Vários aplicativos CX Enterprise.**

Conecte-se uma vez e seu cliente de IA obterá acesso aos aplicativos CX Enterprise com base nas licenças de sua organização.

```
https://cx-enterprise.adobe.io/mcp
```

| aplicativo corporativo CX | O que você pode fazer |
| --- | --- |
| Adobe Analytics | Descoberta do conjunto de relatórios, criação de segmentos e criação de espaços de trabalho |
| Adobe Experience Platform | Detecção de conjuntos de dados, navegação por esquemas e gerenciamento de sandbox |
| Adobe Journey Optimizer | Revisar jornadas, campanhas e configurações de canal |
| Adobe Journey Optimizer B2B edition | Gerenciar jornadas B2B, programas de conta, grupos de compra e personalização |
| Customer Journey Analytics | Relatórios de query, visualizações de dados de descoberta e espaços de trabalho do autor |
| Real-Time CDP | Verifique o status de ativação do público-alvo, a integridade do destino e a integridade do fluxo de dados |

>[!NOTE]
>
>O acesso a cada aplicativo CX Enterprise é baseado nos direitos de sua organização e nas permissões de seu usuário no Adobe Admin Console.

>[!TAB Experience Manager]

O Adobe Experience Manager tem vários servidores MCP para workflows diferentes.

| Servidor MCP | Endpoint | O que você pode fazer |
| --- | --- | --- |
| [AEM (Modo de Código)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/aem` | Acesso direto da API REST ao AEM por meio de pesquisa, leitura, gravação e exclusão em linguagem natural |
| [AEM Cloud Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | Gerenciar programas, ambientes, pipelines e repositórios |
| [Conteúdo do AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | Gerenciar páginas, fragmentos de conteúdo, ativos e lançamentos |
| [Conteúdo Do AEM (Somente Leitura)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | Páginas de detecção e consulta, fragmentos de conteúdo e lançamentos sem acesso de gravação |
| [Criação de documentos do AEM]&#x200B;(TODO: validate) | `https://mcp.adobeaemcloud.com/adobe/mcp/da` | Gerenciar arquivos, histórico de versões e referências de mídia na Criação de documentos |
| [Governança de experiência da AEM](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | Avaliar conteúdo e imagens em relação às diretrizes da marca e às regras de conformidade |
| [Produção de experiência do AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/experience-production/overview) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-production` | Transforme e crie páginas do AEM em escala usando resumos de conteúdo orientados por IA |

>[!NOTE]
>
>O acesso a cada ambiente do AEM depende dos direitos do AEM Cloud Service da sua organização e das permissões do usuário nesse ambiente.

>[!TAB Experience Platform]

| Servidor MCP | Endpoint | O que você pode fazer |
| --- | --- | --- |
| [Adobe Marketing Agent]&#x200B;(TODO: validar) | `https://aep-ai-ama.adobe.io/mcp` | Orquestrar a análise de público-alvo, o diagnóstico AEP e a criação de jornada B2B do AJO em aplicativos da AEP |

>[!NOTE]
>
>O acesso depende dos direitos da Adobe Experience Platform de sua organização e das permissões do usuário.

>[!TAB Marketo Engage]

>[!NOTE]
>
>O Marketo Engage MCP usa credenciais de serviço nativas do Marketo, não o Adobe IMS. Consulte a [documentação do Marketo Engage MCP Server](https://experienceleague.adobe.com/pt-br/docs/marketo-developer/marketo/mcp-server) para obter instruções de configuração de autenticação.

| Servidor MCP | Endpoint | O que você pode fazer |
| --- | --- | --- |
| [Marketo Engage](https://experienceleague.adobe.com/pt-br/docs/marketo-developer/marketo/mcp-server) | `https://marketo-mcp.adobe.io/mcp` | Gerenciar programas, campanhas, clientes potenciais, listas inteligentes, emails e formulários |

>[!NOTE]
>
>O acesso depende da assinatura da Marketo Engage e das permissões do usuário da API.

>[!TAB Target]

O Adobe Target MCP está em beta público. Todas as ferramentas disponíveis no momento são somente leitura. As ferramentas de gravação estão planejadas para disponibilidade geral.

| Servidor MCP | Endpoint | O que você pode fazer |
| --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/pt-br/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | Analisar atividades, ofertas, públicos, mboxes e relatórios de desempenho |

>[!NOTE]
>
>O acesso depende dos direitos da Adobe Target e das permissões do usuário.

>[!TAB Workfront]

| Servidor MCP | Endpoint | O que você pode fazer |
| --- | --- | --- |
| [Adobe Workfront]&#x200B;(TODO: validar) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | Gerenciar trabalhos, projetos, registros de planejamento, insights e aprovações de conteúdo |

>[!NOTE]
>
>O acesso depende das licenças da Adobe Workfront e das permissões do usuário.

>[!ENDTABS]

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

Execute `claude mcp add` para registrar o CX Enterprise MCP. Uma conexão fornece acesso ao AJO, CJA e Real-Time CDP com base nas licenças de sua organização.

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

Adicione o CX Enterprise MCP ao seu arquivo de configuração Cursor `mcp.json` e conecte-se por meio de **Configurações > MCP**.

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

Uma conexão fornece acesso ao AJO, CJA e Real-Time CDP com base nas licenças de sua organização.

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

Adicionar CX Enterprise MCP:

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

## Ferramentas de agente em ação

Consulte servidores MCP corporativos Adobe CX aplicados a fluxos de trabalho de negócios reais.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use CX Enterprise MCP to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use CX Enterprise MCP to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use CX Enterprise MCP to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CX Enterprise MCP and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use CX Enterprise MCP for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Analisar o desempenho da campanha" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Analisar o desempenho da campanha"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="Analisar o desempenho da campanha">Analisar o desempenho da campanha</a>
                    </p>
                    <p class="is-size-6">Use o CX Enterprise MCP para exibir métricas e insights do Customer Journey Analytics de qualquer cliente de IA.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar apresentação</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Consultar públicos" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Consultar públicos"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" title="Consultar públicos">Consultar públicos-alvo</a>
                    </p>
                    <p class="is-size-6">Use o CX Enterprise MCP para consultar dados de público-alvo e destino do Real-Time CDP usando prompts de idioma simples.</p>
                </div>
                <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar apresentação</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="Revisar jornadas do AJO" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="Revisar jornadas do AJO"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="Revisar jornadas do AJO">Analisar jornadas do AJO</a>
                    </p>
                    <p class="is-size-6">Use o CX Enterprise MCP para acessar o AJO jornada, o status da campanha e as condições do jornada no cliente de IA.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar apresentação</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="Gerenciar conteúdo do AEM com IA" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="Gerenciar conteúdo do AEM com IA"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="Gerenciar conteúdo do AEM com IA">Gerenciar conteúdo do AEM com IA</a>
                    </p>
                    <p class="is-size-6">Descubra, atualize e publique páginas e fragmentos de conteúdo no AEM usando a linguagem natural.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar apresentação</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="Otimizar o conteúdo com base nos dados de desempenho" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="Otimizar o conteúdo com base nos dados de desempenho"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="Otimizar o conteúdo com base nos dados de desempenho">Otimizar conteúdo com base nos dados de desempenho</a>
                    </p>
                    <p class="is-size-6">Combine o CX Enterprise MCP e o AEM Content MCP Server para encontrar conteúdo com baixo desempenho e atualizá-lo em uma sessão.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar apresentação</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/cross-channel-campaign-review.md" title="Executar uma revisão de campanha entre canais" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="Executar uma revisão de campanha entre canais"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="Executar uma revisão de campanha entre canais">Executar uma análise de campanha entre canais</a>
                    </p>
                    <p class="is-size-6">Use o CX Enterprise MCP para obter uma visualização unificada da integridade da campanha do AJO, CJA e Real-Time CDP em uma sessão de IA.</p>
                </div>
                <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar apresentação</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

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
