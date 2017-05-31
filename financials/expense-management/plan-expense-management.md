---
title: Konfigurere reiseregning
description: "Denne artikkelen beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du konfigurerer Reiseregning og utlegg i Microsoft Dynamics AX. I området Reiseregning og utlegg kan du blant annet lagre informasjon om betalingsmåter, reiserekvisisjoner, reiseregninger og retningslinjer."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 62bef78c143f7ad83e78982dbecb1c9e4542187d
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="configure-expense-management"></a>Konfigurere reiseregning

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du konfigurerer Reiseregning og utlegg i Microsoft Dynamics AX. I området Reiseregning og utlegg kan du blant annet lagre informasjon om betalingsmåter, reiserekvisisjoner, reiseregninger og retningslinjer. 

Fordi mange av valgene du gjør når du planlegger konfigurasjonen for Reiseregning og utlegg, er basert på organisasjonens hierarki og økonomiske struktur, må du referere til planleggingsdokumentene for disse områdene.

## <a name="intercompany-expenses"></a>Konserninterne utgifter
Når du aktiverer konserninterne utgifter, gir du juridiske enheter og ansatte tillatelse til å pådra seg utgifter på vegne av, og samle inn betaling fra, en annen juridisk enhet i organisasjonen. En ansatt i juridisk enhet A fullfører eksempelvis et prosjekt for juridisk enhet B. Hvis konserninterne utgifter er aktivert, kan den ansatte deretter arkivere en timeregistrering til, og betales av, juridisk enhet B. Hvis organisasjonen ikke har flere juridiske enheter, trenger du ikke å aktivere konserninterne utgifter. **Beslutning:** Vil du aktivere konserninterne utgifter?

## <a name="financial-management"></a>Økonomistyring
Reiseregning og utlegg er tett integrert med økonomistyring av organisasjonen. Store deler av konfigurasjonen for Reiseregning og utlegg vil være basert på valgene du har gjort for organisasjonens økonomi. Delene nedenfor beskriver ulike områder som krever planlegging og avgjørelser basert på organisasjonens økonomiske beslutninger og veiledning fra ledelsesteamet ditt.

### <a name="per-diems"></a>Kostgodtgjørelse

Du må definere kostgodtgjørelse for ansatte som organisasjonen gir. Fordi kostgodtgjørelse vanligvis brukes til å dekke utgifter som måltider, overnatting og andre tilfeldige utgifter, kan du opprette regler for kostgodtgjørelse som organisasjonen skal tilby. Kostgodtgjørelsessatser kan være basert på tid på året, reisemål eller begge deler. Når du definerer en kostgodtgjørelsesregel, kan du angi at en prosentandel av kostgodtgjørelsessatsen skal holdes tilbake hvis en arbeider mottar gratis måltider eller tjenester. Du kan også definere kostgodtgjørelsessatser for å angi minimum og maksimum antall timer som kostgodtgjørelsessatsen kan brukes på en arbeiders reise. **Beslutninger:**

-   Standard kostgodtgjørelsesregler for de første og siste dagene:
    -   Hva er minste antall timer en ansatt kan kreve for en dag og fremdeles motta kostgodtgjørelse?
    -   Er det en reduksjon i beløpet som tilbys for måltider for første og siste dag? Hva er prosentandelen av reduksjonen i så fall?
    -   Er det en reduksjon i beløpet som tilbys for et hotell for første og siste dag? Hva er prosentandelen av reduksjonen i så fall?
    -   Er det en reduksjon i beløpet som tilbys for andre utgifter som inntreffer første og siste dag? Hva er prosentandelen av reduksjonen i så fall?
-   Standard kostgodtgjørelseregler:
    -   Finnes det en prosentvis reduksjon i kostgodtgjørelsen for hvert måltid hvis måltidet eksempelvis er gratis? Hva er reduksjonsprosenten for hvert måltid?
    -   Beregnes måltidsreduksjonen per dag, per tur eller etter antall måltider per dag?
    -   Skal kostgodtgjørelsesbeløpene avrundes vanlig eller oppover?
    -   Beregnes kostgodtgjørelse basert på en periode på 24 timer eller en kalenderdag?
-   Kostgodtgjørelsesregler basert på lokasjon:
    -   Kostgodtgjørelsessatser varierer i henhold til plassering og hvilke lokasjoner som er inkludert?
    -   Hvis kostgodtgjørelsessatsen varierer i henhold til plassering, for hver lokasjon, hvilken prosentandel gis for:
        -   måltider
        -   hotell
        -   andre utgifter

### <a name="expense-management-journals-and-accounts"></a>Journaler og kontoer for reiseregninger og utlegg

Administrasjon av reiseregninger og utlegg krever at du bruker flere journaler og kontoer. Du må angi for eksempel om den samme kontoen brukes for forskudd og kredittkorttvister. **Beslutninger:**

-   Hvilken finansjournal posteres godkjente reiseregninger til?
-   Hvilken konto brukes til forskudd?
-   Bør forskudd posteres umiddelbart?

### <a name="payment-methods"></a>Betalingsmåter

Når du lar ansatte pådra seg utgifter på vegne av firmaet, må du definere betalingsmåtene som ansatte kan bruke. Du kan for eksempel tillate at ansatte kan bruke kontanter eller et firmakredittkort. Du kan også tillate at ansatte skal bruke personlige kredittkort, og deretter tilbakebetale de ansatte. Du må ta følgende avgjørelser for hver enkelt betalingsmåte du godkjenner. **Beslutninger:**

-   Hvilke betalingsmåter er tillatt?
-   Hvem eier betalingsmåteutgiftene?
-   Finnes det en motkontotype? I så fall hvilken?
-   Hvis det finnes en motkonto, hva er kontoen?
-   Hvis betalingsmåten er et kredittkort, bør betalingsmåten bare brukes med importerte transaksjoner?

### <a name="expense-categories-and-shared-categories"></a>Utgiftskategorier og delte kategorier

Når ansatte oppretter en reiseregning, må hver utgift de registrerer, være tilknyttet en utgiftskategori. Utgiftskategorier er avledet fra Delte kategorier som kan deles på tvers av de juridiske enhetene i organisasjonen. Disse kategoriene kan også deles i Prosjektstyring og regnskap, avhengig av hvordan organisasjonen er definert. Basert på definisjonen av din organisasjon og veiledning fra implementeringsteamet må du avgjøre om kategoriene som brukes i reiseregninger og utlegg, bare skal brukes i utgifter, eller om de skal deles mellom prosjekt og utgifter. Legg merke til at disse kategoriene kan deles mellom prosjekt og utgifter eller prosjekt og produksjon, men ikke mellom utgifter og produksjon. Du må ta følgende avgjørelser for hver utgiftskategori. **Beslutninger:**

-   Hva er utgiftskategorien? For eksempel flybilletter, hotell eller kjørelengde.
-   Kan denne utgiftskategorien også brukes i Prosjektstyring og regnskap?
-   Hva er utgiftstypen?
-   Hva er standard betalingsmåte for utgiftskategorien?
-   Må utgifter i denne kategorien spesifiseres?
-   Hva er hovedstandardkontoen for utgiftskategorien?
-   Hva er standard mva-gruppe for vare for utgiftskategorien?
-   Er flere betalingsmåter tillatt for utgiftskategorien? I så fall hvilke?
-   Finnes det underkategorier i denne utgiftskategorien? Hvis dette er tilfelle:
    -   Er noen av underkategoriene utelatt fra skatterefusjon?
    -   Hva er mva-gruppe for vare for underkategoriene?

    Hvis denne utgiftskategorien også brukes i Prosjektstyring og regnskap, svarer du på de gjenværende spørsmålene. Hvis ikke, er du ferdig med denne delen.
-   Hvilke kostnadskontoer brukes til følgende?
    -   Kostnad
    -   Lønnsfordeling
    -   RIA - Kostverdi
    -   Kostnad - vare
    -   RIA - kostverdi - vare
    -   Påløpt tap
    -   RIA - påløpt tap
-   Hvilke inntektskontoer brukes til følgende?
    -   Fakturert omsetning
    -   Påløpte inntekter - salgsverdi
    -   RIA - Salgsverdi
    -   Påløpte inntekter - produksjon
    -   RIA - Produksjon
    -   Påløpte inntekter - fortjeneste
    -   RIA - Fortjeneste
    -   Påløpte inntekter - abonnement
    -   RIA - abonnement

 

### <a name="taxes"></a>Avgifter

For utgiftsrelaterte avgifter må du bestemme hva som inkluderes eller aktivert for reiseregninger. **Beslutninger:**

-   Er mva inkludert i utgiftsbeløp?
-   Skal skatterefusjon aktiveres for utgifter?

Legg merke til at hvis du, under planlegging av økonomimodulen, har besluttet å bruke amerikanske regler for merverdiavgift og use tax, som gjøres ved å velge Ja i feltet **Bruk avgiftsregler for merverdiavgift**, kan du ikke aktivere skatterefusjon på utgifter.

## <a name="policies"></a>Policyer
Du kan opprette utgiftsrapportpolicyer slik at organisasjonen kan spare tid og penger når ansatte pådrar seg utgifter på organisasjonens vegne. Policyer sikre at ansatte holder seg innenfor budsjettet, inneholder all nødvendig informasjon, og at penger bare brukes etter behov. Du må ta følgende avgjørelser for hver utgiftsrapportpolicy og hver utgiftsrapportgodkjenning du oppretter. **Beslutninger:**

-   Hva er navnet på policyen?
-   Hva er utgiftspolicyen for?
-   Hvis du tidligere har bestemt deg for å aktivere konserninterne utgifter, hvilke firmaer i organisasjonen skal denne policyen gjelde for?
-   Når trer policyen i kraft?
-   Når utløper policyen?
-   Hva er policyregelen?
-   Hva er resultatet av policyregelen?





