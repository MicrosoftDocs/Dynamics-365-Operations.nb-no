---
title: Postering av utestående fordringer
description: Denne artikkelen beskriver hvordan posteringer konfigureres i Kunder, og gir eksempler på posteringskonfigurasjoner.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 492bbd31cae08a93cd68e5ce120d02a62141241b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874581"
---
# <a name="accounts-receivable-posting"></a>Kunder-postering

[!include [banner](../includes/banner.md)]

Den primære posteringsprofilen for **Kunder**-modulen er kundeposteringsprofilen. Denne posteringsprofilen bestemmer samlekontoen som brukes når kundesaldoer posteres til økonomimodulen. En samlekonto er en hovedkonto. Den kalles også handelskontoen for kunder.

Hvis du vil ha mer informasjon, kan du se [Kundeposteringsprofiler](../accounts-receivable/customer-posting-profiles.md).

Flere posteringskonfigurasjoner i tillegg til kundeposteringsprofilen er tilgjengelige i Kunder. De følgende delene gir mer informasjon om disse andre posteringskonfigurasjonene.

## <a name="posting-accounts-for-methods-of-payment"></a>Posteringskontoer for betalingsmåter

Betalingsmåter definerer hvordan en betaling skal posteres i økonomimodulen. De kontrollerer også virkemåten til betalingsutdataene. Vanligvis opprettes det én betalingsmåte for hver betalingstype som organisasjonen godtar (for eksempel kontant, sjekk, kredittkort, pengeordre og overføring).

Feltene i **Postering**-delen på hurtigfanen **Generelt** styrer hvordan en betaling posteres i økonomimodulen. Først må du velge en verdi i **Kontotype**-feltet. Kontotypen du velger, styrer virkemåten til **Betalingskonto**-feltet. Vi anbefaler at du velger **Bank** i **Kontotype**-feltet og velger deretter bankkontoen i **Betalingskonto**-feltet. Fordelen med denne tilnærmingen er at systemet vil postere betalingen til Bank-underhovedboken, som støtter avstemming og andre kontantrelaterte prosesser. Følgende tabell viser et eksempel på konfigurasjonen til posteringsprofilen hvis du bruker modulen **Kontant- og bankbehandling**.

| Posteringstype | Kontotype | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Bank | Bank | Bank of Contoso | Bankkonto som er koblet til en ressurs | Kredit | Nei | For hver betalingsmåte angir du hovedkontoen i **Betalingskonto**-feltet. |

Hvis du ikke har planlagt å bruke Kontant- og bankbehandling, bør du velge **Hovedbok** i **Kontotype**-feltet og deretter velge hovedkontoen i **Betalingskonto**-feltet. Følgende tabell viser et eksempel på konfigurasjonen til posteringsprofilen hvis du ikke bruker modulen Kontant- og bankbehandling.

| Posteringstype | Kontotype | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank of Contoso | Objekt | Kredit | Nei | For hver betalingsmåte angir du hovedkontoen i **Betalingskonto**-feltet. |

## <a name="bridging-accounts"></a>Mellomkontoer

Mellompostering er en totrinns prosess som brukes når betalinger posteres. Det er en valgfri funksjon som for eksempel kan brukes med bankkontoer med nullsaldo. Det kan bidra til å sikre en mer problemfri og raskere bankavstemmingsprosess. I det første trinnet posteres en betaling til en midlertidig konto (mellomkontoen). I det andre trinnet tilbakeføres den posterte oppføringen og posteres til bankkontoen når betalingen tømmer banken. Følgende tabell viser et eksempel på posteringsprofilkonfigurasjonen for mellompostering.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Finansjournal | 130725 | Ikke-klarerte kontanter | Gjeld | Debet | Ja | For hver betalingsmåte angir du hovedkontoen i **Mellomkonto**-feltet. |

Hvis du vil ha mer informasjon, kan du se [Definer og behandle mellombetalinger](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="posting-accounts-for-customer-cash-discounts"></a>Posteringskontoer for kundekontantrabatter

Hvis organisasjonen tilbyr kontantrabatter til kunder som retur for rask betaling, må du konfigurere kontantrabattkoder og angi hvordan rabattene skal posteres i økonomimodulen. Det finnes flere alternativer for angivelse av hovedkontoen som brukes til å postere en kundekontantrabatt.

Hvis du vil ha mer informasjon, kan du se [Kontantrabatter](../cash-bank-management/cash-discounts.md).

## <a name="posting-accounts-for-payment-fees"></a>Posteringskontoer for betalingsgebyrer

Ved bruk av betalingsgebyrer kan du automatisk legge til et gebyr i en kundebetaling når et sett med betingelser gjelder. Betalingsgebyrer kan belastes kunden, eller de kan posteres til bankkontoen som en utgift. Her er noen eksempler:

- Du belaster kunder 3 prosent av det totale betalingsbeløpet hvis de betaler med et kredittkort.
- Banken din belaster deg USD 1,00 for hver overføring du behandler, og overføringsgebyret utgiftsbelastes.

Når du konfigurerer et kundebetalingsgebyr, og hvis du setter **Gebyr**-feltet til **Kunde**, blir **Hovedkonto**-feltet ikke tilgjengelig, og systemet bruker kundeposteringsprofilen til å postere gebyret. Hvis du setter **Gebyr**-feltet til **Hovedbok**, må du sette **Hovedkonto**-feltet til hovedkontoen der betalingsgebyret skal posteres. Denne hovedkontoen er som regel en utgiftskonto. Følgende tabell viser et eksempel på posteringsprofilkonfigurasjonen for postering av betalingsgebyrer.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Finansjournal | 618190 | Bankgebyrutgift | Utgift | Debet | Nei |  Hvis **Hovedbok** er valgt i **Gebyr**-feltet, velger du denne kontoen i **Hovedkonto**-feltet for betalingsgebyret. |

Hvis du vil ha mer informasjon, se [Opprette kundebetalingsgebyrer](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Posteringskontoer for tilleggskoder

Hvis du må spore salgsbeløp i tillegg til linjevarer, kan du bruke tilleggskoder. Du kan for eksempel kreve kundene dine for frakt- og håndteringsgebyrer, eller du kan la enkelte frakt- og håndteringsgebyrer påløpe som en utgift internt. Du kan angi om disse beløpene skal posteres til utgiftskontoer eller legges til kostnadene for varene.

Du kan opprette tilleggskoder for kunder og leverandører. Når du konfigurerer en tilleggskode, må du definere posteringen. Posteringen styrer både debetkontoen og kreditkontoen. For hver tilleggskode du oppretter, kan du velge posteringstypen som skal brukes. Følgende tabell viser eksempler på vanlige tilleggskoder for kunder.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Betalingsgebyr | 411400 | Omsetning – gebyrer | Inntekt | Kredit | Nei | **Eksempel på ingen dekning:** Debetkunde-/leverandør- og kreditfinanskonto |
| Ordre, frakt | 403500 | Omsetning – frakt | Inntekt | Kredit | Nei | **Eksempel på frakt som belastes en kunde:** Debetkunde/leverandør og kreditfinanskonto |
| Rabatt\* | 403200 | Rabatt | Inntekt | Debet | Nei | **Eksempel på en kunderabatt:** Debetfinanskonto og kreditkunde/-leverandør |

\* I rabatteksepelet brukes posteringen bare når en tilleggskode legges til i bestillingshodet eller -linjen. Avansert rabattfunksjonalitet som er tilgjengelig i Microsoft Dynamics 365 Supply Chain Management, gir mer kontroll og automatisering av rabatter. Hvis du vil ha mer informasjon, kan du se [Kunderabatter](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

Tabellen over viser tre vanlige eksempler på posteringstyper som kan brukes for tilleggskoder. Den bør brukes som en retningslinje og et eksempel. Det gir ikke en omfattende liste over alle mulige kombinasjoner eller posteringstyper som kan brukes.

Hvis du vil ha mer informasjon, kan du se [Opprett tilleggskode](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Posteringskontoer for provisjoner

Du kan eventuelt konfigurere systemet til å beregne provisjoner for en selger eller en gruppe selgere på en gitt salgsordre. Hvis du aktiverer denne funksjonaliteten, må du konfigurere posteringskontoen som brukes til å beregne provisjonen. Denne konfigurasjonen gjøres på siden **Provisjonspostering** i modulen **Salg og markedsføring**.

Hvis du vil ha mer informasjon, kan du se [Definere regler for salgsprovisjon](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md).
