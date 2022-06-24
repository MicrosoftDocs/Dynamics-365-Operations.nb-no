---
title: TaxTrans-post blir ikke generert
description: Denne artikkelen gir feilsøkingsinformasjon som kan være til hjelp når en TaxTrans-post ikke genereres.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 402b1200e96ec8130034a03447ca071477544a88
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846719"
---
# <a name="taxtrans-record-isnt-generated"></a>TaxTrans-post blir ikke generert

[!include [banner](../includes/banner.md)]

Hvis du velger **Postert merverdiavgift** for en transaksjon, men **Postert merverdiavgift** -siden enten viser ingen mva-linjer eller mangler en mva-linje, kan det hende at **TaxTrans**-posten ikke er generert.

[![Postert merverdiavgift-side som ikke har noen linjeelementer.](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Hvis du vil feilsøke dette problemet, følger du trinnene i de følgende delene etter behov.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Kontroller merverdiavgiften før du posterer transaksjonen

1. Før du posterer transaksjonen, velger du **Merverdiavgift** på siden **Postering av faktura** for å kontrollere beregningen.

    [![Mva-knappen på Postering av faktura-siden.](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Gå gjennom resultatet av beregningen på siden **Midlertidige mva-transaksjoner**. Hvis det ikke beregnes avgift, kan du se [Avgift beregnes ikke eller avgiftsbeløpet er null](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Finn TaxTrans-posten i all postert merverdiavgift

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Merverdiavgiftforespørsler** > **Postert merverdiavgift**.
2. Velg filtersymbolet i **Bilag**-kolonneoverskriften for å finne **TaxTrans**-posten.
3. Hvis du finner mva-postene du leter etter, kan du kontrollere datoen. Hvis datoen er forskjellig fra datoen på journalhodet, oppretter du en Forespørsel om Microsoft-tjeneste for mer støtte.

    [![Siden Postert merverdiavgift.](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Feilsøke for å kontrollere detaljer

1. Hvis du vil ha mer informasjon om hvordan du feilsøker og finner ut om **TmpTaxWorkTrans** og **TaxUncommitted** er riktig generert, kan du se [Feltverdi i TaxTrans er feil](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Hvis **TaxTmpWorkTrans** eller **TaxUncommitted** genereres på riktig måte, legger du til et stoppunkt på **TaxPost::SaveAndPost()** og **Tax::SaveAndPost** for å feilsøke årsaken til at **TaxTrans** ikke er satt inn.

    [![Stoppunkt som er lagt til i kode.](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Resultater av nye stoppunkter.](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Fastslå om det finnes tilpasning

Hvis du har fullført trinnene i de forrige delene, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning. Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
