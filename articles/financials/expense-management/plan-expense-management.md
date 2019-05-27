---
title: Konfigurere reiseregning
description: Denne artikkelen beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du konfigurerer Reiseregning og utlegg i Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ac9959a4ee66e52ead5050897403602e407ca10
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570629"
---
# <a name="configure-expense-management"></a>Konfigurere reiseregning

[!include [banner](../includes/banner.md)]

Dette emnet beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du konfigurerer Reiseregning og utlegg i Microsoft Dynamics 365 for Finance and Operations. I Reiseregning kan du lagre informasjon om betalingsmetoder, reiserekvisisjoner, utgiftsrapporter, retningslinjer, og så videre.

Fordi mange av valgene du gjør når du planlegger konfigurasjonen for Reiseregning og utlegg, er basert på organisasjonens hierarki og økonomiske struktur, må du referere til planleggingsdokumentene for disse områdene.

## <a name="intercompany-expenses"></a>Konserninterne utgifter

Når du aktiverer konserninterne utgifter, tillater du juridiske personer og ansatte å pådra seg utgifter på vegne av en annen juridisk enhet, og samle inn betaling fra den juridiske enheten for ansettelse i organisasjonen din. For eksempel, en ansatt i juridisk enhet A fullfører et prosjekt for juridisk enhet B, og prosjektet har reiserelaterte utgifter. Hvis konserninterne utgifter er aktivert kan ansatte sende inn en utgiftsrapport som legger utgiften til juridisk enhet B, og utgiften må da betales av juridisk enhet A. Hvis organisasjonen ikke har flere juridiske enheter, trenger du ikke å aktivere konserninterne utgifter.

**Beslutning:** Vil du aktivere konserninterne utgifter?

## <a name="financial-management"></a>Økonomistyring

Reiseregning og utlegg er tett integrert med økonomistyring av organisasjonen. Mange konfigurasjoner for reiseregning vil være basert på de beslutningene du har gjort for organisasjonens økonomi. I de følgende avsnittene beskrives de ulike områdene som krever planlegging og beslutninger, basert på organisasjonens økonomiske beslutninger og veiledning fra lederskapet ditt.

### <a name="per-diems"></a>Kostgodtgjørelse

Du må definere kostgodtgjørelse for ansatte som organisasjonen gir. Fordi kostgodtgjørelse vanligvis brukes til å dekke utgifter som måltider, overnatting og andre tilfeldige utgifter, kan du opprette regler for kostgodtgjørelse som organisasjonen skal tilby. kostgodtgjørelsessatser kan være basert på tid på året, reisestedet, eller begge deler. Når du definerer en kostgodtgjørelsesregel, kan du angi at en prosentandel av kostgodtgjørelsessatsen skal holdes tilbake hvis en arbeider mottar gratis måltider eller tjenester. Du kan også definere kostgodtgjørelsessatser for å angi minimum og maksimum antall timer som kostgodtgjørelsessatsen kan brukes på en arbeiders reise.

**Beslutninger:**

- Standard kostgodtgjørelsesregler for de første og siste dagene:

    - Hva er minste antall timer en ansatt kan kreve for en dag og fremdeles motta kostgodtgjørelse?
    - Er det en reduksjon i beløpet som tilbys for måltider for første dag og siste dag? Hvis det er en reduksjon, hva er prosentsatsen for reduksjonen?
    - Er det en reduksjon i beløpet som tilbys for et hotell for den første og siste dagen? Hvis det er en reduksjon, hva er prosentsatsen for reduksjonen?
    - Er det en reduksjon i beløpet som tilbys for andre utgifter som påløper første dag og siste dag? Hvis det er en reduksjon, hva er prosentsatsen for reduksjonen?

- Standard kostgodtgjørelseregler:

    - Finnes det en prosentvis reduksjon i kostgodtgjørelsen for hvert måltid hvis måltidet eksempelvis er gratis? Hvis det er en reduksjon, hva er reduksjonsprosentsatsen for hvert måltid?
    - Beregnes måltidsreduksjonen per dag, per tur eller etter antall måltider per dag?
    - Bør kostgodtgjørelsesbeløp avrundes på vanlig måte eller rundes opp?
    - Beregnes kostgodtgjørelse basert på en periode på 24 timer eller en kalenderdag?

- Kostgodtgjørelse er basert på lokasjon:

    - Er kostgodtgjørelsen ulik basert på lokasjon? Hvilke lokasjoner inkluderes?
    - Hvis kostgodtgjørelsen er ulik basert på lokasjon, hva er prosentsats og beløp som tilbys for følgende typer utgifter, for hver lokasjon:

        - Måltider
        - Hotell
        - Andre utgifter

### <a name="expense-management-journals-and-accounts"></a>Journaler og kontoer for reiseregninger og utlegg

Administrasjon av reiseregninger og utlegg krever at du bruker flere journaler og kontoer. Du må angi for eksempel om den samme kontoen brukes for forskudd og kredittkorttvister.

**Beslutninger:**

- Hvilken finansjournal posteres godkjente reiseregninger til?
- Hvilken konto brukes til forskudd?
- Bør forskudd posteres umiddelbart?

### <a name="payment-methods"></a>Betalingsmåter

Når du lar ansatte pådra seg utgifter på vegne av firmaet, må du definere betalingsmåtene som ansatte kan bruke. Du kan for eksempel tillate at ansatte kan bruke kontanter eller et firmakredittkort. Du kan også tillate at ansatte skal bruke personlige kredittkort, og deretter tilbakebetale de ansatte. Du må ta følgende avgjørelser for hver enkelt betalingsmåte du godkjenner.

**Beslutninger:**

- Hvilke betalingsmåter er tillatt?
- Hvem eier betalingsmåteutgiftene?
- Finnes det en motkontotype? Hvis det finnes en motkontotype, hva er den?
- Hvis det finnes en motkonto, hva er kontoen?
- Hvis betalingsmåten er et kredittkort, bør betalingsmåten bare brukes med importerte transaksjoner?

### <a name="expense-categories-and-shared-categories"></a>Utgiftskategorier og delte kategorier

Når ansatte oppretter en reiseregning, må hver utgift de registrerer, være tilknyttet en utgiftskategori. Utgiftskategorier er hentet fra delte kategorier som kan deles på tvers av juridiske enheter i organisasjonen. Disse kategoriene kan også deles i Prosjektledelse og regnskap, avhengig av hvordan organisasjonen din er definert. Basert på definisjonen for organisasjonen din og veiledningen fra implementeringsteamet, avgjør om kategoriene som brukes i Reiseregning kun skal brukes i Reiseregning, eller om de skal deles mellom Prosjektledelse og regnskap og Utgiftsstyring. Legg merke til at disse kategoriene kan deles mellom prosjekt og utgifter eller prosjekt og produksjon, men ikke mellom utgifter og produksjon. Du må ta følgende avgjørelser for hver utgiftskategori.

**Beslutninger:**

- Hva er utgiftskategorien? Eksempler inkluderer kategorier for flyreiser, hotell eller kjørelengde.
- Kan utgiftskategorien også brukes i Prosjektledelse og regnskap?
- Hva er utgiftstypen?
- Hva er standard betalingsmåte for utgiftskategorien?
- Skal utgifter i utgiftskategorien spesifiseres?
- Hva er hovedstandardkontoen for utgiftskategorien?
- Hva er standard mva-gruppe for vare for utgiftskategorien?
- Er flere betalingsmåter tillatt for utgiftskategorien? Hvis flere betalingsmåter er tillatt, hva er de?
- Er det underkategorier i denne utgiftskategorien? Hvis det er underkategorier, må du også gjøre følgende beslutninger:

    - Er noen av underkategoriene utelatt fra skatterefusjon?
    - Hva er mva-gruppe for vare for underkategoriene?

Hvis utgiftskategorien også brukes i Prosjektledelse og regnskap, besvar følgende gjenstående spørsmål Eller gå videre til neste del.

- Hvilke kostnadsregnskap vil bli brukt til følgende utgifter?

    - Kostnad
    - Lønnsfordeling
    - RIA - Kostverdi
    - Kostnad - vare
    - RIA - kostverdi - vare
    - Påløpt tap
    - RIA - påløpt tap

- Hvilke inntektskontoer brukes til følgende?

    - Fakturert omsetning
    - Påløpte inntekter - salgsverdi
    - RIA - Salgsverdi
    - Påløpte inntekter - produksjon
    - RIA - Produksjon
    - Påløpte inntekter - fortjeneste
    - RIA - Fortjeneste
    - Påløpte inntekter - abonnement
    - RIA - abonnement

### <a name="taxes"></a>Avgifter

For utgiftsrelaterte avgifter må du bestemme hva som inkluderes eller aktivert for reiseregninger.

**Beslutninger:**

- Er mva inkludert i utgiftsbeløp?
- Skal skatterefusjon aktiveres for utgifter?

    > [!NOTE]
    > Når du planlegger hovedboken, kan du ikke aktivere skatteutvinning på utgifter hvis du bestemte deg for å søke om amerikansk omsetningsavgift og bruke skatteregler. (For å søke om amerikansk omsetningsavgift og skatteregler, angi **Søk om omsetningsavgift**-alternativet til **Ja**.)

## <a name="policies"></a>Policyer

Ved å opprette regnskapsrapportpolicyer kan du hjelpe organisasjonen med å spare tid og penger når ansatte pådrar seg utgifter på vegne av denne. Policyene sikrer at ansatte er på budsjett, gir all nødvendig informasjon, og bruker kun penger etter hvert som de trenger det. Du må ta følgende avgjørelser for hver utgiftsrapportpolicy og hver utgiftsrapportgodkjenning du oppretter.

**Beslutninger:**

- Hva er navnet på policyen?
- Hva er utgiftspolicyen for?
- Hvis du tidligere har besluttet å aktivere konserninterne utgifter, hvilke firmaer i organisasjonen din vil denne policyen gjelde for?
- Når trer policyen i kraft?
- Når utløper policyen?
- Hva er policyregelen?
- Hva er resultatet av policyregelen?
