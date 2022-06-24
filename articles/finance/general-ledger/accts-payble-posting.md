---
title: Leverandører-posteringer
description: Denne artikkelen beskriver hvordan posteringer konfigureres i Leverandører, og gir eksempler på posteringskonfigurasjoner.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b3593e01ed4d0a88b5816803f1d67fa7ed5e0f6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908016"
---
# <a name="accounts-payable-posting"></a>Leverandører-postering

[!include [banner](../includes/banner.md)]

Den primære posteringsprofilen for **Leverandører**-modulen er leverandørposteringsprofilen. Denne posteringsprofilen bestemmer samlekontoen som brukes når leverandørsaldoer posteres til økonomimodulen. En samlekonto er en hovedkonto. Den kalles også handelskontoen for leverandører.

Hvis du vil ha mer informasjon, kan du se [Leverandørposteringsprofiler](../accounts-payable/vendor-posting-profiles.md).

Flere posteringskonfigurasjoner i tillegg til leverandørposteringsprofilen er tilgjengelige i Leverandører. De følgende delene gir mer informasjon om disse andre posteringskonfigurasjonene.

## <a name="methods-of-payment-posting-accounts"></a>Posteringskontoer for betalingsmåter

Betalingsmåter definerer hvordan en betaling skal posteres i økonomimodulen. De kontrollerer også virkemåten til betalingsutdataene. Vanligvis opprettes det én betalingsmåte for hver betalingstype som organisasjonen foretar (for eksempel kontant, sjekk, kredittkort, pengeordre og objekt).

Feltene i **Postering**-delen på hurtigfanen **Generelt** på siden **Betalingsmåter** (**Leverandører > Betalingsoppsett > Betalingsmåter**) styrer hvordan en betaling posteres til økonomimodulen. Først må du velge en verdi i **Kontotype**-feltet. Kontotypen du velger, styrer virkemåten til **Betalingskonto**-feltet. Vi anbefaler at du velger **Bank** i **Kontotype**-feltet og velger deretter bankkontoen i **Betalingskonto**-feltet. Fordelen med tilnærmingen er at systemet vil postere betalingen til Bank-underhovedboken, som støtter avstemming og andre kontantrelaterte prosesser. Følgende tabell viser et eksempel på konfigurasjonen til posteringsprofilen hvis du bruker modulen **Kontant- og bankbehandling**.

| Posteringstype | Kontotype | Eksempel på betalingskontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Bank | Bank | Bank of America | Bankkonto som er koblet til en ressurs | Debet | Nei | For hver betalingsmåte angir du hovedkontoen i **Betalingskonto**-feltet. |

Hvis du ikke planlegger å bruke Kontant- og bankbehandling, bør du velge **Hovedbok** i **Kontotype**-feltet og deretter velge hovedkontoen i **Betalingskonto**-feltet. Følgende tabell viser et eksempel på konfigurasjonen til posteringsprofilen hvis du **ikke** bruker modulen Kontant- og bankbehandling.

| Posteringstype | Kontotype |Eksempel på betalingskonto | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank of America | Objekt | Debet | Nei | For hver betalingsmåte angir du hovedkontoen i **Betalingskonto**-feltet. |

## <a name="bridging-accounts"></a>Mellomkontoer

Mellompostering er en totrinns prosess som brukes når betalinger posteres. Det er en valgfri funksjon som for eksempel kan brukes med bankkontoer med nullsaldo. Det kan bidra til å sikre en mer problemfri og raskere bankavstemmingsprosess. I det første trinnet posteres en betaling til en midlertidig konto (mellomkontoen). I det andre trinnet tilbakeføres den posterte oppføringen og posteres til bankkontoen når betalingen tømmer banken. Følgende tabell viser et eksempel på posteringsprofilkonfigurasjonen for mellompostering.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Finansjournal | 130725 | Ikke-klarerte kontanter | Gjeld | Debet | Ja | For hver betalingsmåte angir du hovedkontoen i **Mellomkonto**-feltet. |

Hvis du vil ha mer informasjon, kan du se [Definer og behandle mellombetalinger](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="customer-cash-discounts-posting-accounts"></a>Posteringskontoer for kundekontantrabatter

Hvis organisasjonen mottar kontantrabatter fra leverandører som retur for rask betaling, må du konfigurere kontantrabattkoder og angi hvordan rabattene skal posteres i økonomimodulen. Det finnes flere alternativer for angivelse av hovedkontoen som brukes til å postere en kundekontantrabatt.

Hvis du vil ha mer informasjon, kan du se [Kontantrabatter](../cash-bank-management/cash-discounts.md).

## <a name="payment-fee-posting-accounts"></a>Posteringskontoer for betalingsgebyr

Ved bruk av betalingsgebyrer kan du automatisk legge til et gebyr i en leverandørbetaling når et sett med betingelser gjelder. Betalingsgebyrer kan betales til leverandøren, eller de kan posteres til bankkontoen som en utgift. Her er noen eksempler:

- En leverandør belaster deg 3 prosent av det totale betalingsbeløpet hvis du betaler med et kredittkort.
- Banken din belaster deg USD 1,00 for hver overføring du behandler, og gebyret blir utgiftsbetales.

Når du konfigurerer et leverandørbetalingsgebyr, og hvis du setter **Gebyr**-feltet til **Leverandør**, blir **Hovedkonto**-feltet ikke tilgjengelig, og systemet bruker leverandørposteringsprofilen til å postere gebyret. Hvis du setter **Gebyr**-feltet til **Hovedbok**, må du sette **Hovedkonto**-feltet til hovedkontoen der betalingsgebyret skal posteres. Denne hovedkontoen er som regel en utgiftskonto. Følgende tabell viser et eksempel på posteringsprofilkonfigurasjonen for postering av betalingsgebyrer.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Finansjournal | 618190 | Bankgebyrutgift | Utgift | Debet | Nei | Hvis **Hovedbok** er valgt i **Gebyr**-feltet, velger du denne kontoen i **Hovedkonto**-feltet på **Betalingsgebyr**-siden. |

Hvis du vil ha mer informasjon, kan du se [Definere leverandørbetalingsgebyrer](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Posteringskontoer for tilleggskoder

Hvis du må spore innkjøpsbeløp i tillegg til linjevarer, kan du bruke tilleggskoder. Leverandøren kan for eksempel kreve frakt- og håndteringsgebyrer av deg, eller enkelte frakt- og håndteringsgebyrer kan påløpe som en utgift internt. Du kan angi om disse beløpene skal posteres til utgiftskontoer eller legges til kostnadene for varene.

Du kan opprette tilleggskoder for kunder og leverandører. Når du konfigurerer en tilleggskode, må du definere posteringen. Posteringen styrer både debetkontoen og kreditkontoen. Når du oppretter tilleggskoder, kan du velge posteringstypen som skal brukes for hver tilleggskode. Følgende tabell viser eksempler på vanlige tilleggskoder for leverandører på **Tilleggskoder**-siden.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Innkjøpsgebyr | La feltet stå tomt. | Gjelder ikke | Artikkel | Debet | Nei | **Eksempel for et innkjøpsgebyr for en vare:** </p><ul><li>**Debettype**-feltet = **Vare**</li><li>  **Kredittype**-feltet = **Kunde/leverandør**.</li><li> Vareposteringen bruker hovedkontoen fra lagerposteringsprofilen. |
| Ordre, frakt | 600120 | Frakt i | Inntekt | Debet | Nei | **Eksempel på frakt som betales til en leverandør:** </p><ul><li>**Debettype**-feltet = **Finanskonto**</li><li> **Kredittype**-feltet = **Kunde/leverandør** |
| Rabatt\* | 503160 | Leverandørrabatt (kontra COGS)| Utgift | Kredit | Nei | **Eksempel på en leverandørrabatt:**</p><ul><li>**Debettype**-feltet = **Kunde/leverandør**</li><li>**Kredittype**-feltet = **Finanskonto** |

\* I rabatteksepelet brukes posteringen bare når en tilleggskode legges til i bestillingshodet eller -linjen. Avansert rabattfunksjonalitet som er tilgjengelig i Microsoft Dynamics 365 Supply Chain Management, gir mer kontroll og automatisering av rabatter. Hvis du vil ha mer informasjon, kan du se [Leverandørrabatter](../../supply-chain//procurement/vendor-rebates.md).

Tabellen over viser tre vanlige eksempler på posteringstyper som kan brukes for tilleggskoder. Den bør brukes som en retningslinje og et utvalg av eksempler. Det gir ikke en omfattende liste over alle mulige kombinasjoner eller posteringstyper som kan brukes.

Hvis du vil ha mer informasjon, kan du se [Opprett tilleggskode](../accounts-receivable/create-charges-codes.md).
