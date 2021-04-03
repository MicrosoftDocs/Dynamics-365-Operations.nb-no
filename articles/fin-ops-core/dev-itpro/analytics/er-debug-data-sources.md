---
title: Feilsøke datakilder for et utført ER-format for å analysere dataflyt og transformasjon
description: Dette emnet beskriver hvordan du kan feilsøker datakildene i et utført ER-format for bedre forståelse av den konfigurerte dataflyten og transformasjonen.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: bda81da80996d8cba38ac48e29c47ffef61d3bdb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562196"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Feilsøke datakilder for et utført ER-format for å analysere dataflyt og transformasjon

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Når du [konfigurerer](tasks/er-format-configuration-2016-11.md) en ER-løsning (elektronisk rapportering) for å generere utgående dokumenter, definerer du metoden som brukes til å hente data ut av applikasjonen, og angir den i utdataene som genereres. For å få livssyklusstøtten for ER-løsningen mer effektiv, bør løsningen bestå av en ER [datamodell](general-electronic-reporting.md#DataModelComponent) og kompentene for [tilordning](general-electronic-reporting.md#ModelMappingComponent) og også et ER-[format](general-electronic-reporting.md#FormatComponentOutbound) og de tilhørende tilordningskomponentene, slik at modelltilordningen er programspesifikk mens andre komponenter forblir programagnostiske. Derfor kan flere ER-komponenter [påvirke](general-electronic-reporting.md#FormatComponentOutbound) prosessen med å registrere data i de genererte utdataene.

Noen ganger vil dataene i den genererte utskriften se annerledes ut enn de samme dataene i programdatabasen. I disse tilfellene vil du avgjøre hvilken ER-komponent som er ansvarlig for datatransformasjonen. Feilsøkerfunksjonen for ER-datakilde reduserer tiden og kostnadene som er involvert i denne undersøkelsen betydelig. Du kan avbryte utførelsen av et ER-format og åpne feilsøkergrensesnittet for datakilden. Der kan du bla gjennom de tilgjengelige datakildene og velge en enkelt datakilde for utførelse. Denne manuelle utførelsen simulerer utførelsen av datakilden under den virkelige kjøringen av et ER-format. Resultatet vises på en side der du kan analysere de mottatte dataene.

Hvis du vil aktivere funksjonen for feilsøking av datakilde, setter du alternativet **Aktiver datafeilsøking ved formatkjøring** til **Ja** i ER-brukerparameterne. Du kan deretter starte feilsøking av datakilde mens du kjører et ER-format for å generere utgående dokumenter. Du kan også bruke alternativet for **start feilsøking** for å starte feilsøking av datakilde for et ER-format som er konfigurert i [ER-operasjonsutforming](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).

Dette emnet inneholder retningslinjer for hvordan du starter feilsøking av datakilder for utførte ER-formater. Den forklarer hvordan informasjonen kan hjelpe deg med å forstå dataflyten og datatransformeringene. Eksemplene i dette emnet bruker forretningsprosessen for behandling av leverandørbetalinger.

## <a name="limitations"></a>Begrensninger

Du kan bruke feilsøkingsprogrammet for datakilde til å få tilgang til data i datakilder som brukes i ER-formater som kjøres for å generere utgående dokumenter. Den kan ikke brukes til å feilsøke datakilder med ER-formater som er utformet for å analysere innkommende dokumenter.

Følgende innstillinger for ER-formater er for øyeblikket ikke tilgjengelige for datakildefeilsøking:

- Formattransformasjoner
- Formatere og tilordne valideringsregler
- Aktivere uttrykk
- Detaljer om datainnsamling i minnet

## <a name="prerequisites"></a>Forutsetninger

- Hvis du vil fullføre eksemplene i dette emnet, må du ha tilgang til følgende [roller](../sysadmin/tasks/assign-users-security-roles.md):

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

- Firmaet må settes til **DEMF**.

- Følg trinnene i [tillegg 1](#appendix1) i dette emnet for å laste ned komponentene i Microsoft ER-løsningen som kreves for å behandle leverandørbetalinger.
- Følg trinnene i [tillegg 2](#appendix2) i dette emnet for å klargjøre leverandører for leverandørbetalingsbehandling ved hjelp av ER-løsningen du vil laste ned.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Behandle en leverandørbetaling for å hente en betalingsfil

1. Følg trinnene i [tillegg 3](#appendix3) i dette emnet for å behandle leverandørbetalinger.

    ![Leverandørbetalingsbehandling pågår](./media/er-data-debugger-process-payment.png)

2. Last ned og lagre zip-filen på den lokale datamaskinen.
3. Pakk ut betalingsfilen **ISO20022 Credit transfer.xml** fra zip-filen.
4. Åpne den utpakkede betalingsfilen ved hjelp av visningsprogrammet for XML-filen.

    Betalingsfilen for det internasjonale bankkontonummeret (IBAN) til leverandørens bankkonto inneholder ikke mellomrom. Derfor er det forskjellig fra verdien som ble [angitt](#enteredIBANcode) på siden **Bankkontoer**.

    ![IBAN-kode uten mellomrom](./media/er-data-debugger-payment-file.png)

    Du kan bruke feilsøkingsprogrammet for ER-datakilde til å lære hvilken komponent i ER-løsningen som brukes til å avkorte mellomrom i IBAN-koden.

## <a name="turn-on-data-source-debugging"></a>Aktivere feilsøking for datakilde

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. Sett **Aktiver datafeilsøking ved formatkjøring** til **Ja**.

    > [!NOTE]
    > Denne parameteren er brukerspesifikk og selskapsspesifikk.

    ![Dialogboksen Brukerparametere](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Behandle en leverandørbetaling for feilsøking

1. Følg trinnene i [tillegg 3](#appendix3) i dette emnet for å behandle leverandørbetalinger.
2. I meldingsboksen velger **Ja** for å bekrefte at du vil avbryte leverandørbetalingsbehandling og i stedet starte datakildefeilsøking på siden for **feilsøke datakilder**.

    ![Meldingsboks for bekreftelse](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Feilsøke datakilder som brukes i betalingsbehandling

### <a name="debug-the-model-mapping"></a>Feilsøke modelltilordningen

1. På siden for **feilsøk datakilder** i handlingsruten velger du **Modelltilordning** for å starte feilsøking fra denne ER-komponenten.
2. I datakilderuten til venstre velger du datakilden **\$notSentTransactions**, og velg deretter **Les alle poster**.

    Du kan velge **Les 1 post**, **Les 10 poster**, **Les 100 poster** eller **Les alle poster** for å tvinge det aktuelle antallet poster til å leses fra den valgte datakilden. På denne måten kan du simulere tilgang til datakilden fra det kjørende ER-formatet.

3. Deretter velger du **Vis alle** i dataruten til høyre.

    Du kan se at den valgte datakilden for typen **Postliste** inneholder én enkelt post.

4. Utvid datakilden **\$notSentTransactions**, og velg den nestede **vendBankAccountInTransactionCompany()**-metoden.
5. Utvid **vendBankAccountInTransactionCompany()**-metoden, og velg det nestede **IBAN**-feltet.
6. Velg **Hent verdi**.

    Du kan velge **Hent verdi** for å fremtvinge verdien av et valgt felt i den valgte datakilden som skal leses. På denne måten kan du simulere tilgang til dette feltet fra det kjørende ER-formatet.

7. Velg **Vis alle**.

    ![Verdien til IBAN-feltet i modelltilordningen](./media/er-data-debugger-debugging-model-mapping.png)

    Som du kan se, er ikke modelltilordningen ansvarlig for de avkortede områdene, fordi IBAN-koden som den returnerer for leverandørbankkontoen, omfatter mellomrom. Derfor må du fortsette feilsøkingen av datakilder.

### <a name="debug-the-format-mapping"></a>Feilsøke formattilordningen

1. På siden for **feilsøk datakilder** i handlingsruten velger du **Formattilordning** for å fortsette feilsøkingen fra denne ER-komponenten.
2. Velg datakilden **\$PaymentByDebtor**, og velg deretter **Les alle poster**.
3. Utvid **\$PaymentByDebtor**.
4. Utvid **\$PaymentByDebtor.Lines**, og velg deretter **Les alle poster**.
5. Utvid **\$PaymentByDebtor.Lines.CreditorAccount**.
6. Utvid **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, og velg deretter **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.
7. Velg **Hent verdi**.
8. Velg **Vis alle**.

    ![Verdien til IBAN-feltet i formattilordningen](./media/er-data-debugger-debugging-format-mapping.png)

    Som du kan se, er ikke datakildene i formattilordningen ansvarlig for de avkortede områdene, fordi IBAN-koden som den returnerer for leverandørbankkontoen, omfatter mellomrom. Derfor må du fortsette feilsøkingen av datakilder.

### <a name="debug-the-format"></a>Feilsøke formatet

1. På siden for **feilsøk datakilder** i handlingsruten velger du **Format** for å fortsette feilsøkingen fra denne ER-komponenten.
2. Utvid formatelementene for å velge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf**, og velg deretter **Les alle poster**.
3. Utvid formatelementene for å velge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, og velg deretter **Les alle poster**.
4. Utvid formatelementene for å velge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, og velg deretter **Hent verdi**.
5. Velg **Vis alle**.

    ![Verdien til IBAN-feltet i formatet](./media/er-data-debugger-debugging-format.png)

   Som du kan se, er ikke formatbinding ansvarlig for de avkortede områdene, fordi IBAN-koden som den returnerer for leverandørbankkontoen, omfatter mellomrom. Derfor er **BankIBAN**-elementet konfigurert til å bruke en formattransformering som avkorter mellomrom.

6. Lukk feilsøkingsprogrammet for datakilde.

### <a name="review-the-format-transformations"></a>Se gjennom formattransformasjoner

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På siden **Konfigurasjoner** velger du **Betalingsmodell** \> **ISO20022-kredittoverføring**.
3. Velg **Utforming**, og utvid deretter elementene for å velge **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.

    ![BankIBAN-elementet på Formatutforming-siden](./media/er-data-debugger-referred-transformation.png)

    Som du kan se, er **BankIBAN**-elementet konfigurert til å bruke transformeringen **fjern ikke alfanumerisk**.

4. Velg kategorien **Transformasjoner**.

    ![Kategorien Transformasjoner for BankIBAN-elementet](./media/er-data-debugger-transformation.png)

    Som du kan se, er transformeringen **fjern ikke-alfanumerisk** konfigurert til å bruke et uttrykk som avkorter mellomrom fra tekststrengen som er angitt.

## <a name="start-to-debug-in-the-operation-designer"></a>Start feilsøking i operasjonsutforming

Når du konfigurerer en kladdeversjon av ER-formatet som kan kjøres direkte fra operasjonsutformingen, får du tilgang til datakildefeilsøkeren ved å velge **Start feilsøking** i handlingsruten.

![Knappen Start feilsøking på siden Formatutforming](./media/er-data-debugger-run-from-designer.png)

Formattilordning og formatkomponentene i ER-formatet som redigeres, er tilgjengelige for feilsøking.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Start feilsøking i Modelltilordningsutforming

Når du konfigurerer en ER-modelltilordning som kan kjøres direkte fra siden **Modelltilordning**, får du tilgang til datakildefeilsøkeren ved å velge **Start feilsøking** i handlingsruten.

![Knappen Start feilsøking på siden Modellkartleggingsutforming](./media/er-data-debugger-run-from-designer-mapping.png)

Modelltilordningskomponenten for ER-tilordningen som redigeres, er tilgjengelig for feilsøking.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>Tillegg 1: Få en ER-løsning

### <a name="download-an-er-solution"></a>Laste ned en ER-løsning

Hvis du vil bruke en ER-løsning for å generere en elektronisk betalingsfil for en leverandørbetaling som er behandlet, kan du [laste ned](download-electronic-reporting-configuration-lcs.md) det ER-betalingsformatet **ISO20022-kredittoverføring** som er tilgjengelig fra det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS) eller fra det globale repositoriet.

![Importere ER-betalingsformatet på Konfigurasjonsrepositorium-siden](./media/er-data-debugger-import-from-repo.png)

I tillegg til det valgte ER-formatet må følgende [konfigurasjoner](general-electronic-reporting.md#Configuration) importeres automatisk til Microsoft Dynamics 365 Finance-forekomsten som en del av ER-løsningen **ISO20022-kredittoverføring**:

- **Betalingsmodell** [ER-datamodellkonfigurasjon](general-electronic-reporting.md#DataModelComponent)
- **ISO20022-kredittoverføring** [ER-formatkonfigurasjon](general-electronic-reporting.md#FormatComponentOutbound)
- **Betalingsmodelltilordning 1611** [ER-modelltilordningskonfigurasjon](general-electronic-reporting.md#ModelMappingComponent)
- **Betalingsmodelltilordning til mål ISO20022** – ER-modelltilordningskonfigurasjon

Du finner disse konfigurasjonene på siden **Konfigurasjoner** i ER-rammeverket (**Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**).

![Konfigurasjoner er importert på Konfigurasjoner-siden](./media/er-data-debugger-configurations.png)

Hvis noen av de tidligere angitte konfigurasjonene mangler i konfigurasjonstreet, må du laste dem ned manuelt fra det delte LCS-aktivabibliotek på samme måte som du har lastet ned ER-betalingsformatet **ISO20022-kredittoverføring**.

### <a name="analyze-the-downloaded-er-solution"></a>Analysere den nedlastede ER-løsningen

#### <a name="review-the-model-mapping"></a>Se gjennom modelltilordningen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Velg **Betalingsmodell** \> **Betalingsmodelltilordning 1611**.
3. Velg **Utforming**.
4. Velg tilordningsposten **Betalingsmodelltilordning ISO20022-kredittoverføring**.
5. Velg **Utforming**, og gå deretter gjennom modelltilordningen som åpnes.

    Legg merke til at **Betalinger**-feltet for datamodellen er bundet til **\$notSentTransactions**-datakilden som returnerer listen over leverandørbetalingslinjer som behandles.

    ![Betalinger-feltet på siden for modelltilordningsutforming](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>Se gjennom formattilordningen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Velg **Betalingsmodell** \> **ISO20022-kredittoverføring**.
3. Velg **Utforming**.
4. I kategorien **Tilordning** kontrollerer du formattilordningen som åpnes.

    Legg merke til at **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf**-elementet i **ISO20022CTReports** \> **XMLHeader**-filen er bundet til datakilden **\$PaymentByDebtor**, som er konfigurert til å gruppere poster i datamodellens **Betalinger**-felt.

    ![PmtInf-elementet på Formatutforming-siden](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>Se gjennom format

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Velg **Betalingsmodell** \> **ISO20022-kredittoverføring**.
3. Velg **Utforming**, og gå deretter gjennom formatet som åpnes.

    Merk at formatelementet under **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** er konfigurert til å angi IBAN-koden for leverandørkontoen i betalingsfilen.

    ![BankIBAN-elementet på Formatutforming-siden](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>Tillegg 2: Konfigurere leverandører

### <a name="modify-a-vendor-property"></a>Endre en leverandøregenskap

1. Gå til **Leverandører** \> **Leverandører** \> **Alle leverandører**.
2. Velg leverandør **DE-01002**, og gå deretter til handlingsruten, kategorien **Leverandør** i gruppen **Oppsett**, og velg **Bankkontoer**.
3. I hurtigkategorien **Identifikasjon** i feltet **IBAN** <a name="enteredIBANcode"></a>angir du **GB33 BUKB 2020 1555 5555 55**.
4. Velg **Lagre**.

![IBAN-feltet er satt siden Leverandørbankkontoer](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Definere en betalingsmåte

1. Gå til **Leverandører** \> **Betalingsoppsett** \> **Betalingsmåter**.
2. Velg betalingsmåten **SEPA CT**.
3. I hurtigfanen **Filformater** i delen **Filformater** setter du alternativet **Generelt elektronisk eksportformat** til **Ja**.
4. I feltet **Eksportformatkonfigurasjon** velger du ER-formatet **ISO20022-kredittoverføring**.
5. Velg **Lagre**.

![Filformatinnstillingene på siden for Betalingsmåter](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Legge til en leverandørbetaling

1. Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.
2. Legg til ny betalingsjournal.
3. Velg **Linjer**, og legg til en ny betalingslinje.
4. I feltet **Konto** velger du leverandøren **DE-01002**.
5. Angi en verdi i **Debet**-feltet.
6. Velg **SEPA CT** i feltet **Betalingsmåte**.
7. Velg **Lagre**.

![Leverandørbetaling er lagt til på siden Leverandør](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>Tillegg 3: Behandle en leverandørbetaling

1. Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.
2. På siden **Leverandørbetalingsjournal** velger du betalingsjournalen du opprettet tidligere, og deretter velger du **Linjer**.
3. Velg betalingslinjen, og velg deretter **Betalingsstatus** \> **Ingen**.
4. Velg **Generer betalinger**.
5. Velg **SEPA CT** i feltet **Betalingsmåte**.
6. Velg **DEMF OPER** i feltet **Bankkonto**.
7. Velg **OK** i dialogboksen **Generer betalinger**.
8. I dialogboksen **Parametere for elektronisk rapport** velger du **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]