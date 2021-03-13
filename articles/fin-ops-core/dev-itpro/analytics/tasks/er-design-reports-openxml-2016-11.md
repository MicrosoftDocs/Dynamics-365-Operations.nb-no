---
title: ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format (november 2016)
description: Dette emnet beskriver hvordan du oppretter en ny konfigurasjon for elektronisk rapportering som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b832961061d05e3f1ae046f820bc7a37baaf90c
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092672"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format (november 2016)

[!include [banner](../../includes/banner.md)]

Det emnet forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format. Denne konfigurasjonen vil bli brukt til å behandle leverandørbetalinger.

I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i GBSI-firmaet.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv". Du må også ha en Excel-fil som importeres når du oppretter malen. Denne filen kan åpnes fra [Mal for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266).


## <a name="upload-the-payments-data-model-configuration"></a>Laste opp modellkonfigurasjon for betalingsdata
1. I navigasjonsruten går du til **Moduler > Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering**.
2. I listen velger du konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i fremgangsmåten [Opprette en konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).
3. Velg **Angi som aktiv**.
4. Velg **Repositorier**. Velg et repositorium for operasjonsressurstypen, hvis tilgjengelig. Hvis den er tilgjengelige, hopper du over følgende trinn for hvordan du oppretter et nytt repositorium.  
5. Velg **Legg til** for å åpne nedtrekksdialogen.
6. I feltet **Type konfigurasjonsrepositorium** angir du `Operations resourcesdd`.
7. Velg **Opprett repositorium**.
8. Velg **OK**.
9. Velg **Åpne**.
10. Velg **Betalingsmodell** i treet.
11. Velg **Import**. Importer denne datamodellen. Den vil bli brukt som datakilde i en ny formatkonfigurasjon. Hopp over dette trinnet hvis denne konfigurasjonen allerede er importert.  
12. Velg **Ja**.
13. Lukk sidene til du kommer tilbake til siden for elektronisk rapportering.

## <a name="create-a-new-format-configuration"></a>Opprette en ny formatkonfigurasjon
1. Velg **Rapporteringskonfigurasjoner**.
2. Velg **Betalingsmodell** i treet.
3. Velg **Opprett konfigurasjon** for å åpne nedtrekksdialogen.
4. I **Ny**-feltet angir du `Format based on data model PaymentModel`. Opprett et format som er basert på PaymentModel-datamodellen.
5. I **Navn**-feltet skriver du inn `Sample worksheet report`. Regnearkeksempelrapport  
6. I **Beskrivelse**-feltet skriver du inn `Sample worksheet report for vendors' payments`. Regnearkeksempelrapport for leverandørenes betalinger.  
7. Angi eller velg en verdi i feltet **Definisjon av datamodell**. Velg definisjonen **CustomerCreditTransferInitiation**.  
8. Velg **Opprett konfigurasjon**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Utforme et nytt dokument i OPENXML-regnearkformat
1. Velg **Betalingsmodell\Regnearkeksempelrapport** i treet.
2. Velg **Utforming**.
3. Velg **Importer** på handlingsruten.
4. Velg **Importer fra Excel**.
5. Velg **Vedlegg**. Knytte det eksisterende Excel-dokumentet til som en mal.  
6. Velg **Ny**.
7. Velg **Fil**. Velg den eksisterende Excel-filen.  
8. Lukk siden.
9. Angi eller velg en verdi i feltet **Mal**. Velg at den vedlagte Excel-filen skal brukes som en mal.  
10. Velg **OK**. Legg merke til at ER-formatkomponenter er opprettet i utformingsformatet basert på strukturen til det refererende MS Excel-dokumentet (navngitte områder).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Opprette en ny datakilde for å beregne totaler etter valutakoder
1. Velg fanen **Tilordning**.
2. Klikk på **Legg til rot** for å åpne nedtrekksdialogen.
3. Velg **Funksjoner\Grupper etter** i treet.
4. I **Navn**-feltet skriver du inn `PaymentByCurrency`.
5. Velg **Rediger gruppe etter**.
6. Utvid **modell** i treet, og velg deretter **modell\Betalinger.**
7. Velg **Legg til felt i**.
8. Velg **Hva skal grupperes**.
9. Utvid **modell\Betalinger** i treet, og velg deretter **modell\Betalinger\Valuta**.
10. Velg **Legg til felt i**.
11. Velg **Grupperte felt**.
12. Velg **model\Payments\Instructed Amount(InstructedAmount)** i treet.
13. Velg **Legg til felt i**, og velg deretter **Aggregeringsfelt**.
14. Velg et alternativ i **Metode**-feltet. Velg **mengdefunksjonen SUM**.  
15. I **Navn**-feltet skriver du inn `TotalInstructuredAmount`.
16. Velg **Lagre**.
17. Lukk siden.
18. Velg **OK**.

## <a name="map-format-components-to-data-sources"></a>Tilordne formatkomponenter til datakilder
1. Velg **model\Payments\Initiating Party(InitiatingParty)\Name** og **Excel\ReportHeader\CompanyName** i treet.
2. Velg **Bind**.
3. Velg **model\Payments\Creditor\Identification\Source ID(SourceID)** og **Excel\PaymLines\VendAccountName** i treet.
4. Velg **Bind**.
5. Velg **model\Payments\Creditor\Name** og **Excel\PaymLines\VendName** i treet.
6. Velg **Bind**.
7. Velg **model\Payments\Creditor Agent(CreditorAgent)\Name** og **Excel\PaymLines\Bank** i treet.
8. Velg **Bind**.
9. Velg **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** og **Excel\PaymLines\RoutingNumber** i treet.
10. Velg **Bind**.
11. Velg **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** og **Excel\PaymLines\AccountNumber** i treet.
12. Velg **Bind**.
13. Velg **model\Payments\Instructed Amount(InstructedAmount)** og **Excel\PaymLines\Debit** i treet.
14. Velg **Bind**.
15. Velg **model\Payments\Currency** og **Excel\PaymLines\Currency** i treet.
16. Velg **Bind**.
17. Velg **PaymentByCurrency\grouped\Currency** og **Excel\SummaryLines\SummaryCurrency** i treet.
18. Velg **Bind**.
19. Velg **PaymentByCurrency\aggregated\TotalInstructuredAmount** og **Excel\SummaryLines\SummaryAmount** i treet.
20. Velg **Bind**.
21. Velg **PaymentByCurrency** og **Excel\SummaryLines** i treet.
22. Velg **Bind**.
23. Velg **model\Payments** og **Excel\PaymLines** i treet.
24. Velg **Bind**.
25. Velg **Lagre**, og lukk deretter siden.

## <a name="use-the-created-configuration-for-payments-processing"></a>Bruke den opprettede konfigurasjonen for behandling av betalinger
1. Velg **Endre status**.
2. Velg **Fullfør**.
3. Velg **OK**.
4. I navigasjonsruten går du til **Moduler > Leverandører > Betalingsoppsett > Betalingsmåter**.
5. Bruk hurtigfilteret til å filtrere på **Betalingsmåte**-feltet med verdien **Elektronisk**.
6. Velg **Rediger**.
7. Vis delen **Filformater**.
8. Velg **Ja** i feltet **Generell elektronisk rapportering**.
9. Angi eller velg en verdi i feltet **Eksportformatkonfigurasjon**. Velg konfigurasjonen **Regnearkeksempelrapport**.  
10. Velg **Lagre**.
11. Lukk siden.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Bruke den opprettede konfigurasjonen for testing av behandling av betalingsjournaler
1. Gå til **Moduler > Leverandører > Fakturaer > Betalinger > Betalingsjournal** i navigasjonsruten.
2. Velg **Ny** for å opprette en ny betalingsjournal.
3. Skriv inn **VendPay** i **Navn**-feltet.
4. Velg **Linjer**.
5. I **Konto**-feltet angir du verdiene `GB_SI_000001`.
6. Sett **Debet** til `1000`.
7. Velg **Ny**.
8. I **Konto**-feltet angir du verdiene `GB_SI_000005`.
9. Sett **Debet** til `2000`.
10. I **Valuta**-feltet skriver du inn `EUR`.
11. I **Motkonto**-feltet angir du verdiene `GBSI OPER`.
12. I **Betalingsmåte**-feltet skriver du inn `Electronic`.
13. Velg **Lagre**.
14. Velg **Generer betalinger**.
15. I **Betalingsmåte**-feltet skriver du inn `Electronic`.
16. I **Filnavn**-feltet skriver du inn `Payments`.
17. I **Bankkonto**-feltet skriver du inn `GBSI OPER`.
18. Velg **OK**, og velg deretter **OK** på nytt. Se gjennom det opprettede regnearket, inkludert detaljer om betalingslinjer samt totalene for hver valutakode som brukes i denne betalingsmeldingen.  

