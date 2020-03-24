---
title: Opprette anbefalinger med demonstrasjonsdata
description: Dette dokument gir råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2e790d78b4d5216822ffda3a3895feb674876bd8
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127842"
---
# <a name="create-recommendations-with-demo-data"></a>Opprette anbefalinger med demonstrasjonsdata

[!include [banner](includes/banner.md)]

Dette dokument gir råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.

Produktanbefalinger for omnikanal gir et sett med kuraterte eller programmatisk genererte produktlister. Disse listene kan brukes i flere scenarier, avhengig av forretningsbehovet. Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).

Produktanbefalinger for Lag 2-miljøer og høyere Dynamics 365-miljøer beregnes automatisk basert på kundedata. Bruk av demonstrasjonsdata for produktanbefalinger deaktiverer ikke produktanbefalingerløsninger som allerede er klargjort i miljøet og kostnadene som er knyttet til bruken.

Produktanbefalinger for Lag 1-miljøer er bare basert på statiske demonstrasjonsdata som er lagret i en CSV-fil.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Aktivere demonstrasjonsdata for produktanbefalinger i et miljø
For å aktivere demonstrasjonsdata for produktanbefalinger må du distribuere Dynamics 365 Commerce-forhåndsvisningens demonstrasjonsutvidelse til det aktuelle miljøet. Når du gjør dette, aktiveres demonstrasjonsdata for produktanbefalinger automatisk.

## <a name="default-demo-data"></a>Standard demonstrasjonsdata
Alle miljøer i én boks leveres med forhåndslastede demonstrasjonsdata for produktanbefalinger som er lagret i den kommadelte filen reco_demo_data.csv, som er plassert på Commerce Scale Unit.

Dataene er strukturert langs følgende kolonner.

| Kolonnenavn         | Obligatorisk          | Beskrivelse                                                                                                                                 | Mulige verdier                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Den spesifikke listetypen for produktanbefaling som demonstrasjonsdatapunktet skal generere.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Det spesifikke driftsenhetsnummeret der produktanbefalinger forventes å vises.                                        |                                                                              |
| Kategori            |                    |    Kategorien som den bestemte listen skal returneres for. Hvis det ikke er angitt en kategori, er listen bare for øverste navigasjonshierarki.    |                                                                              |
| SeedItemId          |                    |    For lister som krever utgangsverdi (RecoPeopleAlsoBuy og RecoCart) må produktlistene vise flere produkter.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Ett eller flere produkter som skal returneres som resultat, atskilt med ';'.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Tilpass demonstrasjonsdata
Du kan redigere standard demonstrasjonsdata med all produkt- og kategoriinformasjon konfigurert i HK. Når du oppdaterer CSV-filen, vil produktanbefalingene som returneres til kunder, umiddelbart gjenspeile endringene.

Utvidelsen inneholder en datafil med navnet RecoMockDataset.csv, som lar deg kontrollere datasettet som brukes for de uekte anbefalingene. Filnavnet kan styres via konfigurasjon av utvidelsen ved hjelp av innstillingen **ext.Recommendations.DemoFilePath**. Dette gjør det mulig for deg å ha flere datasett tilgjengelige som enkelt kan byttes ved hjelp av konfigurasjon.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere ADLS i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Legge til lister over anbefalinger på et e-handelsområde](add-reco-list-to-page.md)

[Legge til produktanbefalinger i POS](product.md)

[Legge til anbefalinger på transaksjonsskjermen](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)
