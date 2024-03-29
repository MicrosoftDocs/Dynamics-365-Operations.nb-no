---
title: Leverandørbetalinger for et delbeløp
description: Du kan eventuelt opprette en betaling til en leverandør som er mindre enn beløpet i en faktura. Denne artikkelen beskriver de ulike alternativene for håndtering av dette.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: deb150e35a80cc4c49f46dfc55822625db83cbda
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715386"
---
# <a name="vendor-payments-for-a-partial-amount"></a>Leverandørbetalinger for et delbeløp

[!include [banner](../includes/banner.md)]

Du kan eventuelt opprette en betaling til en leverandør som er mindre enn beløpet i en faktura. Denne artikkelen beskriver de ulike alternativene for håndtering av dette. Hvilke alternativer som er tilgjengelige, avhenger av dine forretningsbehov og konfigurasjon. 

## <a name="cash-discount-amounts"></a>Kontantrabattbeløp

En leverandør kan tilby deg en kontantrabatt for å betale en faktura før forfallsdatoen. Du kan for eksempel registrere en faktura for 100,00 som angir en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager. Forfallsdatoen er om 30 dager. Hvis et betalingsforslag bruker kontantrabatten som et kriterium for å velge en faktura, og hvis forslaget kjøres på eller før kontantrabattdatoen, velges fakturaen for betaling, og betalingen opprettes for 98,00. En kontantrabatt kan også brukes for en engangsbetaling som ble opprettet manuelt.

## <a name="partial-payments-with-cash-discounts"></a>Delbetalinger med kontantrabatter
Når du foretar en delbetaling, kan det hende at du har tenkt å lage en ekstra delbetaling for å utligne fullt ut fakturaen. Hvis tar en kontantrabatt for en delbetaling, må du angi alternativet **Beregn kontantrabatter for delvise betalinger** som **Ja** på siden **Leverandørparametere**. 

Du får for eksempel en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager etter at den utstedes. Det posteres en faktura på 100,00. Hvis du foretar en betaling på 49,00 innen 10 dager, angir du et debetbeløp i 49,00 i en betalingsjournal. Når du utligner delbetalingen delvis på siden **Utlign åpne transaksjoner**, vises **1,00** i feltet **Kontantrabattbeløp som skal brukes**. 

> [!NOTE] 
> Hvis du angir en delbetaling og lar det fullstendige fakturabeløpet stå i feltet **Beløp som skal utlignes**, beregnes feltet **Kontantrabattbeløp som skal brukes** automatisk på nytt når du posterer transaksjonene.

## <a name="credit-notes-with-cash-discounts"></a>Kreditnotaer med kontantrabatter
Du kan returnere noen av elementene på en faktura og motta en kreditnota. Hvis en kontantrabatt ble brukt på den opprinnelige fakturaen, kan du trekke fra verdien av rabatten og få en refundering for riktig beløp. Hvis alternativet **Beregn kontantrabatter for kreditnotaer** er satt til **Ja** på siden **Leverandørparametere**, beregnes rabatten automatisk for kreditnotaen. 

Du får for eksempel en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager etter at den utstedes. Det posteres en faktura på 100,00. Hvis du returnerer varene og mottar en kreditnota, kan du angi kreditnotaen for hele beløpet i den opprinnelige fakturaen 100,00, sammen med 2 prosent kontantrabatt, som også er definert i kreditnotaen.  Når du viser kreditnotaen på siden **Utlign åpne transaksjoner**, vises **98,00** i feltet **Beløp som skal utlignes**, og **-2,00** vises i feltet **Kontantrabattbeløp**. Rabattbeløpet posteres til en kontantrabattkonto.

## <a name="overpaymentunderpayment-amounts"></a>Overbetalings-/underbetalingsbeløp
Du kan foreta en delbetaling der beløpet som fremdeles skal utlignes, er svært lite. Anta for eksempel at leverandørfakturaen gjelder 1 000,00, og du betaler 999,90. Hvis det gjenstående beløpet er mindre enn beløpet som er angitt for overbetalinger eller underbetalinger på siden **Leverandørparametere**, posteres differansen automatisk til en finanskonto for overbetaling/underbetaling.


Hvis du vil ha mer informasjon, kan du se [Oversikt over leverandørbetaling](../cash-bank-management/tasks/vendor-payment-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
