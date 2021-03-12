---
title: Feilsøke salgsordrer
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med salgsordrer.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974791"
---
# <a name="troubleshoot-sales-orders"></a>Feilsøke salgsordrer

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med salgsordrer.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Skatteinformasjonen oppdateres ikke hvis jeg endrer lokasjonen i et salgsordrehode.

### <a name="issue-description"></a>Problembeskrivelse

Hvis område-, lager- eller leveringsadressen endres enten på et salgsordrehode eller på linjenivå, oppdateres ikke skatteinformasjonen for saken automatisk for linjene.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard. Problemet oppstår fordi leveringsadressen, området og lageret ikke automatisk blir endret på linjenivået. Du må oppdatere dem manuelt.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Hvis det finnes to forretningsavtaler for samme periode eller overlappende perioder, blir alltid den samme avtalelinjen valgt.

### <a name="issue-description"></a>Problembeskrivelse

Hvis to forretningsavtaler er definert for samme periode eller ved overlappende perioder, ser det ut til at samme forretningsavtale blir valgt hver gang du oppretter salgsordrelinjer som inneholder disse varene.

### <a name="issue-resolution"></a>Problemløsning

Hvis det finnes mer enn én forretningsavtale for en gitt dato, velges alltid forretningsavtalen som har den laveste prisen. Hvis du vil ha mer informasjon, laster du ned følgende tekniske informasjon: [Forretningsavtaler i Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kan jeg koble en bestilling til en salgsordre for å imøtekomme etterspørselen?

Du kan opprette en bestilling fra en salgsordre. Hvis du vil ha mer informasjon, se [Opprette en bestilling fra en salgsordre](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Jeg kan ikke avbryte eller slette en returordre eller en salgsordre.

Du kan bare kansellere salgsordrer og returordrer som har statusen *Opprettet*. Hvis du vil ha mer informasjon, se [Annullere en returordre](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Når jeg prøver å annullere en salgsordre, får jeg feilen "Reservasjoner kan ikke fjernes fordi det er opprettet arbeid som er avhengig av reservasjonen".

Feilkode: WAX4661

Hvis arbeid er knyttet til en salgsordre, kan du ikke annullere salgsordren før arbeidet er annullert og tilbakeført. Dette kravet gjelder selv om arbeidet som er knyttet til salgsordren, er lukket.

Følg fremgangsmåten nedenfor for å løse problemet.

1. Avbryt arbeidet, og sett lageret tilbake på ønsket sted. Gå til den relevante belastningen for salgsordren, og velg enten **Reduser plukket kvantitet** på belastningslinjen eller **Reverser arbeid** i handlingsruten.

    Arbeidet har nå statusen *Avbrutt*, og nytt lagerflyttingsarbeid opprettes automatisk og behandles for å legge lager tilbake i lokasjonen som ble beskrevet da tilbakeføringen ble avbrutt.

2. Slett belastningen. Forsendelsen slettes også.
3. Du skal nå kunne gå til salgsordren og avbryte den.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Jeg kan ikke avbryte en konsernintern bestilling som er koblet til en salgsordre.

### <a name="issue-description"></a>Problembeskrivelse

Hvis du prøver å annullere en konsernintern bestilling som er koblet til en salgsordre, kan du få feilmelding om at antallet ikke kan reduseres, fordi det gjenstående oppdateringsantallet skifter fortegn.

### <a name="issue-resolution"></a>Problemløsning

Dette problemet ble løst i Microsoft Dynamics 365 Supply Chain Management versjon 10.0.13. I denne versjonen og senere versjoner kan du nå annullere en konsernintern bestilling som er koblet til en salgsordre.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kan jeg gjenopprette en fakturert salgsordre som er slettet?

### <a name="issue-description"></a>Problembeskrivelse

En fakturert salgsordre ble slettet ved en feiltakelse, og du vil gjenopprette den eller vise detaljene for den.

### <a name="issue-resolution"></a>Problemløsning

Hvis den slettede salgsordren allerede er fakturert, kan du gå til **Kundekonto \> Transaksjoner \> Original dokument \> Visningsdetaljer**. Finn fakturaen du er på jakt etter, og velg den for å vise detaljene for den. Disse detaljene omfatter salgsordrereferansen. Du bør også få tilgang til salgsordredetaljene fra denne siden.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Tidsfristen for et salgsordrehode finnes ikke i dataenheten SalesOrderHeaderV2Entity.

Tidsfristfeltet finnes ikke på enheten *SalesOrderHeaderV2Entity*.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Jeg må slette frittstående salgsordreposter.

Hvis du vil rydde opp i frittstående salgsordreposter, kan du kjøre den periodiske jobben *Salgsordresletting* ved å gå til et av følgende steder:

- Salg og markedsføring \> Periodiske oppgaver \> Opprydding \> Slett salgsordrer
- Detaljhandel og handel \> IT for Detaljhandel og handel \> Opprydding \> Slett salgsordrer

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Finnes det en måte å beregne provisjon på fakturaer som allerede er postert?

Supply Chain Management støtter for øyeblikket ikke beregningen av provisjoner for posterte fakturaer.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>En buntvare støttes ikke i en konsernintern prosess.

Buntvaren er ikke tilgjengelig for bestillingen fordi hvis du undersøker salgsordrelinjene for buntvaren, vil du se at antallet er *0* (null), og at statusen er *Avbrutt*. Denne virkemåten er standard. Salgsordren kjøper bare komponentene til buntvaren. Selve buntvaren kjøpes ikke.

Hvis du må kjøpe en bunt, bør du vurdere om du må merke den som buntvare, fordi denne funksjonaliteten er utformet for scenarioer med inntektsføring. Hvis du vil ha mer informasjon om buntvarer, se [Bunter](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).
