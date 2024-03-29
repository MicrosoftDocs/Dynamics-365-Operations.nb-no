---
title: Utforme flerspråklige rapporter i elektronisk rapportering
description: Denne artikkelen beskriver hvordan du kan bruke etiketter for elektronisk rapportering (ER) til å utforme og generere flerspråklige rapporter.
author: kfend
ms.date: 05/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 5575ba3154521e3855ce6b97c5b37d3c4868e3e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285493"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Utforme flerspråklige rapporter i elektronisk rapportering

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Oversikt

Som forretningsbruker kan du bruke rammeverket for [elektronisk rapportering (ER)](general-electronic-reporting.md) til å konfigurere formater for utgående dokumenter som må genereres i overensstemmelse med de juridiske kravene i ulike land eller regioner. Når disse kravene krever at utgående dokumenter genereres på forskjellige språk for forskjellige land eller regioner, kan du konfigurere ett enkelt ER-format som inneholder språkavhengige ressurser. På denne måten kan du bruke formatet til å generere utgående dokumenter for ulike land eller regioner på nytt. Du vil kanskje også bruke ett enkelt ER-format til å generere et utgående dokument på ulike språk for tilsvarende kunder, leverandører, datterselskaper eller andre parter.

Du kan konfigurere ER-datamodeller og modelltilordninger som datakilder for konfigurerte ER-formater for å definere dataflyten som angir hvilke programdata som skal plasseres i genererte dokumenter. Som [leverandør](general-electronic-reporting.md#Provider) av ER-konfigurasjon kan du [publisere](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) konfigurerte datamodeller, modelltilordninger og formater som komponenter av en ER-løsning for å generere bestemte utgående dokumenter. Du kan også tillate at kunder [laster opp](general-electronic-reporting-manage-configuration-lifecycle.md) den publiserte ER-løsningen, slik at den kan brukes og tilpasses. Hvis du forventer at kunder snakker andre språk, kan du konfigurere ER-komponentene, slik at de inneholder språkavhengige ressurser. På den måten kan innholdet i en redigerbar ER-komponent presenteres på kundens brukerforetrukne språk under utformingen.

Du kan konfigurere språkavhengige ressurser som ER-etiketter. Du kan deretter bruke disse etikettene til å konfigurere ER-komponenter for følgende formål:

- Under utformingen:

    - Presenter innholdet for konfigurerte ER-komponenter på det brukerspesifikke språket.

- Under kjøring:

    - Generer språkavhengig innhold for utgående dokumenter.
    - Angi advarsler og feilmeldinger på det brukerspesifikke språket.
    - Be om nødvendige felt på språket som er valgt av brukeren.

ER-etiketter kan konfigureres i alle ER-[konfigurasjoner](general-electronic-reporting.md#Configuration) som inneholder ulike komponenter. Etikettene kan vedlikeholdes uavhengig av de konfigurerte logikkene for ER-datamodeller, ER-modelltilordninger og ER-formatkomponenter.

Hver ER-etikett identifiseres av en ID som er unik i henhold til ER-konfigurasjonen som innehar denne etiketten. Hver etikett kan inneholde etiketteksten for hvert språk som støttes i den gjeldende forekomsten av Microsoft Dynamics 365 Finance. Disse støttede språkene inkluderer språkene for distribuerte tilpasninger.

## <a name="entry"></a>Oppføring

Når du utformer en ER-datamodell, en ER-modelltilordning eller et ER-format, vises **Oversett**-alternativet når du velger et felt som kan inneholde den oversettbare konteksten. Når du velger dette alternativet, kan du koble det valgte feltet til en ER-etikett i **Tekstoversettelse**-<a name="TextTranslationPane">ruten</a>. Du kan velge en eksisterende ER-etikett, eller du kan legge til en ny ER-etikett hvis den ikke er tilgjengelig ennå. Når du velger eller legger til en ER-etikett, kan du legge til relatert tekst for alle språk som støttes i gjeldende Finance-forekomst.

Illustrasjonen nedenfor viser hvordan denne oversettelsen gjøres i en redigerbar ER-datamodell. I dette eksemplet er **Beskrivelse**-attributtet for feltet **PurchaseOrder** for den redigerbare **Fakturamodell** oversatt til østerriksk tysk (DE-AT) og japansk (JA).

![Oversette en ER-etikett i ER-datamodellutforming.](./media/er-multilingual-labels-refer.png)

Det er bare etiketttekst for etiketter som befinner seg i en redigerbar ER-komponent som kan oversettes. Hvis du for eksempel velger **Oversett** for etikettattributtet for en datakilde for ER-modelltilordning og du deretter velger en ER-etikett som ligger i den overordnede ER-datamodellen, vil du se innholdet i etiketten, men du kan ikke endre den. I disse tilfellene er feltet **Oversatt tekst** utilgjengelig, som vist i følgende illustrasjon.

![Se gjennom en oversettelse for en ER-etikett i ER-modelltilordningsutforming.](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Du kan ikke bruke utformere til å slette en etikett som er angitt i en redigerbar ER-komponent.

## <a name="scope"></a>Område

ER-etiketter kan refereres til i flere oversettbare attributter for ER-komponenter.

### <a name="data-model-component"></a>Datamodellkomponent

Når du konfigurerer en ER-datamodell, kan du legge til ER-etiketter for den. Attributtene **Etikett** og **Beskrivelse** for modellelementet, hvert modells felt og hver <a id="LinkModelEnum"></a>-modellopplistingsverdi kan knyttes til en ER-etikett som legges til i ER-datamodellen.

![Angi oversettelse for Beskrivelse-attributtet i ER-datamodellutforming.](./media/er-multilingual-labels-refer.png)

Når en ER-datamodell er konfigurert på denne måten, vil innholdet bli presentert for brukere av ER-datamodellutforming på hver brukers foretrukne språk. Derfor er modellvedlikehold forenklet. Illustrasjonene nedenfor viser hvordan denne funksjonaliteten fungerer for brukere som har DE-AT og JA angitt som foretrukket språk.

![Oppsett for ER-datamodellutformingen for en bruker som har DE-AT angitt som foretrukket språk.](./media/er-multilingual-labels-refer-de.png)

![Oppsett for ER-datamodellutformingen for en bruker som har JA angitt som foretrukket språk.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Modelltilordningskomponent

Fordi ER-modelltilordning er basert på en ER-datamodell, vises etikettene for datamodellelementene som det refereres til, på brukerens foretrukne språk i modelltilordningsdesigneren. Illustrasjonen nedenfor viser hvordan betydningen av feltet **PurchaseOrder** er forklart i den redigerbare modelltilordningen ved å bruke etiketten til attributtet **Beskrivelse** som er lagt til i den konfigurerte datamodellen. Legg merke til at denne etiketten presenteres på brukerens foretrukne språk (DE-AT i dette eksemplet).

![Oppsett for ER-modelltilordningsutforming for en bruker som har DE-AT angitt som foretrukket språk.](./media/er-multilingual-labels-show-mapping.png)

Når **Etikett**-attributtet for datakilden **Inndataparameter** er konfigurert som koblet til en ER-etikett, blir parameterfeltet som tilsvarer denne datakilden, presentert i brukerdialogboksen ved kjøretid til brukere på det foretrukne språket.

### <a name="format-component"></a>Formatkomponent

Når du konfigurerer et ER-format, kan du legge til ER-etiketter for den. Attributtene **Etikett** og **Hjelpetekst** for hver konfigurerte datakilde kan knyttes til en ER-etikett som legges til i ER-formatet. Attributtene **Etikett** og **Beskrivelse** for hver <a id="LinkFormatEnum"></a>formatopplistingsverdi kan også kobles til en ER-etikett som er tilgjengelig fra det redigerbare ER-formatet.

> [!NOTE]
> Du kan også koble disse attributtene til en ER-etikett i den overordnede ER-datamodellen som bruker modellens etiketter på nytt i alle ER-format som er konfigurert for denne datamodellen.

Når et ER-format er konfigurert på denne måten, vil innholdet i formatet bli presentert for brukere av ER-operasjonsutforming på hver brukers foretrukne språk. Derfor er formatvedlikehold og -analyse av den konfigurerte logikken forenklet.

Fordi et ER-format er basert på en ER-datamodell, vises etikettene som det refereres til i datamodellelementene, i ER-formatutforming på brukerens foretrukne språk.

Når **Etikett**-attributtet for datakilden **Inndataparameter** er konfigurert til en ER-etikett, blir feltet som tilsvarer parameteren i brukerdialogboksen ved kjøretid, presentert for brukeren som en ledetekst. Illustrasjonene nedenfor viser hvordan du kan koble **Etikett**-attributtet for datakilden **Inndataparametre for brukere** under utforming til en ER-etikett, slik at brukere blir bedt om å angi parameteren på forskjellige brukerspesifikke språk (vist for språkene engelsk USA (EN-US) og DE-AT) under kjøring.

![Oversette attributter for en brukerinndataparameter for brukere i ER-operasjonsutforming.](./media/er-multilingual-labels-refer-format.png)

![ER-behandling av leverandørbetaling ved kjøring for det brukerspesifikke språket EN-US.](./media/er-multilingual-labels-show-runtime-en.png)

![ER-behandling av leverandørbetaling ved kjøring for det brukerspesifikke språket DE-AT.](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Uttrykk

Hvis du vil bruke en etikett i et ER-[uttrykk](er-formula-language.md), må du bruke syntaksen **@"GER\_LABEL:X"**, der prefikset **@** indikerer at operanden refererer til en etikett, **GER\_LABEL**, som angir at en ER-etikett er involvert, og **X** er ER-etikett-IDen.

![Konfigurere et ER-uttrykk som inneholder en referanse til en ER-etikett i ER-formeldesigneren.](./media/er-multilingual-labels-expression1.png)

Hvis du vil referere til en systemetikett (program), bruker du syntaksen **@"X"**, der prefikset **@** viser at operanden refererer til en etikett, og **X** er systemetikett-IDen.

![Konfigurere et ER-uttrykk som inneholder en referanse til en programetikett i ER-formeldesigneren.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Modelltilordning

Et uttrykk av en ER-modelltilordning kan konfigureres ved å bruke en etikett. Når denne tilordningen kalles av et ER-format som kjøres for å generere et utgående dokument, inkluderer konteksten for utførelsen en språkkode. En konfigurert uttrykksetikett vil bli fylt ut med etiketteksten som er konfigurert for språket for denne konteksten.

Hvis en referanseetikett ikke har noen oversettelse for språket i formatkjøringskonteksten som kaller modelltilordningen, brukes etiketteksten på EN-US-språket i stedet.

#### <a name="format"></a>Formater

Et ER-uttrykk for et ER-format kan konfigureres ved å bruke etiketter. Når dette formatet kjøres for å generere et utgående dokument, inkluderer konteksten for utførelsen en språkkode. En konfigurert uttrykksetikett vil bli fylt ut med etiketteksten som er konfigurert for språket for denne konteksten.

![Oversettelse av en ER-etikett for det redigerbare ER-uttrykket i ER-formeldesigneren.](./media/er-multilingual-labels-refer-in-expression.png)

![Eksempel på databinding som refererer til en ER-etikett i ER-operasjonsutforming.](./media/er-multilingual-labels-refer-in-binding.png)

Du kan konfigurere **FIL**-komponenten for et ET-format til å generere rapporten på brukerens foretrukne språk.

![Definer FIL- komponenten i ER-operasjonsutforming for å generere rapporten på brukerens foretrukne språk.](./media/er-multilingual-labels-language-context-user.png)

Hvis du konfigurerer et ER-format på denne måten, genereres rapporten ved hjelp av den tilhørende teksten til ER-etikettene. Illustrasjonene nedenfor viser eksempler på rapporter for brukerspråkene EN-US og DE-AT.

![Forhåndsvisning av rapporten er generert på EN-US-brukerens foretrukne språk.](./media/er-multilingual-labels-report-preview-en.png)

![Forhåndsvisning av rapporten er generert på DE-AT-brukerens foretrukne språk.](./media/er-multilingual-labels-report-preview-de.png)

Hvis en referanseetikett ikke har noen oversettelse for språket i formatkjøringskonteksten, brukes etiketteksten på EN-US-språket i stedet.

> [!TIP]
> Du kan bruke **MAPPE** og atskilte typer **FIL**-komponenter i det redigerbare ER-formatet for å angi hvordan en utgående fil skal genereres. Hvis du vil gi en generert fil navn, konfigurerer du ER-[uttrykket](er-formula-language.md) for **Filnavn**-parameteren for komponenten. Du kan bruke etiketter i det konfigurerte uttrykket. Fordi parameteren **Filnavn** er språkagnostist som standard, vises teksten i alle etikettene du refererer til i dette uttrykket, i standard EN-US-språk ved kjøretid. I versjon 10.0.28 og senere kan du imidlertid aktivere parameteren **Bruk parameteren Språkinnstillinger for uttrykket Filnavn**. Uttrykket **Filnavn** tar deretter parameteren for **Språkinnstillinger** med i betraktning når det beregnes.

## <a name="language"></a>Språk

ER støtter ulike måter å angi et språk på for en generert rapport. I **Språkinnstillinger**-feltet i kategorien **Format** kan du velge følgende verdier:

- **Firmainnstilling** – Generer en rapport på et firmaspesifikt språk.

    ![Angi et firmaforetrukket språk som språket for en generert rapport i ER-operasjonsutforming.](./media/er-multilingual-labels-language-context-company.png)

- **Brukerinnstilling** – Generer en rapport på brukerens foretrukne språk.
- **Uttrykkelig definert** – Generer en rapport på et språk som er angitt under utformingen.

    ![Angi et språk som er definert under utformingen, som språk for en generert rapport i ER-operasjonsutforming.](./media/er-multilingual-labels-language-context-fixed.png)

- **Definert under kjøring** – Generer en rapport på et språk som er angitt under kjøring. Hvis du velger denne verdien, konfigurerer du et ER-uttrykk i **Språk**-feltet som returnerer språkkoden for språket, for eksempel språket til den tilsvarende kunden.

    ![Angi et språk som er definert under kjøring, som språk for en generert rapport i ER-operasjonsutforming.](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>Kulturspesifikk formatering

ER støtter ulike måter å angi kulturen for en generert rapport. Derfor kan den riktig kulturspesifikke formateringen brukes for dato-, klokkeslett- og numeriske verdier. Når du utformer et ER-format, går du til kategorien **Format** i feltet **Kulturinnstillinger** og velger én av følgende verdier for formatkomponent i **Felles\\Fil**, **Excel\\Fil**, **PDF\\Fil** eller **PDF\\Sammenslåing**-typen:

- **Brukerinnstilling** – Formater verdiene i henhold til brukerens foretrukne kultur. Denne kulturen er definert i feltet **Dato, klokkeslett og nummerformat** i kategorien **Innstillinger** på siden **Brukeralternativer**.

    ![Definere brukerens foretrukne kultur som kultur for en generert rapport i ER-operasjonsutforming.](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **Uttrykkelig definert** – Formater verdiene i henhold til kulturen som er angitt i utformingen.

    ![Definere kulturen som er angitt ved utforming som kultur for en generert rapport i ER-operasjonsutforming.](./media/er-multilingual-labels-culture-context-fixed.png)

- **Definert under kjøring** – Formater verdiene i henhold til kulturen som er angitt under kjøring. Hvis du velger denne verdien, går du til **Tilordning**-kategorien i feltet **Dato, klokkeslett og nummerformat** og konfigurerer et ER-uttrykk som returnerer kulturkoden for kulturen, for eksempel den som tilhører kunden.

    ![Definere kulturen som er definert ved kjøring som kultur for en generert rapport i ER-operasjonsutforming.](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> En ER-komponent som du definerer en bestemt kultur for, kan inneholde underordnede ER-komponenter som er konfigurert til å fylle ut en tekstverdi. Som standard brukes kulturen til den overordnede komponenten til å formatere verdiene til disse komponentene. Du kan bruke følgende innebygde ER-funksjoner til å konfigurere bindinger for disse komponentene, og bruke en alternativ kultur for verdiformatering:
>
> - [DATEFORMAT](er-functions-datetime-dateformat.md#syntax-2)
> - [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md#syntax-2)
> - [NUMBERFORMAT](er-functions-text-numberformat.md#syntax-2)
>
> I versjon 10.0.20 og senere brukes den nasjonale innstillingen for formatkomponentene for typene **Felles\\Fil** og **Excel\\Fil** til å formatere verdiene under [PDF-konvertering](electronic-reporting-destinations.md#OutputConversionToPDF) av et generert dokument.

## <a name="translation"></a>Oversettelse

Du kan legge til nødvendige ER-etiketter i en redigerbar ER-komponent. Når en ER-etikett legges til, kan den oversettes på to måter: manuelt og automatisk.

### <a name="manual-translation"></a>Manuell oversettelse

Når du legger til en ER-etikett i **Tekstoversettelse**-[ruten](#TextTranslationPane), kan du oversette den manuelt til alle språk som støttes i gjeldende Finance-forekomst. Du kan velge foretrukket språk i **Språk**-feltet i delen **Systemspråk** eller **Brukerspråk**, skrive inn den aktuelle teksten i det tilsvarende **Oversatt tekst**-feltet og deretter velge **Oversett**. Denne prosessen må gjentas for hvert nødvendige språk og hver etikett du legger til.

### <a name="automatic-translation"></a>Automatisk oversettelse

Konfigurasjonen av en ER-komponent gjøres i utkastversjonen av ER-konfigurasjonen som den redigerbare ER-komponenten ligger i.

![ER-konfigurasjonssiden gir tilgang til konfigurasjonsversjonen i utkaststatus.](./media/er-multilingual-labels-configurations.png)

Som beskrevet tidligere i denne artikkelen kan du legge til nødvendige ER-etiketter i en redigerbar ER-komponent. På den måten kan du angi teksten til ER-etikettene på EN-US-språket. Du kan deretter eksportere etikettene til ER-komponenten ved hjelp av den innebygde ER-funksjonen. Velg utkastversjonen av en ER-konfigurasjon som inneholder den redigerbare ER-komponenten, og velg deretter **Exchange \> Eksporter etiketter**.

![ER-konfigurasjonsside som tillater eksport av ER-etiketter fra den valgte konfigurasjonsversjonen.](./media/er-multilingual-labels-export.png)

Du kan eksportere enten alle etiketter eller etiketter for ett språk som du angir ved begynnelsen av eksporten. Etiketter eksporteres som en zip-fil som inneholder XML-filer. Hver XML-fil inneholder etiketter for ett enkelt språk.

![Eksempel på eksportert fil som inneholder ER-etiketter for språket DE-AT.](./media/er-multilingual-labels-in-xml.png)

Dette formatet brukes til automatisk oversettelse av etiketter ved hjelp av eksterne oversettelsestjenester som [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md). Når du mottar de oversatte etikettene, kan du importere dem tilbake til utkastversjonen av en ER-konfigurasjon som inneholder ER-komponentene som eier disse etikettene. Velg utkastversjonen av en ER-konfigurasjon som inneholder den redigerbare ER-komponenten, og velg deretter **Exchange \> Last inn etiketter**.

![ER-konfigurasjonsside som tillater import av ER-etiketter til den valgte konfigurasjonsversjonen.](./media/er-multilingual-labels-load.png)

Oversatte etiketter vil bli importert til valgt ER-konfigurasjon. Oversatte etiketter som finnes i denne ER-konfigurasjonen, erstattes. Hvis det mangler en oversatt etikett i ER-konfigurasjonen, blir den lagt til.

## <a name="lifecycle"></a>Livssyklus

Etiketter med en ER-komponent som kan redigeres, beholdes, sammen med annet innhold for komponenten, i riktig versjon av en ER-konfigurasjon.

Etiketter i en basis-ER-komponent kan refereres til en avledet versjon av ER-komponenten som du oppretter for å introdusere endringene.

> [!TIP]
> Når du utformer en ER-løsning, kan du avlede din egen ER-[datamodell](er-overview-components.md#data-model-component)-komponent fra den som følger med. I denne avledede datamodellen kan du introdusere dine egne ER-etiketter og bruke dem i alle ER-formater som skal bruke datamodellen som datakilde. Du kan deretter avlede din egen ER-[format](er-overview-components.md#format-component)-komponenten fra den angitte komponenten ved å velge den avledede ER-datamodellen i stedet for den angitte. I versjon 10.0.28 eller senere, kan du aktivere funksjonen for **Forbedret tilgang til etiketter for den dominerende ER-datamodell** for å få tilgang til etiketter for en dominerende ER-datamodell i avledede ER-formatkomponenter, selv når du valgte en ER-datamodell som er forskjellig fra den som ble brukt i den grunnleggende ER-komponenten, for den avledede ER-komponenten.
>
> Når det samme etikettnavnet brukes i den avledede komponenten og dens stigende komponenter, brukes oversettelsen av etiketten som den mest relevante.

Etikettilordning for ER-versjonskontroller til et hvilket som helst attributt i en ER-komponent. Endringer i etikettilordningen registreres i listen over endringer (delta) i en redigerbar ER-komponent som er opprettet som en avledet versjon av den angitte ER-komponenten. Disse endringene vil bli validert når en avledet versjon rebaseres til en ny basisversjon.

## <a name="functions"></a>Funksjoner

Den innebygde [LISTOFFIELDS](er-functions-list-listoffields.md) ER-funksjonen får tilgang til ER-etiketter som er konfigurert for enkelte elementer i ER-komponenter.

Som beskrevet tidligere i denne artikkelen kan attributene **Etikett** og **Beskrivelse** for hver [modell](#LinkModelEnum) eller hvert [format](#LinkFormatEnum) for ER-opplistingsverdien kobles til en ER-etikett som er tilgjengelig i den gjeldende ER-komponenten. Du kan konfigurere et ER-uttrykk der du kaller funksjonen **LISTOFFIELDS** ved å bruke ER-opplistingen som argument. Dette uttrykket returnerer en liste som inneholder en post for hver verdi av en ER-opplistingsfunksjon som er definert som et argument for denne funksjonen. Hver post inneholder verdien til en ER-etikett som er koblet til en ER-opplistingsverdi:

- Verdien av en ER-etikett som er koblet til **Etikett**-attributtene, lagres i **Etikett**-feltet for den returnerte posten.
- Verdien av en ER-etikett som er koblet til **Beskrivelse**-attributtene, lagres i **Beskrivelse**-feltet for den returnerte posten.

## <a name="performance"></a><a name=performance></a>Ytelse

Når du konfigurerer en ER-formatkomponent til å generere en rapport på ditt foretrukne [språk](#language), eller til å importere et innkommende dokument der innholdet analyseres etter foretrukket språk, anbefaler vi at du aktiverer funksjonen for å **hurtigbufre foretrukket språk for gjeldende bruker for ER-kjøring** i arbeidsområdet [Funksjonsbehandling](../../fin-ops/get-started/feature-management/feature-management-overview.md). Denne funksjonen bidrar til å forbedre ytelsen, spesielt for ER-formatkomponenter som inneholder flere referanser til etiketter i ER-formler og bindinger, og mange [validering](general-electronic-reporting-formula-designer.md#TestFormula)-regler for å generere brukermeldinger på ønsket språk.

Når du endrer statusen til en ER-konfigurasjonsversjon fra **Utkast** til **Fullført**, og hvis konfigurasjonsversjonen inneholder ER-etiketter, lagres disse etikettene i appdatabasen. Lagringsskjemaet avhenger av statusen til funksjonen **Fremskynd ER-etikettlagringen**:

- Hvis funksjonen ikke er aktivert, lagres alle etikettene i feltet **LABELXML** i tabellen **ERSOLUTIONVERSIONTABLE** som én enkelt XML-kodesnutt.
- Hvis funksjonen er aktivert, opprettes det en egen post for hvert språk i tabellen **ERSOLUTIONVERSIONLABELSTABLE**. Feltet **INNHOLD** i denne tabellen lagrer etiketter per språk som en komprimert XML-kodesnutt.

Vi anbefaler at du aktiverer funksjonen **Fremskynd ER-etikettlagringen** i arbeidsområdet **Funksjonsbehandling**. Denne funksjonen kan forbedre utnyttelsen av nettverksbåndbredden og den generelle systemytelsen, fordi ER-etiketter på ett enkelt språk brukes i de fleste tilfeller når du arbeider med én enkelt ER-konfigurasjon.

Hvis du vil bruke det valgte lagringsskjemaet for å beholde etiketter for alle ER-konfigurasjonene i den gjeldende Finance-forekomsten, fullfører du fremgangsmåten nedenfor.

1. Gå til **Organisasjonsstyring** > **Periodisk** > **Bruk det valgte etikettlagringsskjemaet for alle ER-konfigurasjoner**.
2. Velg **OK**.


## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Funksjoner for elektronisk rapportering](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
