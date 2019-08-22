---
title: Mva-betalinger og avrundingsregler
description: Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835004"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Mva-betalinger og avrundingsregler

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.

Med jevne mellomrom må mva rapporteres og betales til skattemyndighetene. Dette kan gjøres ved å kjøre prosessen for utligning og postering av mva på Merverdiavgift-siden. Merverdiavgift for en periode utlignes mot mva-kontoene, og mva-saldoen posteres til mva-utligningskontoen. Mva-saldoen, som posteres på mva-oppgjørskontoen, kan avrundes hvis skattemyndighetene krever det, ved å definere en avrundingsregel på Merverdiavgift-siden. 

Avrundingsdifferansen posteres til mva-avrundingskontoen som velges i feltet Kontoer for automatiske transaksjoner i økonomimodulen.

Eksemplet nedenfor viser hvordan avrundingsregelen i Skattemyndighet fungerer.

## <a name="examples"></a>Eksempler

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
| Egen fordel, for en debetsaldo  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a>Ingen avrunding i det hele tatt, siden avrundingen er 0,00

avrunding (1,0151, 0,00) = 1,0151 avrunding (1,0149, 0,00) = 1,0149

### <a name="normal-round-and-round-precision-is-001"></a>Vanlig avrunding, og avrundingspresisjon er 0,01

<table>
  <tr>
    <td>Avrunding
    </td>
    <td>Beregningsprosessen
    </td>
  </tr>
    <tr>
    <td>avrunding (1,015, 0,01) = 1,02
    </td>
    <td>
      <ol>
        <li>avrunding (1,015 / 0,01, 0) = avrunding (101,5, 0) = 102
        </li>
        <li>102 * 0,01 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>avrunding (1,014, 0,01) = 1,01
    </td>
    <td> <ol>
        <li>avrunding (1,014 / 0,01, 0) = avrunding (101,4, 0) = 101
        </li>
        <li>101 * 0,01 = 1,01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>avrunding (1,011, 0,02) = 1,02
    </td>
    <td> <ol>
        <li>avrunding (1,011 / 0,02, 0) = avrunding (50,55, 0) = 51
        </li>
        <li>51 * 0,02 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>avrunding (1,009, 0,02) = 1,00
    </td>
    <td> <ol>
        <li>avrunding (1,009 / 0,02, 0) = avrunding (50,45, 0) = 50
        </li>
        <li>50 * 0,02 = 1,00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Hvis du velger Egen fordel, skjer avrundingen alltid til fordel for den juridiske enheten. 

Hvis du vil ha mer informasjon, se følgende emner:
- [Oversikt over merverdiavgift](indirect-taxes-overview.md)
- [Opprette en mva-betaling](tasks/create-sales-tax-payment.md)
- [Opprette salgstransaksjoner på dokumenter](tasks/create-sales-tax-transactions-documents.md)
- [Vise posterte mva-transaksjoner](tasks/view-posted-sales-tax-transactions.md)
- [avrundingsfunksjon](https://msdn.microsoft.com/library/aa850656.aspx)


