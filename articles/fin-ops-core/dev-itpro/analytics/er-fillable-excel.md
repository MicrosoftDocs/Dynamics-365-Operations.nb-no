---
title: Utforme en konfigurasjon til å generere dokumenter i Excel-format
description: Dette emnet beskriver hvordan du utformer et format for elektronisk rapportering (ER) for å fylle ut en Excel-mal, og deretter generere utgående dokumenter i Excel-format.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c8d6a18741d57829d1929fb8362dc4ba8e03a1bd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094035"
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

![Siden Konfigurasjoner](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Komponent for Excel-fil

### <a name="manual-entry"></a>Manuell oppføring

Du må legge til en **Excel\\Fil**-komponent for det konfigurerte ER-formatet for å generere et utgående dokument i Excel-format.

![Excel\Fil-komponent](./media/er-excel-format-add-file-component.png)

Hvis du vil angi oppsettet for det utgående dokumentet, knytter du en Excel-arbeidsbok som har filtypen XLSX, til **Excel-\\Fil**-komponenten som malen for utgående dokumenter.

> [!NOTE]
> Når du knytter en mal manuelt, må du bruke en [dokumenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) som er konfigurert for dette formålet i [ER-parameterne](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Legge til et vedlegg i Excel\Fil-komponenten](./media/er-excel-format-add-file-component2.png)

Hvis du vil angi hvordan den tilknyttede malen skal fylles ut når du kjører det konfigurerte ER-formatet, må du legge til nestede komponenter av typen **Ark**, **Område** og **Celle** i **Excel\\Fil**-komponenten. Hver nestede komponent må knyttes til et Excel-navngitt element.

### <a name="template-import"></a>Malimport

Du kan velge **Importer fra Excel** i fanen **Import** i handlingsruten for å importere en ny mal til et tomt ER-format. I dette eksemplet opprettes det en **Excel\\Fil**-komponent automatisk, og den importerte malen blir knyttet til den. Alle nødvendige ER-komponenter vil også bli opprettet automatisk, basert på listen over Excel-navngitte elementer som blir funnet.

![Velge Importer fra Excel](./media/er-excel-format-import-template.png)

> [!NOTE]
> Hvis du vil opprette det valgfrie elementet **Ark** i det redigerbare ER-formatet, setter du alternativet **Opprett Excel-ark-element** til **Ja**.

## <a name="sheet-component"></a>Komponenten Ark

Komponenten **Ark** viser et regneark i den vedlagte Excel-arbeidsboken som må fylles ut. Navnet på regnearket i en Excel-mal er definert i komponenten **Ark** for denne komponenten.

> [!NOTE]
> Denne komponenten er valgfri for Excel-arbeidsbøker som inneholder ett regneark.

I fanen **Tilordning** for ER-operasjonsutformingen kan du konfigurere egenskapen **Aktivert** for en **Ark**-komponent for å angi om komponenten må plasseres i et generert dokument:

- Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Sann** under kjøring, eller hvis ingen uttrykk er konfigurert i det hele tatt, vil det aktuelle regnearket plasseres i det genererte dokumentet.
- Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Usann** under kjøring, vil det genererte dokumentet ikke inneholde et regneark.

![Eksempel på en arkkomponent](./media/er-excel-format-sheet-component.png)

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

## <a name="edit-an-added-er-format"></a>Redigere et tillagt ER-format

### <a name="update-a-template"></a>Oppdatere en mal

Du kan velge **Oppdater fra Excel** i fanen **Import** i handlingsruten for å importere en oppdatert mal til et redigerbart ER-format. I løpet av denne prosessen vil en mal for den valgte **Excel\\Fil**-komponenten bli erstattet med en ny mal. Innholdet i det redigerbare ER-formatet vil bli synkronisert med innholdet i den oppdaterte ER-malen.

- En ny komponent for ER-format vil automatisk opprettes for hvert Excel-navn hvis komponenten for ER format ikke finnes i det redigerbare formatet.
- Alle komponenter for ER-format vil bli slettet fra det redigerbare ER-formatet hvis det riktige Excel-navnet ikke blir funnet for det.

> [!NOTE]
> Sett alternativet **Opprett element for Excel-arkformat** til **Ja** hvis du vil opprette det valgfrie **Ark**-elementet i det redigerbare ER-formatet.
>
> Hvis det redigerbare ER-formatet opprinnelig inneholdt **Ark**-elementer, anbefales det at du setter akternativet **Opprett element for Excel-arkformat** til **Ja** når du importerer en oppdatert mal. Hvis ikke, vil alle nestede elementer i det opprinnelige **Ark**-elementet bli opprettet fra grunnen av. Alle bindinger av elementene for nyopprettet format vil derfor gå tapt i det oppdaterte ER-formatet.

![Alternativet Opprett element for Excel-arkformat i dialogboksen Oppdater fra Excel](./media/er-excel-format-update-template.png)

Hvis du vil finne ut mer om denne funksjonen, kan du følge fremgangsmåten i [Endre formater for elektronisk rapportering ved å bruke Excel-maler på nytt](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Validere et ER-format

Når du validerer et ER-format som kan redigeres, utføres det en konsekvenskontroll for å sikre at Excel-navnet finnes i Excel-malen som brukes for øyeblikket. Du vil bli varslet om eventuelle inkonsekvenser. For noen inkonsekvenser vil alternativet for automatisk korrigering av problemer bli tilbudt.

![Valideringsfeilmelding](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Kontrollere beregningen av Excel-formler

Når et utgående dokument i et Microsoft Excel-arbeidsbokformat genereres, kan noen celler i dokumentet inneholde Excel-formler. Når funksjonen for **Aktivere bruken av EPPlus-bibliotek i Rammeverk for elektronisk rapportering** er aktivert, kan du styre når formlene skal beregnes, ved å endre verdien for **Beregningsalternativer**-[parameteren](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) i Excel-malen som brukes:

- Velg **Automatisk** for å omberegne alle avhengige formler hver gang et generert dokument føyes til av nye områder, celler osv.
    >[!NOTE]
    > Dette kan føre til ytelsesproblemer for Excel-maler som inneholder flere relaterte formler.
- Velg **Manuell** for å unngå omberegning av formler når et dokument genereres.
    >[!NOTE]
    > Omberegning av formler tvinges manuelt når et generert dokument åpnes for forhåndsvisning ved hjelp av Excel.
    > Ikke bruk dette alternativet hvis du konfigurerer et ER-mål som forutsetter bruken av et generert dokument uten forhåndsvisningen i Excel (PDF-konvertering, e-post og så videre), fordi det genererte dokumentet kanskje ikke inneholder verdier i celler som inneholder formler.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Utforme en konfigurasjon for generering av rapporter i OPENXML-format](tasks\er-design-reports-openxml-2016-11.md)

[Endre formater for elektronisk rapportering ved å bruke Excel-maler på nytt](modify-electronic-reporting-format-reapply-excel-template.md)

[Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk](tasks/er-horizontal-1.md)

[Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md)

[Konfigurere elektronisk rapportering (ER) for å hente data til Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)
