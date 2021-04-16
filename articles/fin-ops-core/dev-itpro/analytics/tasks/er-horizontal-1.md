---
title: ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 1 - Utforme format)
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det genererer rapporter som OPENXML-regnearkfiler (Excel). (Del 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9eef9ffaadbd7010129cc9850ded1ba67bc281d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745017"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 1 - Utforme format)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre disse tre oppgaveveiledningene: 

"ER Opprette en konfigurasjonsleverandør og merke den som aktiv"

"ER Bruke finansdimensjoner som en datakilde (del 1: Utforme datamodell)"

"ER Bruke finansdimensjoner som en datakilde (del 2: Modelltilordning)"

Du må også laste ned og lagre en lokal kopi av malen med en eksempelrapport som finnes her: [Eksempel på webtjenesterapport i Finansdimensjoner](https://go.microsoft.com/fwlink/?linkid=862266).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="create-a-new-report-configuration"></a>Opprette en ny rapportkonfigurasjon
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Velg Eksempelmodell for finansdimensjoner i treet.
3. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
4. I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.
    * Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.  
5. Skriv inn Eksempelrapport med vannrett utvidbare områder i Navn-feltet.
    * Eksempelrapport med vannrett utvidbare områder  
6. I Beskrivelse-feltet skriver du inn Lage Excel-utdata ved å legge til kolonner dynamisk.
    * Lage Excel-utdata ved å legge til kolonner dynamisk  
7. Velg Oppføring i Definisjon av datamodell-feltet.
8. Klikk på Opprett konfigurasjon.

## <a name="design-the-report-format"></a>Utforme rapportformatet
1. Klikk på Utforming.
2. Slå på veksleknappen Vis detaljer.
3. Klikk på Import i handlingsruten.
4. Klikk på Importer fra Excel.
5. Klikk på Vedlegg.
    * Importer malen for rapporten. Bruk Excel-filen som du lastet ned for dette.  
6. Klikk på Ny.
7. Klikk på Fil.
8. Lukk siden.
9. Angi eller velg en verdi i feltet Mal.
    * Velg malen du lastet ned.  
10. Klikk på OK.
    * Legg til et nytt område for å opprette Excel-utdata dynamisk med like mange kolonner som du valgte (i brukerdialogskjemaet) for finansdimensjoner. Hver celle for hver enkelt kolonne vil representere navnet på én finansdimensjon.  
11. Klikk på Legg til for å åpne nedtrekksdialogen.
12. Velg Excel\Område i treet.
13. Skriv inn DimNames i feltet Excel-område.
    * DimNames  
14. Velg Vannrett i feltet Replikeringsretning.
15. Klikk på OK.
16. Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.
17. Klikk på Flytt opp.
18. Velg 'Excel = "SampleFinDimWsReport"\Celle<DimNames>' i treet.
19. Klikk på Klipp ut.
20. Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.
21. Klikk på Lim inn.
22. Utvid 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.
23. Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett' i treet.
24. Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.
25. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.
    * Legg til et nytt område for å opprette Excel-utdata dynamisk med like mange kolonner som du valgte (i brukerdialogskjemaet) for finansdimensjoner. Hver celle for hver enkelt kolonne vil representere verdien for én finansdimensjon for hver rapporteringstransaksjon.  
26. Klikk på Legg til område.
27. Skriv inn DimValues i feltet Excel-område.
    * DimValues  
28. Velg Vannrett i feltet Replikeringsretning.
29. Klikk på OK.
30. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<DimValues>' i treet.
31. Klikk på Klipp ut.
32. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.
33. Klikk på Lim inn.
34. Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.

## <a name="map-format-elements-to-data-sources"></a>Tilordne formatelementer til datakilder
1. Klikk på fanen Tilordning.
2. Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.
3. Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.
4. Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.
5. Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.
6. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett\celle<DimValues>' i treet.
7. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.
8. Klikk på Bind.
9. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.
10. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.
11. Klikk på Bind.
12. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Credit>' i treet.
13. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.
14. Klikk på Bind.
15. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Debit>' i treet.
16. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.
17. Klikk på Bind.
18. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Currency>' i treet.
19. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.
20. Klikk på Bind.
21. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransDate>' i treet.
22. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.
23. Klikk på Bind.
24. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransVoucher>' i treet.
25. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.
26. Klikk på Bind.
27. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransBatch>' i treet.
28. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.
29. Klikk på Bind.
30. Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.
31. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.
32. Klikk på Bind.
33. Velg Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett/celle<Batch> i treet.
34. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.
35. Klikk på Bind.
36. Velg Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett i treet.
37. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.
38. Klikk på Bind.
39. Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste i treet.
40. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste\Kode: Streng i treet.
41. Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett\celle<DimNames>' i treet.
42. Klikk på Bind.
43. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste i treet.
44. Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.
45. Klikk på Bind.
46. Velg 'Excel = "SampleFinDimWsReport"\Celle<CompanyName>' i treet.
47. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.
48. Klikk på Bind.
49. Klikk på Lagre.
50. Lukk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]