---
title: ER Bruke finansdimensjoner som en datakilde (del 2 - Modelltilordning)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92efd6a0b36471286c292a80542b81cd14a8eff3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551351"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2-model-mapping"></a>ER Bruke finansdimensjoner som en datakilde (del 2: Modelltilordning)

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 1: Utforme datamodell).


## <a name="add-required-data-sources-to-model-mapping"></a>Legge til obligatoriske datakilder i modelltilordning
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Velg Eksempelmodell for finansdimensjoner i treet.
3. Klikk Utforming.
4. Klikk Tilordne modell til datakilde.
5. Klikk Ny.
6. Velg Oppføring i Definisjon-feltet.
7. Skriv inn Dimensjonsdatatilordning i Navn-feltet.
8. Skriv inn Dimensjonsdatatilordning i Beskrivelse-feltet.
9. Klikk Lagre.
10. Klikk Utforming.
11. Velg Dynamics 365 for Operations\Tabell i treet.
12. Klikk Legg til rot.
13. I Navn-feltet skriver du inn Firma.
14. Skriv inn CompanyInfo i Tabell-feltet.
15. Klikk OK.
16. Velg Funksjoner\Detaljer for finansdimensjoner i treet.
17. Klikk Legg til rot.
    * Denne datakilden angir hvordan omfanget av finansdimensjoner defineres for en rapport som skal bruke denne modellen som datakilde.  
18. Skriv inn en verdi i Navn-feltet.
19. Velg Ja i feltet Be om dimensjoner.
    * Velg Ja hvis du vil at brukeren skal kunne velge dimensjoner under kjøring i dialogboksskjemaet Bruker. Hvis satt til Nei, brukes alle finansdimensjoner for den gjeldende forekomsten som standard.  
20. Velg Juridisk enhet i feltet Valg av finansdimensjoner.
    * Velg Alle for å la brukeren velge ønskede dimensjoner for gjeldende forekomst i oppslagsfeltet.  Velg Juridisk enhet for å la brukeren velge dimensjoner for firmaet i oppslagsfeltet.  Velg Dimensjon for å la brukeren velge dimensjoner ved hjelp av et enkelt dimensjonssett.  
21. Velg Ja i feltet Be om hovedkonto.
    * Sett Be om hovedkonto til Ja for å tillate brukere å velge hovedkontoen som en del av listen med dimensjoner.   Hvis satt til Nei, blir ikke hovedkontoen tatt med i listen over dimensjoner, og alternativet Er obligatorisk for hovedkonto aktiveres. Hvis Er obligatorisk for hovedkonto settes til Ja, inkluderes hovedkontoen i listen over dimensjonere uavhengig av brukerens valg.  
22. Klikk OK.
23. Velg Dynamics 365 for Operations\Tabellposter i treet.
24. Klikk Legg til rot.
25. Skriv inn LedgerJournal i Navn-feltet.
26. Velg Ja i feltet Be om spørring.
27. Skriv inn LedgerJournalTable i Tabell-feltet.
28. Klikk OK.

## <a name="map-data-model-elements-to-added-data-sources"></a>Tilordne datamodellelementer til datakilder som er lagt til
1. Utvid Journal i treet.
2. Utvid Journal\Transaksjon i treet.
3. Utvid Journal\Transaksjon\Dimensjonsdata i treet.
4. Utvid Dimensjonsinnstilling i treet.
5. Utvid LedgerJournal i treet.
6. Utvid LedgerJournal\<Relasjoner i treet.
7. Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans i treet.
8. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Bilag i treet.
9. Velg Journal\Transaksjon\Bilag i treet.
10. Klikk Bind.
11. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension) i treet.
    * Merk at for alle referanser til finansdimensjoner som settes til, for eksempel LedgerDimension, er et tilsvarende datakildeelement tilgjengelig (LedgerDimension.Dimension). Dette datakildeelementet tilbyr finansdimensjonene for dette dimensjonssettet som postens liste.  
12. Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension) i treet.
13. Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner i treet.
14. Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi i treet.
15. Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Definisjon i treet.
16. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Definisjon\Navn i treet.
17. Velg Journal\Transaksjon\Dimensjonsdata\Navn i treet.
18. Klikk Bind.
19. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi\Beskrivelse i treet.
20. Velg Journal\Transaksjon\Dimensjonsdata\Beskrivelse i treet.
21. Klikk Bind.
22. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi\Kode i treet.
23. Velg Journal\Transaksjon\Dimensjonsdata\Kode i treet.
24. Klikk Bind.
25. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner i treet.
26. Velg Journal\Transaksjon\Dimensjonsdata i treet.
27. Klikk Bind.
28. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Debet(AmountCurDebit) i treet.
29. Velg Journal\Transaksjon\Debet i treet.
30. Klikk Bind.
31. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Dato(TransDate) i treet.
32. Velg Journal\Transaksjon\Dato i treet.
33. Klikk Bind.
34. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Valuta(CurrencyCode) i treet.
35. Velg Journal\Transaksjon\Valuta i treet.
36. Klikk Bind.
37. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Kredit(AmountCurCredit) i treet.
38. Velg Journal\Transaksjon\Kredit i treet.
39. Klikk Bind.
40. Velg LedgerJournal\<Relasjoner\LedgerJournalTrans i treet.
41. Velg Journal\Transaksjon i treet.
42. Klikk Bind.
43. Velg LedgerJournal\Journalpartinummer(JournalNum) i treet.
44. Velg Journal\Parti i treet.
45. Klikk Bind.
46. Velg LedgerJournal i treet.
47. Velg Journal i treet.
48. Klikk Bind.
49. Utvid Dimensjoner i treet.
50. Utvid Dimensjoner\Hovedkonto og dimensjoner i treet.
51. Utvid Dimensjoner\Hovedkonto og dimensjoner\Definisjon i treet.
52. Velg Dimensjoner\Hovedkonto og dimensjoner\Definisjon\Navn i treet.
53. Velg Dimensjonsinnstilling\Kode i treet.
54. Klikk Bind.
55. Velg Dimensjoner\Hovedkonto og dimensjoner\Definisjon\Rapportkolonnenavn i treet.
56. Velg Dimensjonsinnstilling\Navn i treet.
57. Klikk Bind.
58. Velg Dimensjoner\Hovedkonto og dimensjoner i treet.
59. Velg Dimensjonsinnstilling i treet.
60. Klikk Bind.
61. Velg Firma i treet.
62. Klikk Rediger.
63. Angi Company.'find()'.'name()' i feltet expressionAsStringText.
    * Company.'find()'.'name()'  
64. Klikk Lagre.
65. Lukk siden.
66. Klikk Lagre.
67. Lukk siden.

## <a name="complete-this-draft-models-version"></a>Fullføre versjonen av denne utkastmodellen
1. Lukk siden.
2. Lukk siden.
3. Klikk Endre status.
4. Klikk Fullført.
5. Klikk OK.

