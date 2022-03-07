---
title: Spore genererte rapportresultater og sammenligne dem med basisverdier
description: Dette emnet forklarer hvordan du kan sammenligne resultatene av genererte ER-rapporter (elektronisk rapportering) med basisrapportverdier.
author: NickSelin
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 9fabdef96b02747c84a76bf42997633842f185e9
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605211"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Spore genererte rapportresultater og sammenligne dem med basisverdier

[!include[banner](../includes/banner.md)]

Du kan spore resultatene av ER-formater (elektronisk rapportering) som genererer utgående elektroniske dokumenter. Når sporingsgenerering er aktivert (ved hjelp av ER-brukerparameteren **Kjør i feilsøkingsmodus**), genereres en ny sporingspost i ER-formatkjøringsloggen hver gang en ER-rapport kjøres. Følgende detaljer er lagret i hvert spor som er generert:

- Alle advarsler som ble generert av valideringsregler
- Alle feil som ble generert av valideringsregler
- Alle genererte filer som lagres som vedlegg i oppføringensposten

Du kan lagre individuelle basisprogramfiler for et hvilket som helst ER-format. Filer regnes som grunnlinjefiler når de beskriver de forventede resultatene av rapporter som kjøres. Hvis en grunnlinjefil er tilgjengelig for et ER-format som kjøres mens sporingsgenerering er aktivert, lagrer sporingen, i tillegg til detaljene som ble nevnt tidligere, resultatet av sammenligningen av det genererte elektroniske dokumentet med grunnlinjefilen. Med ett klikk finner du også det genererte elektroniske dokumentet og grunnlinjefilen i en enkelt zip-fil. Deretter kan du foreta detaljert sammenligning ved hjelp av et eksterne verktøy, for eksempel WinDiff.

Du kan vurdere sporingen for å analysere om de elektroniske dokumentene som genereres, inkluderer det forventede innholdet. Du kan gjøre denne evalueringen i en testemiljø for brukeraksept (UAT) når kodegrunnlaget endres (for eksempel når du overførte til en ny forekomst av programmet, installerte hurtigreparasjonspakker eller distribuerte endringer i koden). På denne måten kan du kontrollere at evalueringen ikke påvirker utførelsen av ER-rapporter som brukes. For mange ER-rapporter kan du gjøre evalueringen i uovervåket modus.

Hvis du vil vite mer om denne funksjonen, kan du spille av oppgaveveiledningene **ER Generere rapporter og sammenligne resultater (del 1)** og **ER Generere rapporter og sammenligne resultater (del 2)**, som er del av forretningsprosessen **7.5.4.3 Teste IT-tjenester/-løsninger (10679)** og kan lastes ned fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Disse oppgaveveiledningene forklarer deg hvordan du konfigurere ER-rammeverket for å bruke grunnlinjefiler for å evaluere genererte elektroniske dokumenter.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Eksempel: Spore genererte rapportresultater og sammenligne dem med grunnlinjeverdier

Denne fremgangsmåten forklarer hvordan du konfigurerer ER-rammeverket for å samle inn informasjon om ER-formatutførelser, og deretter evaluerer resultatene av disse utførelsene. Som en del av denne evalueringen sammenlignes genererte dokumenter med grunnlinjefilene. I dette eksemplet skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet Litware, Inc. Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle tilordnet. Disse trinnene kan fullføres ved hjelp av et hvilket som helst datasett.

For å kunne fullføre trinnene i dette eksemplet må du først fullføre trinnene i fremgangsmåten [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. I delen **Konfigurasjonsleverandører** på siden **Lokaliseringskonfigurasjoner** kontrollerer du at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er oppført og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, følger du trinnene i [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-document-management-parameters"></a>Konfigurere parametere for dokumentstyring

1. Gå til **Organisasjonsstyring** \> **Dokumentstyring** \> **Dokumenttyper**, og opprett en ny dokumenttype for å lagre grunnlinjefiler.
2. I **Klasse**-feltet angir du **Tilknytt fil**.
3. I **Gruppe**-feltet angir du **Fil**.

![Siden Dokumenttyper.](media/GER-BaselineSample-SetupDocumentType.PNG "Skjermbilde av siden Dokumenttyper")

> [!NOTE]
> Du må konfigurere en ny dokumenttype som har det samme navnet, for hvert datasett der du planlegger å bruke ER-grunnlinjefunksjonen.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>Konfigurere ER-parametere for å begynne å bruke grunnlinjefunksjonen

1. I delen **Relaterte koblinger** i arbeidsområdet **Elektronisk rapportering** velger du **Parametere for elektronisk rapportering**.

    ![Arbeidsområdet Elektronisk rapportering.](media/GER-BaselineSample-ERWorkspace.PNG "Skjermbilde av siden arbeidsområdet Elektronisk rapportering")

2. I **Grunnlinje**-feltet i **Vedlegg**-fanen angir eller velger du dokumenttypen du nettopp opprettet.

    ![Vedlegg-kategorien på siden Parametere for elektronisk rapportering.](media/GER-BaselineSample-ERParameters.PNG "Skjermbilde av siden Parametere for elektronisk rapportering")

3. Velg **Lagre**, og lukk deretter siden **Parametere for elektronisk rapportering**.

### <a name="add-a-new-er-model-configuration"></a>Legg til en ny ER-konfigurasjon

1. I delen **Konfigurasjoner** i arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.
2. Velg **Opprett konfigurasjon** i handlingsruten.
3. Skriv inn **Modell for å lære ER-grunnlinjer** i **Navn**-feltet i rullegardinboksen.
4. Velg **Opprett konfigurasjon** for å bekrefte opprettelsen av en ny ER-datamodelloppføring.

![Opprett konfigurasjon-dialogboksen, legg til en ny ER-modellkonfigurasjon.](media/GER-BaselineSample-ModelAdd.PNG "Skjermbilde av Rullegardinlisten Opprett konfigurasjon")

### <a name="design-a-data-model"></a>Utforme en datamodell

1. Velg **Utforming** i handlingsruten på siden **Konfigurasjoner**.
2. Velg **Ny**.
3. Skriv inn **Rot** i **Navn**-feltet i rullegardinboksen.
4. Velg **Legg til**.
5. Velg **Rotreferanse**.
6. Velg **OK**, og velg deretter **Lagre**.
7. Lukk siden **Modellutforming**.
8. Velg **Endre status**.
9. Velg **Fullfør**, og velg deretter **OK**.

![Siden Konfigurasjoner.](media/GER-BaselineSample-ModelComplete.PNG "Skjermbilde av Konfigurasjoner-siden")

### <a name="add-a-new-er-format-configuration"></a>Legg til en ny ER-formatkonfigurasjon

1. Velg **Opprett konfigurasjon** i handlingsruten på siden **Konfigurasjoner**.
2. I feltgruppen **Ny** i rullegardinboksen velger du alternativet **Format basert på datamodellen Modell for å lære ER-grunnlinjer**.
3. I **Navn**-feltet angir du **Format for å lære ER-grunnlinjer**.
4. Velg **Opprett konfigurasjon** for å bekrefte opprettelsen av en ny ER-formatoppføring.

![Opprett konfigurasjon-dialogboksen, legg til en ny ER-formatkonfigurasjon.](media/GER-BaselineSample-FormatAdd.PNG "Skjermbilde av Rullegardinlisten Opprett konfigurasjon")

### <a name="design-a-format"></a>Utforme et format

I dette eksemplet skal du opprette et enkelt ER-format for å generere XML-dokumenter.

1. Velg **Utforming** i handlingsruten på siden **Konfigurasjoner**.
2. Velg **Legg til rot**.
3. Følg disse trinnene i rullegardinboksen:

    1. Velg **Felles\\Fil** i treet.
    2. Angi **Utdata** i **Navn**-feltet.
    3. Velg **OK**.

4. Velg **Legg til**.
5. Følg disse trinnene i rullegardinboksen:

    1. Velg **XML\\Element** i treet.
    2. Angi **Dokument** i **Navn**-feltet.
    3. Velg **OK**.

6. Velg **Utdata\\Dokument** i treet.
7. Velg **Legg til**.
8. Følg disse trinnene i rullegardinboksen:

    1. Velg **XML\\Attributt** i treet.
    2. Angi **ID** i **Navn**-feltet.
    3. Velg **OK**.

    ![Formatutformingsside, XML-attributt valgt i tre.](media/GER-BaselineSample-FormatLayoutDesign.PNG "Skjermbilde av siden Formatutforming")

9. Velg **Slett** i **Tilordning**-fanen.
10. Velg **Legg til rot**.
11. Velg **Generelt\\Brukerinndataparametere** i treet i rullegardinboksen, og følg deretter disse trinnene:

    1. Angi **ID** i **Navn**-feltet.
    2. Angi **Angi ID** i **Etikett**-feltet.
    3. Velg **OK**.

12. Velg **Utdata\\Dokument\\ID** i treet.
13. Velg **Bind**, og velg deretter **Lagre**.

![Formatutformingsside, Tilordning-fane.](media/GER-BaselineSample-FormatMappingDesign.PNG "Skjermbilde av siden Formatutforming")

Det konfigurerte formatet genererer en XML-fil basert på den utformede strukturen. Denne XML-filen inneholder **Rot**-elementet som har **ID**-attributtet som er satt til verdien brukeren angir i dialogboksen for ER-kjøretid.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Generere en ny grunnlinjefil for et utformet ER-format

1. Velg **Kjør** i hurtigfanen **Versjoner** på **Konfigurasjoner**-siden.
2. Angi **1** i **Angi ID**-feltet.
3. Velg **OK**.

    ![Dialogboksen Parametere for elektronisk rapport.](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Skjermbilde av dialogboksen Parametere for elektronisk rapport")

4. Lagre en lokal kopi av filen **out.Admin.xml** som genereres, slik at du kan bruke den senere som en grunnlinje for dette ER-formatet.

    ![Varsling om den genererte filen på Konfigurasjoner-siden.](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Skjermbilde av varslingen om den genererte filen på Konfigurasjoner-siden")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>Konfigurere ER-parametere for å bruke grunnlinjefunksjonen

1. Velg **Brukerparametere** i **Konfigurasjoner**-fanen i handlingsruten på **Konfigurasjoner**-siden.
2. Sett alternativet **Kjør i feilsøkingsmodus** til **Ja**.
3. Velg **OK**.

![Dialogboksen Brukerparametere.](media/GER-BaselineSample-ERUserParameters.PNG "Skjermbilde av dialogboksen Brukerparametere")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Legge til en ny grunnlinje for utformet ER-format

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Velg **Grunnlinjer** i handlingsruten.

    ![Skjermbilde av Grunnlinjer-knapper på Konfigurasjoner-siden.](media/GER-BaselineSample-OpenBaselinePage.PNG "Skjermbilde av Grunnlinjer-knapen på Konfigurasjoner-siden")

3. Velg **Ny** i handlingsruten.
4. Velg ER-formatet **Format for å lære ER-grunnlinjer** du utformet tidligere.
5. Velg **Lagre**.

![Siden Grunnlinjer for elektronisk rapporteringsformat.](media/GER-BaselineSample-AddBaseline.PNG "Skjermbilde av siden Grunnlinjer for elektronisk rapporteringsformat")

Grunnlinjen legges til for formatet **Format for å lære ER-grunnlinjer**.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Konfigurere en grunnlinjeregel for den tilføyde grunnlinjen

1. I handlingsruten på siden **Grunnlinjer for elektronisk rapporteringsformat** velger du **Vedlegg**-knappen (bindersikonet).
2. Velg **Ny** \> **Fil** i handlingsruten. I ER-parameterne skal dokumenttypen **Fil** tidligere ha vært valgt som dokumenttypen som brukes til å lagre grunnlinjefiler.
3. Velg **Bla gjennom**, og velg filen **out.Admin.xml** som ble generert da du kjørte det konfigurerte ER-formatet tidligere.

    ![Vedlegg-siden.](media/GER-BaselineSample-UploadBaselineFile.PNG "Skjermbilde av Vedlegg-siden")

4. Lukk **Vedlegg**-siden.
5. Velg **Ny** i hurtigfanen **Grunnlinjer**.
6. Angi **Grunnlinje 1** i **Navn**-feltet.
7. I feltet **Navn på filkomponent** angir eller velger du **Utdata**. Denne verdien angir at den konfigurerte grunnlinjen blir sammenlignet med en fil som genereres ved hjelp av formatelementet **Utdata**.
8. I feltet **Filnavnmaske** angir du **\*.xml**.

    > [!NOTE]
    > Du kan definere filnavnmasken. Når filnavnmasken er definert, brukes grunnlinjeposten til å evaluere de genererte utdataene bare når navnet på utdatafilen som genereres, samsvarer med denne masken.

9. Hvis den konfigurerte grunnlinjen bare skal brukes når ER-formatet **Format for å lære ER-grunnlinjer** kjøres av brukere som er logget på bestemte firmaer, velger du disse firmaene i **Firmaer**-feltet.
10. I **Grunnlinje**-feltet angir eller velger du vedlegget **out.Admin**.
11. Velg **Lagre**.

![Siden Grunnlinjer for elektronisk rapporteringsformat, Grunnlinjer-hurtigfane med en grunnlinje valgt.](media/GER-BaselineSample-SetupBaselineLine.PNG "Skjermbilde av siden Grunnlinjer for elektronisk rapporteringsformat")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Kjøre det utformede ER-formatet og se gjennom loggen for å analysere resultatene

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Utvid **Modell for å lære ER-grunnlinjer** i treet, og velg deretter **Modell for å lære ER-grunnlinjer\\Format for å lære ER-grunnlinjer**.
3. Velg **Kjør** i hurtigfanen **Versjoner**.
4. Angi **1** i **Angi ID**-feltet.
5. Velg **OK**.
6. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Feilsøkingslogger for konfigurasjon**.

    ![Loggside for kjøring av elektronisk rapportering, med like grunnlinjer.](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Skjermbilde av siden Kjøringslogger for elektronisk rapportering")

    > [!NOTE]
    > Utførelsesloggen inneholder informasjon om resultatene av sammenligningen av den genererte filen med den konfigurerte grunnlinjen. I dette eksemplet angir loggen at den genererte filen og grunnlinjen er like.

7. Velg **Slett alt**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Kjøre det utformede ER-formatet og se gjennom loggen for å analysere resultatene

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Utvid **Modell for å lære ER-grunnlinjer** i treet, og velg deretter **Modell for å lære ER-grunnlinjer\\Format for å lære ER-grunnlinjer**.
3. Velg **Kjør** i hurtigfanen **Versjoner**.
4. Angi **2** i **Angi ID**-feltet.
5. Velg **OK**.
6. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Feilsøkingslogger for konfigurasjon**.

    ![Loggside for kjøring av elektronisk rapportering, med ulike grunnlinjer.](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Skjermbilde av siden Kjøringslogger for elektronisk rapportering")

    > [!NOTE]
    > Utførelsesloggen inneholder informasjon om resultatene av sammenligningen av den genererte filen med den konfigurerte grunnlinjen. I dette eksemplet angir loggen at den genererte filen og grunnlinjen er forskjellige.

7. Velg **Sammenlign**.

> [!NOTE]
> Den genererte filen og grunnlinjefilen tilbys som en ZIP-fil. Du kan bruke eksterne sammenligningsverktøy, for eksempel WinDiff, til å sammenligne filene og se gjennom forskjellene.

## <a name="additional-resources"></a>Tilleggsressurser

- [Konfigurere rammeverket for elektronisk rapportering (ER)](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
