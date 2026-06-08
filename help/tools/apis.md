---
title: APIs para construtores
description: Crie aplicativos e integrações personalizados usando as APIs corporativas do Adobe CX.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 3%

---


# APIs para construtores

<!-- last-modified: 2026-06-02 -->

![APIs do Adobe CX Enterprise](../assets/hero-apis.png)

As APIs corporativas do Adobe CX fornecem aos desenvolvedores e às ferramentas de agente de codificação assistida por IA acesso direto aos dados e fluxos de trabalho do Adobe. Use-os para criar aplicativos personalizados, automatizar integrações e incorporar recursos do Adobe em seus próprios sistemas. As APIs são a escolha certa quando você precisa de controle programático total sobre uma integração de sistema ou quando está criando um aplicativo com base nos dados do Adobe. Para acesso conversacional orientado por agente a fluxos de trabalho do Adobe, consulte [servidores MCP](mcp-servers.md).

## APIs corporativas do Adobe CX

As APIs do Adobe CX Enterprise expõem os dados e as operações principais que alimentam produtos como Adobe Experience Platform, Journey Optimizer e Customer Journey Analytics. Cada API segue um design de API, fornecendo aos desenvolvedores e ferramentas de agente de codificação assistida por IA acesso direto e programável aos mesmos recursos que o Adobe usa internamente. Use-os para criar aplicativos personalizados, automatizar workflows e integrar dados do Adobe em seus próprios sistemas.

<!--
CARDS

* https://developer.adobe.com/audience-manager/
  {title = Audience Manager}
  {description = Audience management and activation workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aam-card.png}

* https://developer.adobe.com/client-sdks/home/
  {title = Client SDKs}
  {description = Mobile SDKs, edge SDKs, and in-app messaging.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/cja-apis/docs/
  {title = Customer Journey Analytics}
  {description = Analytics data access, reporting, and CJA insights workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cja-card.png}

* https://developer.adobe.com/data-collection-apis/docs/
  {title = Data Collection}
  {description = Edge Network data ingestion, real-time event collection, and streaming data delivery.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/developer-console/docs/guides/
  {title = Developer Console}
  {description = API project setup, authentication, and credential management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/events/docs/
  {title = Events}
  {description = Event-driven integrations, webhooks, and automation triggers.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://experienceleague.adobe.com/en/docs/experience-platform/privacy/home
  {title = Privacy}
  {description = Privacy workflows, data governance, and data subject requests.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/experience-platform-apis/
  {title = Adobe Experience Platform}
  {description = CRUD operations for datasets, schemas, profiles, identities, queries, and segmentation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/journey-optimizer-apis/
  {title = Adobe Journey Optimizer}
  {description = Journey orchestration, campaign management, content templates, and offer decisioning.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-ajo-card.png}

* https://developer.adobe.com/analytics-apis/docs/2.0/
  {title = Adobe Analytics}
  {description = Reporting, data feeds, calculated metrics, and segment management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-analytics-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions
  {title = AEM as a Cloud Service}
  {description = Content, asset, and workflow management APIs for Adobe Experience Manager.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aem-card.png}

* https://developer.adobe.com/commerce/webapi/
  {title = Adobe Commerce}
  {description = REST and GraphQL APIs for catalog, cart, orders, customers, and promotions.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-commerce-card.png}

* https://developer.adobe.com/umapi/
  {title = User Management}
  {description = User management, identity administration, and enterprise account automation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}
-->

## APIs para construtores vs. servidores MCP

Use APIs quando precisar de controle total sobre a integração do sistema ou quando estiver criando um aplicativo personalizado. Use servidores MCP quando quiser que um agente de IA trabalhe diretamente com workflows do Adobe.

| | APIs | Servidores MCP |
| --- | --- | --- |
| Integração direta do sistema | Sim | Às vezes |
| Orquestração amigável ao agente | Limitado | Sim |
| Acesso a dados brutos | Sim | Geralmente abstraído |
| Desenvolvimento de aplicativos personalizados | Caso de uso principal | Secundário |
| Fluxos de trabalho assistidos por IA | Suportado | Caso de uso principal |

## Introdução às APIs para construtores

![Um IDE se conectando às APIs do Adobe CX Enterprise](../assets/hero-connect-apis.gif)

As APIs corporativas do Adobe CX exigem duas coisas antes de você poder criar: credenciais autenticadas da Adobe Developer Console e documentação de API adicionada ao seu projeto para que seu agente de codificação possa trabalhar com as APIs da Adobe de forma confiável.

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
