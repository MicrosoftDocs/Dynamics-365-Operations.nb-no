---
title: Oversikt over produktanbefalinger
description: Dette emnet inneholder generell informasjon om produktanbefalinger. Produktanbefalinger gjør at kundene enkelt og raskt kan finne produkter de vil ha, og til og med produkter de ikke opprinnelig hadde tenkt å kjøpe.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024985"
---
# <a name="product-recommendations-overview"></a>Oversikt over produktanbefalinger

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce kan brukes til å vise produktanbefalinger på webområdet for e-handel og salgsstedsenheten. Produktanbefalinger er varer som en kunde kan være interessert i. Anbefalingene er basert på kjøpstendensene for andre kunder i nettbutikker og fysiske butikker.

Produktanbefalinger gjør at kundene enkelt og raskt kan finne produkter de vil ha, samtidig som de får en god handleopplevelse. Krysssalg og ettersalg kan til og med brukes til å hjelpe kunder med å finne flere produkter enn de opprinnelig hadde til hensikt å kjøpe. Når anbefalinger brukes til å hjelpe med produktoppdaging, kan de opprette flere konverteringsmuligheter, øke salgsinntektene og til og med bidra til å forbedre kundetilfredsheten og -loyaliteten.

I Commerce er produktanbefalinger basert på Microsofts anbefalinger fra teknologi for maskinlæring i stor skala.


## <a name="scenarios"></a>Scenarier

Produktanbefalingene er tilgjengelige for følgende scenarier:

- **På en hvilken som helst butikkside for weblesing eller startside i e-handel**: Hvis kunder eller butikkmedarbeidere besøker en butikkside, kan anbefalingsmotoren foreslå produkter i listene **Nye**, **Bestselgere** og **Tendenser**.
- **På Produktdetaljer-siden:** Hvis kunder eller butikkmedarbeidere besøker en **Produktdetaljer**-side, foreslår anbefalingsmotoren ekstra varer som også sannsynligvis blir kjøpt. Disse elementene vises i listen **Folk liker også**.
- **På transaksjonssiden eller utsjekkingssiden:** Anbefalingsmotoren foreslår varer basert på hele listen med elementer i handlekurven. Disse varene vises i listen **Ofte kjøpt sammen**.
- **Tilpassede anbefalinger:** Forhandlere kan tilby påloggede kunder en tilpasset **Plukkinger for deg**-liste i tillegg til ny funksjonalitet som tillater tilpassing av eksisterende listescenarioer basert på den aktuelle kunden. Hvis du vil ha mer informasjon, kan du se funksjonsdokumentasjonen: [Aktivere personlige anbefaleringer.](personalized-recommendations.md)

## <a name="recommendation-service"></a>Anbefalingstjeneste

Produktanbefalinger bruker maskinlæringsteknologi for anbefalinger på følgende måte:

- Data i formatet som anbefalingstjenesten krever, trekkes ut fra den operative Commerce-databasen og sendes til enhetslageret.
- Anbefalingstjenesten bruker dataene til å lære opp anbefalingsmodeller for listene **Folk liker også**, **Ofte kjøpt sammen**, **Nye**, **Bestselgere** og **Tendenser**.

## <a name="additional-resources"></a>Tilleggsressurser

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Oversikt over produktsamlingsmodul](product-collection-module-overview.md)

[Opprette kuraterte produktanbefalingslister](create-editorial-recommendation-lists.md)

[Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md)

[Legge til produktanbefalingslisten på sider](add-reco-list-to-page.md)
