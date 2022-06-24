---
title: Mva-betalinger og avrundingsregler
description: Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.
author: kailiang
ms.date: 10/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: kfend
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c24a9850543e9d08ee1726186f433c7cfd26608
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865690"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Mva-betalinger og avrundingsregler

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.

Med jevne mellomrom må mva rapporteres og betales til skattemyndighetene. Dette kan gjøres ved å kjøre prosessen for utligning og postering av mva på **Merverdiavgift**-siden. Merverdiavgift for en periode utlignes mot mva-kontoene, og mva-saldoen posteres til mva-utligningskontoen. Mva-saldoen, som posteres til mva-oppgjørskontoen, kan avrundes hvis skattemyndighetene krever det, ved å definere en avrundingsregel på **Merverdiavgift**-siden. 

Avrundingsdifferansen posteres til mva-avrundingskontoen som velges i feltet Kontoer for automatiske transaksjoner i økonomimodulen.

Eksemplet nedenfor viser hvordan avrundingsregelen i Skattemyndighet fungerer.

## <a name="examples"></a>Eksempler

Den totale merverdiavgiften for en periode viser en kreditsaldo på -98 765,43. Den juridiske enheten krevde inn mer merverdiavgift enn den betalte. Derfor skylder den juridiske enheten penger til skattemyndighetene. 

Den juridiske enheten ønsker å bruke en avrundingsmetode som runder av saldoen til nærmeste 1,00. Brukeren som er ansvarlig for merverdiavgiftsregnskapet, gjør følgende:

1. Klikk **Avgift** > **Indirekte avgifter** > **Merverdiavgift** > **Skattemyndigheter**.
2. Velg **Normal** i **Avrundingsform**-feltet på hurtigfanen **Generelt**.
3. Angi 1,00 i **Avrund**-feltet.
4. Når tiden er inne for å betale merverdiavgift til skattemyndighetene, går du til **Avgift** > **Deklareringer** > **Merverdiavgift** > **Utlign og poster merverdiavgift**. I mva-oppgjørskontoen kan du se at avgiftsgjeldbeløpet på **98 765,43** avrundes til **98 765**.

Tabellen nedenfor viser hvordan et beløp på 98 765,43 avrundes ved hjelp av hver avrundingsmetode som er tilgjengelig i **Avrundingsform**-feltet på siden **Skattemyndigheter**.

> [!NOTE]                                                                                  
> Hvis avrundingsverdien er angitt som 0,00:
>
> - For vanlig avrunding er avrundingsfunksjonen den samme som for **Avrunding = 0,01**.
> - For **Avrundingsform**, **Nedover**, **Avrundes opp** og **Egen fordel** er virkemåten den samme som for **Avrunding = 1,00**.

| Avrundingsform                | Avrundingsverdi = 0,01 | Avrundingsverdi = 0,10 | Avrundingsverdi = 1,00 | Avrundingsverdi = 100,00 | Avrundingsverdi = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Normal                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Nedover                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Avrundes opp                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Egen fordel, for en kreditsaldo | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Egen fordel, for en debetsaldo  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Vanlig avrunding, og avrundingspresisjon er 0,01

```<table>
  <tr>
    <td>Rounding
    </td>
    <td>Calculation process
    </td>
  </tr>
    <tr>
    <td>round(1.015, 0.01) = 1.02
    </td>
    <td>
      <ol>
        <li>round(1.015 / 0.01, 0) = round(101.5, 0) = 102
        </li>
        <li>102 * 0.01 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.014, 0.01) = 1.01
    </td>
    <td> <ol>
        <li>round(1.014 / 0.01, 0) = round(101.4, 0) = 101
        </li>
        <li>101 * 0.01 = 1.01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.011, 0.02) = 1.02
    </td>
    <td> <ol>
        <li>round(1.011 / 0.02, 0) = round(50.55, 0) = 51
        </li>
        <li>51 * 0.02 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.009, 0.02) = 1.00
    </td>
    <td> <ol>
        <li>round(1.009 / 0.02, 0) = round(50.45, 0) = 50
        </li>
        <li>50 * 0.02 = 1.00
        </li>
      </ol>
    </td>
  </tr>
</table>
```

> [!NOTE]                                                                                  
> Hvis du velger Egen fordel, skjer avrundingen alltid til fordel for den juridiske enheten. 

Hvis du vil ha mer informasjon, se følgende emner:
- [Oversikt over merverdiavgift](indirect-taxes-overview.md)
- [Opprette en mva-betaling](tasks/create-sales-tax-payment.md)
- [Opprette mva-transaksjoner på dokumenter](tasks/create-sales-tax-transactions-documents.md)
- [Vise posterte mva-transaksjoner](tasks/view-posted-sales-tax-transactions.md)
- [avrundingsfunksjon](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
