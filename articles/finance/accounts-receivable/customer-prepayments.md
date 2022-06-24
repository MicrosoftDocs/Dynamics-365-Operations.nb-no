---
title: Kundebetalinger
description: Denne artikkelen beskriver hvordan du konfigurerer og behandler kundeforskuddsbetalinger (kalles også kundeinnskudd).
author: twheeloc
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88773067c472471fb75167712268d1076c1738a5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861567"
---
# <a name="customer-prepayments"></a>Kundebetalinger

[!include [banner](../includes/banner.md)]

Kundeforskuddsbetalinger brukes når du mottar en betaling fra en kunde, men det er ingen faktura som betalingen kan utlignes mot. Denne typen betalinger omtales også som kundeinnbetalinger.

Prosessen med å definere og arbeide med kundeforskuddsbetalinger består av følgende grunnleggende trinn.

1. Opprett en kundeposteringsprofil for forskuddsbetalinger.
2. Angi parameteren **Posteringsprofil ved journalbilag for forskuddsbetaling**.
3. Opprett en kundebetalingsjournal, og merk av for **Journalbilag for forskuddsbetaling** på hver linje.
4. Poster kundebetalingsjournalen.
5. Når en faktura er generert, utligner du forskuddsbetalingen med den ved å bruke siden **Utlign åpne transaksjoner**.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Opprette en kundeposteringsprofil for forskuddsbetalinger

Når du godtar forskuddsbetaling eller innbetalinger fra kundene før varer eller tjenester leveres, eller før det finnes en faktura i systemet, ønsker du vanligvis å registrere kontanter som gjeld i stedet for aktiva i kontoplanen. Kravene til registrering av disse beløpene i økonomimodulen kan imidlertid variere, avhengig av landet eller regionen du bes om. Husk derfor å ta kontakt med regnskapsførere for eventuelle lokale regler som gjelder.

Generelt sett er prosessen for oppretting av en posteringsprofil som kan brukes for forskuddsbetalinger, den samme som prosessen for oppretting av andre posteringsprofiler. Hovedforskjellen er hovedkontoen du velger i **Samlekonto**-feltet. Hvis du vil ha mer informasjon, kan du se [Kundeposteringsprofiler](customer-posting-profiles.md).

## <a name="define-parameters-for-customer-prepayments"></a>Definere parametere for kundeforskuddsbetalinger

Det er to primære kundeparametere du må vurdere når du konfigurerer systemet for kundeforskuddsbetalinger. Gjør følgende for å konfigurere parametere.

1. Gå til **Kunder \> Oppsett \> Kundeparametere**.
2. Valgfritt: I kategorien **Finans og merverdiavgift** i hurtigfanen **Betaling** angir alternativet **Merverdiavgift på journalbilag for forskuddsbetaling** til **Ja**.
3. I feltet **Posteringsprofil ved journalbilag for forskuddsbetaling**, velg kundeposteringsprofilen som skal brukes når kundeforskuddsbetalinger posteres.
4. Lukk siden.

## <a name="create-customer-prepayment-vouchers"></a>Opprette kundeforskuddsbetalingsbilag

Når du oppretter kundebetalingsjournalen, må du sette alternativet **Journalbilag for forskuddsbetaling** til **Ja** på siden **Kundebetalingsjournal**. Følg disse trinnene for å opprette en kundeforhåndsbetaling.

1. Gå til **Kunder \> Betalinger \> Kundebetalingsjournal**.
2. Velg **Ny** for å opprette en journal.
3. Velg journalnavnet som skal brukes, i **Navn**-feltet.

    > [!IMPORTANT]
    > Hvis du setter alternativet **Merverdiavgift på journalbilag for forskuddsbetaling** til **Ja** i den forrige fremgangsmåten, må du velge et journalnavn der parameteren **Beløp inkluderer mva** er valgt. 

4. Valgfritt: Skriv inn en detaljert beskrivelse i **Beskrivelse**-feltet.
5. Velg **Linjer**.
6. Hvis det ikke finnes en tom linje, velger du **Ny** for å opprette en linje.
7. I feltet **Dato** angir du datoen da forskuddsbetalingen skal posteres.
8. Velg kunden for forskuddsbetalingen i **Konto**-feltet.
9. Valgfritt: Skriv inn en detaljert beskrivelse av transaksjonen i **Beskrivelse**-feltet.
10. Angi beløpet for forhåndsbetalingen i **Kredit**-feltet.
11. Velg kontoen du vil motpostere betalingen til, i **Motkonto**-feltet. Du kan for eksempel velge banken eller hovedkontoen som betalingen skal posteres til.
12. Velg kundens betalingsmåte i feltet **Betalingsmåte**.
13. Sett alternativet **Journalbilag for forskuddsbetaling** i kategorien **Betaling** til **Ja**.
14. Gjenta trinn 7 til og med 13 for hver ekstra forskuddsbetaling som må posteres.
15. Velg **Poster** for å fullføre journalen.

## <a name="settle-prepayments-with-invoices"></a>Utligne forskuddsbetalinger med fakturaer

Du kan bruke arbeidsområdet for **Kundebetalinger** til enkelt å finne og utligne betalinger som ikke har blitt helt utlignet.

1. Velg flisen **Kundebetalinger** på **Start**-instrumentbordet.
2. Søk etter og velg betalingen som skal utlignes, i kategorien **Forfalte fakturaer** i **Kundetransaksjoner**-delen.
3. Velg **Utlign transaksjoner**.
4. Merk av for **Merk** for fakturaen og betalingen som skal utlignes.
5. Velg **Poster**.

Hvis du vil ha mer informasjon om hvordan du utligner åpne transaksjoner, kan du se [Oversikt over utligning](/dynamics365/finance/cash-bank-management/settlement-overview).
