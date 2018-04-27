---
title: "Leverandørbetalinger for et delbeløp"
description: "Du kan eventuelt opprette en betaling til en leverandør som er mindre enn beløpet i en faktura. Denne artikkelen beskriver de ulike alternativene for håndtering av dette. Hvilke alternativer som er tilgjengelige, avhenger av dine forretningsbehov og konfigurasjon."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aeef806980665c523f10b373f7662ecf509a8172
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-payments-for-a-partial-amount"></a>Leverandørbetalinger for et delbeløp

[!INCLUDE [banner](../includes/banner.md)]

Du kan eventuelt opprette en betaling til en leverandør som er mindre enn beløpet i en faktura. Denne artikkelen beskriver de ulike alternativene for håndtering av dette. Hvilke alternativer som er tilgjengelige, avhenger av dine forretningsbehov og konfigurasjon. 

<a name="cash-discount-amounts"></a>Kontantrabattbeløp
---------------------

En leverandør kan tilby deg en kontantrabatt for å betale en faktura før forfallsdatoen. Du kan for eksempel registrere en faktura for 100,00 som angir en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager. Forfallsdatoen er om 30 dager. Hvis et betalingsforslag bruker kontantrabatten som et kriterium for å velge en faktura, og hvis forslaget kjøres på eller før kontantrabattdatoen, velges fakturaen for betaling, og betalingen opprettes for 98,00. En kontantrabatt kan også brukes for en engangsbetaling som ble opprettet manuelt.

## <a name="partial-payments-with-cash-discounts"></a>Delbetalinger med kontantrabatter
Når du foretar en delbetaling, kan det hende at du har tenkt å lage en ekstra delbetaling for å utligne fullt ut fakturaen. Hvis tar en kontantrabatt for en delbetaling, må du angi alternativet <strong>Beregn kontantrabatter for delvise betalinger **til**Ja</strong> på siden <strong>Leverandørparametere</strong>. 

Du får for eksempel en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager etter at den utstedes. Det posteres en faktura på 100,00. Hvis du foretar en betaling på 49,00 innen 10 dager, angir du et debetbeløp i 49,00 i en betalingsjournal. Når du utligner delbetalingen delvis på siden **Utlign åpne transaksjoner**, vises **1,00** i feltet **Kontantrabattbeløp som skal brukes**. 

> [!NOTE] 
> Hvis du angir en delbetaling og lar det fullstendige fakturabeløpet stå i feltet **Beløp som skal utlignes**, beregnes feltet **Kontantrabattbeløp som skal brukes** automatisk på nytt når du posterer transaksjonene.

## <a name="credit-notes-with-cash-discounts"></a>Kreditnotaer med kontantrabatter
Du kan returnere noen av elementene på en faktura og motta en kreditnota. Hvis en kontantrabatt ble brukt på den opprinnelige fakturaen, kan du trekke fra verdien av rabatten og få en refundering for riktig beløp. Hvis alternativet <strong>Beregn kontantrabatter for kreditnotaer **er satt til **Ja</strong> på siden <strong>Leverandørparametere</strong>, beregnes rabatten automatisk for kreditnotaen. 

Du får for eksempel en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager etter at den utstedes. Det posteres en faktura på 100,00. Hvis du returnerer varene og mottar en kreditnota, kan du angi kreditnotaen for hele beløpet i den opprinnelige fakturaen 100,00, sammen med 2 prosent kontantrabatt, som også er definert i kreditnotaen.  Når du viser kreditnotaen på siden **Utlign åpne transaksjoner**, vises **98,00** i feltet **Beløp som skal utlignes**, og **-2,00** vises i feltet **Kontantrabattbeløp**. Rabattbeløpet posteres til en kontantrabattkonto.

## <a name="overpaymentunderpayment-amounts"></a>Overbetalings-/underbetalingsbeløp
Du kan foreta en delbetaling der beløpet som fremdeles skal utlignes, er svært lite. Anta for eksempel at leverandørfakturaen gjelder 1 000,00, og du betaler 999,90. Hvis det gjenstående beløpet er mindre enn beløpet som er angitt for overbetalinger eller underbetalinger på siden **Leverandørparametere**, posteres differansen automatisk til en finanskonto for overbetaling/underbetaling.


Hvis du vil ha mer informasjon, kan du se [Oversikt over leverandørbetaling](../cash-bank-management/tasks/vendor-payment-overview.md).

