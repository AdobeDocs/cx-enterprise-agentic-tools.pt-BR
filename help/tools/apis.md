---
title: APIs para construtores
description: Crie aplicativos e integrações personalizados usando as APIs corporativas do Adobe CX.
last-substantial-update: 2026-06-02T00:00:00Z
index: false
source-git-commit: f7ace53bd5988b5902659c89c6da16448398e0c0
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 9%

---


# APIs para construtores

<!-- last-modified: 2026-06-02 -->

![APIs do Adobe CX Enterprise](../assets/hero-apis.png)

As APIs corporativas do Adobe CX fornecem aos desenvolvedores e às ferramentas de agente de codificação assistida por IA acesso direto aos dados e fluxos de trabalho do Adobe. Use-os para criar aplicativos personalizados, automatizar integrações e incorporar recursos do Adobe em seus próprios sistemas. As APIs são a escolha certa quando você precisa de controle programático total sobre uma integração de sistema ou quando está criando um aplicativo com base nos dados do Adobe. Para acesso conversacional orientado por agente a fluxos de trabalho do Adobe, consulte [servidores MCP](mcp-servers.md).

## APIs corporativas do Adobe CX

>[!BEGINTABS]

>[!TAB Adobe Analytics]

Relatórios, feeds de dados, métricas calculadas e gerenciamento de segmentos.

[Explorar API](https://developer.adobe.com/analytics-apis/docs/2.0/)

>[!TAB Adobe Commerce]

APIs REST e GraphQL para catálogo, carrinho, pedidos, clientes e promoções.

[Explorar API](https://developer.adobe.com/commerce/webapi/)

>[!TAB Adobe Experience Platform]

Operações CRUD para conjuntos de dados, esquemas, perfis, identidades, consultas e segmentação.

[Explorar API](https://developer.adobe.com/experience-platform-apis/)

>[!TAB Adobe Journey Optimizer]

Orquestração de jornadas, gestão de campanhas, modelos de conteúdo e offer decisioning.

[Explorar API](https://developer.adobe.com/journey-optimizer-apis/)

>[!TAB AEM as a Cloud Service]

APIs de gerenciamento de conteúdo, ativos e fluxo de trabalho para o Adobe Experience Manager.

[Explorar API](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions)

>[!TAB Audience Manager]

Gerenciamento de público-alvo e fluxos de trabalho de ativação.

[Explorar API](https://developer.adobe.com/audience-manager/)

>[!TAB SDKs do cliente]

SDKs móveis, SDKs de borda e mensagens no aplicativo.

[Explorar API](https://developer.adobe.com/client-sdks/home/)

>[!TAB Customer Journey Analytics]

Workflows de acesso a dados, relatórios e insights do CJA no Analytics.

[Explorar API](https://developer.adobe.com/cja-apis/docs/)

>[!TAB Coleta de dados]

Assimilação de dados do Edge Network, coleção de eventos em tempo real e entrega de dados de transmissão.

[Explorar API](https://developer.adobe.com/data-collection-apis/docs/)

>[!TAB Developer Console]

Configuração do projeto da API, autenticação e gerenciamento de credenciais.

[Explorar API](https://developer.adobe.com/developer-console/docs/guides/)

>[!TAB Eventos]

Integrações orientadas por eventos, webhooks e acionadores de automação.

[Explorar API](https://developer.adobe.com/events/docs/)

>[!TAB Privacidade]

Workflows de privacidade, governança de dados e solicitações de titulares de dados.

[Explorar API](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/home)

>[!TAB Gerenciamento de usuários]

Gerenciamento de usuários, administração de identidades e automação de contas corporativas.

[Explorar API](https://developer.adobe.com/umapi/)

>[!ENDTABS]

## Criar com APIs

![Um IDE se conectando às APIs do Adobe CX Enterprise](../assets/hero-connect-apis.gif)

Agentes de codificação como Claude Code, Cursor e OpenAI Codex são adequados para criação com APIs corporativas do Adobe CX. Adicione uma especificação OpenAPI ao seu projeto e o agente pode descobrir pontos de extremidade, criar solicitações e o motivo do comportamento da API sem fiação manual. Para iniciar, você precisa de duas coisas: credenciais autenticadas do Adobe Developer Console e documentação da API adicionada ao seu projeto.

### Configurar credenciais de API no Adobe Developer Console

Todo o acesso à API do Adobe CX Enterprise é gerenciado por meio do [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/). Crie um projeto, adicione as APIs de que seu aplicativo precisa e gere credenciais.

1. Entre e [crie um projeto](https://developer.adobe.com/developer-console/docs/guides/projects/) no Adobe Developer Console.
2. [Adicione a API](https://developer.adobe.com/developer-console/docs/guides/services/) para o aplicativo Adobe CX Enterprise de que você precisa.
3. Escolha um [tipo de autenticação](https://developer.adobe.com/developer-console/docs/guides/authentication/). Use o **OAuth Server-to-Server** para fluxos de trabalho automatizados ou o **OAuth Web App** para aplicativos voltados para o usuário.
4. Gere suas credenciais. Observe a ID do cliente, o segredo do cliente e o endpoint do token para uso em seu aplicativo.

A maioria das APIs do Adobe CX Enterprise requer licenciamento de aplicativos. Se uma API não estiver disponível em seu projeto do Developer Console, entre em contato com o representante da Adobe.

### Adicionar o contexto da API do Adobe ao seu projeto

Os agentes de codificação de IA podem descobrir e usar APIs do Adobe de maneira confiável quando você adiciona o material de referência correto ao seu projeto. Isso funciona para qualquer API corporativa do Adobe CX que publique uma especificação OpenAPI.

**1. Localizar a especificação de API**

Navegue pelas [APIs do Adobe CX Enterprise](#adobe-cx-enterprise-apis) listadas acima ou vá diretamente para o [catálogo de APIs do Adobe Developer](https://developer.adobe.com/apis).

**2. Baixe a especificação OpenAPI**

Crie um diretório `/specs` em seu projeto. Baixe o OpenAPI YAML da página de referências de API em [developer.adobe.com](https://developer.adobe.com/apis) e salve-o lá. Adicione um `README.md` gravando a URL de origem e a data de download.

```
/specs/README.md
/specs/aem-assets.openapi.yaml
```

>[!TIP]
>Um instantâneo com check-in fornece ao seu agente de codificação um comportamento estável e reprodutível, além de tornar as alterações na API visíveis no seu histórico do Git.

**3. Gerar um índice de API**

Cole esse prompt no seu agente de codificação, substituindo `<API-SPEC-FILE>` pelo seu nome de arquivo:

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and generate /docs/<API-SPEC-FILE>.api.md.

Create a concise API index for AI coding agents. For each operation include: operationId, HTTP method, path, purpose, authentication requirements, required inputs, response shape, common error responses, pagination behavior, asynchronous behavior, and deprecation status.

Do not invent endpoints, parameters, request bodies, response fields, or behavior not present in the OpenAPI specification.
```

**4. Gerar instruções do agente**

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and /docs/<API-SPEC-FILE>.api.md.

Generate AGENTS.md. Instructions should:
- Treat the OpenAPI specification as the source of truth.
- Use the API index as a navigation guide.
- Never invent endpoints, parameters, response fields, or status codes.
- Prefer documented operationIds.
- Avoid deprecated or experimental APIs unless explicitly requested.
- Follow authentication requirements defined in the specification.
- Use the local OpenAPI snapshot for implementation decisions.
```

**5. Verificar**

Peça ao seu agente de codificação para concluir uma tarefa simples usando apenas os arquivos gerados:

```
Write a function that takes an AEM asset ID and returns the asset title and description. Use only /specs/aem-assets.openapi.yaml and /docs/aem-assets.api.md.
```

Se o agente concluí-lo corretamente sem inventar comportamento, a configuração está concluída.

**Estrutura de projeto recomendada**

```
project/
├── specs/
│   ├── README.md
│   └── aem-assets.openapi.yaml
├── docs/
│   └── aem-assets.api.md
└── AGENTS.md
```

**Mantendo as especificações atualizadas**

Quando o Adobe publicar uma nova versão da API: baixe um instantâneo novo no `/specs`, atualize a data em `README.md`, gere novamente o índice e `AGENTS.md`.

## APIs em ação

As APIs oferecem às equipes de desenvolvimento controle programático total para criar aplicativos focados que automatizam fluxos de trabalho específicos do CX Enterprise. Essas apresentações mostram integrações reais criadas de ponta a ponta, desde a configuração de credenciais até o código de trabalho que sua organização pode enviar.

<!--
CARDS

* https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app
  {title = Invoke AEM APIs from a web app}
  {description = Build a web application that authenticates users and calls AEM OpenAPIs using OAuth to deliver governed, programmatic access.}
  {cta = Try with APIs}
  {image = ../assets/using-api-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Invoke AEM APIs from a web app">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" title="Chamar APIs do AEM a partir de um aplicativo web" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/using-api-card.png" alt="Chamar APIs do AEM a partir de um aplicativo web"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" title="Chamar APIs do AEM a partir de um aplicativo web">Invocar APIs do AEM a partir de um aplicativo Web</a>
                    </p>
                    <p class="is-size-6">Crie um aplicativo web que autentique usuários e chame AEM OpenAPIs usando OAuth para fornecer acesso controlado e programático.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Tente com APIs</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
