---
title: Mva-betalinger og avrundingsregler
description: "Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7ec117598a6a008e5b274179659b515824029874
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="sales-tax-payments-and-rounding-rules"></a>Mva-betalinger og avrundingsregler

[!include[banner](../includes/banner.md)]


Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.

Med jevne mellomrom må mva rapporteres og betales til skattemyndighetene. Dette kan gjøres ved å kjøre prosessen for utligning og postering av mva på Merverdiavgift-siden. Merverdiavgift for en periode utlignes mot mva-kontoene, og mva-saldoen posteres til mva-utligningskontoen. Mva-saldoen, som posteres på mva-oppgjørskontoen, kan avrundes hvis skattemyndighetene krever det, ved å definere en avrundingsregel på Merverdiavgift-siden. 

Avrundingsdifferansen posteres til mva-avrundingskontoen som velges i feltet Kontoer for automatiske transaksjoner i økonomimodulen.

Eksemplet nedenfor viser hvordan avrundingsregelen i Skattemyndighet fungerer.

### <a name="example"></a>Eksempel:

Den totale merverdiavgiften for en periode viser en kreditsaldo på -98 765,43. Den juridiske enheten krevde inn mer merverdiavgift enn den betalte. Derfor skylder den juridiske enheten penger til skattemyndighetene. 

Den juridiske enheten ønsker å bruke en avrundingsmetode som runder av saldoen til nærmeste 1,00. Brukeren som er ansvarlig for merverdiavgiftsregnskapet, gjør følgende:

1.  Klikk Avgift &gt; Indirekte avgifter &gt; Merverdiavgift &gt; Skattemyndigheter.
2.  Velg Normal i Avrundingsform-feltet på hurtigfanen Generelt.
3.  Angi 1,00i Avrund-feltet.
4.  Når tiden er inne for å betale merverdiavgift til skattemyndighetene, åpner du siden Utlign og poster merverdiavgift. (Klikk Avgift &gt; Deklareringer &gt; Merverdiavgift &gt; Utlign og poster merverdiavgift.)
5.  I mva-oppgjørskontoen rundes avgiftsgjeldbeløpet på 98 765,43 av til 98 765.

Tabellen nedenfor viser hvordan et beløp på 98 765,43 avrundes ved hjelp av hver avrundingsmetode som er tilgjengelig i Avrundingsform-feltet på siden Skattemyndigheter.

| Avrundingsform                | Avrundingsverdi = 0,01 | Avrundingsverdi = 0,10 | Avrundingsverdi = 1,00 | Avrundingsverdi = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Normal                              | 98 765,43              | 98 765,40              | 98 765,00              | 98 800,00                |
| Nedover                            | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Avrundes opp                         | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |
| Egen fordel, for en kreditsaldo | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Egen fordel, for en debetsaldo  | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |

> [!NOTE]                                                                                  
> Hvis du velger Egen fordel, skjer avrundingen alltid til fordel for den juridiske enheten. 

Hvis du vil ha mer informasjon, kan du se [Oversikt over merverdiavgift](indirect-taxes-overview.md). 




