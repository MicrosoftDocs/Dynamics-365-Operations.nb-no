---
title: Avstemme frakt i transportstyring
description: Denne artikkelen beskriver fraktavstemmingsprosessen.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff29de62de12e8ca8bea0f374921a51b5819222e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844238"
---
# <a name="reconcile-freight-in-transportation-management"></a>Avstemme frakt i transportstyring

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver fraktavstemmingsprosessen.

Fraktavstemming kan gjøres manuelt, eller det kan settes opp til å skje automatisk. Hvis du vil bruke automatisk fraktavstemming, må du opprette en revisjonsstandard der du kan definere kriteriene som bestemmer hvilke fraktbrev som sammenlignes automatisk.

## <a name="the-freight-reconciliation-process"></a>Fraktavstemmingsprosessen

Fraktsatser beregnes av satsmotoren som er tilknyttet med den aktuelle transportøren. Når en last er bekreftet, genereres et fraktbrev og fraktsatser overføres til den. Fraktsatsene fordeles som tillegg til det aktuelle kildedokumentet (bestilling, salgsordre, og/eller overføringsordre), avhengig av oppsettet som brukes for den vanlige faktureringsprosessen. Fraktavstemmingsprosessen (som også kalles kontrollprosessen) kan starte så snart fraktfakturaen mottas fra transportøren. Fakturaen kan mottas elektronisk eller på papir. Hvis fakturaen mottas på papir, kan du generere en elektronisk faktura ved hjelp av fraktbrevet som mal.

[![Fraktavstemmingsprosessen.](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuell avstemming

Hvis du er avstemmer frakt manuelt, må du sammenligne hver fakturalinje med fraktbrevlinjen eller -linjene for lasten som skal faktureres. Du gjør dette på siden **Samsvare fraktbrev og faktura**. Hvis beløpet på fakturalinjen ikke samsvarer med hvor fraktbrevbeløpet, må du velge en avstemmingsårsak for forskjellen. Hvis det er flere årsaker til avstemming, kan du dele de ikke-samsvarte beløpene på tvers av dem. Årsaken til avstemming bestemmer hvordan differansebeløpene posteres i Finans. Når avstemmingen av hele fakturabeløpet er gjort rede for, sendes sendt til godkjenning, og deretter posteres journalen. Illustrasjonen nedenfor viser hvordan du genererer en fraktfaktura og utfører fraktavstemming.

[![Fraktavstemmingsoppgaver.](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>Automatisk avstemming

Hvis du vil bruke automatisk avstemming, må du angi tidsplanen for avstemming og fakturaene og transportørene som skal brukes. Treff for fakturalinjer og fraktbrev gjøres i henhold til oppsettet av typen revisjonsstandard og fraktbrev. Når du har kjørt automatisk avstemming, må du håndtere alle fakturaer som systemet ikke kan samsvare. Du må behandle disse fakturaene manuelt før du kan bokføre alle fakturaene for betaling.

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Samsvare fraktbrev med fraktfakturaer ved hjelp av automatisk eller manuell avstemming

*Samsvaring* er prosessen med å finne fraktsedlene som samsvarer med hver fraktfaktura. Du kan gjøre dette ved å samsvare én fakturalinje om gangen (manuelt samsvar), eller ved å samsvare alle tilgjengelige fakturaer samtidig (automatisk samsvar).

### <a name="auto-matching"></a>Automatisk samsvar

Når flere fraktfakturaer samsvares med samme fraktbrev, fungerer prosessen for automatisk samsvar på følgende måte:

1. Alle fraktfakturaer som ikke samsvarer, sorteres etter beløp, med det største beløpet først.
1. Fraktfakturaene samsvares én om gangen til fraktbrevet ikke har noe gjenstående positivt beløp.
1. Det gjenstående beløpet angis, avhengig av oppsettet for revisjonsstandarden og det gjenstående beløpet på fraktfakturaene.

### <a name="manual-matching"></a>Manuelt samsvar

Alle fraktsedler med positive beløp blir tilgjengelige for samsvar. I likhet med automatisk samsvar kan brukeren bare samsvare fraktfakturaer med negative beløp med fraktsedler som ikke samsvarer helt.

### <a name="example"></a>Eksempel

La oss si at du har en fraktseddel for et beløp på 1500 og har opprettet tre fraktfakturaer for fraktseddelen med én fakturalinje for hver faktura med følgende innstillinger:

- Opprinnelig fraktseddel: beløp på 1500
- Faktura 1 (Fakt1): beløp på 1000
- Faktura 2 (Fakt2): beløp på 600
- Faktura 3 (Fakt3): beløp på -100

#### <a name="automatic-matching-result"></a>Resultat for automatisk samsvar

Automatisk samsvar utføres i følgende rekkefølge:

1. Sorter alle fraktfakturaer i synkende rekkefølge etter beløp: Fakt1 -> Fakt2 -> Fakt3.
1. Samsvar Fakt1 med fraktseddel. Fakt1 har 1000 samsvart, og fraktseddel har beløp på 500 gjenstående, slik at statusen settes til *Delvis samsvar*.
1. Samsvar Fakt2 med fraktseddel. Fakt2 har 500 samsvart, og fraktseddel har beløp på 0 gjenstående, slik at statusen settes til *Fullstendig samsvar*.
1. Siden fraktseddel nå har fullstendig samsvar, behandles ikke Fakt3.

#### <a name="manual-matching-result"></a>Resultat for manuelt samsvar

Når det gjelder manuelt samsvar, varierer resultatene avhengig av samsvarsrekkefølgen, som vist i eksemplene nedenfor.

##### <a name="manual-matching-case-1"></a>Manuelt samsvar – eksempel 1

Det er flere måter å foreta manuelt samsvar på. I dette eksemplet kan du gå frem på følgende måte:

1. Samsvar fraktseddel med Fakt1. Fraktseddel har beløp på 500 gjenstående, slik at statusen settes til *Delvis samsvar*.
1. Samsvar Fakt2 med fraktseddel. Fakt2 har 500 samsvart, og fraktseddel har beløp på 0 gjenstående, slik at statusen settes til *Fullstendig samsvar*.
1. Når Fakt3 samsvares manuelt, finner du ingen fraktsedler uten samsvar.

Dette eksemplet er egentlig det samme som automatisk samsvar

##### <a name="manual-matching-case-2"></a>Manuelt samsvar – eksempel 2

I dette eksemplet skal du gå frem på en annen måte for å foreta manuelt samsvar:

1. Samsvar Fakt3 med fraktseddel. Nå har fraktseddel et gjenstående beløp på 1600, som er det samme som å trekke minus 100 fra 1500. Både fraktseddel og Fakt3 har et samsvarende antall på -100.
1. Samsvar Fakt1 og Fakt2 med fraktseddel én om gangen. Fraktseddel samsvarer fullstendig.

Som dette eksemplet viser bør samsvarende fraktfakturaer med negative beløp bare utføres manuelt. Dette sikrer at det alltid går an å samsvare fraktfakturaene med negative beløp med en fraktseddel som ikke samsvarer fullstendig, fordi det gjør at du kan kontrollere samsvarsrekkefølgen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]