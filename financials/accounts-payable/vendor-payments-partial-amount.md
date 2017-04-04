---
title: "Leverandørbetalinger for et delbeløp"
description: "Du kan eventuelt opprette en betaling til en leverandør som er mindre enn beløpet i en faktura. Denne artikkelen beskriver de ulike alternativene for håndtering av dette. Hvilke alternativer som er tilgjengelige, avhenger av dine forretningsbehov og konfigurasjon."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Leverandørbetalinger for et delbeløp

Du kan eventuelt opprette en betaling til en leverandør som er mindre enn beløpet i en faktura. Denne artikkelen beskriver de ulike alternativene for håndtering av dette. Hvilke alternativer som er tilgjengelige, avhenger av dine forretningsbehov og konfigurasjon. 

<a name="cash-discount-amounts"></a>Kontantrabattbeløp
---------------------

En leverandør kan tilby deg en kontantrabatt for å betale en faktura før forfallsdatoen. Du kan for eksempel registrere en faktura for 100,00 som angir en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager. Forfallsdatoen er om 30 dager. Hvis du bruker et betalingsforslag kontantrabatten som et kriterium for å velge en faktura hvis forslaget kjøres på eller før kontantrabattdatoen, fakturaen er merket for betaling, og betalingen er opprettet for 98,00. En kontantrabatt kan også bli tatt for en engangs betaling som ble opprettet manuelt.

## <a name="partial-payments-with-cash-discounts"></a>Delbetalinger med kontantrabatter
Når du foretar en delbetaling, kan det hende at du har tenkt å lage en ekstra delbetaling for å utligne fullt ut fakturaen. For å få en kontantrabatt for en delbetaling, må du angi den ** beregne kontantrabatter for delvise betalinger ** å **Ja** på den **konto leverandørparametere** siden. 

Du får for eksempel en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager etter at den utstedes. Det posteres en faktura på 100,00. Hvis du foretar en betaling på 49.00 innen 10 dager, kan du angi et debetbeløp i 49.00 i en betalingsjournal. Når du vil utligne betalingen delvis på den **utligne åpne transaksjoner** siden **1.00** vises i den **kontantrabattbeløp til å ta** feltet. 

> [!NOTE] 
> Hvis du angir en akontobetaling og la hele fakturabeløpet i den **beløp som skal utlignes** -feltet i **kontantrabattbeløp til å ta** feltet beregnes automatisk når du bokfører transaksjoner.

## <a name="credit-notes-with-cash-discounts"></a>Kreditnotaer med kontantrabatter
Du kan returnere noen av elementene på en faktura og motta en kreditnota. Hvis en kontantrabatt ble brukt på den opprinnelige fakturaen, kan du trekke fra verdien av rabatten og få en refundering for riktig beløp. Hvis den ** beregne kontantrabatt for kreditnotaer ** alternativet er satt til **Ja** på den **leverandørparametere** siden rabatten beregnes automatisk for kreditnotaen. 

Du får for eksempel en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager etter at den utstedes. Det posteres en faktura på 100,00. Hvis du returnerer varene og mottar en kreditnota, kan du angi kreditnotaen for hele beløpet på den opprinnelige fakturaen, 100,00, sammen med 2 prosent kontantrabatten som også er definert i kreditnotaen.  Når du viser kreditnotaen på den **utligne transaksjoner** siden **98,00** vises i den **beløp som skal utlignes** -feltet og **-2.00** vises i den **kontantrabattbeløpet** feltet. Rabattbeløpet posteres til en kontantrabattkonto.

## <a name="overpaymentunderpayment-amounts"></a>Overbetalings-/underbetalingsbeløp
Du kan foreta en delbetaling der beløpet som fremdeles skal utlignes, er svært lite. Anta for eksempel at leverandørfakturaen gjelder 1 000,00, og du betaler 999,90. Hvis det gjenstående beløpet er mindre enn beløpet som er angitt for overbetalinger eller underbetalinger på siden **Leverandørparametere**, posteres differansen automatisk til en finanskonto for overbetaling/underbetaling.


