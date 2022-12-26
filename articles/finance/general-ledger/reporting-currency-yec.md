---
title: Rapporteringsvaluta er ikke i balanse når årsavslutningen kjøres
description: Denne artikkelen beskriver hvordan rapporteringsvalutaen kan være i ubalanse når årsavslutningen kjøres.
author: kweekley
ms.date: 12/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 31f79791330e076d4fbd7b604ba9f9c6cd9b9195
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850264"
---
# <a name="reporting-currency-out-of-balance-when-the-year-end-close-is-run"></a>Rapporteringsvaluta er ikke i balanse når årsavslutningen kjøres

Når du har aktivert **Forståelse mellom utligning og årsavslutning**-funksjonen (**Forståelse**-funksjonen), vil ikke finanstransaksjoner som er utlignet, lenger inkluderes i åpningssaldoen for det neste regnskapsåret når årsavslutningen i økonomimodulen kjøres. Ekskludering av finanstransaksjoner som er utlignet, kan være en utfordring for kunder ved årsavslutning hvis det er definert en rapporteringsvaluta for finans.

Utligningen utføres bare for regnskapsvalutaen. Når finanstransaksjoner utlignes, bekrefter valideringen bare at regnskapsvalutadebetene er lik regnskapsvalutakredittene. Rapporteringsvalutabeløpene for disse finanstransaksjonene er ikke validert, og det kan hende at debet ikke er lik kredit for dem. I tillegg beregner og posterer ikke utligningen automatisk resultat i rapporteringsvalutaen.

På grunn av disse begrensningene må det finnes en resultattransaksjon i rapporteringsvalutaen når utligning er utført. Hvis det ikke er noe resultat i utligningen, vises en melding om ubalanse når årsavslutningen kjøres.

Følgende eksempel går gjennom trinnene for å ta opp dette problemet før årsavslutningen kjøres.

## <a name="example-setup"></a>Eksempeloppsett

Hvis du vil sette opp dette eksemplet, aktiverer du **Forståelse**-funksjonen og konfigurerer hovedkonto 110180 for utligning. Illustrasjonen nedenfor viser finanstransaksjonene som ble postert i den juridiske enheten DEMF. Regnskapsvalutaen for DEMF er amerikanske dollar (USD), og rapporteringsvalutaen er euro (EUR).

![Posterte finanstransaksjoner i rapporteringsvalutaen.](./media/reporting-currency-1.png)

Siden **Utligninger** viser finanstransaksjoner for hovedkonto 110180. Merk og hold (eller høyreklikk) i rutenettet, og velg deretter **Sett inn kolonner**. Legg til **Beløp i rapporteringsvaluta**-kolonnen slik at alle transaksjonsvaluta-, regnskapsvaluta- og rapporteringsvalutabeløp vises.

![Beløp i rapporteringsvaluta-kolonne som er lagt til på Utligninger-siden.](./media/Ledger-settlement2.png)

De to første finanstransaksjonene for 100,00 EUR utlignes som én gruppe, og de to neste finanstransaksjonene for 200,00 EUR utlignes som en annen gruppe. (De to transaksjonene vil ha ulike utlignings-ID-er.) Dette oppsettet viser at organisasjoner vil ha flere grupper med finanstransaksjoner som utlignes på forskjellige tidspunkt og har ulike utligningsdatoer. Når utligningen er fullført, viser **Utligninger**-siden følgende informasjon når den er filtrert til å vise transaksjoner som har statusen **Utlignet**.

![Utlignede transaksjoner på siden Utligninger.](./media/Settled-trans-filtered3.png)

På siden **Utligninger** velger og holder (eller høyreklikker) du i kolonnen **Beløp** i og velger deretter **Summer denne kolonnen**. Gjenta dette trinnet for **Beløp i rapporteringsvaluta**-kolonner. Regnskapsvalutaen må ha en differanse på 0 (null) for at utligningen skal skje. Det er imidlertid ingen validering av utligningsbeløpet for rapporteringsvalutaen. Illustrasjonen nedenfor viser en forskjell på –27,79 USD for rapporteringsvalutaen.

![Differanse for rapporteringsvalutaen.](./media/Difference4.png)

## <a name="year-end-close"></a>Årsavslutning

Hvis årsavslutningen nå kjøres for 2022, vil prosessen ende i en i ubalanse-feil. Denne feilen forårsakes direkte av at rapporteringsvalutaen ikke har et utligningsbeløp som er netto 0 (null).

![Feilmelding som angir at utligningsbeløpet ikke er 0 (null).](./media/YEC5.png)

## <a name="posting-reporting-currency-gainloss"></a>Postering av rapporteringsvalutaresultat

For at årsavslutningen skal bli kjørt uten feil, må differansen i rapporteringsvalutabeløpet redegjøres for, vanligvis som gevinst eller tap, og være inkludert i utligningen. Rapporteringsvalutaresultat kan posteres på flere måter:

- Hvis hovedkontoen er leverandørgjeld eller utestående fordringer, vil AR/AP-utligningen av disse dokumentene generere det nødvendige resultatet. Denne regnskapsoppføringen må inkluderes i utligningen når de tilsvarende finanstransaksjonene fra fakturaen, betalingene, kreditnotaene og så videre, utlignes.
- Hvis hovedkontoen er en konto i tillegg til leverandørgjeld eller utestående fordringer, må resultatet angis manuelt. Når resultatet posteres, bestemmes detaljnivået for regnskapsoppføringen av organisasjonen.
- Identifiser rapporteringsvalutaresultatbeløpet som må posteres, for hver hovedkonto.

Som beskrevet tidligere, kan denne posteringen gjøres på siden **Utligninger**.

1. Filtrer til datoområdet du vil postere resultat for. Hvis du planlegger å postere resultat per måned, filtrerer du for hver måned. Hvis du planlegger å postere et resultat per regnskapsår, filtrerer du for hele året.
2. Filtrer på hovedkontoen.
3. Filtrer på statusen, slik at bare **utlignede** transaksjoner vises.
4. Legg til en total i kolonnen **Beløp i rapporteringsvaluta**.
5. Hvis du vil postere resultatet på et mer detaljert nivå, kan du gjøre tilleggsfiltrering for utlignings-ID-en, finansdimensjonene og så videre. Totalbeløpet for kolonnen **Beløp i rapporteringsvaluta** representerer beløpet som resultatet blir postert for.
6. Gå til **Økonomimodul \> Journaloppføringer \> Justeringsjournaler for rapporteringsvaluta**.
7. Angi transaksjonen for resultatet. Denne journalen posterer bare en justering i rapporteringsvalutaen. Transaksjonsvalutaen og regnskapsvalutabeløpene som posteres, er alltid 0 (null). Hvis denne journalen ikke er brukt før, må du kanskje opprette et journalnavn som har journaltypen **Justering for rapporteringsvaluta** under **Økonomimodul \> Journaloppsett \> Journalnavn**.
8. Hvis hovedkontoen ikke tillater manuell registrering, blir ikke denne justeringen postert. Det kan derfor hende at du må deaktivere parameteren **Ikke tillat manuell registrering** på siden **Hovedkonto**.

![Manuell registrering på Journalbilag-siden.](./media/Manual-entry6.png)

Når du har postert justeringsjournalen, kan du gå tilbake til **Utligninger**-siden og velge hovedkontoen du posterte resultatet for. Resultatjusteringen må inkluderes i en utligning. Fordi rapporteringsvalutabeløpet ikke må ha netto 0 (null), kan du utligne eventuelle tidligere transaksjoner og deretter utligne dem på nytt, men ta med resultatet denne gangen. Hvor presis du vil være ved posteringen av resultat og utligningen av resultatet i utligninger, er opp til organisasjonen.

Illustrasjonen nedenfor viser at utligning ble opphevet for transaksjonene for 200 EUR og deretter merket for utligning på nytt. Denne gangen vil de inkludere resultatjusteringen.

![Resultatjustering på Utligninger-siden.](./media/gain-loss7.png)

Når transaksjonene er utlignet, endrer du **statusfilteret** slik at siden viser **Utlignede** transaksjoner. Totalen for **Beløp i rapporteringsvaluta**-kolonnen er nå 0 (null). Årsavslutningen kan nå kjøres som den skal.

![Vellykket årsavslutning.](./media/Zero-settled8.png)
