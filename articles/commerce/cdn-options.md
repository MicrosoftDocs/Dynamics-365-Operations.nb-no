---
title: Implementeringsalternativer for innholdsleveringsnettverk
description: Dette emnet gjennomgår de ulike alternativene for CDN-implementering (Content Delivery Network) som kan brukes i Microsoft Dynamics 365 Commerce-miljøer. Disse alternativene omfatter innebygde, Commerce-formidlede forekomster av Azure Front Door og kundeeide forekomster av Azure Front Door.
author: BrianShook
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: eec18dbffe33bc6366b4282d05189b31620616d6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351255"
---
# <a name="content-delivery-network-implementation-options"></a>Implementeringsalternativer for innholdsleveringsnettverk

[!include [banner](includes/banner.md)]

Dette emnet gjennomgår de ulike alternativene for CDN-implementering (Content Delivery Network) som kan brukes i Microsoft Dynamics 365 Commerce-miljøer. Disse alternativene omfatter innebygde, Commerce-formidlede forekomster av Azure Front Door og kundeeide forekomster av Azure Front Door.

Commerce-kunder har flere alternativer når de vurderer hvilken CDN-tjeneste som skal brukes med Commerce-miljøet. Commerce frigis med grunnleggende støtte for Azure Front Door, som dekker grunnleggende driftingskrav og egendefinerte domenekrav. For firmaer som vil ha mer kontroll og mer spesifikke sikkerhetsegenskaper, for eksempel webprogrambrannmur (WAF), kan det være best å bruke enten en kundeeid forekomst av Azure Front Door eller en ekstern CDN-tjeneste.

Følgende tre CDN-implementeringsalternativer kan brukes med Commerce-miljøer:

- Den Commerce-formidlede forekomsten av Azure Front Door
- En kundeeid forekomst av Azure Front Door (for økt kontroll og flere sikkerhetsfunksjoner)
- En ekstern CDN-tjeneste

Alle de tre CDN-implementeringsalternativene leverer bare dynamisk HTML-innhold fra egendefinerte domener. Commerce håndterer automatisk alle JavaScript, gjennomgripende stilark (CSS), bilder, video og annet statisk innhold via Microsoft-administrerte CDN-er. Alternativet du velger, fastslår driftsfunksjonene, kontrollfunksjonene og ytterligere sikkerhetsfunksjoner som er tilgjengelige.

Illustrasjonen nedenfor viser en oversikt over Commerce-arkitekturen.

![Oversikt over Commerce-arkitekturen.](media/Commerce_CDN-Option_ComparisonModels.png)

Hvis du vil ha mer informasjon om hvordan du definerer en forekomst av Azure Front Door for Commerce-området, kan du se [Legg til CDN-støtte](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Bruke den Commerce-formidlede forekomsten av Azure Front Door

I tabellen nedenfor finner du en oversikt over fordeler og ulemper ved å bruke den Commerce-formidlede forekomsten av Azure Front Door til å administrere innholdsendepunkt.

| Fordeler | Ulemper |
|------|------|
| <ul><li>Forekomsten er inkludert i Commerce-kostnaden.</li><li>Ettersom forekomsten administreres av Commerce-teamet, kreves det mindre vedlikehold, og det finnes trinn for delt oppsett.</li><li>Den Azure-driftede infrastrukturen er skalerbar, sikker og pålitelig.</li><li>SSL-sertifikatet (Secure Sockets Layer) krever et engangsoppsett og fornyes automatisk.</li><li>Forekomsten blir overvåket for feil og mangler av Commerce-teamet.</li></ul> | <ul><li>En WAF støttes ikke.</li><li>Det finnes ingen bestemte tilpassinger eller justeringer.</li><li>Forekomsten avhenger av Commerce-teamet for oppdateringer eller endringer.</li><li>En separat forekomst av Azure Front Door kreves for apex-domener, og det kreves ekstra arbeid for å integrere apex-domener Azure DNS.</li><li>Det er ikke angitt noe telemetri om svar per andre (RPS) eller om feilraten til kunden.</li></ul> |

Illustrasjonen nedenfor viser arkitekturen i forekomsten av den Commerce-formidlede forekomsten for Azure Front Door.

![Commerce-formidlet forekomst av Azure Front Door.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Bruke en kundeeid forekomst av Azure Front Door

I tabellen nedenfor finner du en oversikt over fordeler og ulemper ved å bruke en kundeeid forekomst av Azure Front Door til å administrere innholdsendepunkt.

| Fordeler | Ulemper |
|------|------|
| <ul><li>Oppsettet er sikkert og enkelt å administrere.</li><li>Den Azure-driftede infrastrukturen er skalerbar, sikker og pålitelig.</li><li>Forekomsten tillater WAF-integrering og granulære regelkontroller for mer detaljert sikkerhet som er tilpasset spesielt for området.</li><li>Forekomsten gir bedre kontroll over SSL-sertifikater (både kundeeide og Azure Front Door-administrerte) og domenekobling.</li><li>Forekomsten tilbyr en apex-domeneløsning hvis den er paret direkte med Azure DNS.</li><li>Telemetri og varsling følger med.</li><li>SSL-sertifikatet krever et engangsoppsett og fornyes automatisk.</li></ul> | <ul><li>Forekomsten er selvstyrt.</li><li>Innledende kunnskapsoppgradering er nødvendig.</li></ul> |

Illustrasjonen nedenfor viser en Commerce-infrastruktur som omfatter en kundeeid forekomst av Azure Front Door.

![Commerce-infrastruktur som omfatter en kundeeid forekomst av Azure Front Door.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Bruke en ekstern CDN-tjeneste

I tabellen nedenfor finner du en oversikt over fordeler og ulemper ved bruk av en ekstern CDN-tjeneste for å administrere innholdsendepunkter.

| Fordeler | Ulemper |
|------|------|
| <ul><li>Dette alternativet er nyttig når det eksisterende domenet allerede er vert for en ekstern CDN.</li><li>Konkurrerende CDN-er (for eksempel Akamai) kan ha flere WAF-funksjoner.</li></ul> | <ul><li>En separat kontrakt og ekstra etterkalkulering kreves.</li><li>SSL kan påløpe ekstra kostnader.</li><li>Ettersom tjenesten er atskilt fra skystrukturen i Azure, må tilleggsinfrastruktur administreres.</li><li>Tjenesten kan kreve lengre tidsinvesteringer i endepunkts- og sikkerhetsoppsett.</li><li>Tjenesten er selvstyrt.</li><li>Tjenesten er selvovervåket.</li></ul> |

Illustrasjonen nedenfor viser en Commerce-infrastruktur som omfatter en ekstern CDN-tjeneste.

![Commerce-infrastruktur som omfatter en ekstern CDN-tjeneste.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)
