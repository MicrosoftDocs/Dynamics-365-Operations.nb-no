---
title: ER Konfigurere format for å utføre telling og summering (del 3 - Bruke beregninger for å lage utdataene)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b26a7f50a2237e0d3d756f8eebf2e4cd81f24683
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684673"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>ER Konfigurere format for å utføre telling og summering (del 3 - Bruke beregninger for å lage utdataene)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 2: Konfigurere beregninger)".

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Konfigurere denne rapporten for å bruke tellings- og summeringsinformasjon
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Rapporteringskonfigurasjoner.
3. Utvid Intrastat-modell i treet.
4. Utvid Intrastat-modell\Intrastat (DE) i treet.
5. Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.
6. Klikk Utforming.
7. Klikk kategorien Tilordning.
8. Klikk Legg til rot for å åpne nedtrekksdialogen.
    * Legg til en ny datakilde for å hente listen over lagrede blokker.  
9. Velg Funksjoner\Beregnet felt i treet.
10. Skriv inn $BlocksList i Navn-feltet.
    * $BlocksList  
11. Klikk Rediger formel.
12. I treet velger du Datainnsamlingsfunksjoner\COLLECTEDLIST.
13. Klikk Legg til funksjon.
14. Klikk Legg til datakilde.
15. Skriv inn "COLLECTEDLIST('$BlockName', " i Formel-feltet.
    * COLLECTEDLIST('$BlockName',  
16. Skriv inn COLLECTEDLIST('$BlockName', "*") i Formel-feltet.
    * COLLECTEDLIST('$BlockName', "*")  
17. Klikk Lagre.
    * Mønsteret "*" betyr at alle blokker vil bli inkludert i listen for denne posten.  
18. Lukk siden.
19. Klikk OK.
20. Klikk Formater-kategorien.
21. Velg Intrastat\Data i treet.
22. Klikk Legg til for å åpne nedtrekksdialogen.
23. Velg Tekst\Sekvens i treet.
24. Skriv inn Totalsummer etter blokker i Navn-feltet.
    * Totalsummer etter blokker  
25. Velg Ny linje - Windows (CR LF) i Spesialtegn-feltet.
26. Klikk OK.
27. Velg Intrastat\Data\Totalsummer etter blokker i treet.
28. Klikk Legg til for å åpne nedtrekksdialogen.
29. Velg Tekst\Streng i treet.
30. I Navn-feltet skriver du inn Blokkode.
    * Blokkode  
31. Klikk OK.
32. Klikk Legg til streng.
33. Skriv inn Linjetelling i Navn-feltet.
    * Linjetelling  
34. Klikk OK.
35. Klikk Legg til streng.
36. I Navn-feltet skriver du inn Totalbeløp.
    * Totalbeløp  
37. Klikk OK.
38. Klikk kategorien Tilordning.
39. Velg $BlocksList i treet.
40. Klikk Bind.
    * Opprett en summeringslinje for hver lagret blokk.  
41. Klikk Formater-kategorien.
42. Velg Intrastat\Data\Totalsummer etter blokker\Blokkode i treet.
43. Klikk kategorien Tilordning.
44. Klikk Rediger formel.
45. Skriv inn '"Block id: " & ' i Formel-feltet.
    * "Block id: " &  
46. Utvid $BlocksList i treet.
47. Velg $BlocksList\Verdi i treet.
48. Klikk Legg til datakilde.
49. Klikk Lagre.
50. Lukk siden.
51. Klikk Formater-kategorien.
52. Velg Intrastat\Data\Totalsummer etter blokker\Linjetelling i treet.
53. Klikk kategorien Tilordning.
54. Klikk Rediger formel.
    * Opprett utdata for antallet linjer for hver blokk som er presentert i denne rapporten.  
55. Skriv inn '"Antall linjer i denne blokken: " & ' i Formel-feltet.
    * "Antall linjer i denne blokken: " &  
56. Skriv inn '"Antall linjer i denne blokken: " & TEXT('. i Formel-feltet.
    * "Antall linjer i denne blokken: " & TEXT(   
57. I treet velger du Datainnsamlingsfunksjoner\COUNTIFS.
58. Klikk Legg til funksjon.
59. Klikk Legg til datakilde.
60. Skriv inn '"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName',' i Formel-feltet.
    * "Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName',  
61. Utvid $BlocksList i treet.
62. Velg $BlocksList\Verdi i treet.
63. Klikk Legg til datakilde.
64. Skriv inn '"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ' i Formel-feltet.
    * "Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. Velg $RecName i treet.
66. Klikk Legg til datakilde.
67. Skriv inn '"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.
    * "Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Klikk Lagre.
69. Lukk siden.
70. Klikk Formater-kategorien.
71. Velg Intrastat\Data\Totalsummer etter blokker\Totalbeløp i treet.
72. Klikk kategorien Tilordning.
73. Klikk Rediger formel.
    * Opprett utdata som skal være summen av det fakturerte beløpet for hver blokk presentert i denne rapporten.  
74. Skriv inn '"Sum av fakturert beløp: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))' i Formel-feltet.
    * "Sum av fakturert beløp: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Klikk Lagre.
76. Lukk siden.
77. Klikk Lagre.
78. Lukk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]