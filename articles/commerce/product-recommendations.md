---
title: Oversikt over produktanbefalinger
description: Dette emnet inneholder generell informasjon om produktanbefalinger. Produktanbefalinger gjør at kundene enkelt og raskt kan finne produkter de vil ha, og til og med produkter de ikke opprinnelig hadde tenkt å kjøpe.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1769af6663a040c699449eb53841b3f72ab433e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972377"
---
# <a name="product-recommendations-overview"></a>Oversikt over produktanbefalinger

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce kan brukes til å vise produktanbefalinger på webområdet for e-handel og salgsstedsenheten. Produktanbefalinger er varer som en kunde kan være interessert i. Anbefalingene er basert på kjøpstendensene for andre kunder i nettbutikker og fysiske butikker.

Produktanbefalinger gjør at kundene enkelt og raskt kan finne produkter de vil ha, samtidig som de får en god handleopplevelse. Krysssalg og ettersalg kan til og med brukes til å hjelpe kunder med å finne flere produkter enn de opprinnelig hadde til hensikt å kjøpe. Når anbefalinger brukes til å hjelpe med produktoppdaging, kan de opprette flere konverteringsmuligheter, øke salgsinntektene og til og med bidra til å forbedre kundetilfredsheten og -loyaliteten.

I e-handel er produktanbefalinger basert på Microsofts anbefalinger fra teknologi for maskinlæring i stor skala.

## <a name="recommendation-service"></a>Anbefalingstjeneste

Produktanbefalingstjenesten benytter kunstig intelligens og maskinopplæring (AI-ML)-teknologier på følgende måte:

- Data i formatet som anbefalingstjenesten krever, trekkes ut fra den operative Commerce-databasen og sendes til Azure Data Lake Storage eller enhetslageret.
- Anbefalingstjenesten bruker de lagrede dataene til å lære opp anbefalingsmodeller for listene **Folk liker også**, **Ofte kjøpt sammen**, **Nye**, **Bestselgere** og **Tendenser**.

## <a name="scenarios"></a>Scenarier

Produktanbefalingene er tilgjengelige for følgende scenarier:

- **På en hvilken som helst butikkside for weblesing eller startside i e-handel**: Hvis kunder eller butikkmedarbeidere besøker en butikkside, kan anbefalingsmotoren foreslå produkter i listene **Nye**, **Bestselgere** og **Tendenser**.
- **På Produktdetaljer-siden:** Hvis kunder eller butikkmedarbeidere besøker en **Produktdetaljer**-side, foreslår anbefalingsmotoren ekstra varer som også sannsynligvis blir kjøpt. Disse elementene vises i listen **Folk liker også**.
- **På transaksjonssiden eller utsjekkingssiden:** Anbefalingsmotoren foreslår varer basert på hele listen med elementer i handlekurven. Disse varene vises i listen **Ofte kjøpt sammen**.
- **Tilpassede anbefalinger:** Forhandlere kan tilby påloggede kunder en tilpasset **Plukkinger for deg**-liste i tillegg til ny funksjonalitet som tillater tilpassing av eksisterende listescenarioer basert på den aktuelle kunden. Hvis du vil finne ut mer, kan du se [Aktivere personlige anbefalinger](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Typer produktanbefalinger

Følgende tabell beskriver ulike typer automatiserte produktanbefalinger som er tilgjengelige for forhandlere som skal implementeres i Dynamics 365 Commerce-løsningen via [produktsamlingsmodulen](product-collection-module-overview.md). Forhandlere kan også vise personlige resultater for en pålogget bruker hvis områdeforfatteren velger dette alternativet.

| Produktsamlingsmodul  | Type | beskrivelse |
|----------------------------|------|-------------|
| Nye                        | Algoritme | Denne modulen viser en liste over de nyeste produktene som nylig er assortert til kanaler og kataloger. |
| Bestselgere               | Algoritme | Denne modulen viser en liste over produkter som er rangert etter det høyeste salgstallet. |
| Populære                   | Algoritme | Denne modulen viser en oversikt over produkter med høyest ytelse for en gitt periode, rangert etter det høyeste salgstallet.  |
| Kjøpes ofte sammen | AI-ML | Denne modulen anbefaler en liste over produkter som vanligvis kjøpes sammen med innholdet fra forbrukeres gjeldende handlevogn. |
| Andre liker også           | AI-ML | Denne modulen anbefaler produkter for et angitt seed-produkt, basert på forbrukskjøpsmønstre. |
| Plukkinger for deg              | AI-ML | Denne modulen anbefaler en personlig liste over produkter basert på kjøpsmønstre til den påloggede brukeren. For en gjestebruker vil denne listen være skjult. |

## <a name="additional-resources"></a>Tilleggsressurser

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Aktivere Kjøp lignende utseender-anbefalinger](shop-similar-looks.md)

[Legge til produktanbefalinger på salgssted](product.md)

[Legge til anbefalinger i transaksjonsskjermbildet](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)
