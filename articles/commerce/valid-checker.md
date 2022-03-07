---
title: Valider butikktransaksjoner for utdragsberegning
description: Dette emnet beskriver funksjonaliteten for validering av butikktransaksjoner i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 01/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: f51b1f39aa212fe8587761721194db7791bec5bc
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087455"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Valider butikktransaksjoner for utdragsberegning

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjonaliteten for validering av butikktransaksjoner i Microsoft Dynamics 365 Commerce. Valideringsprosessen identifiserer og merker transaksjoner som vil forårsake posteringsfeil, før de plukkes opp av utdragsposteringsprosessen.

Når du prøver å postere et utdrag, kan valideringsprosessen mislykkes på grunn av inkonsekvente data i handelstransaksjonstabellene. Her er noen eksempler på faktorer som kan forårsake disse inkonsekvensene:

- Transaksjonsbeløpet i toppteksttabellen samsvarer ikke med transaksjonsbeløpet på linjene.
- Antall varer som er angitt i toppteksttabellen, stemmer ikke overens med antall varer i transaksjonstabellen.
- Avgifter i toppteksttabellen samsvarer ikke med avgiftsbeløpet på linjene. 

Hvis inkonsekvente transaksjoner blir plukket opp av prosessen, kan salgsfakturaer og betalingsjournaler som er opprettet, føre til at utdragspostering mislykkes. Prosessen **Valider butikktransaksjoner** forhindrer disse problemene ved å sikre at bare transaksjoner som består transaksjonsvalideringsreglene, sendes til beregningsprosessen for transaksjonsutdrag.

Illustrasjonen nedenfor viser regelmessige dagtidsprosesser for opplasting av transaksjoner, validering av transaksjoner og beregning og postering av transaksjonsutdrag samt dagsoppgjørsprosesser for beregning og postering av regnskapsoppgjør.

![Illustrasjon som viser regelmessige dagtidsprosesser for opplasting av transaksjoner, validering av transaksjoner og beregning og postering av transaksjonsutdrag samt dagsoppgjørsprosesser for beregning og postering av regnskapsoppgjør](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Valideringsregler for butikktransaksjon

Partiprosessen **Valider butikktransaksjoner** kontrollerer konsekvensen i handelstransaksjonstabellene basert på følgende valideringsregler.

> [!NOTE]
> Vi forsetter å legge til valideringsregler i senere versjoner.

### <a name="transaction-header-validation-rules"></a>Valideringsregler for transaksjonstopptekst

Tabellen nedenfor viser valideringsreglene for transaksjonstopptekst som blir kontrollert mot toppteksten til handelstransaksjoner, før disse transaksjonene sendes til utdragspostering.

| Regel | Beskrivelse |
|-------|-------------|
| Forretningsdato | Denne regelen validerer at forretningsdatoen for transaksjonen er knyttet til en åpen regnskapsperiode i finans. |
| Valutaavrunding | Denne regelen validerer at transaksjonsbeløpene avrundes i henhold til avrundingsregelen for valuta. |
| Kundekonto | Denne regelen validerer at kunden som brukes i transaksjonen, finnes i databasen. |
| Rabattbeløp | Denne regelen validerer at rabattbeløpet i toppteksten er lik summen av rabattbeløpene på linjene. |
| Posteringsstatus for avgiftsdokument (Brasil) | Denne regelen validerer at regnskapsdokumentet kan posteres på riktig måte. |
| Bruttobeløp | Denne regelen validerer at bruttobeløpet i transaksjonstoppteksten samsvarer med nettobeløpet, inkludert avgift, for transaksjonslinjene pluss gebyr. |
| Netto | Denne regelen validerer at nettobeløpet i transaksjonstoppteksten samsvarer med nettobeløpet, ekskludert avgift, for transaksjonslinjene pluss gebyr. |
| Netto + avgift | Denne regelen validerer at bruttobeløpet i transaksjonstoppteksten samsvarer med nettobeløpet, ekskludert avgift, for transaksjonslinjene pluss alle avgifter og gebyr. |
| Antall varer | Denne regelen validerer at antall varer som er angitt i transaksjonstoppteksten, samsvarer med summen av antall på transaksjonslinjene. |
| Betalingsbeløp | Denne regelen validerer at betalingsbeløpet i transaksjonstoppteksten samsvarer med summen av alle betalingstransaksjoner. |
| Beregning av avgiftsfritak | Denne regelen validerer at summen av det beregnede beløpet og det fritatte avgiftsbeløpet på gebyrlinjene er lik det opprinnelige beregnede beløpet. |
| Priser inkludert avgift | Denne regelen validerer at flagget **Avgiften er inkludert i prisen** er konsekvent på tvers av transaksjonstoppteksten og avgiftstransaksjonene. |
| Transaksjonen er ikke tom | Denne regelen validerer at transaksjonen inneholder linjer, og at minst én linje ikke er annullert. |
| Under-/overbetaling | Denne regelen validerer at differansen mellom bruttobeløpet i toppteksten og betalingsbeløpet ikke er mer enn konfigurasjonen for maksimal under-/overbetaling. |

### <a name="transaction-line-validation-rules"></a>Valideringsregler for transaksjonslinje

Tabellen nedenfor viser valideringsreglene for transaksjonslinje som blir kontrollert mot linjedetaljene til handelstransaksjoner, før disse transaksjonene sendes til utdragspostering.

| Regel | Beskrivelse |
|-------|-------------|
| Strekkode | Denne regelen validerer at alle varestrekkodene som brukes på transaksjonslinjene, finnes i databasen. |
| Gebyrlinjer | Denne regelen validerer at summen av det beregnede beløpet og det fritatte avgiftsbeløpet på gebyrlinjene er lik det opprinnelige beregnede beløpet. |
| Gavekortreturer | Denne regelen validerer at det ikke finnes noen returer av gavekort i transaksjonen. |
| Varevariant | Denne regelen validerer at alle varer og alle varianter som brukes på transaksjonslinjene, finnes i databasen. |
| Linjerabatt | Denne regelen validerer at linjerabattbeløpet samsvarer med summen av rabattransaksjonene. |
| Linjeavgift | Denne regelen validerer at linjeavgiftsbeløpet samsvarer med summen av avgiftstransaksjonene. |
| Negativ pris | Denne regelen validerer at det ikke brukes negative priser på transaksjonslinjene. |
| Serienummerstyrt | Denne regelen validerer at serienummeret finnes i transaksjonslinjen for varer som styres av serienummer. |
| Serienummerdimensjon | Denne regelen validerer at det ikke er angitt et serienummer hvis varens serienummerdimensjon er inaktiv. |
| Fortegnsselvmotsigelse | Denne regelen validerer at fortegnet for antallet og fortegnet for nettobeløpet er det samme på alle transaksjonslinjene. |
| Avgiftsfritt | Denne regelen validerer at summen av linjevareprisen og det fritatte avgiftsbeløpet er lik den opprinnelige prisen. |
| Avgiftsgruppetilordning | Denne regelen validerer at kombinasjonen av mva-gruppen og mva-gruppen for vare produserer et gyldig mva-skjæringspunkt. |
| Måleenhetskonverteringer | Denne regelen validerer at måleenheten til alle linjene har en gyldig konvertering til lagermåleenheten. |

## <a name="enable-the-store-transaction-validation-process"></a>Aktiver valideringsprosessen for butikktransaksjon

Konfigurer jobben **Valider butikktransaksjoner** for periodiske kjøringer i Commerce Headquarters (**Retail og Commerce \> IT for Retail og Commerce \> Salgsstedspostering**). Den satsvise jobben planlegges på grunnlag av butikkens organisasjonshierarki. Vi anbefaler at du konfigurerer denne partiprosessen til å kjøre med samme frekvens som de satvise jobbene for **P-jobb** og **beregning av transaksjonsutdrag**.

## <a name="results-of-the-validation-process"></a>Resultater av valideringsprosessen

Resultatene av partiprosessen **Valider butikktransaksjoner** kan vises på hver detaljhandelstransaksjon. Feltet **Valideringsstatus** i transaksjonsposten er satt til **Vellykket**, **Feil** eller **Ingen**. Feltet **Tidspunkt for siste validering** viser datoen for siste valideringskjøring.

I tabellen nedenfor beskrives hver valideringsstatus.

| Valideringsstatus | Beskrivelse |
|-------------------|-------------|
| Vellykket | Alle aktiverte valideringsregler er bestått. |
| Feil | En aktivert valideringsregel har identifisert en feil. Du kan vise flere detaljer om feilen ved å velge **Valideringsfeil** i handlingsruten. |
| Ingen | Transaksjonstypen krever ikke at valideringsregler brukes. |

![Siden over butikktransaksjoner som viser feltet Valideringsstatus og knappen Valideringsfeil.](./media/valid-checker-validation-status-errors.png)

Bare transaksjoner som har valideringsstatusen **Vellykket**, blir trukket inn i transaksjonsutdragene. Hvis du vil vise transaksjoner som har statusen **Feil**, kan du se gjennom flisen **Valideringsfeil for hentesalg** i arbeidsområdet **Finans for handelsbutikk**.

![Fliser i arbeidsområdet Finans for handelsbutikk.](./media/valid-checker-cash-carry-validation-failures.png)

Hvis du vil ha mer informasjon om hvordan du korrigerer valideringsfeil for hentesalg, kan du se [Rediger og overvåk hentesalgs- og kassastyringstransaksjoner](edit-cash-trans.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Rediger og overvåk hentesalgs- og kassastyringstransaksjoner](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
