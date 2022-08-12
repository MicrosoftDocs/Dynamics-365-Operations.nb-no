---
title: Legge til støtte for et innholdsleveringsnettverk (CDN)
description: Denne artikkelen beskriver hvordan du legger til et innholdsleveringsnettverk (CDN) i Microsoft Dynamics 365 Commerce-miljøet.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2177eeb6497269d580d2baea87ebb4fcd395223b
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069675"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Legge til støtte for et innholdsleveringsnettverk (CDN)

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du legger til et innholdsleveringsnettverk (CDN) i Microsoft Dynamics 365 Commerce-miljøet.

Når du definerer et e-handelsmiljø i Dynamics 365 Commerce, kan du konfigurere det slik at det fungerer med CDN-tjenesten. 

Ditt egendefinerte domene kan aktiveres under klargjøringsprosessen for ditt e-handelsmiljø. Du kan også bruke en serviceforespørsel for å konfigurere den etter at klargjøringsprosessen er fullført. Klargjøringsprosessen for e-handelsmiljøet genererer et vertsnavn som er knyttet til miljøet. Dette vertsnavnet har følgende format, der \<*e-commerce-tenant-name*\> er navnet på miljøet ditt:

&lt;e-handel-leier-navn&gt;.commerce.dynamics.com

Vertsnavnet eller endepunktet som genereres under klargjøringsprosessen, støtter bare et SSL-sertifikat (Secure Sockets Layer) for \*.commerce.dynamics.com. Den støtter ikke SSL for egendefinerte domener. Derfor må du avslutte SSL for egendefinerte domener i CDN og videresende trafikk fra CDN til vertsnavnet eller endepunktet som Commerce genererte. 

I tillegg betjenes *statistiske filer* (JavaScript- eller Cascading Style Sheets \[CSS\]-filer) fra Commerce fra endepunktet som Commerce genererte (\*.commerce.dynamics.com). Statistiske filer kan bare hurtigbufres hvis vertsnavnet eller endepunktet som Commerce genererte, plasseres bak CDN.

## <a name="set-up-ssl"></a>Definer SSL

Når du har klargjort handelsmiljøet med det tilpassede domenet som er oppgitt, eller etter at du har angitt det egendefinerte domenet for miljøet ditt ved å bruke en tjenesteforespørsel, må du arbeide med Commerce-introduksjonsgruppen for å planlegge DNS-endringene.

Som tidligere nevnt støtter det genererte vertsnavnet eller endepunktet bare et SSL-sertifikat for \*.commerce.dynamics.com. Den støtter ikke SSL for egendefinerte domener.

## <a name="cdn-services"></a>CDN-tjenester

Alle CDN-tjenester kan brukes med et handelsmiljø. Her er to eksempler:

- **Microsoft Azure Front Door Service** – Azure CDN-løsningen. Hvis du vil ha mer informasjon om Azure Front Door Service, se [Dokumentasjon for Azure Front Door Service](/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** – For mer informasjon, se [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CND-oppsett

Installasjonsprosessen for CDN består av disse generelle trinnene:

1. Legg til en frontvert.
1. Konfigurer et serverdelsutvalg.
1. Angi regler for ruting.

### <a name="add-a-front-end-host"></a>Legg til en frontvert

Alle CDN-tjenester kan brukes, men for eksempel i denne artikkelen brukes Azure Front Door Service. 

Hvis du vil ha informasjon om hvordan du konfigurerer Azure Front Door Service, se [Hurtigstart: Opprette en hovedinngang for et høyt tilgjengelig globalt webprogram](/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Konfigurere et serverdelsutvalg i Azure Front Door Service

Følg disse trinnene for å konfigurere et serverdelsutvalg i Azure Front Door Service.

1. Legg til **&lt;ecom-leier-navn&gt;.commerce.dynamics.com** i et serverdelutvalg som en egendefinert vert som har et serverdelvertshode som er det samme som **&lt;ecom-leier-navn&gt;.commerce.dynamics.com**.
1. Under **Belastningsfordeling** lar du standardverdiene være.
1. Deaktiver tilstandskontroll for serverdelutvalget.

Følgende illustrasjon viser dialogboksen **Legg til en serverdel** i Azure Front Door Service, der vertsnavnet for serverdelen er angitt.

![Legge til en dialogboks for serverdelsutvalg.](./media/CDN_BackendPool.png)

Følgende illustrasjon viser dialogboksen **Legg til et serverdelutvalg** i Azure Front Door Service med standardverdier for belastningsfordeling.

![Legge til en dialogboks for serverdelsutvalg (fortsettelse).](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Pass på at du deaktiverer **Helsetilstand** når du setter opp din egen Azure Front Door Service for Commerce.


### <a name="set-up-rules-in-azure-front-door-service"></a>Definere regler i Azure Front Door Service

Følg disse trinnene for å opprette en rutingsregel i Azure Front Door Service.

1. Legge til en rutingsregel.
1. Angi **standard** i feltet **Navn**.
1. I feltet **Godkjent protokoll** velger du **HTTP og HTTPS**.
1. I feltet **Frontverter** angir du **dynamics-ecom-leiernavn.azurefd.net**.
1. Under **Mønstre som skal samsvare** angir du **/\*** i det øvre feltet.
1. Under **Rutedetaljer** angir du alternativet **Rutetype** til **Fremover**.
1. I feltet **Serverdelsutvalg** velger du **ecom-backend**.
1. I feltet **Videresendingsprotokoll** velger du alternativet **Samsvar forespørsel**. 
1. Angi at alternativet **URL rewrite** skal være **Deaktivert**.
1. Angi at alternativet **Bufring** skal være **Deaktivert**.


> [!WARNING]
> Hvis domenet du skal bruke, allerede er aktivt og direkte, oppretter du en støtteforespørsel fra **Støtte**-flisen i [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) for å få hjelp til de neste trinnene. Hvis du vil ha mer informasjon, kan du se [Få støtte for økonomi- og driftsapper eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Hvis domenet er nytt og det ikke er et direkte domene som allerede finnes, kan du legge til det egendefinerte domenet i konfigurasjonen for Azure Front Door Service. Dette vil gjøre det mulig for nettrafikk å dirigere til nettstedet ditt via Azure Front Door-forekomsten. Hvis du vil legge til det egendefinerte domenet (for eksempel `www.fabrikam.com`), må du konfigurere et kanonisk navn (CNAME) for domenet.

Følgende illustrasjon viser dialogboksen **CNAME-konfigurasjon** i Azure Front Door Service.

![Dialogboksen CNAME-konfigurasjon.](./media/CNAME_Configuration.png)

Du kan bruke Azure Front Door Service til å administrere sertifikatet, eller du kan bruke ditt eget sertifikat for det egendefinerte domenet.

Den følgende illustrasjonen viser dialogboksen for **HTTPS for egendefinert domene** i Azure Front Door Service.

![Dialogboksen for HTTPS for egendefinert domene.](./media/Custom_Domain_HTTPS.png)

Hvis du vil ha detaljerte instruksjoner om hvordan du legger til et tilpasset domene i Azure Front Door, kan du se [Legge til et egendefinert domene i Front Door](/azure/frontdoor/front-door-custom-domain).

CDN skal nå være riktig konfigurert slik at det kan brukes sammen med ditt handelsområde.

## <a name="additional-resources"></a>Tilleggsressurser

[Implementeringsalternativer for innholdsleveringsnettverk](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
