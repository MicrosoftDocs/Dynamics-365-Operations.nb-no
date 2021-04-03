---
title: ER Bruke finansdimensjoner som en datakilde (del 1 - Utforme datamodell)
description: Dette emnet beskriver hvordan du konfigurerer en ER-modell (Elektronisk rapportering) for å bruke finansdimensjoner som en datakilde for ER-rapporter. (Del 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570198"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a>ER Bruke finansdimensjoner som en datakilde (del 1 - Utforme datamodell)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".


## <a name="create-a-new-data-model"></a>Opprette en ny datamodell
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Forsikre deg om at leverandøren Litware, Inc er tilgjengelig og merket som aktiv.  
2. Klikk på Rapporteringskonfigurasjoner.
3. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
4. Skriv inn Eksempelmodell for finansdimensjoner i Navn-feltet.
5. Klikk på Opprett konfigurasjon.
6. Klikk på Utforming.
7. Klikk på Ny for å åpne nedtrekksdialogen.
8. I Navn-feltet skriver du inn Oppføring.
9. Klikk på Legg til.
10. Klikk på Ny for å åpne nedtrekksdialogen.
11. I Navn-feltet skriver du inn Firma.
12. Klikk på Legg til.
    * Vi vil legge til en ny postliste i modellen vår. Denne listen vil vise (for ER-rapporter som bruker denne modellen som datakilde) innstillingene for valgte finansdimensjoner. Hver finansdimensjon vil bli presentert i denne listen som en post med aktuelle felt som representerer dimensjonens innstilling.  
13. Klikk på Ny for å åpne nedtrekksdialogen.
14. Skriv inn Dimensjonsinnstilling i Navn-feltet.
15. Velg Postliste i Varetype-feltet.
16. Klikk på Legg til.
17. Klikk på Ny for å åpne nedtrekksdialogen.
18. I Navn-feltet skriver du inn Kode.
19. Velg Streng i Varetype-feltet.
20. Klikk på Legg til.
21. Klikk på Ny for å åpne nedtrekksdialogen.
22. I Navn-feltet skriver du inn Navn.
23. Klikk på Legg til.
24. Velg Oppføring i treet.
25. Klikk på Ny for å åpne nedtrekksdialogen.
26. I Navn-feltet skriver du inn Journal.
27. Velg Postliste i Varetype-feltet.
28. Klikk på Legg til.
29. Klikk på Ny for å åpne nedtrekksdialogen.
30. Skriv inn Parti i Navn-feltet.
31. Velg Streng i Varetype-feltet.
32. Klikk på Legg til.
33. Klikk på Ny for å åpne nedtrekksdialogen.
34. Skriv inn Transaksjon i Navn-feltet.
35. Velg Postliste i Varetype-feltet.
36. Klikk på Legg til.
37. Klikk på Ny for å åpne nedtrekksdialogen.
38. Skriv inn Dato i Navn-feltet.
39. Velg Dato i Varetype-feltet.
40. Klikk på Legg til.
41. Klikk på Ny for å åpne nedtrekksdialogen.
42. I Navn-feltet skriver du inn Debet.
43. Velg Faktisk i Varetype-feltet.
44. Klikk på Legg til.
45. Klikk på Ny for å åpne nedtrekksdialogen.
46. I Navn-feltet skriver du inn Kredit.
47. Klikk på Legg til.
48. Klikk på Ny for å åpne nedtrekksdialogen.
49. I Navn-feltet skriver du inn Valuta.
50. Velg Streng i Varetype-feltet.
51. Klikk på Legg til.
52. Klikk på Ny for å åpne nedtrekksdialogen.
53. I Navn-feltet skriver du inn Bilag.
54. Klikk på Legg til.
55. Klikk på Ny for å åpne nedtrekksdialogen.
56. Skriv inn Dimensjonsdata i Navn-feltet.
57. Velg Postliste i Varetype-feltet.
58. Klikk på Legg til.
    * Vi la til en ny postliste i modellen vår. Denne listen vil vise (for ER-rapporter som bruker denne modellen som datakilde) verdiene for valgte finansdimensjoner. Hver finansdimensjon vil bli presentert i denne listen som en post med aktuelle felt som representerer dimensjonens verdier. Dimensjonsnavn blir også presentert i denne posten som et felt som skal brukes, om nødvendig, for utvalgsformål.  
59. Klikk på Ny for å åpne nedtrekksdialogen.
60. I Navn-feltet skriver du inn Kode.
61. Velg Streng i Varetype-feltet.
62. Klikk på Legg til.
63. Klikk på Ny for å åpne nedtrekksdialogen.
64. Skriv inn Beskrivelse i Navn-feltet.
65. Klikk på Legg til.
66. Klikk på Ny for å åpne nedtrekksdialogen.
67. I Navn-feltet skriver du inn Navn.
68. Klikk på Legg til.
69. Klikk på Lagre.
70. Lukk siden.

![Siden ER-datamodellutforming](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]