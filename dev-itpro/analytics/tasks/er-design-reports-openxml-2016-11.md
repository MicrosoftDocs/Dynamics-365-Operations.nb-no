--- 
title: "Utforme en konfigurasjon for å generere rapporter i OpenXML-format for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d552dbcf932813de4d060b4f2190cf388eddb1bf
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>Utforme en konfigurasjon for å generere rapporter i OpenXML-format for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format. Denne konfigurasjonen vil bli brukt til å behandle leverandørbetalinger.



I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i GBSI-firmaet.



For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv". Du må også ha en Excel-fil som importeres når du oppretter malen. Denne filen kan åpnes fra: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx


## <a name="upload-the-payments-data-model-configuration"></a>Laste opp modellkonfigurasjon for betalingsdata
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Merk den valgte raden i listen.
    * Velg konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".  
3. Klikk Angi som aktiv
4. Klikk Repositorier.
    * Velg et repositorium for operasjonsressurstypen, hvis tilgjengelig. Hvis den er tilgjengelige, hopper du over følgende trinn for hvordan du oppretter et nytt repositorium.  
5. Klikk Legg til for å åpne nedtrekksdialogen.
6. Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.
7. Klikk Opprett repositorium.
8. Klikk OK.
9. Klikk Åpne.
10. Velg Betalingsmodell i treet.
11. Klikk Importer.
    * Importer denne datamodellen. Den vil bli brukt som datakilde i en ny formatkonfigurasjon. Hopp over dette trinnet hvis denne konfigurasjonen allerede er importert.  
12. Klikk Ja.
13. Lukk siden.
14. Lukk siden.

## <a name="create-a-new-format-configuration"></a>Opprette en ny formatkonfigurasjon
1. Klikk Rapporteringskonfigurasjoner.
2. Velg Betalingsmodell i treet.
3. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
4. I feltet Ny angir du Format basert på datamodell PaymentModel.
    * Opprett et format som er basert på PaymentModel-datamodellen.  
5. Skriv inn Regnearkeksempelrapport i feltet Navn.
    * Regnearkeksempelrapport  
6. Skriv inn Regnearkeksempelrapport for leverandørenes betalinger i Beskrivelse-feltet.
    * Regnearkeksempelrapport for leverandørenes betalinger.  
7. Angi eller velg en verdi i feltet Definisjon av datamodell.
    * Velg definisjonen CustomerCreditTransferInitiation.  
8. Klikk Opprett konfigurasjon.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Utforme et nytt dokument i OPENXML-regnearkformat
1. Velg Betalingsmodell\Regnearkeksempelrapport i treet.
2. Klikk Utforming.
3. Klikk Import i handlingsruten.
4. Klikk Importer fra Microsoft Excel.
5. Klikk Vedlegg.
    * Knytte det eksisterende Excel-dokumentet til som en mal.  
6. Klikk Ny.
7. Klikk Fil.
    * Velg den eksisterende Excel-filen.  
8. Lukk siden.
9. Angi eller velg en verdi i feltet Mal.
    * Velg at den vedlagte Excel-filen skal brukes som en mal.  
10. Klikk OK.
    * Legg merke til at ER-formatkomponenter er opprettet i utformingsformatet basert på strukturen til det refererende MS Excel-dokumentet (navngitte områder).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Opprette en ny datakilde for å beregne totaler etter valutakoder
1. Klikk kategorien Tilordning.
2. Klikk Legg til rot for å åpne nedtrekksdialogen.
3. Velg Funksjoner\Grupper etter i treet.
4. Skriv inn PaymentByCurrency i Navn-feltet.
    * PaymentByCurrency  
5. Klikk Rediger gruppe etter.
6. Utvid noden 'model' i treet.
7. Velg modell\Betalinger i treet.
8. Klikk Legg til felt i.
9. Klikk Hva skal grupperes.
10. Utvid modell\Betalinger i treet.
11. Velg model\Payments\Currency i treet.
12. Klikk Legg til felt i.
13. Klikk Grupperte felt.
14. Velg model\Payments\Instructed Amount(InstructedAmount) i treet.
15. Klikk Legg til felt i.
16. Klikk Aggregeringsfelt.
17. Velg et alternativ i Metode-feltet.
    * Velg mengdefunksjonen SUM.  
18. Skriv inn TotalInstructuredAmount i Navn-feltet.
    * TotalInstructuredAmount  
19. Klikk Lagre.
20. Lukk siden.
21. Klikk OK.

## <a name="map-format-components-to-data-sources"></a>Tilordne formatkomponenter til datakilder
1. Utvid noden 'model' i treet.
2. Utvid modell\Betalinger i treet.
3. Vis modell\Betalinger\Initialiseringspart(InitiatingParty) i treet.
4. Velg model\Payments\Initiating Party(InitiatingParty)\Name i treet.
5. Vis Excel\ReportHeader i treet.
6. Velg Excel\ReportHeader\CompanyName i treet.
7. Klikk Bind.
8. Utvid modell\Betalinger\Kreditor i treet.
9. Vis modell\Betalinger\Kreditor\Identifikasjon i treet.
10. Velg model\Payments\Creditor\Identification\Source ID(SourceID) i treet.
11. Vis Excel\PaymLines i treet.
12. Velg Excel\PaymLines\VendAccountName i treet.
13. Klikk Bind.
14. I treet velger du modell\Betalinger\Kreditor\Navn.
15. Velg Excel\PaymLines\VendName i treet.
16. Klikk Bind.
17. Vis modell\Betalinger\Kreditoragent(CreditorAgent) i treet.
18. Velg model\Payments\Creditor Agent(CreditorAgent)\Name i treet.
19. Velg Excel\PaymLines\Bank i treet.
20. Klikk Bind.
21. Velg model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber) i treet.
22. Velg Excel\PaymLines\RoutingNumber i treet.
23. Klikk Bind.
24. Utvid model\Payments\Creditor Account(CreditorAccount) i treet.
25. Utvid model\Payments\Creditor Account(CreditorAccount)\Identification i treet.
26. Velg model\Payments\Creditor Account(CreditorAccount)\Identification\Number i treet.
27. Velg Excel\PaymLines\AccountNumber i treet.
28. Klikk Bind.
29. Velg model\Payments\Instructed Amount(InstructedAmount) i treet.
30. Velg Excel\PaymLines\Debit i treet.
31. Klikk Bind.
32. Utvid modell\Betalinger\Kreditor i treet.
33. Utvid model\Payments\Creditor Account(CreditorAccount) i treet.
34. Vis modell\Betalinger\Kreditoragent(CreditorAgent) i treet.
35. Velg model\Payments\Currency i treet.
36. Velg Excel\PaymLines\Valuta i treet.
37. Klikk Bind.
38. Vis PaymentByCurrency i treet.
39. Vis PaymentByCurrency\grouped i treet.
40. Velg PaymentByCurrency\grouped\Currency i treet.
41. Vis Excel\SummaryLines i treet.
42. Velg Excel\SummaryLines\SummaryCurrency i treet.
43. Klikk Bind.
44. Vis PaymentByCurrency\aggregated i treet.
45. Velg PaymentByCurrency\aggregated\TotalInstructuredAmount i treet.
46. Velg Excel\SummaryLines\SummaryAmount i treet.
47. Klikk Bind.
48. Velg PaymentByCurrency i treet.
49. Velg Excel\SummaryLines i treet.
50. Klikk Bind.
51. Velg modell\Betalinger i treet.
52. Velg Excel\PaymLines i treet.
53. Klikk Bind.
54. Klikk Lagre.
55. Lukk siden.

## <a name="use-the-created-configuration-for-payments-processing"></a>Bruke den opprettede konfigurasjonen for behandling av betalinger
1. Klikk Endre status.
2. Klikk Fullført.
3. Klikk OK.
4. Lukk siden.
5. Lukk siden.
6. Gå til Leverandører > Betalingsoppsett > Betalingsmåter.
7. Bruk hurtigfilteret til å filtrere på Betalingsmåte-feltet med verdien Elektronisk.
    * Elektronisk  
8. Klikk Rediger.
9. Vis delen Filformater.
10. Velg Ja i feltet Generell elektronisk rapportering.
11. Angi eller velg en verdi i feltet Eksportformatkonfigurasjon.
    * Velg konfigurasjonen Regnearkeksempelrapport.  
12. Klikk Lagre.
13. Lukk siden.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Bruke den opprettede konfigurasjonen for testing av behandling av betalingsjournaler
1. Gå til Leverandører > Betalinger > Betalingsjournal.
2. Klikk Ny.
    * Opprett ny betalingsjournal.  
3. Skriv inn VendPay i Navn-feltet.
    * VendPay  
4. Klikk Linjer.
5. Angi verdiene GB_SI_000001 i Konto-feltet.
    * GB_SI_000001  
6. Sett Debet til 1000.
7. Klikk Ny.
8. Angi verdiene GB_SI_000005 i Konto-feltet.
    * GB_SI_000005  
9. Sett Debet til 2000.
10. Skriv inn EUR i feltet Valuta.
    * EUR  
11. Angi verdiene GBSI OPER i Motkonto-feltet.
    * GBSI OPER  
12. Skriv inn Elektronisk i Betalingsmåte-feltet.
    * Elektronisk  
13. Klikk Lagre.
14. Klikk Generer betalinger.
15. Skriv inn Elektronisk i Betalingsmåte-feltet.
    * Elektronisk  
16. Skriv inn Betalinger i Filnavn-feltet.
    * Skriv for eksempel inn Betalinger.  
17. Skriv inn GBSI OPER i feltet Bankkonto.
    * GBSI OPER  
18. Klikk OK.
19. Klikk OK.
    * Se gjennom det opprettede regnearket, inkludert detaljer om betalingslinjer samt totalene for hver valutakode som brukes i denne betalingsmeldingen.  


