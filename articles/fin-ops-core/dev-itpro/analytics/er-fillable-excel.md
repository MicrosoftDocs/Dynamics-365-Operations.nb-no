---
title: Utforme en konfigurasjon til å generere dokumenter i Excel-format
description: Dette emnet beskriver hvordan du utformer et format for elektronisk rapportering (ER) for å fylle ut en Excel-mal, og deretter generere utgående dokumenter i Excel-format.
author: NickSelin
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd3171ad24f9c06f04372b30f2682b6da516bcb6
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488144"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Utforme en konfigurasjon til å generere dokumenter i Excel-format

[!include[banner](../includes/banner.md)]

Du kan utforme en konfigurasjon av format for [Elektronisk rapportering (ER)](general-electronic-reporting.md) som har en [formatkomponent](general-electronic-reporting.md#FormatComponentOutbound) for ER som du kan konfigurere til å generere et utgående dokument i et Microsoft Excel-arbeidsbokformat. Spesielle formatkomponenter for ER må brukes til dette formålet.

Hvis du vil ha mer informasjon om denne funksjonen, kan du følge fremgangsmåten i emnet [Utforme en konfigurasjon for generering av rapporter i OPENXML-format](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Legge til et nytt ER-format

Når du legger til en ny formatkonfigurasjon for ER for å generere et utgående dokument i et Excel-arbeidsbokformat, må du velge **Excel**-verdien for attributtet **Formattype** for formatet, eller la verdien for attributtet **Formattype** stå tom.

- Hvis du velger **Excel**, kan du konfigurere formatet til å generere et utgående dokument bare i Excel-format.
- Hvis du lar attributtet stå tomt, kan du konfigurere formatet til å generere et utgående dokument i et format som støttes av ER-rammeverket.

Hvis du vil konfigurere formatkomponenten for ER for konfigurasjonen, velger du **Utforming** i handlingsruten og åpner formatkomponenten for ER for redigering i ER-operasjonsutformingen.

![Siden Konfigurasjoner.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Komponent for Excel-fil

### <a name="manual-entry"></a>Manuell oppføring

Du må legge til en **Excel\\Fil**-komponent for det konfigurerte ER-formatet for å generere et utgående dokument i Excel-format.

![Excel\Fil-komponent.](./media/er-excel-format-add-file-component.png)

Hvis du vil angi oppsettet for det utgående dokumentet, knytter du en Excel-arbeidsbok som har filtypen XLSX, til **Excel-\\Fil**-komponenten som malen for utgående dokumenter.

> [!NOTE]
> Når du knytter en mal manuelt, må du bruke en [dokumenttype](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) som er konfigurert for dette formålet i [ER-parameterne](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Legge til et vedlegg i Excel\Fil-komponenten.](./media/er-excel-format-add-file-component2.png)

Hvis du vil angi hvordan den tilknyttede malen skal fylles ut når du kjører det konfigurerte ER-formatet, må du legge til nestede komponenter av typen **Ark**, **Område** og **Celle** i **Excel\\Fil**-komponenten. Hver nestede komponent må knyttes til et Excel-navngitt element.

### <a name="template-import"></a>Malimport

Du kan velge **Importer fra Excel** i fanen **Import** i handlingsruten for å importere en ny mal til et tomt ER-format. I dette eksemplet opprettes det en **Excel\\Fil**-komponent automatisk, og den importerte malen blir knyttet til den. Alle nødvendige ER-komponenter vil også bli opprettet automatisk, basert på listen over Excel-navngitte elementer som blir funnet.

![Velge Importer fra Excel.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Hvis du vil opprette det valgfrie elementet **Ark** i det redigerbare ER-formatet, setter du alternativet **Opprett Excel-ark-element** til **Ja**.

## <a name="sheet-component"></a>Komponenten Ark

Komponenten **Ark** viser et regneark i den vedlagte Excel-arbeidsboken som må fylles ut. Navnet på regnearket i en Excel-mal er definert i komponenten **Ark** for denne komponenten.

> [!NOTE]
> Denne komponenten er valgfri for Excel-arbeidsbøker som inneholder ett regneark.

I fanen **Tilordning** for ER-operasjonsutformingen kan du konfigurere egenskapen **Aktivert** for en **Ark**-komponent for å angi om komponenten må plasseres i et generert dokument:

- Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Sann** under kjøring, eller hvis ingen uttrykk er konfigurert i det hele tatt, vil det aktuelle regnearket plasseres i det genererte dokumentet.
- Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Usann** under kjøring, vil det genererte dokumentet ikke inneholde et regneark.

![Eksempel på en arkkomponent.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Områdekomponent

Komponenten **Område** angir et Excel-område som må kontrolleres av denne ER-komponenten. Navnet på området er definert i egenskapen **Excel-område** for denne komponenten.

Egenskapen **Replikeringsretning** angir om og hvordan området skal gjentas i et generert dokument:

- Hvis egenskapen **Replikeringsretning** er satt til **Ingen replikering**, blir ikke det riktige Microsoft Excel-området gjentatt i det genererte dokumentet.
- Hvis egenskapen **Replikeringsretning** er satt til **Vertikal**, blir ikke det riktige Microsoft Excel-området gjentatt i det genererte dokumentet. Hvert replikerte område er plassert under det opprinnelige området i en Excel-mal. Antall repetisjoner defineres av antall poster i en datakilde for typen **Postliste** som er bundet til denne ER-komponenten.
- Hvis egenskapen **Replikeringsretning** er satt til **Horisontal**, blir ikke det riktige Microsoft Excel-området gjentatt i det genererte dokumentet. Hvert replikerte område er plassert til høyre for det opprinnelige området i en Excel-mal. Antall repetisjoner defineres av antall poster i en datakilde for typen **Postliste** som er bundet til denne ER-komponenten.

Hvis du vil finne ut mer om horisontal replikering, kan du følge trinnene i [Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk](tasks/er-horizontal-1.md).

Komponenten **Område** kan ha andre nestede komponenter som brukes til å angi verdier i de riktige navngitte områdene i Excel.

- Hvis en av komponentene i gruppen **Tekst** brukes til å angi verdier, angis verdien i et Excel-område som en tekstverdi.

    > [!NOTE]
    > Bruk dette mønsteret til å formatere angitte verdier basert på den nasjonale innstillingen som er definert i appen.

- Hvis komponenten **Celle** i **Excel**-gruppen brukes til å angi verdier, angis verdien i et Excel-område som en verdi av datatypen som er definert av bindingen for den **Celle**-komponenten (for eksempel **Streng**, **Kommatall** eller **Heltall**).

    > [!NOTE]
    > Bruk dette mønsteret til å la Excel formatere angitte verdier basert på den nasjonale innstillingen til den lokale datamaskinen som åpner det utgående dokumentet.

I fanen **Tilordning** for ER-operasjonsutformingen kan du konfigurere egenskapen **Aktivert** for en **Område**-komponent for å angi om komponenten må plasseres i et generert dokument:

- Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Sann** under kjøring, eller hvis ingen uttrykk er konfigurert i det hele tatt, vil det aktuelle området bli fylt ut i det genererte dokumentet.
- Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Usann** under kjøring, og hvis området ikke representerer hele rader eller kolonner, vil ikke det aktuelle området fylles ut i det genererte dokumentet.
- Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Usann** under kjøring, og hvis området representerer hele rader eller kolonner, vil det genererte dokumentet inneholde de radene og kolonnene som skjulte rader og kolonner.

## <a name="cell-component"></a>Komponenten Celle

Komponenten **Celle** brukes til å fylle ut Excel-navngitte celler, figurer og bilder. Hvis du vil angi et Excel-navngitt objekt som må fylles ut av en ER-komponent ofr **Celle**, må du angi navnet på dette objektet i egenskapen **Excel-område** for komponenten **Celle**.

I fanen **Tilordning** for ER-operasjonsutformingen kan du konfigurere egenskapen **Aktivert** for en **Celle**-komponent for å angi om objektet må fylles ut i et generert dokument:

- Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Sann** under kjøring, eller hvis ingen uttrykk er konfigurert i det hele tatt, vil det aktuelle objektet bli fylt ut i det genererte dokumentet. Bindingen for denne **Celle**-komponenten angir en verdi som plasseres i det aktuelle objektet.
- Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Usann** under kjøring, vil det aktuelle objektet ikke bli fylt ut i det genererte dokumentet.

Når en **Celle**-komponent er konfigurert til å angi en verdi i en celle, kan den bindes til en datakilde som returnerer verdien av en primitiv datatype (for eksempel **Streng**, **Kommatall** eller **Heltall**). I dette tilfellet angis verdien i cellen som en verdi av den samme datatypen.

Når en **Celle**-komponent er konfigurert til å angi en verdi i en Excel-figur, kan den bindes til en datakilde som returnerer en verdi av en primitiv datatype (for eksempel **Streng**, **Kommatall** eller **Heltall**). I dette tilfellet angis verdien i Excel-figuren som teksten for den figuren. For verdier for datatyper som ikke er en **Streng**, utføres konverteringen til tekst automatisk.

> [!NOTE]
> Du kan konfigurere en **Celle**-komponent slik at den bare fyller ut en figur i tilfeller der en figurtekstegenskap støttes.

Når en **Celle**-komponent er konfigurert til å angi en verdi i et Excel-bilde, kan den bindes til en datakilde som returnerer en verdi for datatypen **Container** som representerer et bilde i binærformat. I dette tilfellet angis verdien i Excel-bildet som et bilde.

> [!NOTE]
> Alle Excel-bilder og -figurer anses å være forankret ved øverste venstre hjørne til en bestemt Excel-celle eller -område. Hvis du vil replikere et Excel-bilde eller -figur, må du konfigurere cellen eller området som den er forankret til, som en replikert celle eller et replikert område.

Hvis du vil finne ut mer om hvordan du bygger inn bilder og figurer, kan du se [Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Komponeten Sideskift

Komponenten **PageBreak** tvinger Excel til å starte en ny side. Denne komponenten er ikke nødvendig når du vil bruke standard sideveksling i Excel, men du bør bruke den når du vil at ER-formatet skal strukturere sideveksling for Excel.

## <a name="page-component"></a><a name="page-component"></a>Sidekomponent

### <a name="overview"></a>Oversikt

Du kan bruke **Side**-komponenten når du vil at Excel skal følge ER-formatet og strukturpagineringen i et generert utgående dokument. Når et ER-format kjører komponenter som er under **Side**-komponenten, legges de nødvendige sideskiftene til automatisk. I løpet av denne prosessen vurderes størrelsen på det genererte innholdet, sideoppsettet i Excel-malen og papirstørrelsen som er valgt i Excel-malen.

Hvis du må dele et generert dokument i forskjellige deler, der hver del har forskjellig sidepaginering, kan du konfigurere flere **Side**-komponenter i hver [Ark](er-fillable-excel.md#sheet-component)-komponent.

### <a name="structure"></a><a name="page-component-structure"></a>Struktur

Hvis den første komponenten under **Side**-komponenten er en [Område](er-fillable-excel.md#range-component)-komponent der egenskapen for **Replikeringsretning** er satt til **Ingen replikering**, regnes dette området som sidehodet for paginering som er basert på innstillingene til den gjeldende **Side**-komponenten. Excel-området som er knyttet til denne formatkomponenten, gjentas øverst på hver side som genereres ved hjelp av innstillingene for gjeldende **Side**-komponent.

> [!NOTE]
> For riktig paginering, hvis [Radene som skal gjentas øverst](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409) i området, er konfigurert i Excel-malen, må adressen for dette Excel-området tilsvare adressen til Excel-området som er tilknyttet den tidligere beskrevne **Område**-komponenten.

Hvis den siste komponenten under **Side**-komponenten er en **Område**-komponent der egenskapen for **Replikeringsretning** er satt til **Ingen replikering**, regnes dette området som sidebunntekst for paginering som er basert på innstillingene til den gjeldende **Side**-komponenten. Excel-området som er knyttet til denne formatkomponenten, gjentas nederst på hver side som genereres ved hjelp av innstillingene for gjeldende **Side**-komponent.

> [!NOTE]
> For riktig sideginering bør du ikke endre størrelsen på Excel-områdene som er knyttet til **Område**-komponentene ved kjøretid. Vi anbefaler ikke at du formaterer celler i dette området ved å bruke Excel-[alternativene](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84) **Bryt tekst i en celle** og **Beste tilpassing av radhøyde**.

Du kan legge til flere andre **Område**-komponenter mellom de valgfrie **Område**-komponentene for å angi hvordan et generert dokument fylles ut.

Hvis settet med nestede **Område**-komponenter i **Side**-komponenten ikke samsvarer med strukturen som beskrives tidligere, oppstår det en validerings[feil](er-components-inspections.md#i17) ved utformingen i ER-formatutformingen. Feilmeldingen informerer deg om at problemet kan forårsake problemer ved kjøretid.

> [!NOTE]
> Hvis du vil generere riktig utdata, angir du ikke en binding for **Område**-komponenter under **Side**-komponenten hvis egenskapen for **Replikeringsretning** for **Område**-komponenten er satt til **Ingen replikering**, og området er konfigurert til å generere sidetopptekster- eller bunntekster.

Hvis du vil ha pagineringsrelatert summering og opptelling for å beregne kjørende totaler og totaler per side, anbefaler vi at du konfigurerer de nødvendige [Datainnsamling](er-data-collection-data-sources.md)-datakildene. Hvis du vil lære hvordan du bruker **Side**-komponenten for å paginere et generert Excel-dokument, kan du fullføre fremgangsmåtene i [Utforme et ER-format for å paginere genererte dokumenter i Excel](er-paginate-excel-reports.md).

### <a name="limitations"></a><a name="page-component-limitations"></a>Begrensninger

Når du bruker **Side**-komponenten for Excel-sidenummerering, vet du ikke det endelige antallet sider i et generert dokument før sidenummereringen er fullført. Derfor kan du ikke beregne det totale antall sider ved å bruke ER-formler, og skrive ut det riktige antallet sider for et generert dokument på en hvilken som helst side før den siste siden.

> [!TIP]
> Hvis du vil oppnå dette resultatet i en Excel-topptekst eller -bunntekst ved hjelp av spesiell [Excel](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers)-formatering for topptekst og bunntekst.

Konfigurerte **Side**-komponenter vurderes ikke når du oppdaterer en Excel-mal i det redigerbare formatet i Dynamics 365 Finance versjon 10.0.22. Denne funksjonaliteten vurderes for ytterligere versjoner av Finance.

Hvis du konfigurerer Excel-malen til å bruke [betinget formatering](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting), vil den kanskje ikke fungere som forventet i noen tilfeller.

### <a name="applicability"></a>Relevans

**Side**-komponenten fungerer bare for [Excel-fil](er-fillable-excel.md#excel-file-component)-formatkomponenten når denne komponenten er konfigurert til å bruke en mal i Excel. Hvis du [erstatter](tasks/er-design-configuration-word-2016-11.md) Excel-malen med en Word-mal og deretter kjører det redigerbare ER-formatet, blir **Side**-komponenten ignorert.

**Side**-komponenten fungerer bare når funksjonen **Aktivere bruken av EPPlus-bibliotek i Rammeverk for elektronisk rapportering** er aktivert. Et unntak skjer ved kjøretid hvis ER prøver å behandle **Side**-komponenten mens denne funksjonen er deaktivert.

> [!NOTE]
> Et unntak skjer ved kjøretid hvis et ER-format behandler **Side**-komponenten for en Excel-mal som inneholder minst én formel som refererer til en celle som ikke er gyldig. For å forhindre kjøretidsfeil kan du korrigere Excel-malen slik det beskrives under [Hvordan du retter en #REF!-feil](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

## <a name="footer-component"></a>Bunntekstkomponent

Komponenten **Bunntekst** brukes til å fylle ut bunntekster nederst i et generert regneark i en Excel-arbeidsbok.

> [!NOTE]
> Du kan legge til denne komponenten for hver komponent av typen **Ark** for å angi ulike bunntekster for forskjellige regneark i en generert Excel-arbeidsbok.

Når du konfigurerer en komponent av typen **Bunntekst**, kan du bruke egenskapen **Utseende for topptekst/bunntekst** til å angi sidene som komponenten skal brukes til. Følgende verdier er tilgjengelige:

- **Alle** – Kjør den konfigurerte komponenten av typen **Bunntekst** for en side i det overordnede Excel-regnearket.
- **Første** – Kjør den konfigurerte komponenten av typen **Bunntekst** for bare den første siden i det overordnede Excel-regnearket.
- **Partall** – Kjør den konfigurerte komponenten av typen **Bunntekst** for bare partallssidene i det overordnede Excel-regnearket.
- **Oddetall** – Kjør den konfigurerte komponenten av typen **Bunntekst** for bare oddetallssidene i det overordnede Excel-regnearket.

For en komponent av typen **Ark** kan du legge til flere komponenter av typen **Bunntekst**, der hver har forskjellig verdi for egenskapen **Utseende for topptekst/bunntekst**. På denne måten kan du generere forskjellige bunntekster for ulike typer sider i et Excel-regneark.

> [!NOTE]
> Sørg for at hver komponent av typen **Bunntekst** du legger til i en komponent av typen **Ark**, har en annen verdi for egenskapen **Utseende for topptekst/bunntekst**. Ellers oppstår det en [valideringsfeil](er-components-inspections.md#i16). Feilmeldingen du mottar, varsler deg om inkonsekvensen.

Under den tillagte komponenten av typen **Bunntekst** legger du til de obligatoriske, nestede komponentene av typen **Tekst\\Streng**, **Tekst\\Dato og klokkeslett** eller en annen type. Konfigurer bindingene for disse komponentene til å angi hvordan bunnteksten på siden fylles ut.

Du kan også bruke spesielle [formateringskoder](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) til å formatere innholdet i en generert bunntekst på riktig måte. Hvis du vil lære hvordan du bruker denne fremgangsmåten, følger du trinnene i [Eksempel 1](#example-1) senere i dette emnet.

> [!NOTE]
> Når du konfigurerer ER-formater, må du huske å vurdere Excel-[grensen](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) og det maksimale antallet tegn for én topptekst eller bunntekst.

## <a name="header-component"></a>Topptekstkomponent

Komponenten **Topptekst** brukes til å fylle ut topptekster øverst i et generert regneark i en Excel-arbeidsbok. Den brukes på samme måte som komponenten **Bunntekst**.

## <a name="edit-an-added-er-format"></a>Redigere et tillagt ER-format

### <a name="update-a-template"></a>Oppdatere en mal

Du kan velge **Oppdater fra Excel** i fanen **Import** i handlingsruten for å importere en oppdatert mal til et redigerbart ER-format. I løpet av denne prosessen vil en mal for den valgte **Excel\\Fil**-komponenten bli erstattet med en ny mal. Innholdet i det redigerbare ER-formatet vil bli synkronisert med innholdet i den oppdaterte ER-malen.

- En ny komponent for ER-format vil automatisk opprettes for hvert Excel-navn hvis komponenten for ER format ikke finnes i det redigerbare formatet.
- Alle komponenter for ER-format vil bli slettet fra det redigerbare ER-formatet hvis det riktige Excel-navnet ikke blir funnet for det.

> [!NOTE]
> Sett alternativet **Opprett element for Excel-arkformat** til **Ja** hvis du vil opprette det valgfrie **Ark**-elementet i det redigerbare ER-formatet.
>
> Hvis det redigerbare ER-formatet opprinnelig inneholdt **Ark**-elementer, anbefales det at du setter akternativet **Opprett element for Excel-arkformat** til **Ja** når du importerer en oppdatert mal. Hvis ikke, vil alle nestede elementer i det opprinnelige **Ark**-elementet bli opprettet fra grunnen av. Alle bindinger av elementene for nyopprettet format vil derfor gå tapt i det oppdaterte ER-formatet.

![Alternativet Opprett element for Excel-arkformat i dialogboksen Oppdater fra Excel.](./media/er-excel-format-update-template.png)

Hvis du vil finne ut mer om denne funksjonen, kan du følge fremgangsmåten i [Endre formater for elektronisk rapportering ved å bruke Excel-maler på nytt](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Validere et ER-format

Når du validerer et ER-format som kan redigeres, utføres det en konsekvenskontroll for å sikre at Excel-navnet finnes i Excel-malen som brukes for øyeblikket. Du vil bli varslet om eventuelle inkonsekvenser. For noen inkonsekvenser vil alternativet for automatisk korrigering av problemer bli tilbudt.

![Valideringsfeilmelding.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Kontrollere beregningen av Excel-formler

Når et utgående dokument i et Microsoft Excel-arbeidsbokformat genereres, kan noen celler i dokumentet inneholde Excel-formler. Når funksjonen for **Aktivere bruken av EPPlus-bibliotek i Rammeverk for elektronisk rapportering** er aktivert, kan du styre når formlene skal beregnes, ved å endre verdien for **Beregningsalternativer**-[parameteren](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) i Excel-malen som brukes:

- Velg **Automatisk** for å omberegne alle avhengige formler hver gang et generert dokument føyes til av nye områder, celler osv.

    >[!NOTE]
    > Dette kan føre til ytelsesproblemer for Excel-maler som inneholder flere relaterte formler.

- Velg **Manuell** for å unngå omberegning av formler når et dokument genereres.

    >[!NOTE]
    > Omberegning av formler tvinges manuelt når et generert dokument åpnes for forhåndsvisning ved hjelp av Excel.
    > Ikke bruk dette alternativet hvis du konfigurerer et ER-mål som forutsetter bruken av et generert dokument uten forhåndsvisningen i Excel (PDF-konvertering, e-post og så videre), fordi det genererte dokumentet kanskje ikke inneholder verdier i celler som inneholder formler.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Eksempel 1: Format for bunntekstinnhold

1. Bruk ER-konfigurasjonene som følger med, til å [generere](er-generate-printable-fti-forms.md) et FTI-dokument (free text invoice).
2. Gå gjennom bunnteksten til det genererte dokumentet. Legg merke til at det inneholder informasjon om det gjeldende sidetallet og totalt antall sider i dokumentet.

    ![Gå gjennom bunnteksten til et generert dokument i Excel-format.](./media/er-fillable-excel-footer-1.gif)

3. I ER-formatutformingen [åpner](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) du eksempel-ER-formatet for gjennomgang.

    Bunnteksten i regnearket **Faktura** genereres basert på innstillingene til to komponenter av typen **Streng** som ligger under komponenten **Bunntekst**:

    - Den første komponenten av typen **Streng** fyller ut følgende spesielle formateringskoder for å tvinge Excel til å bruke bestemt formatering:

        - **&C** – Juster bunnteksten i midten.
        - **&"Segoe UI,Regular"&8** – Viser bunnteksten i skriften "Segoe UI Regular" med en størrelse på 8 punkt.

    - Den andre komponenten av typen **Streng** fyller ut teksten som inneholder det gjeldende sidenummeret og totalt antall sider i det gjeldende dokumentet.

    ![Gå gjennom komponenten for bunntekst-ER-formatet på siden Formatutforming.](./media/er-fillable-excel-footer-2.png)

4. Tilpass ER-eksemplets format for å endre den gjeldende bunnteksten på siden:

    1. [Opprett](er-quick-start2-customize-report.md#DeriveProvidedFormat) et avledet ER-format for **Tilpasset fritekstfaktura (Excel)** som er basert på eksempel-ER-formatet.
    2. Legg til det første nye paret med komponenter av typen **Streng** for komponenten **Bunntekst** i regnearket **Faktura**:

        1. Legg til en komponent av typen **Streng** som justerer firmanavnet til venstre, og presenterer det i 8-punkters "Segoe UI Regular"-skrifttype (**"&L&"Segoe UI,Regular"&8"**).
        2. Legg til en komponent av typen **Streng** som fyller ut firmanavnet (**model.InvoiceBase.CompanyInfo.Name**).

    3. Legg til det andre nye paret med komponenter av typen **Streng** for komponenten **Bunntekst** i regnearket **Faktura**:

        1. Legg til en komponent av typen **Streng** som justerer behandlingsdatoen til høyre, og presenterer det i 8-punkters "Segoe UI Regular"-skrifttype (**"&R&"Segoe UI,Regular"&8"**).
        2. Legg til en komponent av typen **Streng** som fyller ut behandlingsdatoen i et egendefinert format (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).

        ![Gjennomgang av komponenten for bunntekst-ER-formatet på siden Formatutforming.](./media/er-fillable-excel-footer-3.png)

    4. [Fullfør](er-quick-start2-customize-report.md#CompleteDerivedFormat) utkastversjonen for det avledede ER-format et for **Tilpasset fritekstfaktura (Excel)**.

5. [Konfigurer](er-generate-printable-fti-forms.md#configure-print-management) Utskriftsbehandling for å bruke det avledede ER-formatet for **Tilpasset fritekstfaktura (Excel)** i stedet for eksempel-ER-formatet.
6. Generer et utskrivbart FTI-dokument, og gå gjennom bunnteksten til det genererte dokumentet.

    ![Gjennomgang av bunnteksten til et generert dokument i Excel-format.](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Utform en konfigurasjon for generering av rapporter i OPENXML-format](tasks\er-design-reports-openxml-2016-11.md)

[Endre formater for elektronisk rapportering ved å bruke Excel-maler på nytt](modify-electronic-reporting-format-reapply-excel-template.md)

[Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk](tasks/er-horizontal-1.md)

[Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md)

[Konfigurere elektronisk rapportering (ER) for å hente data til Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
