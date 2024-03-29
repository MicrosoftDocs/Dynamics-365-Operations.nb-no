---
title: Kundebetalinger for et delbeløp
description: Noen ganger betaler kunder et beløp som er mindre enn beløpet på en faktura. Denne artikkelen beskriver de ulike alternativene for håndtering av dette. Hvilke alternativer som er tilgjengelige, avhenger av dine forretningsbehov og konfigurasjon.
author: ShivamPandey-msft
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymEntry
audience: Application User
ms.reviewer: kfend
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b688e62fcf1f223668b79ca6014da85b01000715
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713479"
---
# <a name="customer-payments-for-a-partial-amount"></a>Kundebetalinger for et delbeløp

[!include [banner](../includes/banner.md)]

Noen ganger betaler kunder et beløp som er mindre enn beløpet på en faktura. Denne artikkelen beskriver de ulike alternativene for håndtering av dette. Hvilke alternativer som er tilgjengelige, avhenger av dine forretningsbehov og konfigurasjon.

## <a name="partial-payment-with-no-discount"></a>Delbetaling uten rabatt

Kunder kan utføre en delbetaling fordi de ikke har nok kontanter for hånden til å betale fakturaen i sin helhet, eller fordi det har oppstått en konflikt om en vare på fakturaen. I slike situasjoner kan fakturaen utlignes delvis med betalingen. Fakturaen forblir åpen og viser en saldo.

## <a name="discount-amounts"></a>Rabattbeløp
Du kan tilby kunder en kontantrabatt for å betale en faktura før forfallsdatoen. Du kan for eksempel registrere en faktura for 100,00 som angir en kontantrabatt på 2 prosent hvis fakturaen betales innen ti dager. Forfallsdatoen er om 30 dager. Hvis du mottar en betaling på 98,00 innen ti dager, kan du angi betalingen av 98,00. Deretter, når fakturaen er merket for utligning, brukes kontantrabatten automatisk.

## <a name="partial-payments-with-cash-discounts"></a>Delbetalinger med kontantrabatter
Når kunder foretar en delbetaling, kan det hende at de har tenkt å lage en ekstra delbetaling for å utligne fullt ut fakturaen. Hvis tar en kontantrabatt for en delbetaling, må du angi alternativet **Beregn kontantrabatter for delvise betalinger** som **Ja** på siden **Leverandørparametere**. 

Du tilbyr for eksempel en kontantrabatt på 2 prosent hvis fakturaen er betalt innen ti dager etter at den utstedes. Det posteres en faktura på 100,00. Hvis du mottar en betaling på 49,00 innen ti dager, kan du angi et kreditbeløp på 49,00 i en betalingsjournal. Når du utligner delbetalingen delvis på siden **Utlign transaksjoner**, vises **1,00** i feltet **Kontantrabattbeløp som skal brukes**. Rabattbeløpet posteres til en kontantrabattkonto. 

> [!NOTE] 
> Hvis du angir en delbetaling og lar det fullstendige fakturabeløpet stå i feltet **Beløp som skal utlignes**, beregnes feltet **Kontantrabattbeløp som skal brukes** automatisk på nytt når du posterer transaksjonene.

## <a name="credit-notes-with-discounts"></a>Kreditnotaer med rabatter
Hvis kunder returnerer noen av varene på en faktura, kan du utstede en kreditnota. Hvis det ble brukt en kontantrabatt på den opprinnelige fakturaen, skal kreditnotaen til kunden være netto av kontantrabatten som ble brukt for kunden. Hvis alternativet **Beregn kontantrabatter for kreditnotaer** er satt til **Ja** på siden **Kundeparametere**, beregnes rabatten automatisk for kreditnotaen. 

Du tilbyr for eksempel betalingsbetingelser som angir en kontantrabatt på 2 prosent hvis fakturaen betales innen ti dager etter at den utstedes. En faktura på 100,00 ble postert, og kunden fikk kontantrabatten. Hvis kunden returnerer varene og du utsteder en kreditnota, kan du angi -100.00 på kreditnotaen. Når du viser kreditnotaen på siden **Utlign åpne transaksjoner**, vises **98,00** i feltet **Beløp som skal utlignes**, og **-2,00** vises i feltet **Kontantrabattbeløp**. Rabattbeløpet posteres til en kontantrabattkonto.

## <a name="overpaymentunderpayment-amounts"></a>Overbetalings-/underbetalingsbeløp
Når kunder betaler, kan det være et lite beløp som fremdeles må utlignes. Eksempel: Du fakturerer kunden 1 000,00, og kunden betaler 999,90. Hvis det gjenstående beløpet er mindre enn beløpet som er angitt for overbetalinger eller underbetalinger på siden **Kundeparametere**, posteres differansen automatisk til en finanskonto for overbetaling/underbetaling.

## <a name="full-settlement"></a>Full utligning
Kunder kan utføre en delbetaling der det restbeløpet ikke blir betalt, men det er større enn underbetalingsbeløpet som er angitt på siden **Leverandørparametere**. Hvis du vil merke fakturaen som er fullstendig utlignet, kan du bruke alternativet **Full utligning** på siden **Utlign transaksjon**. (Du kan aktivere funksjonen Full utligning ved hjelp av en konfigurasjonsnøkkel.) Eksempel: En faktura posteres for 1 000,00, og kunden betaler 990,00. Du har avtalt at kunden ikke behøver å betale de gjenværende 10,00. Når du har merket fakturaen for utligning, kan du også merke av for **Full utligning**. Fakturaen vil deretter anses som fullstendig utlignet. Differansen på 10,00 posteres til en kontantrabattkonto som et ekstra kontantrabattbeløp.


Hvis du vil ha mer informasjon, kan du se [Betale inn kundebetalinger](tasks/deposit-customer-payments.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
