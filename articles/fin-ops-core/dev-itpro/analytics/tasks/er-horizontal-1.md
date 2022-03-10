---
title: ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 1 - Utforme format)
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det genererer rapporter som OPENXML-regnearkfiler (Excel). (Del 1)
author: NickSelin
ms.date: 04/23/2021
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
ms.openlocfilehash: ab360c259af37ce3995d3cd2560bc2e765e0bceb
ms.sourcegitcommit: e3290eb58ae569a59d6ae2e6922e7d8be8f1980f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2021
ms.locfileid: "7551782"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 1 - Utforme format)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre disse tre oppgaveveiledningene:

"ER Opprette en konfigurasjonsleverandør og merke den som aktiv"

"ER Bruke finansdimensjoner som en datakilde (del 1: Utforme datamodell)"

"ER Bruke finansdimensjoner som en datakilde (del 2: Modelltilordning)"

Du må også laste ned og lagre en lokal kopi av malen med en eksempelrapport som finnes her: [Eksempel på webtjenesterapport i Finansdimensjoner](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.

## <a name="create-a-new-report-configuration"></a>Opprette en ny rapportkonfigurasjon

1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Velg `Financial dimensions sample model` i treet.
3. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
4. I Ny-feltet angir du `Format based on data model Financial dimensions sample model`.
    * Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.  
5. I Navn-feltet skriver du inn `Sample report with horizontally expandable ranges`.
    * Eksempelrapport med vannrett utvidbare områder  
6. I Beskrivelse-feltet skriver du inn `To make Excel output with dynamically adding columns`.
    * Lage Excel-utdata ved å legge til kolonner dynamisk  
7. Velg Oppføring i Definisjon av datamodell-feltet.
8. Klikk på Opprett konfigurasjon.

## <a name="design-the-report-format"></a>Utforme rapportformatet

1. Klikk på Utforming.
2. Slå på veksleknappen `Show details`.
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
12. Velg `Excel\Range` i treet.
13. Skriv inn `DimNames` i Excel-område-feltet.
    * DimNames  
14. Velg `Horizontal` i feltet Replikeringsretning.
15. Klikk på OK.
16. Velg `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` i treet.
17. Klikk på Flytt opp.
18. Velg `Excel = "SampleFinDimWsReport"\Cell<DimNames>` i treet.
19. Klikk på Klipp ut.
20. Velg `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` i treet.
21. Klikk på Lim inn.
22. Utvid `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` i treet.
23. Utvid `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical` i treet.
24. Utvid `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` i treet.
25. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` i treet.
    * Legg til et nytt område for å opprette Excel-utdata dynamisk med like mange kolonner som du valgte (i brukerdialogskjemaet) for finansdimensjoner. Hver celle for hver enkelt kolonne vil representere verdien for én finansdimensjon for hver rapporteringstransaksjon.  
26. Klikk på Legg til område.
27. Skriv inn `DimValues` i Excel-område-feltet.
    * DimValues  
28. Velg `Horizontal` i feltet Replikeringsretning.
29. Klikk på OK.
30. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>` i treet.
31. Klikk på Klipp ut.
32. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` i treet.
33. Klikk på Lim inn.
34. Utvid `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` i treet.

## <a name="map-format-elements-to-data-sources"></a>Tilordne formatelementer til datakilder

1. Klikk på fanen Tilordning.
2. Utvid `model: Data model Financial dimensions sample model` i treet.
3. Utvid `model: Data model Financial dimensions sample model\Journal: Record list` i treet.
4. Utvid `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list` i treet.
5. Utvid `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list` i treet.
6. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>` i treet.
7. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String` i treet.
8. Klikk på Bind.
9. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` i treet.
10. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list` i treet.
11. Klikk på Bind.
12. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>` i treet.
13. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real` i treet.
14. Klikk på Bind.
15. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>` i treet.
16. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real` i treet.
17. Klikk på Bind.
18. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>` i treet.
19. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String` i treet.
20. Klikk på Bind.
21. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>` i treet.
22. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date` i treet.
23. Klikk på Bind.
24. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>` i treet.
25. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String` i treet.
26. Klikk på Bind.
27. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>` i treet.
28. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String` i treet.
29. Klikk på Bind.
30. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` i treet.
31. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list` i treet.
32. Klikk på Bind.
33. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>` i treet.
34. Velg `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String` i treet.
35. Klikk på Bind.
36. Velg `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical` i treet.
37. Velg `model: Data model Financial dimensions sample model\Journal: Record list` i treet.
38. Klikk på Bind.
39. Utvid `model: Data model Financial dimensions sample model\Dimensions setting: Record list` i treet.
40. Velg `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String` i treet.
41. Velg `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>` i treet.
42. Klikk på Bind.
43. Velg `model: Data model Financial dimensions sample model\Dimensions setting: Record list` i treet.
44. Velg `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` i treet.
45. Klikk på Bind.
46. Velg `Excel = "SampleFinDimWsReport"\Cell<CompanyName>` i treet.
47. Velg `model: Data model Financial dimensions sample model\Company: String` i treet.
48. Klikk på Bind.
49. Klikk på Lagre.
50. Lukk siden.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
