---
title: Grensesnitt for Rapportutforming
description: Denne artikkelen beskriver hvordan du navigerer gjennom Rapportutforming og hvordan du bruker de forskjellige alternativene som oppfyller dine spesifikke behov.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e9b77e2b510a72d1e3fe3c68c997d58245a86a27
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "368036"
---
# <a name="report-designer-interface"></a>Grensesnitt for Rapportutforming

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du navigerer gjennom Rapportutforming og hvordan du bruker de forskjellige alternativene som oppfyller dine spesifikke behov.

## <a name="report-designer-menu-commands"></a>Menykommandoer for Rapportutforming

Tabellen nedenfor beskriver menykommandoer og alternativer som du kan bruke når du utformer finansrapporter. Noen menykommandoer og alternativer er bare tilgjengelige i spesielle tilfeller. Kommandoene for forfremmelse og degradering av rapporteringsenheter er for eksempel bare tilgjengelige når du endrer en rapporteringstredefinisjon.

### <a name="file-menu"></a>Fil-menyen

**Fil**-menyen er tilgjengelig for alle brukere, og den inneholder kommandoene nedenfor.

| Kommando                           | Beskrivelse |
|-----------------------------------|-------------|
| Nye                               | Opprett en ny rapportdefinisjon, raddefinisjon, kolonnedefinisjon, rapporteringstredefinisjon, rapportdefinisjon for gruppe eller mappe. Flere alternativer er tilgjengelige, avhengig av brukerrollen din. |
| Åpen                              | Åpne en eksisterende raddefinisjon, kolonnedefinisjon, rapporteringstredefinisjon eller rapportdefinisjon. |
| Lukk                             | Lukk gjeldende byggeblokk. |
| Lukk alle                         | Lukk alle byggeblokker. |
| Lagre                              | Lagre gjeldende raddefinisjon, kolonnedefinisjon, rapporteringstredefinisjon eller rapportdefinisjon. |
| Lagre som                           | Lagre gjeldende raddefinisjon, kolonnedefinisjon, rapporteringstredefinisjon eller rapportdefinisjon med et nytt navn. |
| Egenskaper                        | Åpne dialogboksen **Egenskaper** der du kan endre navnet og beskrivelsen for en rapport. |
| Generer                          | Generer gjeldende rapport. Denne kommandoen er tilgjengelig fra en rapportdefinisjon. |
| Vis rapport                       | Åpne den nyeste versjonen av den genererte rapporten i Finance and Operations. Denne kommandoen er tilgjengelig fra en rapportdefinisjon hvis du har generert minst én rapport. |
| Sist brukte rapportdefinisjoner         | Vis en liste over rapporter som nylig er opprettet eller endret. Du kan deretter velge en rapport i listen. |
| Sist brukte raddefinisjoner            | Vis en liste over raddefinisjoner som nylig er opprettet eller endret. Du kan deretter velge en raddefinisjon i listen. |
| Sist brukte kolonnedefinisjoner         | Vis en liste over kolonnedefinisjoner som nylig er opprettet eller endret. Du kan deretter velge en kolonnedefinisjon i listen. |
| Sist brukte rapporteringstredefinisjoner | Vis en liste over rapporteringstredefinisjoner som nylig er opprettet eller endret. Du kan deretter velge en rapporteringstredefinisjon i listen. |
| Avslutt                              | Avslutt Rapportutforming. |

### <a name="edit-menu"></a>Rediger-menyen

**Rediger**-menyen er tilgjengelig for brukere som har **Utformer**- eller **Administrator**-rollen. Denne menyen inneholder følgende kommandoer:

| Kommando                                | Beskrivelse |
|----------------------------------------|-------------|
| Angre                                   | Angre den siste handlingen. |
| Gjør om                                   | Gjør om den siste angrehandlingen. |
| Klipp ut                                    | Slett den valgte teksten, og kopier den til utklippstavlen |
| Kopier                                   | Kopier den valgte teksten til utklippstavlen. |
| Lim inn                                  | Sette inn siste utklipp eller kopierte tekst fra utklippstavlen. |
| Fjern                                  | Slett innholdet i den valgte byggeblokkcellen. |
| Søk etter                                   | Åpne dialogboksen **Søk og erstatt** der du kan søke etter tekst i visningsruten. |
| Erstatt                                | Åpne dialogboksen **Søk og erstatt** der du kan søke etter og erstatte tekst i visningsruten. |
| Sette inn rader fra dimensjoner            | Åpne dialogboksen **Sett inn rader fra dimensjoner** der du kan velge dimensjonsverdier som skal tas med i raddefinisjonen. Denne kommandoen er tilgjengelig fra en raddefinisjon. |
| Nummerer rader                          | Nummerer alle numeriske radkoder. Denne kommandoen er tilgjengelig fra en raddefinisjon. |
| Radkoblinger                              | Åpne dialogboksen **Radkoblinger** der du kan angi kildene for datakoblinger i raddefinisjoner og rapporteringstredefinisjoner. Denne kommandoen er tilgjengelig fra en raddefinisjon. |
| Avrundingsjustering                    | Åpne dialogboksen **Avrundingsjusteringer** der du kan angi parameterne for avrunding. Denne kommandoen er tilgjengelig fra en raddefinisjon. |
| Behandle dimensjonssett                  | Åpne dialogboksen **Dimensjonssett** der du kan opprette og endre dimensjonssett. Denne kommandoen er tilgjengelig fra en raddefinisjon eller rapporteringstredefinisjon. |
| Sett inn rad                             | Sette inn en tom rad i raddefinisjon eller en tom overskriftsrad i kolonnedefinisjonen. Denne kommandoen er tilgjengelig fra en rad- eller kolonnedefinisjon. |
| Slett rad                             | Slett den valgte raden fra raddefinisjonen eller den valgte overskriftsraden fra kolonnedefinisjonen. Denne kommandoen er tilgjengelig fra en rad- eller kolonnedefinisjon. |
| Sett inn kolonne                          | Sette inn en tom kolonne i kolonnedefinisjonen. Denne kommandoen er tilgjengelig fra en kolonnedefinisjon. |
| Slett kolonne                          | Slett den valgte kolonnen fra kolonnedefinisjonen. Denne kommandoen er tilgjengelig fra en kolonnedefinisjon. |
| Sette inn rapporteringsenheter fra dimensjoner | Åpne dialogboksen **Rapporteringsenheter fra dimensjoner** der du kan velge dimensjonsverdier som skal tas med i rapporteringstredefinisjonen. Denne kommandoen er tilgjengelig fra en rapporteringstredefinisjon. |
| Importer dimensjonssetthierarki         | Åpne dialogboksen **Dimensjonssetthierarki** der du kan importere et dimensjonssetthierarki fra de økonomiske dataene. Denne kommandoen er tilgjengelig fra en ..\\financial-dimensions\\dimension-based system. |
| Sett inn rapporteringsenhet                  | Sette inn en tom rad i rapporteringstredefinisjonen. Denne kommandoen er tilgjengelig fra en rapporteringstredefinisjon. |
| Slett rapporteringsenhet                  | Slett den merkede raden for rapporteringsenhet fra rapporteringstredefinisjonen. Denne kommandoen er tilgjengelig fra en rapporteringstredefinisjon. |

### <a name="view-menu"></a>Vis-menyen

**Vis**-menyen er tilgjengelig for alle brukere, og den inneholder kommandoene nedenfor.

| Kommando         | Beskrivelse                                                            |
|-----------------|------------------------------------------------------------------------|
| Navigasjonsruten | Vise eller skjule navigasjonsruten.                                      |
| Verktøylinjer        | Velg verktøylinjene som vises.                                  |
| Statuslinje      | Vis eller skjul statusinformasjonen i vinduet **Rapportutforming**. |
| Velkomstside    | Åpne **velkomstsiden**.                                             |

### <a name="format-menu"></a>Format-menyen

**Format**-menyen er tilgjengelig for brukere som har **Utformer**- eller **Administrator**-rollen. Denne menyen inneholder følgende kommandoer:

| Kommando               | Beskrivelse |
|-----------------------|-------------|
| Stiler og formatering | Åpne dialogboksen **Stiler og formatering** der du kan opprette og endre stilen for tekst i raddefinisjoner og kolonnedefinisjoner. Denne kommandoen er tilgjengelig fra en rad- eller kolonnedefinisjon. |
| Kolonnebredde          | Åpne dialogboksen **Kolonnebredde** der du kan angi bredden på den valgte kolonnen. Denne kommandoen er tilgjengelig fra en raddefinisjon, kolonnedefinisjon eller rapporteringstredefinisjon. |
| Skjul                  | Skjul den merkede kolonnen. Denne kommandoen er tilgjengelig fra en raddefinisjon, kolonnedefinisjon eller rapporteringstredefinisjon. |
| Vis                | Vis de skjulte kolonnene mellom de merkede kolonnene. Denne kommandoen er tilgjengelig fra en raddefinisjon, kolonnedefinisjon eller rapporteringstredefinisjon. |

### <a name="company-menu"></a>Firma-menyen

**Firma**-menyen er tilgjengelig for brukere som har **Utformer**- eller **Administrator**-rollen. Denne menyen inneholder følgende kommandoer:

| Kommando               | Beskrivelse                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Firmaer             | Åpne dialogboksen **Firmaer** der du kan opprette og endre firmaer.                                          |
| Byggeblokkgrupper | Åpne dialogboksen **Byggeblokkgrupper** der du kan opprette, endre, importere og eksportere byggeblokkgrupper. |

### <a name="go-menu"></a>Start-menyen

**Start**-menyen er tilgjengelig for alle brukere og inneholder følgende kommandoer.

> [!NOTE]
> Disse har ingen synlig effekt hvis navigasjonsruten ikke vises.

| Kommandoer                   | Beskrivelse                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Rapportdefinisjoner         | Vis rapportdefinisjoner i navigasjonsruten.                                    |
| Raddefinisjoner            | Vis raddefinisjoner i navigasjonsruten.                                       |
| Kolonnedefinisjoner         | Vis kolonnedefinisjoner i navigasjonsruten.                                    |
| Rapporteringstredefinisjoner | Vis rapporteringstredefinisjoner i navigasjonsruten.                            |
| Sikkerhet                   | Vis sikkerhetsinformasjon for brukere, grupper og firmaer i navigasjonsruten. |

### <a name="tools-menu"></a>Verktøy-menyen

**Verktøy**-menyen er tilgjengelige for alle brukere, men enkelte kommandoer har begrenset tilgjengelighet. Denne menyen inneholder følgende kommandoer:

| Kommando                       | Beskrivelse |
|-------------------------------|-------------|
| Beskytt                       | Angi et passord for gjeldende byggeblokk. Denne kommandoen er tilgjengelig for brukere som har **Utformer**- eller **Administrator**-rollen. |
| Status for rapportkø           | Åpne dialogboksen **Status for rapportkø** der du kan se alle sist genererte rapporter og detaljene for hver rapport. |
| Informasjon om kildesystem     | Vis innstillingene for Microsoft Dynamics ERP-systemet. Denne kommandoen er tilgjengelig for brukere som har **Utformer**- eller **Administrator**-rollen. |
| Utsjekkede elementer             | Vis raddefinisjoner, kolonnedefinisjoner rapporteringstredefinisjoner og rapportdefinisjoner som er åpne. Denne kommandoen er tilgjengelig for brukere som har **Utformer**- eller **Administrator**-rollen. |
| Oppdater hurtigbufrede økonomiske data | Oppdater dataene i kolonnen finansdimensjoner. |
| Opsjoner                       | Åpne dialogboksen **Alternativer** der du kan endre brukerinnstillingene for Rapportutforming. |

### <a name="window-menu"></a>Vindu-menyen

**Vindu**-menyen er tilgjengelig for alle brukere, og den inneholder kommandoene nedenfor.

| Kommando              | Beskrivelse |
|----------------------|-------------|
| Side ved side vannrett    | Vis alle åpne vinduer ved siden av hverandre. |
| Side ved side loddrett      | Vis alle åpne vinduer over hverandre. |
| Overlappende              | Plasser alle åpne vinduer lagvis, slik at tittellinjen på hvert vindu vises. |
| Frys vannrett    | Frys den merkede raden, slik at når du blar, vises denne raden fortsatt i vinduet. Denne kommandoen er tilgjengelig for brukere som har **Utformer**- eller **Administrator**-rollen. |
| Frys loddrett      | Frys den merkede kolonnen, slik at når du blar, vises denne kolonnen fortsatt i vinduet. Denne kommandoen er tilgjengelig for brukere som har **Utformer**- eller **Administrator**-rollen. |
| Liste over åpne vinduer | Vis en liste over vinduer som er åpne. Velg et vindu for å flytte det fremst. |

### <a name="help-menu"></a>Hjelp-menyen

**Hjelp**-menyen er tilgjengelig for alle brukere, og den inneholder kommandoene nedenfor.

| Kommando | beskrivelse                                                              |
|---------|--------------------------------------------------------------------------|
| Hjelp    | Åpne emnesiden for hjelp for Finance and Operations for finansrapportering. |
|         |                                                                          |

## <a name="report-designer-toolbar-buttons"></a>Verktøylinjeknapper for Rapportutforming
Tabellen nedenfor beskriver knappene på verktøylinjen som du kan bruke når du utformer rapporter. Noen verktøylinjeknapper er bare tilgjengelige i spesielle tilfeller. Knappene for forfremmelse og degradering av rapporteringsenheter er for eksempel bare tilgjengelige når du endrer en rapporteringstredefinisjon.

### <a name="standard-toolbar"></a>Standardverktøylinjen

Standardverktøylinjen gir rask tilgang til filen og redigeringskommandoer. Denne verktøylinjen inneholder knappene nedenfor.

| Knapp                                                                                       | Beskrivelse |
|----------------------------------------------------------------------------------------------|-------------|
| [![Ny-knappen](./media/rowc130389.png)](./media/rowc130389.png)                              | Opprett en ny (tom) rapportdefinisjon, raddefinisjon, kolonnedefinisjon eller rapporteringstredefinisjon. |
| [![Åpne-knappen](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Åpne en eksisterende raddefinisjon, kolonnedefinisjon, rapporteringstredefinisjon eller rapportdefinisjon. |
| [![Lagre-knappen](./media/savec130389.png)](./media/savec130389.png)                           | Lagre gjeldende raddefinisjon, kolonnedefinisjon, rapporteringstredefinisjon eller rapportdefinisjon. |
| [![Kopier-knappen](./media/copyc130389.png)](./media/copyc130389.png)                           | Kopier den valgte teksten til utklippstavlen. |
| [![Klipp ut-knappen](./media/cutc130389.png)](./media/cutc130389.png)                              | Slett den valgte teksten, og kopier den til utklippstavlen |
| [![Lim inn-knappen](./media/pastec130389.png)](./media/pastec130389.png)                        | Sett inn tekst fra utklippstavlen. |
| [![Angre-knappen](./media/undoc130389.png)](./media/undoc130389.png)                           | Angre den siste handlingen. |
| [![Gjør om-knappen](./media/redoc130389.png)](./media/redoc130389.png)                           | Gjør om den siste angrehandlingen. |
| [![Søk-knappen](./media/findc130389.png)](./media/findc130389.png)                           | Åpne dialogboksen **Søk og erstatt** der du kan søke etter og erstatte tekst i det aktive vinduet. |
| [![Sett inn rad-knappen](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Sette inn en tom rad i raddefinisjon eller en tom overskriftsrad i kolonnedefinisjonen. Denne knappen er tilgjengelig fra en rad- eller kolonnedefinisjon. |
| [![Sett inn kolonne-knappen](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Sette inn en tom kolonne i kolonnedefinisjonen. Denne knappen er tilgjengelig fra en kolonnedefinisjon. |
| [![Lås-knappen](./media/lockc130389.png)](./media/lockc130389.png)                           | Angi et passord for gjeldende byggeblokk. Denne knappen er tilgjengelig for brukere som har **Utformer**- eller **Administrator**-rollen. |
| [![Radkobling-knappen](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Åpne dialogboksen **Radkoblinger** der du kan angi kildene for datakoblinger i raddefinisjoner og rapporteringstredefinisjoner. Denne knappen er tilgjengelig fra en raddefinisjon. |
| [![Forfrem-knappen](./media/promotec130389.png)](./media/promotec130389.png)                  | Forfremme en enhet i rapporteringstredefinisjonen. Når du velger en underordnet enhet og deretter klikker **Forfrem**, flyttes den underordnede enheten til samme nivå som den overordnede enheten. |
| [![Senk-knappen](./media/demotec130389.png)](./media/demotec130389.png)                     | Senk en enhet i rapporteringstredefinisjonen. Når du velger en enhet og deretter klikker **Senk**, blir enheten en underordnet av den foregående enheten. |
| [![Vis-knappen](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Vis alle enheter i rapporteringstredefinisjonen på nivået til den valgte enheten. |
| [![Skjul-knappen](./media/collapsec130389.png)](./media/collapsec130389.png)               | Skjul rapporteringstreet. |
| [![Hjelp-knappen](./media/helpc130389.png)](./media/helpc130389.png)                           | Åpne Hjelp. |

### <a name="formatting-toolbar"></a>Formateringsverktøylinjen

Formateringsverktøylinjen gir enkel tilgang til kommandoer for stil. Denne verktøylinjen inneholder knappene nedenfor.

| Knapp                                                                                                       | Beskrivelse                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Skriftstil-knappen](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Bruke den valgte skriftstilen på gjeldende tekst.      |
| [![Skrift-knappen](./media/fonttype.png)](./media/fonttype.png)                                                 | Bruk den valgte skriften for gjeldende tekst.              |
| [![Skriftstørrelse-knappen](./media/fontsize.png)](./media/fontsize.png)                                            | Bruk den valgte skriftstørrelsen (i punkter) for gjeldende tekst. |
| [![Fet-knappen](./media/boldc130389.png)](./media/boldc130389.png)                                           | Gjør gjeldende tekst fet.                             |
| [![Kursiv-knappen](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Gjør gjeldende tekst kursiv.                           |
| [![Understrek-knappen](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Gjør gjeldende tekst understreket.                             |
| [![Reduser innrykk-knappen](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Reduser innrykket for gjeldende tekst.                |
| [![Øk innrykk-knappen](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Øk innrykket for gjeldende tekst.                |
| [![Bakgrunnsfarge-knappen](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Endre bakgrunnsfargen for gjeldende celle.        |
| [![Skriftfarge-knappen](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Endre fargen for gjeldende tekst.                   |

### <a name="report-designer-toolbar"></a>Verktøylinje for Rapportutforming

Verktøylinjen for rapportutformingen gir rask tilgang til kommandoer for å navigere i rapportutformingen. Denne verktøylinjen inneholder knappene nedenfor.

| Knapp                                                                                              | Beskrivelse |
|-----------------------------------------------------------------------------------------------------|-------------|
| [![Rapportdefinisjon-knappen](./media/reportc130389.png)](./media/reportc130389.png)                 | Vis rapportdefinisjon som vises på **Vindu**-menyen. |
| [![Raddefinisjon-knappen](./media/rowc130389.png)](./media/rowc130389.png)                          | Vis raddefinisjonen som er tilordnet den aktive rapportdefinisjonen. |
| [![Kolonnedefinisjon-knappen](./media/columnc130389.png)](./media/columnc130389.png)                 | Vis kolonnedefinisjonen som er tilordnet den aktive rapportdefinisjonen. |
| [![Rapporteringstredefinisjon-knappen](./media/treec130389.png)](./media/treec130389.png)             | Vis rapporteringstredefinisjonen som er tilordnet den aktive rapportdefinisjonen. |
| [![Rapportvisning-knappen](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Start Rapportvisning, og vis den nyeste versjonen av den genererte rapporten. Denne knappen er tilgjengelig fra en rapportdefinisjon hvis du har generert minst én rapport. |
| [![Generer rapport-knappen](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Genererer en rapport fra den aktive rapportdefinisjonen. Denne knappen er tilgjengelig fra en rapportdefinisjon. |

## <a name="additional-resources"></a>Tilleggsressurser

[Finansrapportering](financial-reporting-intro.md)

[Generere en finansrapport](generate-financial-report.md)
