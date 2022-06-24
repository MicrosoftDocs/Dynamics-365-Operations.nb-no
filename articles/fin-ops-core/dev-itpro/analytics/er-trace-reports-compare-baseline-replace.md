---
title: Forbedre sporing av resultater av genererte ER-rapporter for å sammenligne med grunnlinjeverdier
description: Denne artikkelen beskriver forbedringer i ER-grunnlinjefunksjonen i Microsoft Dynamics 365 for Finance and Operations versjon 10.0.3 (juni 2019).
author: NickSelin
ms.date: 06/19/2019
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
ms.openlocfilehash: 3b9ac7dcac4d020759d04fec75e17c43ed627e25
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847408"
---
# <a name="improve-tracing-the-results-of-generated-er-reports-to-compare-with-baseline-values"></a>Forbedre sporing av resultater av genererte ER-rapporter for å sammenligne med grunnlinjeverdier

[!include[banner](../includes/banner.md)]

Denne artikkelen beskriver det første settet med forbedringer i grunnlinjefunksjonen i rammeverket for elektronisk rapportering (ER). Disse forbedringene er tilgjengelige i Microsoft Dynamics 365 for Finance and Operations versjon 10.0.3 (juni 2019) og nyere.

## <a name="automate-the-setting-of-baseline-rules"></a>Automatisere innstillingen for grunnlinjeregler

Artikkelen [Spore genererte rapportresultater og sammenligne dem med grunnlinjeverdier](er-trace-reports-compare-baseline.md) forklarer hvordan du konfigurerer ER-rammeverket slik at det samler inn informasjon om ER-formatutførelser og evaluerer resultatene av disse utførelsene. Eksemplet i denne artikkelen viser trinnene som må fullføres.

Her er noen av trinnene:

- Kjør et ER-format for å generere en utgående fil, og lagre filen lokalt.
- Legg til den lokalt lagrede filen som et vedlegg til grunnlinjen som ble lagt til for et ER-format.
- Konfigurer grunnlinjeregelen for den tilføyde grunnlinjen. Denne konfigurasjonen omfatter følgende trinn:

    - Angi et ER-formatelement som brukes til å generere en utgående fil.
    - Velg vedlegget som refererer til den genererte utgående filen.

> [!NOTE]
> Disse trinnene må gjøres manuelt selv om de nye ER-funksjonene gjør at de kan automatiseres. Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet nedenfor.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Eksempel: Automatisere innstillingen for grunnlinjeregler

For å kunne fullføre trinnene i dette eksemplet må du først fullføre trinnene i eksemplet i artikkelen [Spore genererte rapportresultater og sammenligne dem med grunnlinjeverdier](er-trace-reports-compare-baseline.md) frem til delen «Legge til en ny grunnlinje for et utformet ER-format».

### <a name="review-added-baseline"></a>Se gjennom tilføyd grunnlinje

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Velg **Grunnlinjer**.

    > [!NOTE]
    > **Grunnlinjer**-knappen i handlingsruten er bare tilgjengelig når ER-brukerparameteren **Kjør i feilsøkingsmodus** er aktivert for det gjeldende firmaet.

Grunnlinjen er lagt til for det valgte formatet **Format for å lære ER-grunnlinjer**, men grunnlinjereglene er ennå ikke lagt til for denne grunnlinjen.

![Siden Grunnlinjer for elektronisk rapporteringsformat, ingen regler ennå.](media/GER-BaselineSample-AddBaseline2.PNG "Skjermbilde av siden Grunnlinjer for elektronisk rapporteringsformat")

### <a name="make-a-new-baseline-rule"></a>Lage en ny grunnlinjeregel

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Utvid **Modell for å lære ER-grunnlinjer** i treet.
3. Velg **Modell for å lære ER-grunnlinjer\\Format for å lære ER-grunnlinjer** i treet.
4. Velg **Kjør** i hurtigfanen **Versjoner**.
5. Angi **1** i **Angi ID**-feltet.
6. Sett alternativet **Lag grunnlinjefiler** til **Ja**.
7. Velg **OK**.
8. Velg **Grunnlinjer**.

    ![Siden Grunnlinjer for elektronisk rapporteringsformat, grunnlinjer valgt.](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Skjermbilde av siden Grunnlinjer for elektronisk rapporteringsformat")

    Den genererte utgående filen knyttes automatisk til grunnlinjen for det utførte ER-formatet. Grunnlinjeregelen har blitt lagt til denne grunnlinjen automatisk og inneholder også referansen til den vedlagte filen.

9. Angi **Grunnlinje 1** i **Navn**-feltet.
10. I feltet **Filnavnmaske** angir du **.xml**.
11. Velg **Lagre**.

### <a name="run-the-format"></a>Kjøre formatet

Du er nå klar til å fullføre resten av trinnene i eksemplet i artikkelen [Spore genererte rapportresultater og sammenligne dem med grunnlinjeverdier](er-trace-reports-compare-baseline.md) ved å starte fra delen «Kjøre det utformede ER-formatet og se gjennom loggen for å analysere resultatene».

> [!NOTE]
> Når du sletter den automatisk tilføyde grunnlinjeregelen i hurtigfanen **Grunnlinjer**, blir ikke vedlegget som det refereres til, slettet automatisk.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Konfigurere grunnlinjen slik at den ignorerer deler av ER-utdataene som er i stadig endring

Når et ER-format er utformet slik at det inneholder informasjon som endres når formatet kjøres, må formatet bruke ER-grunnlinjefunksjonen til å sammenligne de genererte resultatene med grunnlinjeverdier. Informasjonen kan for eksempel være behandlingsdatoen og -klokkeslettet eller den unike identifikatoren til et generert dokument i ulike formater (globalt unik identifikator \[GUID\] og så videre). De nye ER-funksjonene gjør at du kan konfigurere grunnlinjeregelen slik at den ignorerer elementer som kan endres, i et ER-format når formatet kjøres for å sammenligne grunnlinjeverdier med resultatene av formatets utførelse. Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet nedenfor.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Eksempel: Konfigurere grunnlinjen slik at den ignorerer deler av ER-utdataene som er i stadig endring

For å kunne fullføre trinnene i dette eksemplet må du først fullføre trinnene i eksemplet i artikkelen [Spore genererte rapportresultater og sammenligne dem med grunnlinjeverdier](er-trace-reports-compare-baseline.md).

### <a name="modify-a-configured-er-format"></a>Endre et konfigurert ER-format

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Utvid **Modell for å lære ER-grunnlinjer** i treet.
3. Velg **Modell for å lære ER-grunnlinjer\\Format for å lære ER-grunnlinjer** i treet.
4. Velg **Utforming**.
5. Velg **Utdata\\Dokument** i treet.
6. Velg **Legg til**.
7. Velg **XML\\Attributt** i treet i rullegardinboksen.
8. I **Navn**-feltet angir du **ProcessingDateTime**.
9. Velg **OK**.
10. Velg **Utdata\\Dokument\\ProcessingDateTime** i treet i **Tilordning**-fanen.
11. Velg **Rediger formel**.
12. I **Formel**-feltet angir du følgende uttrykk: **DATETIMEFORMAT(NOW(), "O")**
13. Velg **Lagre**, og velg deretter **Test**.
14. Velg **Test** på nytt for å teste det konfigurerte uttrykket på nytt.

    ![Formeldesigner-siden.](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Skjermbilde av siden Formelutforming")

    > [!NOTE]
    > Fanen **Testresultat** viser at det konfigurerte uttrykket returnerer en ny verdi for dato og klokkeslett hver gang det kalles.

15. Lukk **Formeldesigner**-siden, og velg deretter **Lagre**.

    ![Formatutformingsside.](media/GER-BaselineSample-FormatMappingDesign2.PNG "Skjermbilde av siden Formatutforming")

16. Lukk **Formatutforming**-siden.

### <a name="remove-an-existing-baseline-rule"></a>Fjerne en eksisterende grunnlinjeregel

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Velg **Grunnlinjer**.
3. I listen over grunnlinjer velger du grunnlinjen som konfigureres for formatet **Format for å lære ER-grunnlinjer**.
4. I hurtigfanen **Grunnlinjer** velger du **Slett** for å fjerne grunnlinjeregelen du konfigurerte tidligere.

![Siden Grunnlinjer for elektronisk rapporteringsformat, slettet.](media/GER-BaselineSample-AddBaseline3.PNG "Skjermbilde av siden Grunnlinjer for elektronisk rapporteringsformat")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Definere erstatninger for bindinger for utformet ER-format

1. Velg **Velg komponenter** i hurtigfanen **Erstatninger** på **Konfigurasjoner**-siden.
2. Utvid **Utdata** i treet for formatkomponenter, utvid **Utdata\\Dokument**, og merk deretter av for **Utdata\\Dokument\\ProcessingDateTime**.
3. Velg **OK**.

![Siden Grunnlinjer for elektronisk rapporteringsformat, komponenter.](media/GER-BaselineSample-AddBaseline4.PNG "Skjermbilde av siden Grunnlinjer for elektronisk rapporteringsformat")

Den valgte ER-formatkomponenten er lagt til i listen over komponenter i hurtigfanen **Erstatninger**. Når basis-ER-formatet kjører i feilsøkingsmodus, erstattes formatets binding for hver komponent med bindingen som vises i **Binding**-kolonnen. Hvis du vil endre standardbindingen for en komponent som er oppført i hurtigfanen **Erstatninger**, velger du **Rediger**.

### <a name="make-a-new-baseline-rule"></a>Lage en ny grunnlinjeregel

Følg trinnene i delen «Eksempel: Automatisere innstillingen for grunnlinjeregler» tidligere i denne artikkelen. En varsling advarer deg om at den utgående filen er generert ved hjelp av grunnlinjeinnstillinger, og at det har oppstått en tvungen erstatning av formatbindingene.

![Varsling om Konfigurasjoner-siden.](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Skjermbilde av varslingen på Konfigurasjoner-siden")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Utelate advarsler om erstatningen av formatbindinger

Hvis du angir bestemte ER-parametere, kan du utelate varslinger med advarsel om erstatning av formatbindinger. Denne utelatelsen kan være nyttig når formatbindinger erstattes i en uovervåket modus ved hjelp av Regression Suite Automation Tool. I dette tilfellet kan advarselen regnes som en feil i testtilfellet som kjører.

1. Velg **Brukerparametere** i **Konfigurasjoner**-fanen i handlingsruten på **Konfigurasjoner**-siden.
2. Sett alternativet **Utelat grunnlinjeadvarsler** til **Ja**, og velg deretter **OK**.

### <a name="review-the-generated-baseline-file"></a>Se gjennom den genererte grunnlinjefilen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Velg **Grunnlinjer**.
3. Velg **Vedlegg**.
    > [!NOTE]
    > Den genererte filen inneholder teksten for behandlingsdato og -klokkeslett (**"#"**) fra bindingen som ble konfigurert i den tilføyde grunnlinjeregelen, ikke fra formatets binding.
    
4. Lukk **Vedlegg**-siden.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Kjøre det utformede ER-formatet og se gjennom loggen for å analysere resultatene

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Utvid **Modell for å lære ER-grunnlinjer** i treet.
3. Velg **Modell for å lære ER-grunnlinjer\\Format for å lære ER-grunnlinjer** i treet.
4. Velg **Kjør** i hurtigfanen **Versjoner**.
5. Skriv inn **1** i **Angi ID**-feltet.
6. Velg **OK**.
7. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Feilsøkingslogger for konfigurasjon**.

Utførelsesloggen inneholder informasjon om resultatene av sammenligningen av den genererte filen med den konfigurerte grunnlinjen. Loggen angir at den genererte filen og grunnlinjen er like, selv om det utførte formatet inneholder bindingen for å angi en verdi for dato og klokkeslett som er i stadig endring, i den utgående filen.

> [!NOTE]
> Selv om den utgående filen er generert ved hjelp av grunnlinjeinnstillinger som fremtvinger erstatningen av formatets bindinger, får du ingen advarsler om erstatningen.

## <a name="exchange-baseline-settings-between-environments"></a>Utveksle grunnlinjeinnstillinger mellom miljøer

### <a name="export-baseline-settings"></a>Eksportere grunnlinjeinnstillinger

De nye ER-funksjonene gjør at du kan eksportere grunnlinjeinnstillinger for det valgte ER-formatet fra det gjeldende miljøet og lagre dem som XML-filer. 

Hvis du vil eksportere grunnlinjeinnstillinger, velger du **Eksporter** på siden **Grunnlinjer for elektronisk rapporteringsformat**.

### <a name="import-baseline-settings"></a>Importer grunnlinjeinnstillinger

Eksporterte grunnlinjeinnstillinger kan importeres til et annet miljø. Miljøet må først importeres som et ER-format. Du kan deretter importere grunnlinjeinnstillingene.

Hvis du vil importere grunnlinjeinnstillinger fra en lokalt lagret XML-fil, velger du **Importer** på siden **Grunnlinjer for elektronisk rapporteringsformat**, og deretter velger du **Bla gjennom** for å velge XML-filen.

![Dialogboksen Importer grunnlinjeinnstillinger.](media/GER-BaselineSample-ImportBaseline1.PNG "Skjermbilde av dialogboksen Importer grunnlinjeinnstillinger")

Hvis du vil importere grunnlinjeinnstillinger fra en XML-fil som er lagret på Microsoft SharePoint Server, basert på gjeldende innstillinger for dokumentstyring og den valgte dokumenttypen, velger du **Importer fra kilde** på siden **Grunnlinjer for elektronisk rapporteringsformat**. Velg deretter dokumenttypen og XML-filen. Dokumenttypen som kreves for å få tilgang til SharePoint-mappen, må konfigureres på forhånd.

![Dialogboksen Importer fra kilde.](media/GER-BaselineSample-ImportBaseline2.PNG "Skjermbilde av dialogboksen Importer fra kilde")

> [!NOTE]
> Du kan bruke Oppgaveopptaker til å ta opp trinnene for å velge den nødvendige dokumenttypen og filnavnet i dialogboksen **Importer fra kilde**. På denne måten kan du beholde de nødvendige grunnlinjeinnstillingene på SharePoint Server og deretter automatisk importere dem ved å spille av et oppgaveopptak når du kjører automatiserte tester ved hjelp av Regression Suite Automation Tool.

## <a name="additional-resources"></a>Tilleggsressurser

- [Spore genererte rapportresultater og sammenligne dem med grunnlinjeverdier](er-trace-reports-compare-baseline.md)
- [Ressurser for Oppgaveregistrering](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
