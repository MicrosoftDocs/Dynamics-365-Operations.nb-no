---
title: Demonstrasjonsdata for produktanbefalinger for omnikanal
description: Målet med dette dokument er å gi råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2226277"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Demonstrasjonsdata for produktanbefalinger for omnikanal

Målet med dette dokument er å gi råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.

Produktanbefalinger for omnikanal gir et sett med ordnet liste over produkter som er kuratert eller programmatisk generert. Disse listene kan brukes i flere scenarier, avhengig av forretningsbehovet. Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendaitons-overview.md)

Produktanbefalinger for Lag 2-miljøer og høyere for Dynamics, beregnes automatisk basert på kundedata.
Bruk av demonstrasjonsdata for produktanbefalinger deaktiverer ikke produktanbefalingerløsninger som allerede er klargjort i miljøet og kostnadene som er knyttet til bruken.

Produktanbefalinger for Lag 1-miljøer er bare basert på statiske demonstrasjonsdata som er lagret i en CSV-fil.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Aktivere demonstrasjonsdata for produktanbefalinger i et miljø

Kunder må distribuere **Dynamics 365 Commerce-forhåndsvisningens demonstrasjonsutvidelse** til det aktuelle miljøet, som automatisk aktiverer demonstrasjonsdata for produktanbefalinger.

## <a name="default-demo-data"></a>Standard demonstrasjonsdata
Alle miljøer i én boks leveres med forhåndslastede demonstrasjonsdata for produktanbefalinger som er lagret i den kommadelte filen **reco_demo_data.csv**, som er plassert i samme mappe som dette dokumentet på Retail Server.

Disse dataene er strukturert langs følgende kolonner

| Kolonnenavn         | Obligatorisk          | Beskrivelse                                                                                                                                 | Mulige verdier                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Den spesifikke listetypen for produktanbefaling som demonstrasjonsdatapunktet skal generere.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Det spesifikke driftsenhetsnummeret der produktanbefalinger forventes å vises.                                        |                                                                              |
| Kategori            |                    |    Kategorien som den bestemte listen skal returneres for. Hvis det ikke er angitt en kategori, er listen bare for øverste navigasjonshierarki.    |                                                                              |
| SeedItemId          |                    |    For lister som krever utgangsverdi (RecoPeopleAlsoBuy og RecoCart) må produktlistene vise flere produkter.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Ett eller flere produkter som skal returneres som resultat, atskilt med **";"**.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Tilpass demonstrasjonsdata
Kunder kan redigere standard demonstrasjonsdata med all produkt- og kategoriinformasjon som er konfigurert i HK. Når CSV er oppdatert, vil produktanbefalingene som returneres til kunder, umiddelbart gjenspeile endringene.

Utvidelsen inneholder en datafil med navnet RecoMockDataset.csv, som lar kunden kontrollere datasettet som brukes til for de uekte anbefalingene. Filnavnet kan styres via konfigurasjon av utvidelsen ved hjelp av innstillingen **ext.Recommendations.DemoFilePath**. Dette gjør det mulig for kundene å ha flere datasett tilgjengelige som enkelt kan byttes ved hjelp av konfigurasjon.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations-overview.md)

[Miljøplanlegging](environment-planning.md)
