---
title: ER Konfigurere format for å utføre telling og summering (del 2 - Konfigurere beregninger)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ef657b13bc1f7f4a84676821e4175ace32c069a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "338918"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2-configure-computations"></a>ER Konfigurere format for å utføre telling og summering (del 2: Konfigurere beregninger)

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 1: Opprette format)".

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Opprette en formatkonfigurasjon for å legge til tellings- og summeringsdetaljer
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Rapporteringskonfigurasjoner.
3. Utvid Intrastat-modell i treet.
4. Velg Intrastat-modell\Intrastat (DE) i treet.
    * Anta at du må tilpasse formatet fra Microsoft ved å legge til linjer med sammendragsdetaljer på slutten av Intrastat-rapporten. Du må gjøre dette ved å avlede vår egen forekomst av Intrastat-konfigurasjonen fra Microsoft-forekomsten for å gjøre endringer.  
5. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
6. I Ny-feltet angir du Avled fra navnet: Intrastat (DE), Microsoft.
7. I Navn-feltet skriver du inn Intrastat (DE) med telling og summering.
8. Klikk Opprett konfigurasjon.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Konfigurere denne rapporten for å utføre telling og summering basert på utdatadetaljene
1. Klikk Utforming.
2. Velg Ja i feltet Samle inn utdatadetaljer.
    * Dette flagget vil under kjøring aktivere prosessen for innsamling av utdatadetaljer for generering av Intrastat-filen.  
    * Du må utføre telling for forskjellige Intrastat-retninger, så legg til en dedikert modellopplisting i datakildenes liste for denne formatkonfigurasjonen.  
3. Klikk kategorien Tilordning.
4. Klikk Legg til rot for å åpne nedtrekksdialogen.
5. Velg Datamodell\Opplisting i treet.
6. I Navn-feltet skriver du inn Retning-
7. Angi eller velg en verdi i Modellopplisting-feltet.
    * Velg verdien Retning.  
8. Klikk OK.
9. Klikk Legg til rot for å åpne nedtrekksdialogen.
10. Velg Funksjoner\Beregnet felt i treet.
11. Skriv inn $BlockName i Navn-feltet.
12. Klikk Rediger formel.
13. Skriv inn block i Formel-feltet.
14. Klikk Lagre.
15. Lukk siden.
16. Klikk OK.
17. Klikk Legg til rot for å åpne nedtrekksdialogen.
18. Velg Funksjoner\Beregnet felt i treet.
19. Skriv inn $RecName i Navn-feltet.
20. Klikk Rediger formel.
21. Skriv inn record i Formel-feltet.
22. Klikk Lagre.
23. Lukk siden.
24. Klikk OK.
25. Klikk Legg til rot for å åpne nedtrekksdialogen.
26. Velg Funksjoner\Beregnet felt i treet.
27. Skriv inn $InvName i Navn-feltet.
28. Klikk Rediger formel.
29. Skriv inn InvoicedAmountEUR i Formel-feltet.
30. Klikk Lagre.
31. Lukk siden.
32. Klikk OK.
33. Velg Intrastat\Data i treet.
34. Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.
35. Klikk Legg til datakilde.
    * $BlockName  
36. Klikk Lagre.
37. Lukk siden.
38. Klikk Rediger-knappen for feltet Verdi for innsamlet datanøkkel.
39. Angi IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export") i Formel-feltet.
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. Klikk Lagre.
41. Lukk siden.
    * Tell linjene i denne sekvensen. Resultatene vil bli brukt med navnet "blokk" separat for forskjellige retninger. Verdien "Import" vil bli brukt for hvilke som helst Intrastat-transaksjoner for ankomster. Verdien "Eksport" vil bli brukt for hvilke som helst Intrastat-transaksjoner for utsendelser. Se på dette som et virtuelt Excel-regneark. For hver transaksjon fylles det ut en rad der den første kolonnen"blokk" fylles ut med verdiene "Import" og "Eksport".  
42. Utvid Intrastat\Data: Sekvens i treet.
43. Velg Intrastat\Data: Sekvens\Ankomster? i treet.
44. Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.
    * Tell linjene i denne sekvensen. Resultatene blir lagret ved hjelp av navnet "post".  
45. Velg $RecName i treet.
46. Klikk Legg til datakilde.
47. Klikk Lagre.
48. Lukk siden.
49. Klikk Rediger-knappen for feltet Verdi for innsamlet datanøkkel.
50. I Formel-feltet skriver du inn Intrastat.CommodityRecord.CommodityCode.
51. Klikk Lagre.
52. Lukk siden.
    * Tell linjene i denne sekvensen. Resultatene vil bli brukt med navnet "post" separat for forskjellige varekoder. Se på dette som et virtuelt Excel-regneark. For hver transaksjon fylles det ut en rad der den første kolonnen "blokk" fylles ut med verdiene "Import" og "Export" henholdsvis, og den andre blokken "post" med varekodeverdien  
53. Velg Intrastat\Data: Sekvens\Fordelinger? i treet.
54. Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.
55. Velg $RecName i treet.
56. Klikk Legg til datakilde.
57. Klikk Lagre.
58. Lukk siden.
59. Klikk Rediger-knappen for feltet Verdi for innsamlet datanøkkel.
60. I Formel-feltet skriver du inn Intrastat.CommodityRecord.CommodityCode.
61. Klikk Lagre.
62. Lukk siden.
63. Utvid Intrastat\Data: Sekvens\Fordelinger: Sekvens? i treet.
64. Utvid Intrastat\Data: Sekvens\Fordelinger: Sekvens?\Post = Intrastat.CommodityRecord i treet.
65. Klikk Formater-kategorien.
66. Velg Intrastat\Data\Fordelinger\Post\Fakturabeløp EUR i treet.
67. Klikk kategorien Tilordning.
68. Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.
69. Velg $InvName i treet.
70. Klikk Legg til datakilde.
71. Klikk Lagre.
72. Lukk siden.
    * Summer de fakturerte beløpsverdiene for linjer i denne sekvensen. Resultatene vil bli brukt med navnet "InvoicedAmountEUR" separat for forskjellige Intrastat-retninger og varekoder. Se på dette som en virtuell opprettelse i Excel-regneark. For hver transaksjon fylles det ut en rad der den første kolonnen"blokk" fylles ut med verdiene "Import" og "Eksport". Den andre blokken "post" fylles ut med varekodeverdien og den tredje kolonnen "InvoicedAmountEUR" fylles ut med fakturabeløpsverdien.  
73. Utvid Intrastat\Data\Ankomster? i treet.
74. Utvid Intrastat\Data\Ankomster?\Post = Intrastat.CommodityRecord i treet.
75. Klikk Formater-kategorien.
76. Velg Intrastat\Data\Ankomster\Post\Fakturabeløp EUR i treet.
77. Klikk kategorien Tilordning.
78. Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.
79. Velg $InvName i treet.
80. Klikk Legg til datakilde.
81. Klikk Lagre.
82. Lukk siden.
83. Klikk Lagre.
84. Lukk siden.

