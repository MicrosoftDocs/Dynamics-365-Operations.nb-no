---
title: Oversikt over evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce-evalueringsmiljøet.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599769"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>Oversikt over evalueringsmiljø for Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce-evalueringsmiljøet.

> [!NOTE]
> Commerce-evalueringsmiljøer er ikke generelt tilgjengelige, og gis til partnere og kunder på et per forespørsel-grunnlag. Hvis du vil ha mer informasjon, ta kontakt med din Microsoft-partnerkontakten din.

## <a name="overview"></a>Oversikt

Commerce-evalueringssmiljøet er et valgfritt ende-til-ende-miljø for Dynamics 365 Commerce som gjør det mulig for partnere og potensielle kunder å prøve ut Commerce-produktet.

Evalueringsmiljøer er delvis forhåndskonfigurert til å redusere de nødvendige trinnene etter klargjøring.

I tillegg til noen mindre begrensninger som ikke påvirker funksjonalitet, gir Commerce-evalueringsmiljøet den komplette Commerce-opplevelsen, og kan brukes av kunder og implementeringspartnere til å evaluere produktet, gi tilbakemelding og utføre tilpassings-/gapanalyse.

## <a name="limitations-of-the-commerce-evaluation-environment"></a>Begrensninger i evalueringsmiljøet for Commerce

Selv om evalueringsmiljøet i Commerce inneholder det fullstendige settet med Commerce-funksjoner, er det noen mindre begrensninger:

- Selv om selve Commerce-evalueringsmiljøet ikke har noen geografiske begrensninger, skal komponenter i miljøet, for eksempel Retail Cloud Scale Unit (RCSU) og e-handelsprogrammer, bare klargjøres i USA.
- Bruk av evalueringsmiljøet for Commerce har en 30-dagers tidsbegrensning fra datoen for klargjøring av e-handel.
- Evalueringsmiljøet for Commerce kan med hell distribueres og initialiseres bare i et miljø som bruker demonstrasjonstopologien, der alle komponentene i et miljø distribueres på én enkelt skybasert virtuell maskin (VM). Den største begrensningen for denne topologien er antall samtidige brukere som miljøet kan støtte.

## <a name="get-started"></a>Kom i gang

Hvis du vil klargjøre evalueringsmiljøet for Commerce, kan du se [Klargjøre et Commerce-evalueringsmiljø](provisioning-guide.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Klargjøre et evalueringsmiljø for Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce](cpe-bopis.md)

[Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce](cpe-optional-features.md)

[Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)
