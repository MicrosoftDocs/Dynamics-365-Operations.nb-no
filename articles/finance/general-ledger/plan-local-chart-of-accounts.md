---
title: Planlegg den lokale kontoplanen
description: Denne artikkelen gir informasjon som vil hjelpe deg med å planlegge kontoplanen når du har krav til lovpålagte/lokale krav for organisasjonen.
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: twheeloc
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78379fd51cf24985fce83e2b6aa9a475af7df363
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946252"
---
# <a name="plan-your-local-chart-of-accounts"></a>Planlegg den lokale kontoplanen

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon som vil hjelpe deg med å planlegge kontoplanen når organisasjonen har juridiske enheter som må oppfylle krav for bestemte lokaliteter der de gjør forretninger. Denne artikkelen bruker følgende termer til å beskrive kontoplaner:

- **Global** – Kontoplanen som organisasjonen bruker globalt. I de fleste tilfeller vil du konsolidere til denne kontoplanen.
- **Lokal** – En kontoplan som brukes i juridiske enheter i et bestemt land eller område.
- **Delt** – En kontoplan som mer enn én juridisk enhet kan bruke. Både den globale kontoplanen og lokale kontoplaner kan deles.

Du kan opprette og dele flere kontoplaner. En delt kontoplan kan brukes av mer enn én juridisk enhet, men bare én kontoplan kan tilordnes hver juridiske enhet. Kontoplanen som brukes en juridisk enhet bruker, er definert på **Finans**-siden.

Når kontoplanen utformes, ønsker mange organisasjoner en global kontoplan. Ved hjelp av den delte kontoplanfunksjonen kan du opprette en global kontoplan. Det er fordeler ved oppretting og bruk av en enkelt kontoplan. For eksempel er styre og kontroll, vedlikehold og rapportering enklere.

De fleste organisasjoner foretrekker en global kontoplan, og det er den enkleste typen å implementere. Likevel krever noen juridiske enheter en lokal kontoplan av følgende årsaker:

- Lokale lovbestemte krav
- Krav til lokale regnskapsstandarder
- Industrikrav
- Firmaspesifikke krav til rapportering og analyse

Hvis organisasjonen krever at en juridisk enhet bruker en lokal kontoplan, er to alternativer tilgjengelige for å implementere den:

- Tilordne den globale kontoplanen, og definer andre metoder for å møte de lokale kravene.
- Tilordne en lokal kontoplan til den juridiske enheten, og definer relasjoner til den globale kontoplanen.

Organisasjonsstrukturen og rapporteringsstrukturen bestemmer hvilket alternativ som skal brukes.

[![Diagram som viser hvordan organisasjonsstrukturen bestemmer om det skal brukes en global eller lokal kontoplan](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Hvis den globale kontoplanen er tilordnet den juridiske enheten, er følgende alternativer tilgjengelige for å møte lokale rapporteringskrav:

- Utføre lokal konsolidering.
- Bruk en finansdimensjon til å spore den lokale kontoplanen.
- Opprett lokale hovedkontoer i den globale kontoplanen.
- Utfør lokal tilordning til den lokale kontoplanen.

Hvis den lokale kontoplanen er tilordnet den juridiske enheten, er eneste tilgjengelige alternativ for å imøtekomme globale rapporteringskrav, global konsolidering.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Global kontoplan tilordnet en juridisk enhet

Hvis du må tilordne den globale kontoplanen til en juridisk enhet, er fire alternativer tilgjengelige for konfigurering av systemet, som beskrevet tidligere. For alle fire alternativene konfigureres og kobles én enkelt kontoplan til hver juridiske enhet på **Finans**-siden. Hvert alternativ bruker deretter en annen tilnærming for å tilfredsstille lokaliseringskravene. Delene nedenfor beskriver trinnene på høyt nivå for å konfigurere systemet for lokaliseringskravene. De beskriver også fordelene og ulempene ved hvert alternativ.

### <a name="do-local-consolidation"></a>Utføre lokal konsolidering

Lokal konsolidering er den anbefalte tilnærmingen for å imøtekomme lokale kontoplanbehov og dra nytte av systemfunksjonaliteten som ble utformet for dette formålet.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Definere konsolidering for en lokal kontoplan

1. Opprett en enkelt, global kontoplan som inkluderer alle de nødvendige hovedkontoene.
2. Tilordne den globale kontoplanen på siden **Finans** i hver juridiske enhet.
3. Opprett en juridisk enhet for konsolidering for hver lokalisering som er nødvendig.
4. Følg ett av disse trinnene:

    - Hvis det bare kreves én lokalisering, konfigurerer du konsolideringskontoen på siden **Hovedkonto** eller bruker sidene **Konsolideringsgrupper** og **Flere konsolideringskontoer**.
    - Hvis det kreves mer enn én lokalisering, eller hvis både kontonummeret og kontonavnet krever oversettelse, bruker du sidene **Konsolideringsgrupper** og **Flere konsolideringskontoer** til å representere lokaliseringskravene.

5. Kjør konsolideringsprosessen for å transformere verdien fra den juridiske kildeenheten som bruker den globale kontoplanen, til konsolideringsfirmaet som bruker den lokale kontoplanen.

#### <a name="advantages"></a>Fordeler

- Denne fremgangsmåten gir en konsekvent måte å jobbe på i hele organisasjonen.
- En oversettelse av den lokale stillingen er utført.
- Denne fremgangsmåten støtter oversettelse av både hovedkonto-IDen og navnet på hver hovedkonto.
- Den støtter flere lokaliseringer.

#### <a name="disadvantages"></a>Ulemper

- Det opprettes et ekstra konsolideringsfirma.
- En ekstra konsolideringsprosess fullføres.
- Denne fremgangsmåten kan rapportere i det lokale diagrammet bare etter at konsolideringsprosessen er fullført.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Bruke en finansdimensjon til å spore den lokale kontoplanen

Denne fremgangsmåten bruker en finansdimensjon der finansdimensjonsverdiene representerer de lokale hovedkontoene som er nødvendige for lokaliseringen. Det fungerer godt hvis bare én lokalisering er nødvendig. Den blir imidlertid mindre anvendelig når du legger til flere lokaliseringer og finansdimensjoner.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Opprette en finansdimensjon for en lokal kontoplan

1. Opprett en enkelt, global kontoplan som inkluderer alle de nødvendige hovedkontoene.
2. Tilordne den globale kontoplanen på siden **Finans** i hver juridiske enhet.
3. Opprett en finansdimensjon som representerer den lokale kontoplanen.
4. Opprett finansdimensjonsverdire som representerer hovedkontoen i den lokale kontoplanen.
5. Oppdater kontostrukturen slik at den inkluderer finansdimensjonen "lokal kontoplan".
6. Sørg for at den lokale kontoplanens finansdimensjon alltid har en verdi, og at den ikke tillater en tom verdi. Vurder å bruke avledede dimensjoner eller faste dimensjoner.
7. Opprett et finansdimensjonssett der finansdimensjonen i den lokale kontoplanen er den første valgte finansdimensjonen. Finansdimensjonssettet kan brukes når råbalansen genereres.

#### <a name="advantages"></a>Fordeler

- Hovedkontoene for både globale og lokale kontoplaner finnes på transaksjonsnivå. Hovedkontoen er global, og finansdimensjonsverdien er lokal.
- Denne fremgangsmåten gir rapportering i sanntid og visninger av både den globale finansposisjonen og den lokale finansposisjonen.

#### <a name="disadvantages"></a>Ulemper

- Hvis feltet **Verdiene som brukes for samlekonto** er satt til **Regnskapsdistribusjoner** i økonomimodulparametere, blir finansdimensjonene som representerer hovedkontoen for utgift/aktiva/omsetning, feil brukt for samlekontoen for kunder og leverandører. Vi anbefaler at du angir feltet til et kildedokument i stedet for å sikre at de riktige finansdimensjonsverdiene brukes.
- Hvis det kreves mange lokale kontoplaner, og én finansdimensjon brukes for alle, kan listen over finansdimensjonsverdier som brukes, bli lang og vanskelig å arbeide med.
- Hvis det kreves mange lokale kontoplaner, og en egen finansdimensjon brukes til å representere hver enkelt, kan systemets brukervennlighet og ytelse påvirkes når det legges til finansdimensjoner og finansdimensjonssett.
- Vi anbefaler at du nøye vurderer antallet finansdimensjoner du krever, antall verdier i hvert sett og antall finansdimensjonssett, fordi alle disse faktorene kan påvirke systemets ytelse.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Opprette lokale hovedkontoer i den globale kontoplanen

*Hva kopieringsredigeringsprogrammet spør om*: I denne fremgangsmåten vil de lokale hovedkontoene i den globale kontoplanen inkludere hovedkontoene i den lokale kontoplanen i den globale kontoplanen.

*Opprinnelig versjon*: De lokale hovedkontoene i den globale kontoplantilnærmingen er at de lokale kontoplanhovedkontoene er inkludert i den globale kontoplanen.

*Hvis det står dette*: I denne fremgangsmåten inkluderes de lokale hovedkontoene i den lokale kontoplanen i den globale kontoplanen.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Opprette lokale hovedkontoer i den globale kontoplanen

1. Opprett en enkelt kontoplan som inkluderer hovedkontoene for både den globale kontoplanen og den lokale kontoplanen.
2. Tilordne kontoplanen på siden **Finans** i hver juridiske enhet.
3. Opprett totalkontoer i kontoplanen for å summere hovedkontoene som representerer det samme formålet.
4. Opprett overstyringer for juridisk enhet for hver lokale konto for å forhindre transaksjoner fra andre juridiske enheter som den lokale kontoen ikke er beregnet på.
5. Opprett juridiske enhetsoverstyringer på hver globale konto for å forhindre transaksjoner fra de juridiske enhetene for lokalisering.

#### <a name="advantages"></a>Fordeler

- En sanntidsvisning av både den globale finansstillingen og den lokale finansstillingen er tilgjengelig på bestemte rapporter og i bestemte visninger i systemet, for eksempel en finansrapport for balanse. Du får også tilgang til dette ved å bruke **Periode**-knappen i totalkontoen.
- Du har ikke et tilleggssegment i finanskontoen.

#### <a name="disadvantages"></a>Ulemper

- Total kontobruk og synlighet er begrenset. For eksempel vises ikke totalkontoer på **Råbalanse**-listesiden.
- Vedlikehold krever ekstra arbeid.
- Oppretting av finansrapporter krever ekstra manuelt arbeid.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Utfør lokal tilordning til den lokale kontoplanen

Når en global kontoplan initialiseres, forutsettes det at du administrerer tilordning og lokalisering utenfor systemet. I denne fremgangsmåten oppretter du bare én enkelt, global kontoplan i Microsoft Dynamics 365 Finance og håndterer kravene utenfor systemet.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Opprette ekstern tilordning til en lokal kontoplan

1. Opprett en enkelt, global kontoplan som inkluderer alle de nødvendige hovedkontoene.
2. Tilordne den globale kontoplanen på siden **Finans** i hver juridiske enhet.
3. Utfør tilordningen til den lokale kontoplanen utenfor Finance.

#### <a name="advantages"></a>Fordeler

- Denne fremgangsmåten gir enhetlige måter å jobbe på i hele organisasjonen.

#### <a name="disadvantages"></a>Ulemper

- Ingen lokal rapportering fra systemet er tilgjengelig.
- Denne fremgangsmåten kan føre til feil når det opprettes finansrapporter.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Lokal kontoplan tilordnet en juridisk enhet

Hvis organisasjonen bestemmer seg for ikke å bruke en global kontoplan på tvers av juridiske enheter, opprettes det en egen kontoplan for hver unike, lokale kontoplan. Hver juridiske enhet er da koblet til den tilsvarende kontoplanen på **Finans**-siden.

### <a name="do-global-consolidation"></a>Utføre global konsolidering

I denne fremgangsmåten brukes et konsolideringsfirma til å rulle opp og kombinere saldoene fra hvert lokale kildefirma til den kombinerte globale kontoplanen i konsolideringsfirmaet. Denne fremgangsmåten krever at du vedlikeholder en tilordning av hver lokale kontoplan til den globale kontoplanen i konsolideringsfirmaet.

#### <a name="set-up-global-consolidation"></a>Opprette global konsolidering

1. Opprett en separat kontoplan for hver juridiske enhet som har ulike lokale kontoplaner. Hvis en juridisk enhet har samme lokale kontoplan, kreves det bare én lokal kontoplan, og den kan deles.
2. Tilordne den riktige kontoplanen på siden **Finans** i hver juridiske enhet.
3. Valgfritt: Opprett en kontoplan for den globale kontoplanen for hvert konsolideringsfirma som har en forskjellig global kontoplan.
4. Opprett en juridisk konsolideringsenhet for hvert konsolideringsnivå som er nødvendig, og tilordne den riktige kontoplanen på **Finans**-siden.
5. Følg ett av disse trinnene:

    - Hvis det bare kreves én konsolidering, konfigurerer du konsolideringskontoen på **Hovedkonto**-siden.
    - Hvis det kreves mer enn én konsolidering, eller hvis både kontonummeret og kontonavnet krever oversettelse, bruker du sidene **Konsolideringsgrupper** og **Flere konsolideringskontoer** til å representere kravene for den globale kontoplanen.

6. Kjør konsolideringsprosessen for å overføre saldoene fra de lokale juridiske enhetene til den konsoliderte juridiske enheten. Den konsoliderte juridiske enheten bruker konsolideringskontoene du definerte i trinn 5.

#### <a name="advantages"></a>Fordeler

- Det lokale regnskapsstandardformatet brukes opprinnelig.
- Denne fremgangsmåten gir det lokale økonomiteamet en enklere måte å jobbe på.

#### <a name="disadvantages"></a>Ulemper

- Ingen sanntidsvisning av den globale stillingen er tilgjengelig.
- Konsolideringsprosessen kan kjøres oftere.

## <a name="additional-resources"></a>Tilleggsressurser

- [Planlegge kontoplanen](plan-chart-of-accounts.md)
- [Konfigurere finans](configure-ledger.md)
- [Finansdimensjoner og postering](Default-dimensions.md#balancing-dimension)
- [Finansdimensjonssett](financial-dimension-sets.md)
- [Konsoliderings- og elimineringsoversikt](../budgeting/consolidation-elimination-overview.md)
- [Konsolideringskontogrupper og en ekstra konsolideringskontoer](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
