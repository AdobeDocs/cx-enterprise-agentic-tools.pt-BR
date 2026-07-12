---
title: Servidores MCP
description: Conecte qualquer cliente de IA compatível com MCP aos workflows corporativos do Adobe CX usando os servidores do Protocolo de contexto de modelo.
last-substantial-update: 2026-06-17T00:00:00Z
source-git-commit: 331736994515eb978ab9f24208d65f05ecd4c0b4
workflow-type: tm+mt
source-wordcount: '2408'
ht-degree: 6%

---


# Servidores MCP

<!-- last-modified: 2026-06-11 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Os servidores MCP corporativos do Adobe CX fornecem a qualquer cliente de IA compatível acesso direto e controlado a dados e workflows da Adobe. Conecte-se uma vez e poderá consultar o desempenho da campanha, ativar públicos, revisar jornadas, gerenciar conteúdo e muito mais, tudo em linguagem simples, sem sair do ambiente de IA. Como os servidores MCP ficam entre o cliente de IA e os sistemas subjacentes da Adobe, você obtém flexibilidade de linguagem natural enquanto os controles de acesso e a governança de dados de sua organização permanecem em vigor.

Os servidores MCP do Adobe seguem o padrão [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro) aberto. Qualquer cliente de IA compatível com MCP se conecta a qualquer servidor MCP do Adobe.

## Servidores MCP do CX Enterprise {#cx-enterprise-mcp-servers}

>[!CONTEXTUALHELP]
>id="cx-enterprise-agentic-tools_mcp_servers_cx-enterprise"
>title="MCP do CX Enterprise"
>abstract="Seus aplicativos CX Enterprise, acessíveis por meio de um único ponto de acesso MCP. Pergunte, analise e execute ações em linguagem simples dos clientes de IA."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/mcp/overview" text="Documentação do MCP do CX Enterprise"

![O CX Enterprise MCP conecta seu cliente de IA a ferramentas em todo o Adobe CX Enterprise Suite](../assets/mcp-gateway-hero.gif)

Selecione um aplicativo para exibir o endpoint e os recursos.

>[!BEGINTABS]

>[!TAB CX Enterprise MCP]

**Um ponto de extremidade. Vários aplicativos CX Enterprise.**

Conecte-se uma vez e seu cliente de IA obterá acesso aos aplicativos CX Enterprise com base nas licenças de sua organização. Para habilitar sua organização, envie um email para [cxo-mcp-feedback@adobe.com](mailto:cxo-mcp-feedback@adobe.com) para solicitar acesso.

```
https://cx-enterprise.adobe.io/mcp
```

| aplicativo corporativo CX | O que você pode fazer | Direito extra necessário |
| --- | --- | --- |
| [Adobe Analytics](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/analytics-mcp) | Descoberta do conjunto de relatórios, criação de segmentos e criação de espaços de trabalho | Não |
| Campaign Classic | Descoberta de instância de campanha, navegação de esquema, execução de consulta, controle de fluxo de trabalho e execução de SOAP/JS | Sim |
| [Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/aep-mcp) | Detecção de conjuntos de dados, navegação por esquemas e gerenciamento de sandbox | Não |
| Experimentação | Relatórios de experimento A/B, MVT e MAB, métricas, insights, oportunidades e planejamento de tamanho de amostra | Não |
| GenStudio para marketing de desempenho | Acessar dados de desempenho do anúncio e insights criativos | Sim |
| [Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/ajo-mcp) | Revisar jornadas, campanhas e configurações de canal | Não |
| Adobe Journey Optimizer B2B edition | Gerenciar jornadas B2B, programas de conta, grupos de compra e personalização | Não |
| [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp) | Revisar atividades, ofertas, públicos, mboxes, relatórios de desempenho e URLs de visualização | [Sim](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp-get-started#mcp-security) |
| [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/cja-mcp) | Relatórios de query, visualizações de dados de descoberta e espaços de trabalho do autor | Não |
| [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server) | Gerenciar programas, campanhas, clientes potenciais, listas inteligentes, emails e formulários | [Sim](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server#get-marketo-credentials) |
| [Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/rtcdp-mcp) | Verifique o status de ativação do público-alvo, a integridade do destino e a integridade do fluxo de dados | Não |

Para obter a documentação completa, consulte [CX Enterprise MCP](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/mcp/overview).

>[!NOTE]
>
>O acesso a cada aplicativo CX Enterprise é baseado nos direitos de sua organização e nas permissões de seu usuário no Adobe Admin Console. Para habilitar o CX Enterprise MCP para sua organização, envie um email para [cxo-mcp-feedback@adobe.com](mailto:cxo-mcp-feedback@adobe.com).

>[!TAB Experience Manager]

O Adobe Experience Manager tem vários servidores MCP para workflows diferentes.

| Servidor MCP | Endpoint | O que você pode fazer |
| --- | --- | --- |
| [AEM Cloud Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | Gerenciar programas, ambientes, pipelines e repositórios |
| [Conteúdo do AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | Gerenciar páginas, fragmentos de conteúdo, ativos e lançamentos |
| [Conteúdo Do AEM (Somente Leitura)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | Páginas de detecção e consulta, fragmentos de conteúdo e lançamentos sem acesso de gravação |
| [Governança de experiência da AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | Avaliar conteúdo e imagens em relação às diretrizes da marca e às regras de conformidade |

>[!NOTE]
>
>O acesso a cada ambiente do AEM depende dos direitos do AEM Cloud Service da sua organização e das permissões do usuário nesse ambiente.

>[!TAB Experience Platform]

| Servidor MCP | Endpoint | O que você pode fazer |
| --- | --- | --- |
| Adobe Marketing Agent | `https://aep-ai-ama.adobe.io/mcp` | Orquestrar a análise de público-alvo, o diagnóstico AEP e a criação de jornada B2B do AJO em aplicativos da AEP |

>[!NOTE]
>
>O acesso depende dos direitos da Adobe Experience Platform de sua organização e das permissões do usuário.

>[!TAB Target]

O Adobe Target MCP está em beta público. Todas as ferramentas disponíveis no momento são somente leitura. As ferramentas de gravação estão planejadas para disponibilidade geral.

| Servidor MCP | Endpoint | O que você pode fazer |
| --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | Revisar atividades, ofertas, públicos, mboxes, relatórios de desempenho e URLs de visualização |

>[!NOTE]
>
>O acesso depende dos direitos da Adobe Target e das permissões do usuário.

>[!TAB Workfront]

| Servidor MCP | Endpoint | O que você pode fazer |
| --- | --- | --- |
| [Adobe Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | Gerenciar trabalhos, projetos, registros de planejamento, insights e aprovações de conteúdo |

>[!NOTE]
>
>O acesso depende das licenças da Adobe Workfront e das permissões do usuário.

>[!ENDTABS]

## Conectar ao cliente de IA

A maioria dos servidores MCP do Adobe usa o OAuth com o Adobe Identity Management Service (IMS). Selecione a organização IMS correta quando solicitado. Escolher o errado é a fonte mais comum de erros de autenticação.

![Um agente de IA se conectando a um servidor MCP do Adobe](../assets/hero-connect-mcp-servers.gif)

As etapas abaixo usam o endpoint do CX Enterprise MCP como exemplo. O mesmo processo se aplica a qualquer servidor MCP do Adobe: troque o URL do ponto de extremidade pelo servidor que você deseja conectar.

>[!BEGINTABS]

>[!TAB Claude.ai]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Recomendado"> Usar um conector gerenciado

Vá para o [Registro do Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) e pesquise seu aplicativo do Adobe. Se um conector Claude estiver listado (por exemplo, o [conector Adobe Experience Manager](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), siga as instruções de configuração em vez das etapas abaixo.

### Conectar usando um conector personalizado

O Claude.ai oferece suporte a servidores MCP remotos por meio dos Conectores personalizados nas configurações da conta.

1. Vá para **Configurações > Integrações**.
2. Clique em **Adicionar conector personalizado**.
3. Insira o endpoint do servidor como a URL (por exemplo, `https://cx-enterprise.adobe.io/mcp` para o CX Enterprise MCP) e um nome para exibição de sua escolha.
4. Clique em **Conectar** e entre com sua Adobe ID. Selecione a organização IMS correta.

Configuração completa: [documentação dos Conectores personalizados do Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Código Claude]

### Uso da CLI

Execute `claude mcp add` para registrar um servidor MCP do Adobe. Substitua o nome do servidor e o URL pelos valores do servidor que você deseja conectar. Este exemplo usa o CX Enterprise MCP:

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### Editar seu arquivo de configurações

Adicione o servidor a `~/.claude.json` (global) ou `.mcp.json` na raiz do projeto (nível de projeto). Substitua a chave e o URL pelos valores do servidor que você deseja conectar:

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

Adicione um servidor Adobe MCP ao arquivo de configuração Cursor `mcp.json` e conecte-se por meio de **Configurações > MCP**. Substitua a chave e o URL pelos valores do servidor que você deseja conectar. Este exemplo usa o CX Enterprise MCP:

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

Depois de adicionados, os servidores MCP aparecem em **Servidores MCP instalados** nas Configurações do Cursor. Selecione **Conectar** ao lado de qualquer servidor que mostre que **Precisa de autenticação** e entre com sua Adobe ID. Selecione a organização IMS que tem acesso ao aplicativo.

![Configuração do servidor MCP do cursor mostrando os servidores MCP Adobe instalados e mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

Configuração completa: [Documentação de MCP do cursor](https://cursor.com/docs/mcp)

>[!TAB GPTchat]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Recomendado"> Usar um conector gerenciado

Vá para o [Registro do Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) e pesquise seu aplicativo do Adobe. Se um conector de ChatGPT estiver listado, siga as instruções de configuração em vez das etapas abaixo.

### Conectar usando um servidor MCP remoto

O ChatGPT dá suporte a servidores MCP remotos por meio do [Modo de Desenvolvedor](https://developers.openai.com/api/docs/guides/developer-mode), disponível nos planos Pro, Plus, Business, Enterprise e Education.

1. Habilite o Modo de Desenvolvedor em **Configurações de ChatGPT**.
2. Vá para **Configurações > Integrações**.
3. Clique em **Adicionar conector personalizado** e escolha **Servidor MCP remoto**.
4. Insira o endpoint do servidor como a URL (por exemplo, `https://cx-enterprise.adobe.io/mcp` para o CX Enterprise MCP) e um nome para exibição de sua escolha.
5. Defina a autenticação como **OAuth**.
6. Clique em **Conectar** e entre com sua Adobe ID. Selecione a organização IMS correta.

Configuração completa: [Documentação de MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB CLI do OpenAI Codex]

A CLI do OpenAI Codex oferece suporte a servidores MCP remotos por meio da configuração TOML.

**Locais do arquivo de configuração:**

- **Nível de usuário (todos os projetos):** `~/.codex/config.toml`
- **Com escopo de projeto:** `.codex/config.toml` na raiz do projeto

Substitua o nome da seção e o URL pelos valores do servidor que você deseja conectar. Este exemplo usa o CX Enterprise MCP:

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
4. No Assistente de integração do MCP, insira os detalhes do servidor. Por exemplo, para o CX Enterprise MCP:
   - **Nome do servidor:** `Adobe CX Enterprise`
   - **URL do Servidor:** `https://cx-enterprise.adobe.io/mcp`
5. Defina a autenticação como **OAuth 2.0** e configure com sua autorização do Adobe IMS e URLs de token.
6. Selecione **Criar** e **Adicionar ao agente**.

>[!NOTE]
>
>As conexões de servidor MCP no Copilot Studio passam pela Power Platform. As políticas de prevenção de perda de dados (DLP) de sua organização se aplicam.

Configuração completa: [Documentação do Copilot Studio MCP](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## Servidores MCP em ação

Consulte os servidores Adobe CX Enterprise MCP colocados para trabalhar em problemas reais de negócios. Cada passo a passo começa com um desafio operacional genuíno e mostra como um cliente de IA o resolve em linguagem simples, sem alternar ferramentas ou escrever código.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* ../use-cases/query-audiences.md
  {title = Audience activation at a glance}
  {description = See which audiences are live, where they are flowing, and whether destinations are healthy, without navigating Real-Time CDP.}
  {cta = Check audience activation}

* ../use-cases/manage-ajo-journeys.md
  {title = Catch journey issues early}
  {description = Monitor active journeys and surface operational issues before they reach your audience.}
  {cta = Monitor your journeys}

* ../use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Close content performance gaps}
  {description = Surface conversion gaps in CJA, trace them to underperforming content in AEM, and apply the fix in a single AI session.}
  {cta = Close performance gaps}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Insights do Campaign sem relatórios">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Insights do Campaign sem relatórios"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" title="Insights do Campaign sem relatórios">Insights da campanha sem relatórios</a>
                    </p>
                    <p class="is-size-6">Faça perguntas de desempenho em linguagem simples e obtenha respostas do Customer Journey Analytics, sem criar um único relatório.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Insights de campanha de superfície</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Audience activation at a glance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Principais características da ativação de público-alvo">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Principais características da ativação de público-alvo"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="Principais características da ativação de público-alvo">Principais características da ativação de público-alvo</a>
                    </p>
                    <p class="is-size-6">Veja quais públicos-alvo estão ativos, onde estão fluindo e se os destinos estão íntegros, sem navegar no Real-Time CDP.</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Verificar ativação de público-alvo</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Catch journey issues early">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="Problemas de jornada de capturas antecipadas">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="Problemas de jornada de capturas antecipadas"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" title="Problemas de jornada de capturas antecipadas">Detectar problemas de jornada antecipadamente</a>
                    </p>
                    <p class="is-size-6">Monitore jornadas ativas e detecte problemas operacionais antes que eles atinjam seu público-alvo.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Monitorar suas jornadas</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="Enviar atualizações de conteúdo mais rapidamente">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="Enviar atualizações de conteúdo mais rapidamente"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" title="Enviar atualizações de conteúdo mais rapidamente">Enviar atualizações de conteúdo mais rapidamente</a>
                    </p>
                    <p class="is-size-6">Encontre, atualize e publique páginas e fragmentos de conteúdo do AEM com mais rapidez, sem alternar para a interface do AEM.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Enviar conteúdo mais rápido</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Close content performance gaps">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="Fechar as lacunas de desempenho do conteúdo">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="Fechar as lacunas de desempenho do conteúdo"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" title="Fechar as lacunas de desempenho do conteúdo">Fechar lacunas de desempenho de conteúdo</a>
                    </p>
                    <p class="is-size-6">Superar falhas de conversão no CJA, rastreá-las até o conteúdo com baixo desempenho no AEM e aplicar a correção em uma única sessão de IA.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Fechar lacunas de desempenho</span>
                
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Precisa de mais ajuda?

As conexões do MCP envolvem autenticação, seleção de organização e permissões no nível do aplicativo. Se algo não estiver funcionando como o esperado, essas etapas abordam as causas mais comuns.

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
