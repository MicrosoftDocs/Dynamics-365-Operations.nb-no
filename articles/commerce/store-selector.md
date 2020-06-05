---
title: Butikkvelgermodul
description: Dette emnet dekker butikkvelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378214"
---
# <a name="store-selector-module"></a>Butikkvelgermodul

[!include [banner](includes/banner.md)]

Dette emnet dekker butikkvelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En butikkvelgermodul brukes til kundescenarioet "Kjøpe på Internett og hente i butikk" (BOPIS). Det viser en liste over butikker der et produkt er tilgjengelig for henting, i tillegg til butikkens åpningstimer og produktbeholdninger for hver butikk.

Butikkvelgermodulen krever konteksten for et produkt og en søkeplassering for å finne butikker. Ved fravær av en søkeplassering, brukes som standard kundens leserplassering, forutsatt at kunden gir samtykke. Modulen har en inndataboks som gir kunden muligheten til å angi en lokasjon (postnummer, poststed og delstat) for å finne butikker som er i nærheten.

Butikkvelgermodulen er integrert med API-en (programmeringsgrensesnittet) for Bing-kart-geoplasseringsprogrammet for å konvertere lokasjonen til en breddegrad og lengdegrad. En API-nøkkel for Bing-kart kreves, og den må legges til på siden Delte parametere for Commerce i Dynamics 365 Commerce.

Butikkvelgermodulen kan legges til en kjøpsboksmodul på produktdetaljsiden (PDP) for å vise butikkene der et produkt er tilgjengelig for henting. Den kan også legges til i en handlekurvmodul. Når butikkvelgermodulen legges til i en handlekurvmodul, vises hentealternativer for hvert linjeelement for handlekurven. I tillegg kan denne modulen med egendefinert koding legges til andre sider eller moduler via utvidelser og tilpassinger.

For at BOPIS-scenarioet skal fungere, bør produktene konfigureres med leveringsmodusen "kundehenting". Ellers vil ikke modulen vises på de respektive sidene. Hvis du vil ha informasjon om hvordan du konfigurerer leveringsmodus, kan du se [Definer leveringsmåter](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Bildet nedenfor viser et eksempel på en butikkvelgermodul som brukes på en PDP.

![Eksempel på en butikkvelgermodul](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Bruk av butikkvelgermodul i e-handel

- En butikkvelgermodul kan brukes på en produktdetaljside (PDP) for å finne nærliggende butikker der et produkt er tilgjengelig for henting.
- En butikkvelgermodul kan brukes på en handlekurvside for å finne nærliggende butikker der et produkt i handlekurven er tilgjengelig for henting.

## <a name="store-selector-module-properties"></a>Egenskaper for butikkvelgermodul

| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Søkeradius | Tall | Definerer søkeradius for butikkene, i mil. Hvis ingen verdi er angitt, brukes standard søkeradius på 50 engelske mil.|
|Vilkår for bruk | URL    |  URL-adressen for vilkår for bruk kreves for Bing-kart-tjenesten. |

## <a name="add-a-store-selector-module-to-a-page"></a>Legge til en butikkvelgermodul på en side

En butikkvelgermodul trenger konteksten til et produkt, og kan derfor bare brukes i kjøpsboks- og handlemoduler. Butikkvelgermoduler fungerer ikke utenfor disse modulene.

- Hvis du vil ha informasjon om hvordan du legger til en butikkvelgermodul i en kjøpsboksmodul, kan du se [Kjøpsboksmodul](add-buy-box.md). 
- Hvis du vil ha informasjon om hvordan du legger til en butikkvelgermodul i en handlekurvmodul, kan du se [Handlekurvmodul](add-cart-module.md)

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Hurtiginnføring i PDP](quick-tour-pdp.md)

[Hurtiginnføring i handlekurv og kasse](quick-tour-cart-checkout.md)

[Definer leveringsmåter](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Behandle Bing-kart for organisasjonen](dev-itpro/manage-bing-maps.md)
