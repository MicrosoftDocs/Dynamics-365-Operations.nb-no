---
title: Legge til analyse i arbeidsområder ved hjelp av Power BI Embedded
description: Dette emnet forklarer hvordan du bygger inn en Power BI-rapport i kategorien Analyse i et arbeidsområde.
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 1a357c4623f4f9dc441fe328ec0d5481c14ae4af
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771639"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Legge til analyse i arbeidsområder ved hjelp av Power BI Embedded

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Denne funksjonen støttes i Finance and Operations (versjon 7.2 og nyere).

## <a name="introduction"></a>Innledning
Dette emnet forklarer hvordan du bygger inn en Microsoft Power BI-rapport i kategorien **Analyse** i et arbeidsområde. For eksempelet som er angitt her, vil vi utvide arbeidsområdet **Reservasjonsbehandling** i programmet Fleet Management til å bygge inn et analytisk arbeidsområde på en **Analyse**-kategori.

## <a name="prerequisites"></a>Forutsetninger
+ Tilgang til et utviklermiljø som kjører plattformoppdatering 8 eller senere.
+ En analytisk rapport (.pbix-fil) som ble opprettet ved hjelp av Microsoft Power BI Desktop, og som har en datamodell som har Enhetslager-databasen som kilde.

## <a name="overview"></a>Oversikt
Enten du utvider et eksisterende arbeidsområde for programmet eller introdusere et nytt arbeidsområde på egen hånd, kan du bruke innebygde analytiske visninger for å levere innsiktsfulle og interaktive visninger av forretningsdataene. Prosessen for å legge til en analytisk arbeidsområdet kategori har fire trinn.

1. Legge til en .pbix-fil som en ressurs for Dynamics 365.
2. Definer en analytisk arbeidsområdet-kategorien.
3. Bygge inn ressursen .pbix i kategorien arbeidsområde.
4. Valgfritt: Legg til filtyper hvis du vil tilpasse visningen.

> [!NOTE]
> Hvis du vil ha mer informasjon om hvordan du oppretter analyserapporter, se [Komme i gang med Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/). Denne siden er en god kilde for innsikt som kan hjelpe deg med å opprette overbevisende analytiske rapporteringsløsninger.

## <a name="add-a-pbix-file-as-a-resource"></a>Legge til en .pbix-fil som en ressurs
Før du begynner, må du opprette eller få tak i Power BI-rapporten som du vil bygge inn i arbeidsområdet. Hvis du vil ha mer informasjon om hvordan du oppretter analyserapporter, se [Komme i gang med Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).

Følg denne fremgangsmåten for å legge til en .pbix-fil som en artefakt i et Visual Studio-prosjekt.

1. Opprett et nytt prosjekt i den aktuelle modellen.
2. Velg prosjektet i Solution Explorer, høyreklikk, og velg deretter **Legg til** \> **Nytt element**.
3. I dialogboksen **Legg til nytt element** under **Operations-artefakter** velger du **Ressurs**-malen.
4. Angi et navn som skal brukes til å referere til rapporten i X++-metadataene, og klikk deretter **Legg til**.

    ![Dialogboksen Legg til nytt element](media/analytical-workspace-add.png)

5. Finn .pbix-filen som inneholder definisjonen av den analytiske rapporten, og klikk deretter **Åpne**.

    ![Velge en Ressursfil-dialogboks](media/analytical-workspace-select-resource.png)

Nå som du har lagt til .pbix-filen som en Dynamics 365-ressurs, kan du bygge inn rapportene i arbeidsområder og legge til direkte koblinger ved å bruke menyelementer.

## <a name="add-a-tab-control-to-an-application-workspace"></a>Legge til en kategorikontroll i et arbeidsområde for program
I dette eksemplet vil vi utvide arbeidsområdet **Reservasjonsbehandling** i Fleet Management-modellen ved å legge til **Analyse**-kategorien med definisjonen av **FMClerkWorkspace**-skjemaet.

Illustrasjonen nedenfor viser hvordan **FMClerkWorkspace**-skjemaet ser ut i utformingen i Microsoft Visual Studio.

![FMClerkWorkspace-skjemaet før endringer](media/analytical-workspace-definition-before.png)

Følg denne fremgangsmåten for å utvide skjemadefinisjonen for den **Reservasjonsbehandling**-arbeidsområdet.

1. Åpne skjemautformingen for å utvide definisjonen av utformingen.
2. I designdefinisjonen velger du det øverste elementet som heter **Design | Pattern: Workspace Operational**.
3. Høyreklikk, og velg deretter **Ny** \> **Kategori** for å legge til en ny kontroll som heter **FormTabControl1**.
4. Velg **FormTabControl1** i skjemautformingen.
5. Høyreklikk, og velg deretter **Ny kategoriside** for å legge til en ny kategoriside.
6. Endre navnet på kategorisiden til noe som gir mening, som **Arbeidsområde**.
7. Velg **FormTabControl1** i skjemautformingen.
8. Høyreklikk, og velg deretter **Ny kategoriside**.
9. Endre navnet på kategorisiden til noe som gir mening, som **Analyse**.
10. I skjemautformingen velger du **Analyse (kategoriside)**.
11. Angi **Tekst**-egenskapen til **Analyse**.
12. Høyreklikk kontrollen, og velg deretter **Ny** \> **Gruppe** for å legge til en ny skjemagruppekontroll.
13. Endre navnet på skjemagruppen til noe som gir mening, som **powerBIReportGroup**.
14. I skjemautformingen velger du **PanoramaBody (kategori)**, og dra deretter kontrollen til **Arbeidsområde**-kategorien.
15. I designdefinisjonen velger du det øverste elementet som heter **Design | Pattern: Workspace Operational**.
16. Høyreklikk, og velg deretter **Fjern mønster**.
17. Høyreklikk på nytt, og velg deretter **Legg til mønster** \> **Arbeidsområde med kategorier**.
18. Utfør et bygg for å bekrefte endringene.

Illustrasjonen nedenfor viser hvordan utformingen ser ut etter at endringene er brukt.

![FMClerkWorkspace etter endringer](media/analytical-workspace-definition-after.png)

Nå som du har lagt til skjemakontrollene som skal brukes til å bygge inn arbeidsområderapporten, må du definere størrelsen på den overordnede kontrollen, slik at den passer for oppsettet. Som standard er både **filterrutesiden** og **kategorisiden** synlig i rapporten. Du kan imidlertid endre synligheten for disse kontrollene etter behov for rapportens målbruker.

> [!NOTE]
> For innebygde arbeidsområder anbefaler vi at du bruker tilleggene for å skjule både **filtreringsruten** og **kategorisidene**, for konsekvens.

Du har nå fullført oppgaven for å utvide programskjemadefinisjonen. Hvis du vil ha mer informasjon om hvordan du bruker tillegg til å gjøre tilpasninger, se [Tilpasse via utvidelse og overlag](../extensibility/customization-overlayering-extensions.md).

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a>Legge til X ++-forretningslogikk for å bygge inn en visningskontroll
Gjør følgende for å legge til forretningslogikk som initialiserer rapportvisningskontrollen som er innebygd i arbeidsområdet **Reservasjonsbehandling**.

1. Åpne **FMClerkWorkspace**-skjemautformingen for å utvide definisjonen av utformingen.
2. Trykk F7 for å få tilgang til koden bak kodedefinisjonen.
3. Legg til følgende X++-kode

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Utfør et bygg for å bekrefte endringene.

Du har nå fullført oppgaven med å legge til forretningslogikk for å initialisere den innebygde rapportvisningskontrollen. Illustrasjonen nedenfor viser hvordan arbeidsområdet ser ut etter at endringene er brukt.

![Rapport som er innebygd i arbeidsområdet](media/analytical-workspace-final.png)

> [!NOTE]
> Du kan få tilgang til den eksisterende operasjonelle visningen ved hjelp av arbeidsområde-kategoriene under sidetittelen.

## <a name="reference"></a>Referanse

### <a name="pbireporthelperinitializereportcontrol-method"></a>PBIReportHelper.initializeReportControl-metoden
Denne delen gir informasjon om hjelpeklassen som brukes til å bygge inn en Power BI-rapport (.pbix-ressurs) i en skjemagruppekontroll.

#### <a name="syntax"></a>Syntaks
```
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a>Parametere

| Navn             | beskrivelse                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| resourceName     | Navnet på .pbix-ressursen.                                                                              |
| formGroupControl | Skjemagruppekontrollen der Power BI-rapporten skal brukes.                                              |
| defaultPageName  | Standard sidenavn.                                                                                       |
| showFilterPane   | En boolsk verdi som angir om filtreringsruten skal vises (**true**) eller skjules (**false**).     |
| showNavPane      | En boolsk verdi som angir om navigasjonsruten skal vises (**true**) eller skjules (**false**). |
| defaultFilters   | Standardfiltrene for Power BI-rapporten.                                                                 |
