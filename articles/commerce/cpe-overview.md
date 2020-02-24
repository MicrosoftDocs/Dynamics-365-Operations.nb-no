---
title: Oversikt over miljø for forhåndsvisning av Dynamics 365 Commerce
description: Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljøet.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024689"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a>Oversikt over miljø for forhåndsvisning av Dynamics 365 Commerce


[!include [banner](includes/banner.md)]

Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljøet.

## <a name="overview"></a>Oversikt

Commerce-forhåndsvisningsmiljøet er et valgfritt ende-til-ende forhåndsvisningsmiljø for Dynamics 365 Commerce som gjør det mulig for potensielle kunder prøve ut Commerce-produktet før den generelle utgivelsen til offentligheten.

I tillegg til noen mindre begrensninger som ikke påvirker funksjonalitet, gir forhåndsvisningsmiljøet i Commerce den komplette Commerce-opplevelsen, og kan brukes av kunder og implementeringspartnere til å evaluere produktet, gi tilbakemelding og utføre tilpassings-/gapanalyse.

## <a name="limitations-of-the-commerce-preview-environment"></a>Begrensninger i forhåndsvisningsmiljøet for Commerce

Selv om forhåndsvisningsmiljøet i Commerce inneholder det fullstendige settet med Commerce-funksjoner, er det noen mindre begrensninger:

- Selv om selve Commerce-forhåndsvisningsmiljøet ikke har noen geografiske begrensninger, kan komponenter i miljøet, for eksempel Retail Cloud Scale Unit (RCSU) og e-handelsprogrammer, bare klargjøres i USA.
- Bruk av forhåndsvisningsmiljøet for Commerce har en 30-dagers tidsbegrensning fra datoen for klargjøring av e-handel.
- Forhåndsvisningsmiljøet for Commerce kan med hell distribueres og initialiseres bare i et miljø som bruker demonstrasjonstopologien, der alle komponentene i et miljø distribueres i én enkelt virtuell maskin (VM). Den største begrensningen for denne OneBox VM-topologien er antall samtidige brukere som gorhåndsvisningsmiljøet kan støtte.
- Forhåndsvisningsmiljøet for Commerce kan bare evalueres til det generelle tilgjengeligheten (GA) for Commerce-produktet. Nye demomiljøer vil være tilgjengelig etter GA.

## <a name="get-started"></a>Komme i gang

Hvis du vil klargjøre forhåndsvisningsmiljøet for Commerce, kan du se [Klargjøre et Commerce-forhåndsvisningsmiljø](provisioning-guide.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Klargjøre et miljø for forhåndsvisning av Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurere et miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurere valgfrie funksjoner for et miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-optional-features.md)

[Vanlige spørsmål om miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-faq.md)
