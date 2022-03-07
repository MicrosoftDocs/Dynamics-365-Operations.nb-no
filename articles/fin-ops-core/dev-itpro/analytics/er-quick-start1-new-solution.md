---
title: Utforme en ny ER-løsning for å skrive ut en egendefinert rapport
description: Dette emnet forklarer hvordan du utformer en ER-løsning (elektronisk rapportering) for å skrive ut en egendefinert rapport.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f5a3ac7cae58d17409ea081ec30f61cecf29ce9
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224040"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Utforme en ny ER-løsning for å skrive ut en egendefinert rapport

[!include[banner](../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker en rolle som systemansvarlig, utvikler av elektronisk rapportering eller funksjonskonsulent for elektronisk rapportering kan konfigurere parametere for ER-rammeverket, utforme nødvendige ER-konfigurasjoner for en ny ER-løsning for å få tilgang til dataene i et bestemt forretningsdomene og generere en egendefinert rapport i Microsoft Office-format. Denne fremgangsmåten kan gjennomføres i firmaet **USMF**.

- [Konfigurere ER-rammeverket](#ConfigureFramework)

    - [Konfigurere ER-parametere](#ConfigureParameters)
    - [Aktivere en ER-konfigurasjonsleverandør](#ActivateProvider)

        - [Se gjennom listen over ER-konfigurasjonsleverandører](#ReviewProvidersList)
        - [Legg til en ny ER-konfigurasjonsleverandør](#AddProvider)
        - [Aktivere en ER-konfigurasjonsleverandør](#ActivateAddedProvider)

- [Utforme en domenespesifikk datamodell](#DesignModel)

    - [Importere en ny datamodellkonfigurasjon](#ImportDataModel)
    - [Opprett en ny datamodellkonfigurasjon](#DesignDataModel)

        - [Gi navn til datamodellen](#NameDataModel)
        - [Legge til datamodellfelt](#FieldsEntry)
        - [Fullføre utformingen av datamodellen](#CompleteDataModel)

- [Utforme en modelltilordning for den konfigurerte datamodellen](#DesignMapping)

    - [Importere en ny modelltilordningskonfigurasjon](#ImportModelMapping)
    - [Opprette en ny modelltilordningskonfigurasjon](#CreateModelMapping)

        - [Utforme en ny modelltilordningskomponent](#DesignMappingComponent)
        - [Legge til datakilder for å få tilgang til apptabeller](#AddMmDataSource1)
        - [Legge til datakilder for å få tilgang til appopplistinger](#AddMmDataSource2)
        - [Legge til ER-etiketter for å generere en rapport på et angitt språk](#AddMmLabels)
        - [Legge til en datakilde for å transformere resultatene av å sammenligne opplistingsverdier med en tekstverdi](#AddMmDataSource3)
        - [Binde datakilder til datamodellfelt](#AddMmBindings1)
        - [Fullføre utformingen av modelltilordningen](#CompleteModelMapping)

- [Utforme en mal for en egendefinert rapport](#DesignReportTemplate)
- [Utforme et format](#DesignFormat)

    - [Importere en konstruert formatkonfigurasjon](#FormatImport)
    - [Opprette en ny formatkonfigurasjon](#FormatCreate)

        - [Importere en rapportmal](#ImportReportTemplate)
        - [Konfigurere et format](#ConfigureFormat)
        - [Definere databinding for en rapporttittel](#DefineFormatBindings)
        - [Gå gjennom modelldatakilden](#ReviewModelDataSource)
        - [Binde formatelementer til datakildefelt](#BindFormatElements)

    - [Kjøre et designet format fra ER](#RunFormatFromER)

- [Justere et designet format](#TuneFormat)

    - [Endre et format for å endre navnet på et generert dokument](#ModifyToChangeName)
    - [Endre et format for å endre rekkefølgen på spørsmål](#ModifyToOrder)
    - [Kjøre et endret format fra ER](#RunFormatFromER2)
    - [Fullføre formatutformingen](#CompleteFormat)

- [Utarbeide appartefakter for å kalle den utformede rapporten](#DevelopCustomCode)

    - [Endre kildekode](#ModifySourceCode)

        - [Legge til en datakontraktklasse](#DataContractClass)
        - [Legge til en grensesnittbyggerklasse](#UIBuilderClass)
        - [Legge til en dataleverandørklasse](#DataProviderClass)
        - [Legge til en etikettfil](#LabelsFile)
        - [Legge til en rapporttjenesteklasse](#ServiceClass)
        - [Legge til en rapportkontrollerklasse](#ControllerClass)
        - [Legge til et menyelement](#MenuItem)
        - [Legge til et menyelement i en meny](#Menu)
        - [Bygge et Visual Studio-prosjekt](#BuildVSProject)

    - [Kjøre et format fra appen](#RunFormatFromApp)

- [Justere en utviklet ER-løsning](#TuneSolution)

    - [Endre en modelltilordning](#ModifyModelMapping)

        - [Legge til datakilder for å få tilgang til et datakontraktobjekt](#AddDataSource1)
        - [Legge til en datakilde for å få tilgang til ER-formattilordningsposter](#AddDataSource2)
        - [Legge til en datakilde for å få tilgang til en formattilordningspost for et kjørende ER-format](#AddDataSource3)
        - [Angi navnet på det kjørende ER-formatet i datamodellen](#AddBinding)
        - [Fullføre utformingen av modelltilordningen](#CompleteModelMapping2)

    - [Endre et format](#ModifyFormat)

        - [Legge til et nytt formatelement](#AddFormatElement)
        - [Binde formatelementet som er lagt til](#BindAddedFormatElement)
        - [Fullføre formatutformingen](#CompleteFormat2)

    - [Kjøre et format fra appen](#RunFormatFromApp2)
    - [Kjøre et format fra ER](#RunFormatFromER3)
    - [Konfigurere et formatmål for forhåndsvisning på skjermen](#ConfigureDestination)
    - [Kjøre et format fra appen for å forhåndsvise det som et PDF-dokument](#RunFormatFromApp3)

- [Tilleggsressurser](#References)

I dette eksemplet skal du opprette en ny ER-løsning for [Spørreskjema](../../../human-resources/hr-learning-questionnaires.md)-modulen. Denne nye ER-løsningen lar deg utforme en rapport ved å bruke et Microsoft Excel-regneark som en mal. Deretter kan du generere **Spørreskjema**-rapporten i Excel- eller PDF-format, i tillegg til å generere den eksisterende SQL Server Reporting Services-rapporten (SSRS). Du kan også endre den nye rapporten senere på forespørsel. Ingen koding er nødvendig.

1. Hvis du vil kjøre den eksisterende rapporten, går du til **Spørreskjema** \> **Utforming** \> **Spørreskjemaer-rapporten**.

    ![Velge menyelementet Spørreskjemaer-rapport i Spørreskjema-modulen for å kjøre den eksisterende SSRS-rapporten](./media/er-quick-start1-application-menu-origin.png)

2. I dialogboksen **Spørreskjemaer-rapport** angir du utvalgskriterier. Bruk et filter slik at rapporten bare inneholder **SBCCrsExam**-spørreskjemaet.

    ![Angi utvalgskriterier i dialogboksen Spørreskjemaer-rapport](./media/er-quick-start1-ssrs-report-dialog.png)

Følgende illustrasjon viser den genererte versjonen av SSRS-rapporten for **SBCCrsExam**-spørreskjemaet.

![Generert SSRS-rapport](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>Konfigurere ER-rammeverket

Som en bruker i rollen som utvikler av elektronisk rapportering må du konfigurere minimumssettet av ER-parametere før du kan begynne å bruke ER-rammeverket til å utforme en ny ER-løsning.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>Konfigurere ER-parametere

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. I arbeidsområdet **Elektronisk rapportering** velger du **Parametere for elektronisk rapportering**.
3. På **Parametere for elektronisk rapportering**-siden, i **Generelt**-fanen angi **Aktiver utformingsmodus** til **Ja**.
4. Angi følgende parametere i fanen **Vedlegg**:

    - Sett **Konfigurasjoner**-feltet til **Fil** for **USMF**-firmaet.
    - Sett feltene **Jobbarkiv**, **Midlertidig**, **Grunnlinje** og **Annet** til **Fil**.

Hvis du vil ha mer informasjon om ER-parametere, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>Aktivere en ER-konfigurasjonsleverandør

Hver ER-konfigurasjon er merket som eid av en ER-konfigurasjonsleverandør. Derfor må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet før du begynner å legge til eller redigere ER-konfigurasjoner.

> [!NOTE]
> Bare eieren av en ER-konfigurasjon kan redigere den. Derfor, før en ER-konfigurasjon kan redigeres, må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>Se gjennom listen over ER-konfigurasjonsleverandører

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. I delen **Relaterte koblinger** i arbeidsområdet **Elektronisk rapportering** velger du **Konfigurasjonsleverandører**.
3. På siden **Konfigurasjonsleverandører** har hver konfigurasjonsleverandørpost et unikt navn og en unik URL-adresse. Se gjennom innholdet på denne siden. Hvis det allerede finnes en post for **Litware, Inc.** (`https://www.litware.com`), hopper du over den neste fremgangsmåten og [legger til en ny ER-konfigurasjonsleverandør](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Legg til en ny ER-konfigurasjonsleverandør

1. Velg **Ny** på siden **Konfigurasjonsleverandører**.
2. I **Navn**-feltet angir du **Litware, Inc.**
3. I **Internett-adresse**-feltet angir du `https://www.litware.com`.
4. Velg **Lagre**.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>Aktivere en ER-konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. I arbeidsområdet **Elektronisk rapportering** velger du konfigurasjonsleverandøren **Litware, Inc.**.
3. Velg **Angi som aktiv**.

Hvis du ha mer informasjon om ER-konfigurasjonsleverandører, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Utforme en domenespesifikk datamodell

Du må opprette en ny ER-konfigurasjon som inneholder en komponent av typen [datamodell](general-electronic-reporting.md#data-model-and-model-mapping-components) for bedriftsdomenet **Spørreskjema**. Denne datamodellen vil senere bli brukt som datakilde når du utformer et ER-format for å generere **Spørreskjema**-rapporten.

Ved å fullføre trinnene under [Importere en ny datamodellkonfigurasjon](#ImportDataModel) kan du importere den nødvendige datamodellen fra den angitte XML-filen. Du kan også fullføre trinnene i delen [Opprett en ny datamodellkonfigurasjon](#DesignDataModel) for å utforme denne datamodellen fra grunnen av.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Importere en ny datamodellkonfigurasjon

1. Last ned filen [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448), og lagre den på den lokale datamaskinen.
2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
4. I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.
5. Velg **Bla gjennom**, og finn og velg filen **Questionnaires model.version.1.xml**.
6. Velg **OK** for å importere konfigurasjonen.

For å fortsette hopper du over neste prosedyre, [Opprett en ny datamodellkonfigurasjon](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Opprett en ny datamodellkonfigurasjon

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
3. Velg **Opprett konfigurasjon**.
4. Skriv inn **Spørreskjemamodell** i **Navn**-feltet i rullegardinboksen.
5. Velg **Opprett konfigurasjon** for å opprette konfigurasjonen.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Gi navn til datamodellen

1. På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemamodell**.
2. Velg **Utforming**.
3. På siden **Datamodellutforming**, på hurtigfanen **Generelt**, i **Navn**-feltet, angir du <a name="DataModeName"></a>**Spørreskjemaer**.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Legge til nye datamodellfelt

1. Velg **Ny** på siden **Datamodellutforming**.
2. I dialogboksen for å legge til en datamodellnode gjør du følgende:

    1. Velg **Modellrot** som typen for den nye noden.
    2. I **Navn** feltet skriver du inn <a name="RootDefinitionName"></a>**Rot**.
    3. Velg **Legg til** for å legge til den nye noden.

    Denne rotbeskrivelsen vil bli brukt til å angi data for **Spørreskjema**-rapporten. Én enkelt datamodell kan ha flere beskrivelser. Hver beskrivelse kan angis for ett enkelt ER-format, for å identifisere data som kreves for å generere rapporten.

3. Velg **Ny** på nytt, og deretter gjør du følgende i dialogboksen for å legge til en datamodellnode:

    1. Velg **Underordnet for en aktiv node** som typen for den nye noden.
    2. Angi **Bedriftsnavn** i **Navn**-feltet.
    3. Velg **Streng** i **Varetype**-feltet.
    4. Velg **Legg til** for å legge til det nye feltet.

    Dette feltet er nødvendig for å overføre navnet på det gjeldende firmaet til en ER-rapport som bruker denne datamodellen som en datakilde.

4. Velg **Ny** på nytt, og deretter gjør du følgende i dialogboksen for å legge til en datamodellnode:

    1. Velg **Underordnet for en aktiv node** som typen for den nye noden.
    2. Angi **Spørreskjema** i **Navn**-feltet.
    3. Velg **Postliste** i **Varetype**-feltet.
    4. Velg **Legg til** for å legge til det nye feltet.

    Dette feltet brukes til å overføre listen over spørreskjemaer til en ER-rapport som bruker denne datamodellen som en datakilde.

5. Velg **Spørreskjema**-noden.
6. Fortsett å legge til de nødvendige feltene i den redigerbare datamodellen på samme måte helt til du har fullført den følgende datamodellstrukturen.

    | Feltbane                                                    | Datatype   | Feltbetegnelse / returnert verdi |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Rot                                                          |             | Referansepunktet for å be om spørreskjemadata. |
    | Root\\CompanyName                                             | Streng      | Navnet på gjeldende bedrift. |
    | Root\\ExecutionContext                                        | Registrer      | Utførelsesdetaljer for formatet. |
    | Root\\ExecutionContext\\FormatName                            | Streng      | Navnet på ER-formatet som kjøres. |
    | Root\\Questionnaire                                           | Postliste | Listen over spørreskjemaer |
    | Root\\Questionnaire\\Active                                   | Streng      | Status for gjeldende spørreskjema. |
    | Root\\Questionnaire\\Code                                     | Streng      | Kode for gjeldende spørreskjema. |
    | Root\\Questionnaire\\Description                              | Streng      | Beskrivelse av gjeldende spørreskjema. |
    | Root\\Questionnaire\\QuestionnaireType                        | Streng      | Typen gjeldende spørreskjema. |
    | Root\\Questionnaire\\QuestionOrder                            | Streng      | Den numeriske rekkefølgen for det gjeldende spørreskjemaet. |
    | Root\\Questionnaire\\ResultsGroup                             | Registrer      | Resultatparameterne for det gjeldende spørreskjemaet. |
    | Root\\Questionnaire\\ResultsGroup\\Code                       | Streng      | Identifikasjonskoden for den gjeldende resultatgruppen. |
    | Root\\Questionnaire\\ResultsGroup\\Description                | Streng      | Beskrivelse av gjeldende resultatgruppe. |
    | Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Kommatall        | Maksimalt antall poeng som kan oppnås. |
    | Root\\Questionnaire\\Question                                 | Postliste | Listen over spørsmål for det gjeldende spørreskjemaet. |
    | Root\\Questionnaire\\Question\\CollectionSequenceNumber       | Heltall     | Sekvensnummeret for den gjeldende svarsamlingen. |
    | Root\\Questionnaire\\Question\\Id                             | Streng      | Identifikasjonskoden for det gjeldende spørsmålet. |
    | Root\\Questionnaire\\Question\\MustBeCompleted                | Streng      | Et flagg som angir om det gjeldende spørsmålet må besvares. |
    | Root\\Questionnaire\\Question\\PrimaryQuestion                | Streng      | Et flagg som angir om det gjeldende spørsmålet er primært. |
    | Root\\Questionnaire\\Question\\SequenceNumber                 | Heltall     | Sekvensnummeret for det gjeldende spørsmålet. |
    | Root\\Questionnaire\\Question\\Text                           | Streng      | Teksten for det gjeldende spørsmålet. |
    | Root\\Questionnaire\\Question\\Answer                         | Postliste | Listen over svar for det gjeldende spørsmålet. |
    | Root\\Questionnaire\\Question\\Answer\\CorrectAnswer          | Streng      | Et flagg som angir om det gjeldende svaret er korrekt. |
    | Root\\Questionnaire\\Question\\Answer\\Points                 | Kommatall        | Poengene som er opptjent når det gjeldende svaret er valgt. |
    | Root\\Questionnaire\\Question\\Answer\\SequenceNumber         | Heltall     | Sekvensnummeret for det gjeldende svaret. |
    | Root\\Questionnaire\\Question\\Answer\\Text                   | Streng      | Teksten for det gjeldende svaret. |

    Følgende illustrasjon viser den fullførte, redigerbare datamodellen på siden **Datamodellutforming**.

    ![Konfigurert datamodell i ER-datamodellutforming](./media/er-quick-start1-model2.png)

7. Lagre endringene.
8. Lukk siden **Datamodellutforming**.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Fullføre utformingen av datamodellen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemamodell**.
3. I hurtigfanen **Versjoner** velger du konfigurasjonsversjonen med statusen **Utkast**.
4. Velg **Endre status** \> **Fullført**.

Statusen til versjon 1 av denne konfigurasjonen endres fra **Utkast** til **Fullført**. Versjon 1 kan ikke lenger endres. Denne versjonen inneholder den konfigurerte datamodellen og kan brukes som basis for andre ER-konfigurasjoner. Versjon 2 av denne konfigurasjonen opprettes og har statusen **Utkast**. Du kan redigere denne versjonen for å justere **Spørreskjema**-datamodellen.

![Versjoner av den redigerbare konfigurasjonen på Konfigurasjoner-siden](./media/er-quick-start1-model-configuration.png)

Hvis du vil ha mer informasjon om versjonskontroll for ERkonfigurasjoner, kan du se [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Den konfigurerte datamodellen er den abstrakte representasjonen av **Spørreskjema**-bedriftsdomenet og inneholder ingen relasjoner til artefakter som er spesifikke for Microsoft Dynamics 365 Finance.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Utforme en modelltilordning for den konfigurerte datamodellen

Som en bruker med rollen som utvikler av elektronisk rapportering må du opprette en ny ER-konfigurasjon som inneholder en [modelltilordning](general-electronic-reporting.md#data-model-and-model-mapping-components)-komponent for **Spørreskjema**-datamodellen. Fordi denne komponenten implementerer den konfigurerte datamodellen for Finance, er den Finance-spesifikk. Du må konfigurere komponenten for modelltilordning for å angi appobjektene som må brukes til å fylle ut den konfigurerte datamodellen med appdata ved kjøring. For å fullføre denne oppgaven må du være oppmerksom på implementeringsdetaljene for datastrukturen i **Spørreskjema**-bedriftsdomenet i Finance.

Ved å fullføre trinnene under [Importere en ny modelltilordningskonfigurasjon](#ImportModelMapping) som følger, kan du importere den nødvendige modelltilordningskonfigurasjonen fra den angitte XML-filen. Du kan også fullføre trinnene i delen [Opprette en ny modelltilordningskonfigurasjon](#CreateModelMapping) for å utforme denne modelltilordningen fra grunnen av.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Importere en ny modelltilordningskonfigurasjon

1. Last ned filen [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448), og lagre den på den lokale datamaskinen.
2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
4. I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.
5. Velg **Bla gjennom**, og finn og velg filen **Questionnaires mapping.version.1.1.xml**.
6. Velg **OK** for å importere konfigurasjonen.

For å fortsette hopper du over neste prosedyre, [Opprette en ny modelltilordningskonfigurasjon](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Opprette en ny modelltilordningskonfigurasjon

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemamodell**.
3. Velg **Opprett konfigurasjon**.
4. Følg disse trinnene i rullegardinboksen:

    1. I feltet **Ny** velger du **Modelltilordning basert på datamodellspørreskjemaer**.
    2. I **Navn**-feltet angir du **Spørreskjematilordning**.
    3. I feltet **Definisjon av datamodell** velger du **Rot**-definisjonen.
    4. Velg **Opprett konfigurasjon** for å opprette konfigurasjonen.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Utforme en ny modelltilordningskomponent

1. På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjematilordning**.
2. Velg **Utforming** for å åpne listen over tilordninger.
3. Velg tilordningen **Spørreskjematilordning** som ble automatisk lagt til for **Rot**-definisjonen
4. Velg **Utforming** for å begynne å konfigurere den valgte tilordningen.

Det blir automatisk lagt til en ny tilordning for **Rot**-definisjonen. Denne tilordningen har **Til modell**-retningen. Denne tilordningen kan derfor brukes til å fylle ut en datamodell med påkrevde data.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Legge til datakilder for å få tilgang til apptabeller

Du må konfigurere datakilder for å få tilgang til apptabellene som inneholder spørreskjemadetaljer.

1. På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Dynamics 365 for Operations\\Tabellposter**.
2. Legg til en ny datakilde som skal brukes for å få tilgang til KMCollection-tabellen, der hver post representerer ett enkelt spørreskjema:

    1. I **Datakilder**-ruten velger du **Legg til rot**.
    2. Skriv inn **Spørreskjema** i **Navn**-feltet i dialogboksen.
    3. I **Tabell**-feltet angir du **KMCollection**.
    4. Sett alternativet **Be om spørring** til **Ja**. Du kan deretter angi alternativer for [filtrering](../../fin-ops/get-started/advanced-filtering-query-options.md) for denne tabellen i dialogboksen for systemspørring ved kjøring.
    5. Velg **OK** for å legge til den nye datakilden.

3. I ruten **Datakildetyper** velger du **Dynamics 365 for Operations\\Tabellposter**.
4. Legg til en ny datakilde som skal brukes for å få tilgang til KMQuestion-tabellen, der hver post representerer ett enkelt spørsmål på et spørreskjema:

    1. I **Datakilder**-ruten velger du **Legg til rot**.
    2. Skriv inn **Spørsmål** i **Navn**-feltet.
    3. I **Tabell**-feltet angir du **KMQuestion**.
    4. Velg **OK** for å legge til den nye datakilden.

5. I ruten **Datakildetyper** velger du **Dynamics 365 for Operations\\Tabellposter**.
6. Legg til et nytt datakildeforsøk som skal brukes for å få tilgang til KMAnswer-tabellen, der hver post representerer ett enkelt svar på et spørsmål på et spørreskjema:

    1. I **Datakilder**-ruten velger du **Legg til rot**.
    2. Angi **Svar** i **Navn**-feltet.
    3. I **Tabell**-feltet angir du **KMAnswer**.
    4. Velg **OK** for å legge til den nye datakilden.

7. I ruten **Datakildetyper** velger du **Funksjoner\\Beregnet felt**.
8. Legg til et nytt beregnet felt som skal brukes til å få tilgang til en post i KMQuestionResultGroup-tabellen fra hver post i den overordnede KMCollection-tabellen:

    1. I **Datakilder**-ruten velger du **Spørreskjema**.
    2. Velg **Legg til**.
    3. Angi **\$ResultGroup** i **Navn**-feltet.
    4. Velg **Rediger formel**.
    5. I [ER-formelredigeringsprogram](general-electronic-reporting-formula-designer.md), i **Formel**-feltet, angir du **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** til å bruke [banen](er-formula-language.md#paths) til én-til-mange-relasjonen mellom tabellene KMCollection og KMQuestionResultGroup.
    6. Velg **Lagre**, og lukk formelredigeringsprogrammet.
    7. Velg **OK** for å legge til det nye beregnede feltet.

9. I ruten **Datakildetyper** velger du **Funksjoner\\Beregnet felt**.
10. Legg til et nytt beregnet felt som skal brukes til å få tilgang til spørsmålsposter i KMQuestion-tabellen fra hver post i den overordnede KMCollectionQuestion-tabellen:

    1. I **Datakilder**-ruten velger du **Spørreskjema**.
    2. Utvid **\<Relasjoner**-noden som inneholder én-til-mange-relasjoner fra KMCollection-tabellen.
    3. Velg den tilknyttede **KMCollectionQuestion**-tabellen, og velg deretter **Legg til**.
    4. Skriv inn **\$Question** i **Navn**-feltet.
    5. Velg **Rediger formel**.
    6. I formelredigeringsprogrammet, i **Formel**-feltet, angir du **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** for å returnere de aktuelle spørsmålspostene fra KMQuestion-tabellen.
    7. Velg **Lagre**, og lukk formelredigeringsprogrammet.
    8. Velg **OK** for å legge til det nye beregnede feltet.

11. I ruten **Datakildetyper** velger du **Funksjoner\\Beregnet felt**.
12. Legg til et nytt beregnet felt som skal brukes til å få tilgang til svarposter i KMAnswer-tabellen fra hver post i den overordnede KMQuestion-tabellen:

    1. I **Datakilder**-ruten velger du **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, og velg deretter **Legg til**.
    2. Skriv inn **\$Answer** i **Navn**-feltet.
    3. Velg **Rediger formel**.
    4. I formelredigeringsprogrammet, i **Formel**-feltet, angir du **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** for å returnere de aktuelle svarpostene fra KMAnswer-tabellen.
    5. Velg **Lagre**, og lukk formelredigeringsprogrammet.
    6. Velg **OK** for å legge til det nye beregnede feltet.

13. I ruten **Datakildetyper** velger du **Dynamics 365 for Operations\\Tabell**.
14. Legg til en ny datakilde som skal brukes til å få tilgang til metoder i CompanyInfo-tabellen. Legg merke til at **find()**-metoden for denne tabellen returnerer en post som representerer et firma for gjeldende Finance-forekomst, som denne tilordningen kalles i sammenheng med.

    1. I **Datakilder**-ruten velger du **Legg til rot**.
    2. Skriv inn **CompanyInfo** i **Navn**-feltet.
    3. I **Tabell**-feltet angir du **CompanyInfo**.
    4. Velg **OK** for å legge til den nye datakilden.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Legge til datakilder for å få tilgang til appopplistinger

Du må konfigurere datakilder for å få tilgang til appopplistinger og sammenligne verdiene med verdiene i felt av typen **Opplisting** i apptabellene. Du må bruke resultatet av sammenligningen for å fylle ut de aktuelle feltene i datamodellen.

1. På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Dynamics 365 for Operations\\Opplisting**.
2. Legg til en ny datakilde som skal brukes til å få tilgang til verdier i **EnumAppNoYes**-opplistingen:

    1. I **Datakilder**-ruten velger du **Legg til rot**.
    2. Skriv inn **EnumAppNoYes** i **Navn**-feltet.
    3. I **Opplisting**-feltet angir du **NoYes**.
    4. Velg **OK** for å legge til den nye datakilden.

3. I ruten **Datakildetyper** velger du **Dynamics 365 for Operations\\Opplisting**.
4. Legg til en ny datakilde som skal brukes til å få tilgang til verdiene i **KMCollectionQuestionMode**-opplistingen:

    1. I **Datakilder**-ruten velger du **Legg til rot**.
    2. Skriv inn **EnumAppQuestionOrder** i **Navn**-feltet i dialogboksen.
    3. I **Opplisting**-feltet angir du **KMCollectionQuestionMode**.
    4. Velg **OK** for å legge til den nye datakilden.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>Legge til ER-etiketter for å generere en rapport på et angitt språk

Du kan legge til ER-etiketter for å konfigurere noen av datakildene til returverdier som er avhengig av språket som er definert i konteksten til modelltilordningens kall.

1. På siden **Modelltilordningsutforming**, i ruten **Datakilder**, velger du **Svar**, og deretter velger du **Rediger**.
2. Aktiver **Etikett**-feltet.
3. Velg **Oversett**.
4. Følg disse trinnene i dialogboksen **Tekstoversettelse**:

    1. I feltet **Etikett-ID** angir du **PositiveAnswer**.
    2. I feltet **Tekst på standardspråk** angir du **Ja**.
    3. Velg **Oversett**.
    4. I feltet **Etikett-ID** angir du **NegativeAnswer**.
    5. I feltet **Tekst på standardspråk** angir du **Nei**.
    6. Velg **Oversett**.

5. Lukk dialogboksen **Tekstoversettelse**.
6. Velg **Avbryt**.

![Legge til ER-etiketter for den redigerbare modelltilordningen](./media/er-quick-start1-adding-labels.png)

Du har angitt ER-etiketter bare for standardspråket. Hvis du vil ha informasjon om hvordan ER-etiketter kan oversettes til andre språk, kan du se [Utforme flerspråklige rapporter](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Legge til en datakilde for å transformere resultatene av å sammenligne opplistingsverdier med en tekstverdi

Fordi du må transformere resultatene av sammenligningen mellom opplistingsverdier og tekstverdier flere ganger for forskjellige kilder, kan det være lurt å konfigurere denne logikken som én enkelt datakilde. Hvis du vil at denne datakilden skal kunne brukes på nytt, må du imidlertid konfigurere den som en parameterisert datakilde. For mer informasjon, se [Støtte for parametriserte kall av ER-datakilder av felttypen Beregnet](er-calculated-field-type.md).

1. På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Generelt\\Tom container**.
2. Legg til en ny containerdatakilde:

    1. I **Datakilder**-ruten velger du **Legg til rot**.
    2. Skriv inn **Hjelpeprogram** i **Navn**-feltet i dialogboksen.
    3. Velg **OK** for å legge til den nye containerdatakilden.

3. I ruten **Datakildetyper** velger du **Funksjoner\\Beregnet felt**.
4. Legg til en ny datakilde:

    1. I **Datakilder**-ruten velger du **Hjelpeprogram**.
    2. Velg **Legg til**.
    3. Skriv inn **NoYesEnumToString** i **Navn**-feltet i dialogboksen.
    4. Velg **Rediger formel**.
    5. Velg **Parametere** i formelredigeringsprogrammet.
    6. Følg denne fremgangsmåten for å angi parametere for det konfigurerte uttrykket:

        1. Velg **Ny**.
        2. Skriv inn **Argument** i **Navn**-feltet.
        3. I **Type**-feltet velger du datatypen **Boolsk**.
        4. Velg **OK**.

    7. I **Formel**-feltet angir du **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** for å returnere teksten for den aktuelle ER-etiketten, avhengig av språket i kjøringskonteksten og verdien av den angittet parameteren.
    8. Velg **Lagre**, og lukk formelredigeringsprogrammet.
    9. Velg **OK** for å legge til den nye datakilden.

![Konfigurert modelltilordning i ER-modelltilordningsutforming](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Binde datakilder til datamodellfelt

Du må binde de konfigurerte datakildene til feltene i datamodellen for å angi hvordan datamodellen skal fylles ut med appdata ved kjøring.

1. På siden **Modelltilordningsutforming**, i ruten **Datamodell**, velger du **Bedriftsnavn**.
2. I **Datakilder**-ruten utvider du **CompanyInfo**, og deretter gjør du følgende:

    1. Utvid noden **CompanyInfo.find()** som representerer **find()**-metoden i CompanyInfo-tabellen.
    2. Velg **CompanyInfo.find().Name**.
    3. Velg **Bind** for å fylle ut navnet på firmaet som den konfigurerte modelltilordningen kalles i, i konteksten for kjøretid.

3. I **Datamodell**-ruten velger du **Spørreskjema**.
4. I **Datakilder**-ruten velger du **Spørreskjema**, og deretter velger du **Bind** for å fylle ut spørreskjemaposter.
5. I **Datamodell**-ruten utvider du **Spørreskjema**, og deretter gjør du følgende:

    1. I **Datamodell**-ruten velger du **Aktiv**.
    2. I **Datamodell**-ruten velger du **Rediger**.
    3. I **Formel**-feltet skriver du inn **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** for å fylle ut det tekstavhengige og språkavhengige resultatet av sammenligningen mellom opplistingsverdier.

6. Fortsett med å binde datakilder til datamodellfelt på samme måte til du oppnår følgende resultat.

    | Feltbane                                              | Datatype   | Handling | Bindingsuttrykk |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | Bedriftsnavn                                             | Streng      | Bind   | CompanyInfo.'find()'.Name |
    | Spørreskjema                                           | Postliste | Bind   | Spørreskjema |
    | Questionnaire\\Active                                   | Streng      | Rediger   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Questionnaire\\Code                                     | Streng      | Bind   | \@.kmCollectionId |
    | Questionnaire\\Description                              | Streng      | Bind   | \@.Description |
    | Questionnaire\\QuestionnaireType                        | Streng      | Bind   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Questionnaire\\QuestionOrder                            | Streng      | Rediger   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Betinget",<br>EnumAppQuestionOrder.Random, "Tilfeldig (prosentverdi på spørreskjema)",<br>EnumAppQuestionOrder.RandomGroup, "Tilfeldig (prosentverdi i resultatgrupper)",<br>EnumAppQuestionOrder. Sequence, "Sekvensiell",<br>"") |
    | Questionnaire\\ResultsGroup                             | Registrer      |        | |
    | Questionnaire\\ResultsGroup\\Code                       | Streng      | Bind   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Questionnaire\\ResultsGroup\\Description                | Streng      | Bind   | \@.'\$ResultGroup'.description |
    | Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Kommatall        | Bind   | \@.'\$ResultGroup'.maxPoint |
    | Questionnaire\\Question                                 | Postliste | Bind   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Questionnaire\\Question\\CollectionSequenceNumber       | Heltall     | Bind   | \@.answerCollectionSequenceNumber |
    | Questionnaire\\Question\\Id                             | Streng      | Bind   | \@.kmQuestionId |
    | Questionnaire\\Question\\MustBeCompleted                | Streng      | Rediger   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\PrimaryQuestion                | Streng      | Bind   | \@.parentQuestionId |
    | Questionnaire\\Question\\SequenceNumber                 | Heltall     | Bind   | \@.SequenceNumber |
    | Questionnaire\\Question\\Text                           | Streng      | Bind   | \@.'\$Question'.text |
    | Questionnaire\\Question\\Answer                         | Postliste | Bind   | \@.'\$Question'.'\$Answer' |
    | Questionnaire\\Question\\Answer\\CorrectAnswer          | Streng      | Rediger   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\Answer\\Points                 | Kommatall        | Bind   | \@.point |
    | Questionnaire\\Question\\Answer\\SequenceNumber         | Heltall     | Bind   | \@.sequenceNumber |
    | Questionnaire\\Question\\Answer\\Text                   | Streng      | Bind   | \@.text |

    Den følgende illustrasjonen viser den endelige tilstanden til den konfigurerte modelltilordningen på siden **Modelltilordningsutforming**.

    ![Fullstendig konfigurert modelltilordning i ER-modelltilordningsutforming](./media/er-quick-start1-mapping2.png)

7. Lagre endringene.
8. Lukk siden **Modelltilordningsutforming**.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Fullføre utformingen av modelltilordningen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjematilordning**.
3. I hurtigfanen **Versjoner** velger du konfigurasjonsversjonen med statusen **Utkast**.
4. Velg **Endre status** \> **Fullført**.

Statusen til versjon 1.1 av denne konfigurasjonen endres fra **Utkast** til **Fullført**. Versjon 1.1 kan ikke lenger endres. Denne versjonen inneholder den konfigurerte modelltilordningen og kan brukes som basis for andre ER-konfigurasjoner. Versjon 1.2 av denne konfigurasjonen opprettes og har statusen **Utkast**. Du kan redigere denne versjonen for å justere konfigurasjonen **Spørreskjematilordning**.

![Versjoner av den redigerbare ER-konfigurasjonen på Konfigurasjoner-siden](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Den konfigurerte modelltilordningen er den Finance-spesifikke implementeringen av den abstrakte datamodellen som representerer bedriftsdomenet **Spørreskjema**.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Utforme en mal for en egendefinert rapport

ER-rammeverket bruker forhåndsdefinerte maler til å generere rapporter i Microsoft Office-formater (Excel-arbeidsbøker eller Word-dokumenter). Mens den påkrevde rapporten genereres, fylles det ut en mal med nødvendige data i samsvar med den konfigurerte dataflyten. Derfor må du først utforme en mal for den egendefinerte rapporten. Denne malen må utformes som en Excel-arbeidsbok, der strukturen representerer oppsettet til en egendefinert rapport. Du må gi navn til alle Excel-elementer du planlegger å fylle ut med nødvendige data.

1. Last ned filen [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448), og lagre den på den lokale datamaskinen.
2. Åpne filen i Excel, og gå gjennom strukturen til arbeidsboken.

Som den følgende illustrasjonen viser, er den nedlastede malen utformet for å skrive ut bestemte spørreskjemaer som presenterer spørsmålene i et spørreskjema sammen med riktige svar.

![Excel-mal for utskrift av angitte spørreskjemaer](./media/er-quick-start1-template-layout.png)

Excel-navn er lagt til denne malen for å fylle ut spørreskjemadetaljene. Du kan bruke Navnebehandling til å se gjennom Excel-navnene.

![Bruke Navnebehandling til å se gjennom Excel-navn i den angitte Excel-malen](./media/er-quick-start1-template-names.png)

Rapportetiketter er lagt til som fast tekst på norsk. Du kan erstatte rapportetikettene med nye Excel-navn som fyller ut etikettene med språkavhengig tekst, ved å bruke [etiketter](#AddMmLabels) i ER-format, som du gjorde for språkavhengige uttrykk i den konfigurerte modelltilordningen. I dette tilfellet må ER-etiketter legges til i det redigerbare ER-formatet.

Som den følgende illustrasjonen viser, er det egendefinerte rapporthodet angitt for at Excel skal kunne utføre sideveksling.

![Egendefinert rapporthode i den angitte Excel-malen](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Utforme et format

Som en bruker med rollen som funksjonsrådgiver for elektronisk rapportering må du opprette en ny ER-konfigurasjon som inneholder en komponent av typen [format](general-electronic-reporting.md#FormatComponentOutbound). Du må konfigurere formatkomponenten til å angi hvordan en rapportmal skal fylles ut med nødvendige data ved kjøring.

Ved å fullføre trinnene under [Importere en konstruert formatkonfigurasjon](#FormatImport) kan du importere det nødvendige formatet fra den angitte XML-filen. Du kan også fullføre trinnene i delen [Opprette en ny formatkonfigurasjon](#FormatCreate) for å utforme dette formatet fra grunnen av.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Importere en konstruert formatkonfigurasjon

1. Last ned filen [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448), og lagre den på den lokale datamaskinen.
2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
4. I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.
5. Velg **Bla gjennom**, og finn og velg filen **Questionnaires format.version.1.1.xml**.
6. Velg **OK** for å importere konfigurasjonen.

For å fortsette hopper du over neste prosedyre, [Opprette en ny formatkonfigurasjon](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Opprette en ny formatkonfigurasjon
 
1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemamodell**.
3. Velg **Opprett konfigurasjon**.
4. Følg disse trinnene i rullegardinboksen:

    1. I feltet **Ny** velger du **Format basert på datamodellspørreskjemaer**.
    2. I **Navn**-feltet angir du **Spørreskjemarapport**.
    3. I feltet **Datamodellversjon** velger du **1**.

        > [!NOTE]
        > - Hvis du velger en bestemt versjon av basisdatamodellen, vil strukturen i den tilsvarende versjonen av datamodellen vises som strukturen til **Modell**-datakilden i formatet som opprettes.
        > - Du kan la dette feltet være tomt. I så fall vises strukturen til **Utkast**-versjonen av datamodellen som strukturen til **Modell**-datakilden i formatet som er opprettet. Du kan deretter justere modellen og umiddelbart se justeringene i formatet. Denne fremgangsmåten kan forbedre effektiviteten for ER-løsningsutformingen når du konfigurerer datamodellen, modelltilordningen og formatet samtidig.
        > - Hvis du velger en bestemt versjon av basisdatamodellen, kan du bytte til å bruke **Utkast**-versjonen senere, når du begynner å redigere et format.

    4. I feltet **Definisjon av datamodell** velger du **Rot**-definisjonen.

5. Velg **Opprett konfigurasjon** for å opprette konfigurasjonen.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Importere en rapportmal

1. På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemarapport**.
2. Velg **Utforming** for å begynne å konfigurere et egendefinert format.
3. På siden **Formatutforming**, i handlingsruten, velger du **Importer** \> **Importer fra Excel**.
4. Følg disse trinnene i dialogboksen:

    1. Velg **Legg til mal**.
    2. Finn og velg den lokalt lagrede filen **Questionnaires report template.xslx**, og velg deretter **Åpne**.
    3. Velg **OK** for å importere malen.

    ![Importere en rapportmal](./media/er-quick-start1-template-import.png)

Formatet **Excel\\Fil** legges automatisk til i det redigerbare formatet som et rotelement.. I tillegg legges enten formatelementet **Excel\\Område** eller formatelementet **Excel\\Celle** til automatisk for hvert gjenkjente Excel-navn på den importert malen. Formatet **Excel\\Heode** som har det nestede **Streng**-elementet, legges til automatisk for å gjenspeile hodeinnstillingene i den importerte malen.

![Formatstruktur som inkluderer automatisk tilføyde elementer i ER-operasjonsutforming](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Konfigurere et format

1. På siden **Formatutforming**, i formattreet, velger du **Excel**-rotelementet.
2. På **Format**-fanen til høyre på siden, i **Navn**-feltet angir du <a name="AddFormatRootElement"></a>**Rapport**.
3. I **Språkinnstilling**-feltet velger du **Brukerinnstilling** for å kjøre rapporten på brukerens foretrukne språk.
4. I **Kulturinnstillinger**-feltet velger du **Brukerinnstilling** for å kjøre rapporten i brukerens foretrukne kultur.

    Hvis du vil ha informasjon om hvordan du angir språk- og kulturkontekster for en ER-prosess, kan du se [Utforme flerspråklige rapporter](er-design-multilingual-reports.md).

    ![Konfigurere språk- og kulturinnstillinger for den utformede rapporten i ER-operasjonsutforming](./media/er-quick-start1-template-format-structure1.png)

5. Utvid rotnoden i formattreet, og velg deretter **ResultsGroup**.
6. På **Format**-fanen i feltet **Replikeringsretning** velger du **Ingen replikering** fordi du ikke forventer å ha flere resultatgrupper for ett enkelt spørreskjema.

    ![Definere replikeringsretningen for Område-formatelementer i ER-operasjonsutforming](./media/er-quick-start1-template-format-structure2.png)

7. Velg **Lagre**.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Definere databinding for en rapporttittel

Du må angi en databinding for et formatelement som brukes til å fylle ut tittelen til en generert rapport.

1. På siden **Formatutforming**, på **Tilordning**-fanen til høyre, velger du elementet **Rapport\\ReportTitle**.
2. Velg **Rediger formel**.
3. Velg **Oversett** i formelredigeringsprogrammet.
4. Følg disse trinnene i dialogboksen **Tekstoversettelse**:

    1. I feltet **Etikett-ID** angir du **ReportTitle**.
    2. I feltet **Tekst på standardspråk** angir du **Spørreskjemarapport**.
    3. Velg **Oversett**, og velg deretter **Lagre**.
    4. Velg **Oversett** for å lukke dialogboksen **Tekstoversettelse**.

5. Lukk formelredigeringsprogrammet.

    ![Konfigurere bindingen for å fylle ut tittelen til en generert rapport](./media/er-quick-start1-add-report-title-label.png)

Du kan bruke denne metoden til å endre alle andre etiketter for gjeldende malspråk. Hvis du vil ha informasjon om hvordan de tilføyde etikettene for en enkelt ER-konfigurasjon kan oversettes til alle støttede språk, kan du se [Utforme flerspråklige rapporter](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Gå gjennom modelldatakilden

1. På siden **Formatutforming**, på **Tilordning**-fanen, velger du <a name="ModelDSName"></a>**modell**-datakilden som representerer basisdatamodellen til dette ER-formatet.
2. Velg **Rediger**.
3. Se gjennom informasjonen i dialogboksen **Egenskaper for datakilde**. Denne datakilden representerer versjon 1 av datamodellkomponenten **Spørreskjemaer** som ligger i ER-konfigurasjonen **Spørreskjemamodell**.

![Egenskaper for modelldatakilden i ER-operasjonsutforming](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Binde formatelementer til datakildefelt

Hvis du vil angi hvordan en mal skal fylles ut ved kjøring, må du binde hvert formatelement som er knyttet til et passende Excel-navn, til et enkelt felt i formatets datakilde.

1. På siden **Formatutforming**, i formattreet, velger du formatelementet **Rapport\\CompanyName**.
2. På **Tilordning**-fanen velger du datakildefeltet **model.CompanyName** for **Streng**-typen.
3. Velg **Bind** for å skrive inn et firmanavn i en mal.
4. I formattreet velger du elementet **Rapport\\Spørreskjema**.
5. På **Tilordning**-fanen velger du datakildefeltet **model.Questionnaire** for **Postliste**-typen.
6. Velg **Bind**.
7. Velg **Vis detaljer** for å se flere detaljer for formatelementer.

    Formatelementet for **Spørreskjema**-området konfigureres som vertikalt replikert. Når det er bundet til en datakilde av typen **Postliste**, gjentas det aktuelle **Spørreskjema**-området for Excel-malen for hver post i den bundne datakilden.
 
    ![Binde formatelementet Spørreskjema-område til de riktige datakildene for postliste i ER-operasjonsutforming](./media/er-quick-start1-bindings1.png)

    Siden **Spørreskjema**-området i Excel-malen er definert fra rad 5 til og med rad 14, gjentas disse radene for hvert rapporterte spørreskjema.

    ![Rader i Excel-malen som blir gjentatt i en generert rapport for hver post i datakildene for postliste](./media/er-quick-start1-template-questionnaire-range.png)

8. Konfigurer lignende bindinger for de gjenværende formatelementene, som beskrevet i følgende tabell.

    > [!NOTE]
    > I denne tabellen antar informasjonen i kolonnen "Datakildebane" at ER-funksjonen [Relativ bane](relative-path-data-bindings-er-models-format.md) er aktivert.

    | Formatelementbane                                      | Datakildebane |
    |----------------------------------------------------------|------------------|
    | Excel\\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Questionnaire                                     | **model.Questionnaire** |
    | Excel\\Questionnaire\\Active                             | **\@.Active**, der **\@** er **model.Questionnaire** |
    | Excel\\Questionnaire\\Code                               | **\@.Code** |
    | Excel\\Questionnaire\\Description                        | **\@.Description** |
    | Excel\\Questionnaire\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Questionnaire\\QuestionOrder                      | **\@.QuestionOrder** |
    | Excel\\Questionnaire\\ResultsGroup\\Code\_               | **\@.ResultsGroup.Code** |
    | Excel\\Questionnaire\\ResultsGroup\\Description\_        | **\@.ResultsGroup.Description** |
    | Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Questionnaire\\Question                           | **\@.Question** |
    | Excel\\Questionnaire\\Question\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**, der **\@** er **model.Questionnaire.Question** |
    | Excel\\Questionnaire\\Question\\Id                       | **\@.Id** |
    | Excel\\Questionnaire\\Question\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Questionnaire\\Question\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Questionnaire\\Question\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Questionnaire\\Question\\Text                     | **\@.Text** |
    | Excel\\Questionnaire\\Question\\Answer                   | **\@.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer    | **\@.CorrectAnswer**, der **\@** er **model.Questionnaire.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\Points           | **\@.Points** |
    | Excel\\Questionnaire\\Question\\Answer\\Text             | **\@.Text** |

9. Når du er ferdig, velg **Lagre**.

Den følgende illustrasjonen viser den endelige tilstanden til de konfigurerte databindingene på siden **Formatutforming**.

![Konfigurerte databindinger i ER-datamodellutforming](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Hele samlingen av angitte datakilder og bindinger representerer en formattilordningskomponent i det konfigurerte formatet. Denne formattilordningen kalles når du kjører det konfigurerte formatet for rapportgenerering.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Kjøre et designet format fra ER

Du kan nå kjøre et designet format for testformål fra **Konfigurasjoner**-siden.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjon**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjemarapport**.
3. Velg **Utforming** for formatversjonen som har statusen **Utkast**.
4. På **Formatutforming**-siden velger du **Kjør**.
5. I dialogboksen **ER-parametere**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.
6. Velg **OK** for å bekrefte filtreringsalternativet.
7. Velg **OK** for å kjøre rapporten.
8. Gå gjennom den genererte rapporten.

Som [standard](electronic-reporting-destinations.md#default-behavior) leveres en generert rapport som en Excel-fil du kan laste ned. Illustrasjonen nedenfor viser to sider i den genererte rapporten i Excel-format.

![Eksempel på en generert rapport i Excel-format, side 1](./media/er-quick-start1-report1a.png)

![Eksempel på en generert rapport i Excel-format, side 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Justere et designet format

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Endre et format for å endre navnet på et generert dokument

Som standard navngis et generert dokument ved å bruke aliaset til den gjeldende brukeren. Når du endrer formatet, kan du endre denne virkemåten slik at et generert dokument navngis basert på den egendefinerte logikken. Navnet på et generert dokument kan for eksempel være basert på gjeldende dato og klokkeslett for en økt, og på rapportens tittel.

1. På siden **Formatutforming** velger du rotelementet **Rapport**.
2. På **Tilordning**-fanen velger du **Rediger filnavn**.
3. I **Formel**-feltet skriver du inn **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.
4. Velg **Lagre**, og lukk formelredigeringsprogrammet.
5. Velg **Lagre**.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Endre et format for å endre rekkefølgen på spørsmål

Spørsmålene er ikke riktig sortert i en generert rapport. Du kan endre rekkefølgen ved å endre formatet.

1. På siden **Formatutforming** velger du rotelementet **Rapport**.
2. På **Tilordning**-fanen i formattreet utvider du **Rapport\\Spørreskjema\\Spørsmål**.

    ![Spørsmål-formatelement for Område-typen i ER-operasjonsutforming](./media/er-quick-start1-bindings3.png)

3. På **Tilordning**-fanen velger du **model.Questionnaire**.
4. Velg **Legg til** \> **Funksjoner\\Beregnet felt**, og skriv deretter inn **OrderedQuestions** i **Navn**-feltet.
5. Velg **Rediger formel**.
6. I formularedigeringsprogrammet, i **Formel**-feltet, skriver du inn **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** for å sortere listen over spørsmål i det gjeldende spørreskjemaet etter sekvensordrenummeret.
7. Velg **Lagre**, og lukk formelredigeringsprogrammet.
8. Velg **OK** for å fullføre registreringen av et nytt beregnet felt.
9. På **Tilordning**-fanen velger du **model.Questionnaire.OrderedQuestions**.
10. I formattreet velger du **Excel\\Spørreskjema\\Spørsmål**.
11. Velg **Bind**, og bekreft deretter at den gjeldende banen **model.Questionnaire.Questions** er erstattet av den nye banen **model.Questionnaire.OrderedQuestions** i alle bindinger av nestede elementer.
12. Velg **Lagre**.

![Binde Spørsmål-formatelementet til den konfigurerte OrderedQuestions-datakilden i ER-operasjonsutforming](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Kjøre et endret format fra ER

Du kan nå kjøre et endret format for testformål fra ER-rammeverket.

1. På **Formatutforming**-siden velger du **Kjør**.
2. I dialogboksen **ER-parametere**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.
3. Velg **OK** for å bekrefte filtreringsalternativet.
4. Velg **OK** for å kjøre rapporten.
5. Gå gjennom den genererte rapporten.

Den følgende illustrasjonen viser en generert rapport i Excel-format der spørsmålene er riktig sortert.

![Generert rapport i Excel-format som har spørsmål som er riktig sortert](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Fullføre formatutformingen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjemarapport**.
3. I hurtigfanen **Versjoner** velger du konfigurasjonsversjonen med statusen **Utkast**.
4. Velg **Endre status** \> **Fullført**.

Statusen til versjon 1.1 av denne konfigurasjonen endres fra **Utkast** til **Fullført**. Versjon 1.1 kan ikke lenger endres. Denne versjonen inneholder formatet som er konfigurert, og kan brukes til å skrive ut den egendefinerte rapporten. Versjon 1.2 av denne konfigurasjonen opprettes og har statusen **Utkast**. Du kan redigere denne versjonen for å justere formatet til **Spørreskjema**-rapporten.

![Redigerbar ER-konfigurasjon på Konfigurasjoner-siden](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Det konfigurerte formatet er din utforming av **Spørreskjema**-rapporten og inneholder ingen relasjoner til de Finance-spesifikke artefaktene.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Utarbeide appartefakter for å kalle den utformede rapporten

Som en bruker i Systemansvarlig-rollen må du utvikle ny logikk slik at det konfigurerte ER-formatet kan kalles fra brukergrensesnittet (UI) i appen for å generere den egendefinerte rapporten. For øyeblikket tilbyr ikke ER funksjonalitet for å konfigurere denne typen logikk. Derfor kreves noe utviklingsarbeid. 

For å utvikle den nye logikken må du distribuere en topologi som støtter fortløpende bygging. Hvis du vil ha mer informasjon, kan du se [Distribuere topologier som støtter sammenhengende automatisering av bygging og testing](../perf-test/continuous-build-test-automation.md). Du må også ha tilgang til utviklingsmiljøet for denne topologien. Hvis du vil ha mer informasjon om det tilgjengelige API-et for ER, kan du se [API for ER-rammeverk](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Endre kildekode

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Legge til en datakontraktklasse

Legg til den nye **QuestionnairesErReportContract**-klassen i Microsoft Visual Studio-prosjektet ditt, og skriv kode som spesifiserer datakontrakten som skal brukes til å kjøre det konfigurert ER-formatet.

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>Legge til en grensesnittbyggerklasse

Legg til den nye **QuestionnairesErReportUIBuilder**-klassen i Visual Studio-prosjektet ditt, og skriv kode for å generere en dialogboks for kjøretid som skal brukes til å slå opp formattilordnings-ID-en for ER-formatet som må kjøres. Den angitte koden slår bare opp ER-formater som inneholder en datakilde av typen **Datamodell** som refererer til **[Spørreskjemaer](#DataModeName)**-datamodellen ved å bruke **[Rot](#RootDefinitionName)**-definisjonen.

> [!NOTE]
> Du kan også bruke ER-integreringspunkter til å filtrere ER-formater. Hvis du vil ha mer informasjon, kan du se [API for å vise et formattilordningssoppslag](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Legge til en dataleverandørklasse

Legg til den nye **QuestionnairesErReportDP**-klassen i Visual Studio-prosjektet ditt, og skriv kode som introduserer dataleverandøren som skal brukes til å kjøre det konfigurerte ER-formatet. Den angitte koden inkluderer bare datakontrakten for denne dataleverandøren.

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Legge til en etikettfil

Legg til den nye **QuestionnairesErReportLabels\_nb-NO**-etikettfilen i Visual Studio-prosjektet ditt, og angi følgende etiketter for nye UI-ressurser:

- **\@QuestionnairesReport**-etiketten for et nytt menyelement som inneholder følgende tekst på norsk (nb-NO): **Spørreskjemarapport (drevet av ER)**
- **\@QuestionnairesReportBatchJobDescription**-etiketten for tittelen på en satsvis jobb hvis et valgt ER-format er planlagt for kjøring som en satsvis jobb

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Legge til en rapporttjenesteklasse

Legg til den nye **QuestionnairesErReportService**-klassen i Visual Studio-prosjektet ditt, og skriv kode som kaller opp et ER-format, identifiserer det med en formattilordnings-ID og leverer en datakontrakt som en parameter.

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

Når du må bruke et ER-format som kjører appdata, må du konfigurere en datakilde av typen **Datamodell** i formattilordningen. Denne datakilden refererer til en bestemt del av den angitte datamodellen ved hjelp av én enkelt rotdefinisjon. Når ER-formatet kjøres, kaller det denne datakilden for å få tilgang til den riktige ER-modelltilordningen som er konfigurert for en angitt modell og rotdefinisjon.

All informasjon du kanskje forbereder i kildekoden og lageret som en del av datakontrakten, kan sendes til det aktive ER-formatet ved å bruke en ER-modelltilordning av denne typen. I ER-modelltilordningen må du konfigurere en datakilde av typen **Objekt** som refererer til **[QuestionnairesErReportContract](#DataContractClass)**-klassen. Hvis du vil identifisere en modelltilordning, må du angi en datakilde som kaller denne modelltilordningen. I den angitte koden er denne datakilden angitt av **ERModelDataSourceName**-konstanten som har **[modell](#ModelDSName)**-verdien. Hvis du vil identifisere hvilken datakilde som brukes til å eksponere datakontrakten i modelltilordningen, må du angi et datakildenavn. I den angitte koden er dette navnet datakilden angitt av **ParametersDataSourceName**-konstanten som har <a name="DataContractDSName"></a>**RunTimeParameters**-verdien.

> [!NOTE]
> I et nytt miljø må du kanskje oppdatere ER-metadataene, slik at denne typen klasse er tilgjengelig i ER-modelltilordningsutformingen. Hvis du vil ha mer informasjon, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Legge til en rapportkontrollerklasse

Legg til den nye **QuestionnairesErReportController**-klassen i Visual Studio-prosjektet ditt, og skriv kode som kjører et ER-format i enten synkron modus eller satsvis modus, som du foretrekker, i dialogboksen som er bygd basert på logikken til den angitte **QuestionnairesErReportUIBuilder**-klassen.

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Legge til et menyelement

Legg til det nye menyelementet **QuestionnairesErReport** i Visual Studio-prosjektet ditt. I **Objekt**-egenskapen refererer dette menyelementet til **QuestionnairesErReportController**-klassen, og det brukes til å angi en brukertillatelse for å velge og kjøre et ER-format. I **Etikett**-egenskapen refererer dette menyelementet til **\@QuestionnairesReport**-etiketten du opprettet tidligere, slik at riktig tekst vises i appgrensesnittet.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Legge til et menyelement i en meny

Legg til den eksisterende **KM**-menyen i Visual Studio-prosjektet ditt. Du må legge til et nytt **QuestionnairesErReport**-element av typen **Utdata** på denne menyen. Dette elementet må referere til menyelementet **QuestionnairesErReport** som er beskrevet i den forrige delen.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Bygge et Visual Studio-prosjekt

Bygg prosjektet for å gjøre et nytt menyelement tilgjengelig for brukere.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Kjøre et format fra appen

1. Gå til **Spørreskjema** \> **Utforming** \> **Spørreskjemarapport (drevet av ER)**.

    ![Velge menyelementet Spørreskjemarapport (drevet av ER) i Spørreskjema-modulen for å kjøre det konfigurerte ER-formatet](./media/er-quick-start1-application-menu-modified.png)

2. I feltet **Formattilordning** i dialogboksen velger du **Spørreskjemarapport**.
3. Velg **OK**.
4. I dialogboksen **Parametere for elektronisk rapport**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.
5. Velg **OK** for å bekrefte filtreringsalternativet.
6. Velg **OK** for å kjøre rapporten.

    ![Angi utvalgskriteriene i dialogboksen Elektronisk rapport](./media/er-quick-start1-report-run-dialog-page.png)

7. Gå gjennom den genererte rapporten.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Justere en utviklet ER-løsning

Du kan endre den konfigurerte ER-løsningen slik at den bruker dataleverandørklassen du har utviklet, for å få tilgang til detaljer i det kjørende ER-formatet, og slik at den legger inn navnet på dette ER-formatet i en generert rapport.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Endre en modelltilordning

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Legge til datakilder for å få tilgang til et datakontraktobjekt

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjematilordning**.
3. Velg **Utforming** for å åpne siden **Tilordning av modell til datakilde**.
4. Velg **Utforming** for å åpne den valgte tilordningen i modelltilordningsutformingen.
5. På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Dynamics 365 for Operations\\Objekt**.
6. I **Datakilder**-ruten velger du **Legg til rot**.
7. I **Navn**-feltet i dialogboksen skriver du inn **[RunTimeParameters](#DataContractDSName)**, som definert i kildekoden til **QuestionnairesErReportService**-klassen.
8. I **Klasse**-feltet skriver du inn **[QuestionnairesErReportContract](#DataContractClass)**, som ble kodet tidligere.
9. Velg **OK**.
10. Utvid **RunTimeParameters**.

Den tilføyde datakilden inneholder informasjon om post-ID-en for den kjørende ER-formattilordningen.

![Tilføyd datakilde i ER-modelltilordningsutformingen](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Legge til en datakilde for å få tilgang til ER-formattilordningsposter

Fortsett med å redigere den valgte modelltilordningen ved å legge til en datakilde for å få tilgang til ER-formattilordningsposter.

1. På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Dynamics 365 for Operations\\Tabellposter**.
2. I **Datakilder**-ruten velger du **Legg til rot**.
3. Skriv inn **ER1** i **Navn**-feltet i dialogboksen.
4. I **Tabell**-feltet angir du **ERFormatMappingTable**.
5. Velg **OK**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Legge til en datakilde for å få tilgang til en formattilordningspost for et kjørende ER-format

Fortsett med å redigere den valgte modelltilordningen ved å legge til en datakilde for å få tilgang til formattilordningen for det kjørende ER-formatet.

1. På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Funksjoner\\Beregnet felt**.
2. I **Datakilder**-ruten velger du **Legg til rot**.
3. Skriv inn **ER2** i **Navn**-feltet i dialogboksen.
4. Velg **Rediger formel**.
5. I formelredigeringsprogrammet, i **Formel**-feltet, skriver du inn **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.
6. Velg **Lagre**, og lukk formelredigeringsprogrammet.
7. Velg **OK**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Angi navnet på det kjørende ER-formatet i datamodellen

Fortsett med å redigere den valgte modelltilordningen, slik at navnet på det kjørende ER-formatet blir angitt i datamodellen.

1. På siden **Modelltilordningsutforming**, i **Datamodell**-ruten, utvider du **ExecutionContext**, og deretter velger du **ExecutionContext\\FormatName**.
2. I **Datamodell**-ruten velger du **Rediger** for å konfigurere en databinding for feltet til den valgte datamodellen.
3. I formelredigeringsprogrammet, i **Formel**-feltet, skriver du inn **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.
4. Velg **Lagre**, og lukk formelredigeringsprogrammet.

Fordi du brukte **FormatName**-feltet, viser den konfigurerte modelltilordningen nå navnet på et ER-format som kaller opp denne modelltilordningen under utføring.

![Binde datamodellfeltet til metoden for den tilføyde datakilden i ER-modelltilordningsutformingen](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Fullføre utformingen av modelltilordningen

1. Velg **Lagre** på siden **Modelltilordningsutforming**.
2. Lukk siden.
3. Lukk siden Modelltilordninger.
4. I konfigurasjonstreet på **Konfigurasjoner**-siden kontrollerer du at konfigurasjonen **Spørreskjematilordning** fortsatt er valgt. På hurtigfanen **Versjoner** velger du deretter konfigurasjonsversjonen med statusen **Utkast**.
5. Velg **Endre status** \> **Fullført**.

Statusen til versjon 1.2 av denne konfigurasjonen endres fra **Utkast** til **Fullført**. Versjon 1.2 kan ikke lenger endres. Denne versjonen inneholder den konfigurerte modelltilordningen og kan brukes som basis for andre ER-konfigurasjoner. Versjon 1.3 av denne konfigurasjonen opprettes og har statusen **Utkast**. Du kan redigere denne versjonen for å justere **Spørreskjema**-modelltilordningen.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Endre et format

Du kan endre det konfigurerte ER-formatet slik at navnet vises i bunnteksten til en rapport som genereres når ER-formatet kjøres.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Legge til et nytt formatelement

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjemarapport**.
3. Velg **Utforming**.
4. På siden **Formatutforming** velger du rotelementet **Rapport**.
5. Velg **Legg til** for å legge til et nytt nestet formatelement for det valgte **Rapport**-rotelementet.
6. Velg **Excel\\Bunntekst**.
7. Angi **Bunntekst** i **Navn**-feltet.
8. Velg **Rapport\Bunntekst**, og velg deretter **Legg til**.
9. Velg **Tekst\\Streng**.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Binde formatelementet som er lagt til

1. På **Formatutforming**-siden på **Tilordning**-fanen i formattreet for det aktive **Bunntekst\\Streng**-elementet velger du **Rediger formel**.
2. I formelredigeringsprogrammet, i **Formel**-feltet, skriver du inn **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.
3. Velg **Lagre**, og lukk formelredigeringsprogrammet.
4. Velg **Lagre**.

Det konfigurerte formatet er nå endret slik at navnet blir angitt i bunnteksten for en generert rapport ved hjelp av **Bunntekst\\Streng**-elementet.

![Legge til Bunntekst-formatelementet i det konfigurerte formatet i ER-operasjonsutformingen](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Fullføre formatutformingen

1. Lukk **Formatutforming**-siden.
2. I konfigurasjonstreet på **Konfigurasjoner**-siden kontrollerer du at konfigurasjonen **Spørreskjemarapport** fortsatt er valgt. På hurtigfanen **Versjoner** velger du deretter konfigurasjonsversjonen med statusen **Utkast**.
3. Velg **Endre status** \> **Fullført**.

Statusen til versjon 1.2 av denne konfigurasjonen endres fra **Utkast** til **Fullført**. Versjon 1.2 kan ikke lenger endres. Denne versjonen inneholder det konfigurerte formatet og kan brukes som basis for andre ER-konfigurasjoner. Versjon 1.3 av denne konfigurasjonen opprettes og har statusen **Utkast**. Du kan redigere denne versjonen for å justere **Spørreskjema**-rapporten.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Kjøre et format fra appen

1. Gå til **Spørreskjema** \> **Utforming** \> **Spørreskjemarapport (drevet av ER)**.
2. I feltet **Formattilordning** i dialogboksen velger du **Spørreskjemarapport**.
3. Velg **OK**.
4. I dialogboksen **ER-parametere**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.
5. Velg **OK** for å bekrefte filtreringsalternativet.
6. Velg **OK** for å kjøre rapporten.
7. Se gjennom den genererte rapporten i Excel-format.

Legg merke til at bunnteksten i den genererte rapporten inneholder navnet på ER-formatet som ble brukt til å generere den.

![Generert rapport i Excel-format](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Kjøre et format fra ER

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjemarapport**.
3. Velg **Kjør** i handlingsruten.
4. I dialogboksen **Parametere for elektronisk rapport**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.
5. Velg **OK** for å bekrefte filtreringsalternativet.
6. Velg **OK** for å kjøre rapporten.
7. Se gjennom den genererte rapporten i Excel-format.

Legg merke til at bunnteksten i den genererte rapporten ikke inneholder navnet på ER-formatet som ble brukt til å generere den, fordi datakontraktobjektet ikke ble sendt til den kjørende modelltilordningen da den ble kalt med formatet som ble kjørt fra ER.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Konfigurere et formatmål for forhåndsvisning på skjermen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Mål for elektronisk rapportering**.
2. På siden **Mål for elektronisk rapportering** legger du til en målpost for det konfigurerte ER-formatet **Spørreskjema**.
3. På hurtigfanen **Filmål** konfigurerer du **Skjerm**-[målet](er-destination-type-screen.md) for **Rapport**-formatkomponenten som er [lagt til](#AddFormatRootElement) som rotelement for det konfigurerte ER-formatet **Spørreskjemarapport**.
4. På hurtigfanen **PDF-konverteringsinnstillinger** konfigurerer du målet for å konvertere en rapport til [PDF-format](electronic-reporting-destinations.md#OutputConversionToPDF) som bruker sideretningen **Liggende**.

![Konfigurere det egendefinerte Skjerm-målet for ER-formatet på målsiden for elektronisk rapportering](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Kjøre et format fra appen for å forhåndsvise det som et PDF-dokument

1. Gå til **Spørreskjema** \> **Utforming** \> **Spørreskjemarapport (drevet av ER)**.
2. I feltet **Formattilordning** i dialogboksen velger du **Spørreskjemarapport**.
3. Velg **OK**.
4. I dialogboksen **Parametere for elektronisk rapport**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.
5. Velg **OK** for å bekrefte filtreringsalternativet.

    På hurtigfanen **Mål** kan du merke deg at **Utdata**-feltet er angitt til **Skjerm**. Hvis du vil endre det konfigurerte målet, velger du **Endre**.

    ![Dialogboksen for ER-rapportkjøretid, der du kan endre det konfigurerte målet](./media/er-quick-start1-run-settings.png)

6. Velg **OK** for å kjøre rapporten.
7. Se gjennom den genererte rapporten i PDF-format.

    ![Forhåndsvisning på skjermen av den genererte rapporten i PDF-format](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Formelspråk i elektronisk rapportering](er-formula-language.md)
- [Utforme flerspråklige rapporter](er-design-multilingual-reports.md)
- [API for ER-rammeverk](er-apis-app73.md)
- [CASE-funksjonen](er-functions-logical-case.md)
- [CONCATENATE-funksjonen](er-functions-text-concatenate.md)
- [DATETIMEFORMAT-funksjonen](er-functions-datetime-datetimeformat.md)
- [FILTER-funksjonen](er-functions-list-filter.md)
- [FIRSTORNULL-funksjonen](er-functions-list-firstornull.md)
- [FORMAT-funksjonen](er-functions-text-format.md)
- [IF-funksjonen](er-functions-logical-if.md)
- [ORDERBY-funksjonen](er-functions-list-orderby.md)
- [SESSIONNOW-funksjonen](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
