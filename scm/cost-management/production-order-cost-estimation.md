---
title: Kostnadsberegning for produksjonsordrer
description: "Denne artikkelen inneholder informasjon om kostnadsestimat for produksjonen. Kostnadsestimat for produksjonen gir deg forventede kostnader til materialer og kapasitetsforbruk som går med i produksjon av en vare i produksjonsforslagets antall."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3d43b186335b42fd5b7b6c84456d012f51b26799
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-cost-estimation"></a>Kostnadsberegning for produksjonsordrer

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon om kostnadsestimat for produksjonen. Kostnadsestimat for produksjonen gir deg forventede kostnader til materialer og kapasitetsforbruk som går med i produksjon av en vare i produksjonsforslagets antall. 

Når du oppretter en produksjonsordre, må du beregne produksjonskostnader. Formålet er å gi et estimat for vare- og ruteforbruk for produksjonsprosessen, fordi disse estimatene brukes som grunnlaget for fremtidige planleggings- og produksjonsprosesser.

## <a name="production-cost-estimation"></a>Kostnadsberegning for produksjon
Estimater for produksjonskostnader er basert på følgende informasjon:

-   Antallet for produksjonsordren.
-   Komponentene i produksjonsstykklistene
-   Ruteoperasjonene i produksjonsruten
-   De indirekte kostnadene som gjelder for komponenter og operasjoner
-   De aktive kostnadsdataene på beregningsdatoen

Hvis det finnes en fantomvarelinje i produksjonsstykklisten, gjenspeiler beregningene fantomvarens komponenter og rutingoperasjoner. Du kan bruke estimeringsoppgaven til å omberegne kostnadsestimater, slik at de gjenspeiler oppdatert informasjon. Den oppdaterte informasjonen kan for eksempel være endringer i antallet i produksjonsordren, komponentene i produksjonsstykklisten, ruteoperasjonene i produksjonsruten, de indirekte kostnadene som gjelder for disse komponentene og operasjonene, eller de aktive kostnadsdataene på omberegningsdatoen. Beregningene av kostnadsestimatet foreslår også en salgspris for produksjonsvaren basert på kostnader pluss påslag. Beregningene av kostnadsestimatet kan om ønskelig også brukes på referanseordrer som gjenspeiler andre produksjonsordrer som er knyttet til produksjonsordren.

## <a name="view-the-estimated-costs"></a>Vise de estimerte kostnadene
Når du har kjørt anslag, kan du vise resultatene på siden **Prisberegning**. Anslaget beregner følgende verdier:

-   **Produksjonskostnad** – Produksjonskostnaden er den øverste linjen i estimatet. Den viser de samlede kostnadene fra kjøring av produksjonsordren og samlet salgspris for produksjonen. Det er summen av alle kostnadslinjer i estimatet.
-   **Rute- eller kostnader** – Rute- eller ressurskostnadene er kostnadene for produksjonsoperasjonene. De inkluderer kostnadene for elementer som oppstillingstid, operasjonstid og administrasjonskostnader.
-   **Materialkostnader** – Materialkostnader er kostnadene og prisene fra stykklistekomponenter som kreves for å produsere varen. Disse kostnadene er på forhånd fastsatt og registrert i systemet.

## <a name="other-uses-of-cost-estimation"></a>Annen bruk av kostnadsestimater
Et kostnadsestimat gir også følgende informasjon:

-   Nyttige pristilbud.
-   Estimater for ordrens lønnsomhet
-   Estimater for råvareforbruk
-   Sammenligninger av kostnadsinformasjon fra tidligere produksjoner
-   Budsjett- og prognoseinformasjon
-   Estimater for produksjonsstørrelsen som kreves for å beholde en bestemt kostnad




