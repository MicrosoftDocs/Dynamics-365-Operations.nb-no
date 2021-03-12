---
title: Legge til støtte for et innholdsleveringsnettverk (CDN)
description: Dette emnet beskriver hvordan du legger til et innholdsleveringsnettverk (CDN) i Microsoft Dynamics 365 Commerce-miljøet.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1d9482a45cb8f2ea52e7f58d55e30cfe56694d04
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985960"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Legge til støtte for et innholdsleveringsnettverk (CDN)


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til et innholdsleveringsnettverk (CDN) i Microsoft Dynamics 365 Commerce-miljøet.

## <a name="overview"></a>Oversikt

Når du definerer et e-handelsmiljø i Dynamics 365 Commerce, kan du konfigurere det slik at det fungerer med CDN-tjenesten. 

Ditt egendefinerte domene kan aktiveres under klargjøringsprosessen for ditt e-handelsmiljø. Du kan også bruke en serviceforespørsel for å konfigurere den etter at klargjøringsprosessen er fullført. Klargjøringsprosessen for e-handelsmiljøet genererer et vertsnavn som er knyttet til miljøet. Dette vertsnavnet har følgende format, der \<*e-commerce-tenant-name*\> er navnet på miljøet ditt:

&lt;e-handel-leier-navn&gt;.commerce.dynamics.com

Vertsnavnet eller endepunktet som genereres under klargjøringsprosessen, støtter bare et SSL-sertifikat (Secure Sockets Layer) for \*.commerce.dynamics.com. Den støtter ikke SSL for egendefinerte domener. Derfor må du avslutte SSL for egendefinerte domener i CDN og videresende trafikk fra CDN til vertsnavnet eller endepunktet som Commerce genererte. 

I tillegg betjenes *statistiske filer* (JavaScript- eller Cascading Style Sheets \[CSS\]-filer) fra Commerce fra endepunktet som Commerce genererte (\*.commerce.dynamics.com). Statistiske filer kan bare hurtigbufres hvis vertsnavnet eller endepunktet som Commerce genererte, plasseres bak CDN.

## <a name="set-up-ssl"></a>Definer SSL

For å sikre at SSL er konfigurert, og at statistiske filer bufres, må du konfigurere CDN slik at det er tilknyttet vertsnavnet som Commerce har generert for miljøet ditt. Du må også bufre det følgende mønsteret bare for statistiske filer: 

/\_msdyn365/\_scnr/\*

Når du har klargjort handelsmiljøet med det tilpassede domenet som er oppgitt, eller etter at du har angitt det egendefinerte domenet for miljøet ditt ved å bruke en tjenesteforespørsel, kan du peke det tilpassede domenet til vertsnavnet eller endepunktet som Commerce laget.

Som tidligere nevnt støtter det genererte vertsnavnet eller endepunktet bare et SSL-sertifikat for \*.commerce.dynamics.com. Den støtter ikke SSL for egendefinerte domener.

## <a name="cdn-services"></a>CDN-tjenester

Alle CDN-tjenester kan brukes med et handelsmiljø. Her er to eksempler:

- **Microsoft Azure Front Door Service** – Azure CDN-løsningen. Hvis du vil ha mer informasjon om Azure Front Door Service, se [Dokumentasjon for Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** – For mer informasjon, se [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CND-oppsett

Installasjonsprosessen for CDN består av disse generelle trinnene:

1. Legg til en frontvert.
1. Konfigurer et serverdelsutvalg.
1. Definer regler for ruting og bufring.

### <a name="add-a-front-end-host"></a>Legg til en frontvert

Alle CDN-tjenester kan brukes, men for eksempel i dette emnet brukes Azure Front Door Service. 

Hvis du vil ha informasjon om hvordan du konfigurerer Azure Front Door Service, se [Hurtigstart: Opprette en hovedinngang for et høyt tilgjengelig globalt webprogram](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Konfigurere et serverdelsutvalg i Azure Front Door Service

Følg disse trinnene for å konfigurere et serverdelsutvalg i Azure Front Door Service.

1. Legg til **&lt;ecom-leier-navn&gt;.commerce.dynamics.com** til et serverdelsutvalg som en egendefinert vert som har et tomt serverdelvertshode.
1. Under **Belastningsfordeling** lar du standardverdiene være.

Følgende illustrasjon viser dialogboksen **Legg til en serverdel** i Azure Front Door Service, der vertsnavnet for serverdelen er angitt.

![Legge til en dialogboks for serverdelsutvalg](./media/CDN_BackendPool.png)

Følgende illustrasjon viser dialogboksen **Legg til et serverdelutvalg** i Azure Front Door Service med standardverdier for belastningsfordeling.

![Legge til en dialogboks for serverdelsutvalg (fortsettelse)](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Definere regler i Azure Front Door Service

Følg disse trinnene for å opprette en rutingsregel i Azure Front Door Service.

1. Legge til en rutingsregel.
1. Angi **standard** i feltet **Navn**.
1. I feltet **Godkjent protokoll** velger du **HTTP og HTTPS**.
1. I feltet **Frontverter** angir du **dynamics-ecom-leiernavn.azurefd.net**.
1. Under **Mønstre som skal samsvare** angir du **/\** _ i det øvre feltet.
1. Under _*Rutedetaljer** angir du alternativet **Rutetype** til **Videresend**.
1. I feltet **Serverdelsutvalg** velger du **ecom-backend**.
1. I feltet **Videresendingsprotokoll** velger du alternativet **Samsvar forespørsel**. 
1. Angi at alternativet **URL rewrite** skal være **Deaktivert**.
1. Angi at alternativet **Bufring** skal være **Deaktivert**.

Følg disse trinnene for å opprette en bufringsregel i Azure Front Door Service.

1. Legg til en bufringsregel.
1. Angi **statistiske filer** i feltet **Navn**.
1. I feltet **Godkjent protokoll** velger du **HTTP og HTTPS**.
1. I feltet **Frontverter** angir du **dynamics-ecom-leiernavn.azurefd.net**.
1. Under **Mønstre som skal samsvare** i det øvre feltet angir du **/\_msdyn365/\_scnr/\** _.
1. Under _*Rutedetaljer** angir du alternativet **Rutetype** til **Videresend**.
1. I feltet **Serverdelsutvalg** velger du **ecom-backend**.
1. I feltet **Videresendingsprotokoll** velger du alternativet **Samsvar forespørsel**.
1. Angi at alternativet **URL rewrite** skal være **Deaktivert**.
1. Angi at alternativet **Bufring** skal være **Deaktivert**.
1. Velg **Bufre hver unike URL-adresse** i **Hurtigbufring for spørringsstreng**.
1. I feltet **Dynamisk komprimering** velger du alternativet **Aktivert**.

Følgende illustrasjon viser dialogboksen **Legg til en regel** i Azure Front Door Service.

![Dialogboksen Legg til en regel](./media/CDN_CachingRule.png)

> [!WARNING]
> Hvis domenet du skal bruke, allerede er aktivt og direkte, oppretter du en støtteforespørsel fra **Støtte**-flisen i [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) for å få hjelp til de neste trinnene. Hvis du vil ha mer informasjon, kan du se [Få støtte for Finance and Operations-apper eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Hvis domenet er nytt og det ikke er et direkte domene som allerede finnes, kan du legge til det egendefinerte domenet i konfigurasjonen for Azure Front Door Service. Dette vil gjøre det mulig for nettrafikk å dirigere til nettstedet ditt via Azure Front Door-forekomsten. Hvis du vil legge til det egendefinerte domenet (for eksempel `www.fabrikam.com`), må du konfigurere et kanonisk navn (CNAME) for domenet.

Følgende illustrasjon viser dialogboksen **CNAME-konfigurasjon** i Azure Front Door Service.

![Dialogboksen CNAME-konfigurasjon](./media/CNAME_Configuration.png)

Du kan bruke Azure Front Door Service til å administrere sertifikatet, eller du kan bruke ditt eget sertifikat for det egendefinerte domenet.

Den følgende illustrasjonen viser dialogboksen for **HTTPS for egendefinert domene** i Azure Front Door Service.

![Dialogboksen for HTTPS for egendefinert domene](./media/Custom_Domain_HTTPS.png)

Hvis du vil ha detaljerte instruksjoner om hvordan du legger til et tilpasset domene i Azure Front Door, kan du se [Legge til et egendefinert domene i Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).

CDN skal nå være riktig konfigurert slik at det kan brukes sammen med ditt handelsområde.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Distribuere en ny e-handelsleier](deploy-ecommerce-site.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et Dynamics 365 Commerce-nettsted til en nettkanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Laste opp masseomdirigeringer for URL-adresse](upload-bulk-redirects.md)

[Konfigurere en B2C-leier i Commerce](set-up-B2C-tenant.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)
