---
title: Konfigurere handlingsavhengige ER-mål
description: Denne artikkelen forklarer hvordan du konfigurerer handlingsavhengige mål for et ER-format (Elektronisk rapportering) som er konfigurert til å generere utgående dokumenter.
author: kfend
ms.date: 12/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 80a432a431891c02e4bf5c71cfe2bd9642c41c75
ms.sourcegitcommit: e9000d0716f7fa45175b03477c533a9df2bfe96d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/13/2022
ms.locfileid: "9843804"
---
# <a name="configure-action-dependent-er-destinations"></a>Konfigurere handlingsavhengige ER-mål

[!include [banner](../includes/banner.md)]

Du kan konfigurere [mål](electronic-reporting-destinations.md) for hver utdatakomponent (mappe eller fil) i en [konfigurasjon](general-electronic-reporting.md#Configuration) for et [ER-format (Elektronisk rapportering)](general-electronic-reporting.md) som brukes til å generere et utgående dokument. Brukere som kjører et ER-format av denne typen og har nødvendige tilgangsrettigheter, kan også endre de konfigurerte målinnstillingene ved kjøretid.

I Microsoft Dynamics 365 Finance **versjon 10.0.17 og nyere** kan et ER-format kjøres ved å [klargjøre](er-apis-app10-0-17.md) en handlingskode som brukeren utfører ved å kjøre dette ER-formatet. I **Kunder**-modulen i innstillingene for utskriftsbehandling kan du for eksempel velge et ER-format som genererer et bestemt forretningsdokument, for eksempel en fritekstfaktura. Du kan deretter velge **Vis** for å forhåndsvise fakturaen eller **Skriv ut** for å sende den til en skriver. Hvis en brukerhandling sendes for det kjørende ER-formatet ved kjøretid, kan du konfigurere ulike ER-mål for ulike brukerhandlinger. Denne artikkelen beskriver hvordan du konfigurerer ER-mål for denne typen ER-format.

## <a name="make-action-dependent-er-destinations-available"></a>Gjøre handlingsavhengige ER-mål tilgjengelige

Hvis du vil konfigurere handlingsavhengige ER-mål i gjeldende Finance-forekomst og aktivere den [nye](er-apis-app10-0-17.md) ER-API-en, åpner du arbeidsområdet [Funksjonsbehandling](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) og aktiverer funksjonen **Konfigurer bestemte ER-mål slik at de kan brukes for ulike PM-handlinger**. Hvis du vil bruke konfigurerte ER-mål for rapporter ved kjøretid, aktiverer du funksjonen **Rut utdata fra PM-rapporter basert på ER-mål som er spesifikke for brukerhandlinger (bølge 1)**.

## <a name="configure-action-dependent-er-destinations"></a>Konfigurere handlingsavhengige ER-mål

Når du aktiverer funksjonen **Konfigurer bestemte ER-mål slik at de kan brukes for ulike PM-handlinger**, kan du konfigurere handlingsavhengige ER-mål i hurtigfanen **Filmål** på siden **Mål for elektronisk rapportering**. For hver komponent kan du legge til en post og aktivere bestemte ER-mål. For hver post må du angi dokumenttypen de konfigurerte ER-målene skal gjelde for. I feltet **Dokumenttype** velger du en av følgende verdier:

- Velg **Elektronisk** for å bruke de konfigurerte målene hvis ingen brukerhandlingskode angis ved kjøretid.
- Velg **Utskriftsbehandling** for å bruke de konfigurerte målene hvis en brukerhandlingskode angis ved kjøretid.
- Velg **Hvilken som helst** hvis du alltid vil bruke de konfigurerte målene, uavhengig av om en brukerhandlingskode angis ved kjøretid.

Hvis du velger dokumenttypen **Utskriftsbehandling**, må du angi brukerhandlingene som de konfigurerte ER-målene skal gjelde for. I feltet **Handling for utskriftsbehandling** velger du en av følgende verdier:

- Velg **Vis** for å bruke de konfigurerte målene hvis brukerhandlingen **Vis** angis ved kjøretid.
- Velg **Skriv ut** for å bruke de konfigurerte målene hvis brukerhandlingen **Skriv ut** angis ved kjøretid.
- Velg **Send** for å bruke de konfigurerte målene hvis brukerhandlingen **Send** angis ved kjøretid.

> [!NOTE]
> Du kan velge flere handlinger for én målpost.

Hvis du velger dokumenttypen **Hvilken som helst**, blir **Identifisert automatisk** valgt automatisk i feltet **Handling for utskriftsbehandling**, og følgende virkemåte forekommer:

- Hvis ingen brukerhandlingskode angis ved kjøretid, brukes alle konfigurerte ER-mål.
- Hvis en brukerhandlingskode angis ved kjøretid, brukes et ER-mål som er forhåndsdefinert for en bestemt handling, **uavhengig av om den er aktivert**:

    - Når **Vis**-handlingen angis ved kjøretid, brukes ER-målet **Skjerm**.
    - Når **Send**-handlingen angis ved kjøretid, brukes ER-målet **E-post**.
    - Når **Skriv ut**-handlingen angis ved kjøretid, brukes ER-målet **Skriver**.

Du kan for eksempel bruke ER-formatet **Fritekstfaktura (Excel)** til å skrive ut en [fritekstfaktura](../../../finance/accounts-receivable/create-free-text-invoice-new.md) når du posterer den. Hvis du vil rute et generert dokument, må du konfigurere ER-mål for dette ER-formatet. Det kan for eksempel hende at du må konfigurere disse ER-målene for å kunne gjøre følgende med et generert dokument:

- arkivere dokumentet hvis ER-formatet kjøres, men ingen handlingskode er angitt (for eksempel når dokumentet blir sendt elektronisk)
- forhåndsvise dokumentet i en nettleser når en bruker utfører **Vis**-handlingen.
- arkivere og skrive ut dokumentet når en bruker utfører **Skriv ut**-handlingen
- arkivere dokumentet og sende det som et vedlegg i en utgående e-postmelding når en bruker utfører **Send**-handlingen

Illustrasjonen nedenfor viser hvordan du kan oppnå denne konfigurasjonen av ER-mål som sett med individuelle målposter, når hver post er konfigurert for en individuell brukerhandling:

![Målside for elektronisk rapportering som har handlingsavhengige målinnstillinger for et ER-format når hver målpost er konfigurert for en individuell brukerhandling.](./media/er-destination-action-dependent-01.png)

Illustrasjonen nedenfor viser hvordan du kan oppnå den samme alternative konfigurasjonen av ER-mål som sett med individuelle målposter, når hver post er konfigurert for et enkeltmål:

![Målside for elektronisk rapportering som har handlingsavhengige målinnstillinger for et ER-format når hver målpost er konfigurert for et enkeltmål.](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Hvis det angis en handlingskode for det kjørende ER-formatet, men ingen mål er konfigurert for denne handlingskoden, brukes den [standard](electronic-reporting-destinations.md#default-behavior) målvirkemåten.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Endre handlingsavhengige ER-mål ved kjøretid

Hvis brukerhandlinger er klargjort av brukere som har de aktuelle [tillatelsene](electronic-reporting-destinations.md#security-considerations) til å endre konfigurerte målinnstillinger ved kjøretid, når et ER-format kjøres, vises det en dialogboks der du kan endre de konfigurerte målinnstillingene. Denne dialogboksen er valgfri, og utseendet avhenger av hvordan oppkallet som ER-rammeverket utfører for å kjøre et ER-format, er implementert. Hvis denne dialogboksen vises, blir ER-målet i den aktivert i henhold til brukerhandlingen som angis.

Illustrasjonen nedenfor viser et eksempel på dialogboksen **Mål for elektronisk rapporteringsformat** som vises når en fritekstfaktura [posteres](../../../finance/accounts-receivable/create-free-text-invoice-new.md) og ER-formatet **Fritekstfaktura (Excel)** kjøres for å generere dette dokumentet, hvis **Skriver**-handlingen ble klargjort og ER-mål ble konfigurert for dette formatet som vist tidligere i denne artikkelen.

![Dialogboks der du kan endre de opprinnelig konfigurerte ER-målene for kjøring av ER-format.](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Hvis du har konfigurert ER-mål for flere komponenter i det kjørende ER-formatet, vises et eget alternativ for hver konfigurerte komponent i ER-formatet.

Hvis flere ER-formater gjelder som rapportmaler for det valgte dokumentet, vises alle ER-mål for alle aktuelle ER-rapportmaler i dialogboksen og er tilgjengelige for manuell justering ved kjøretid.

Hvis ingen [SSRS-rapportmaler (SQL Server Reporting Services)](SSRS-report.md) gjelder for det valgte dokumentet, er standardvalget Utskriftsbehandlingsmål dynamisk skjult.

Fra og med Finance-versjon **10.0.31** kan du manuelt endre de tildelte ER-målene ved kjøretid for følgende forretningsdokumenter:

- Kontoutskrift for kunde
- Rentenota
- Purrenota
- Betalingsmelding for kunde
- Betalingsmelding for leverandør

Hvis du vil aktivere muligheten til å endre ER-mål ved kjøretid, aktiverer du funksjonen **Tillat ER-måljustering ved kjøretid** i arbeidsområdet [Funksjonsbehandling](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace).

> [!IMPORTANT]
> I rapportene **Betalingsmelding for kunde** og **Betalingsmelding for leverandør** er muligheten til å endre ER-mål manuelt bare tilgjengelig hvis **ForcePrintJobSettings**-testversjonen er aktivert.

[![Justering av ER-mål ved kjøretid.](./media/ERdestinaiotnChangeUI.jpg)](./media/ERdestinaiotnChangeUI.jpg)

> [!NOTE]
> Når alternativet **Bruk utskriftsbehandlingsmål** er satt til **Ja**, bruker systemet standard ER-mål som er konfigurert for bestemte ER-rapporter. Alle manuelle endringer som gjøres i dialogboksen, ignoreres. Angi alternativet **Bruk utskriftsbehandlingsmål** til **Nei** for å behandle dokumenter til ER-målene som er definert i dialogboksen rett før du kjører rapportene.

Følgende forretningsdokumenter forutsetter ikke eksplisitt brukervalg av en handling når de kjøres:

- Kontoutskrift for kunde
- Rentenota
- Purrenota
- Betalingsmelding for kunde
- Betalingsmelding for leverandør

Følgende logikk brukes til å avgjøre hvilken handling som skal brukes mens de foregående rapportene behandles:

- Hvis **ForcePrintJobSettings**-testversjon er aktivert:

    - Hvis alternativet **Bruk utskriftsbehandlingsmål** er satt til **Ja**, brukes **Skriv ut**-handlingen.
    - Hvis alternativet **Bruk utskriftsbehandlingsmål** er satt til **Nei**, brukes **Vis**-handlingen.

- Hvis **ForcePrintJobSettings**-testversjon ikke er aktivert:

    - Hvis alternativet **Bruk utskriftsbehandlingsmål** er satt til **Ja**, brukes **Skriv ut**-handlingen for rapportene **Betalingsmelding for kunde** og **Betalingsmelding for leverandør**.
    - Hvis alternativet **Bruk utskriftsbehandlingsmål** er satt til **Nei**, brukes alltid standard SSRS-rapportmal for rapportene **Betalingsmelding for kunde** og **Betalingsmelding for leverandør**, uansett eventuelle ER-innstillinger som er konfigurert.
    - **Skriv ut**-handlingen brukes alltid for rapportene **Kontoutskrift for kunde**, **Rentenota** og **Purrenota**.

For den forrige logikken kan handlingene **Skriv ut** eller **Vis** brukes til å konfigurere handlingsavhengige ER-rapportmål. Ved kjøretid filtreres bare ER-mål som er konfigurert for en bestemt handling, i dialogboksen.

## <a name="verify-the-provided-user-action"></a>Kontrollere den angitte brukerhandlingen

Du kan kontrollere hvilken brukerhandling som eventuelt angis for det kjørende ER-formatet, når du utfører en bestemt brukerhandling. Denne kontrollen er viktig når du må konfigurere handlingsavhengige ER-mål, men du er usikker på hvilken brukerhandlingskode som eventuelt angis. Når du for eksempel begynner å postere en fritekstfaktura og angir **Ja** for alternativet **Skriv ut faktura** i dialogboksen **Poster fritekstfaktura**, kan du angi **Ja** eller **Nei** for alternativet **Bruk utskriftsbehandlingsmål**.

Følg denne fremgangsmåten for å kontrollere brukerhandlingskoden som angis.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i fanen **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. I dialogboksen **Brukerparametere** [angir](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) du **Ja** for alternativet **Kjør i feilsøkingsmodus**.
4. Utfør en brukerhandling ved å kjøre et ER-format. Husk at ER-brukerparametere er firmaspesifikke og brukerspesifikke.
5. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Feilsøkingslogger for konfigurasjon**.
6. Filtrer ER-kjøringsloggene på siden **Feilsøkingslogger for konfigurasjon** for å finne loggen for ER-formatkjøring.
7. Se gjennom loggoppføringene som må inneholde posten som viser den angitte brukerhandlingskoden, hvis det er angitt en handling for ER-formatkjøringen.

    ![Siden Kjøringslogger for elektronisk rapportering, som inneholder informasjon om brukerhandlingskoden som er angitt for den filtrerte kjøringen av et ER-format.](./media/er-destination-action-dependent-03.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md)

[API-endringer for elektronisk rapporteringsrammeverk for Application update 10.0.17](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
