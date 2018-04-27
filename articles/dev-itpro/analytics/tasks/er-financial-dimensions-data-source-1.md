--- 
title: Utforme datamodell for bruk av finansdimensjoner som en datakilde
description: "De følgende trinnene forklarer hvordan en systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3e55eedba1955ae79733afee1a0b3c7072147bb5
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source"></a>Utforme datamodell for bruk av finansdimensjoner som en datakilde 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".


## <a name="create-a-new-data-model"></a>Opprette en ny datamodell
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Forsikre deg om at leverandøren Litware, Inc er tilgjengelig og merket som aktiv.  
2. Klikk Rapporteringskonfigurasjoner.
3. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
4. Skriv inn Eksempelmodell for finansdimensjoner i Navn-feltet.
5. Klikk Opprett konfigurasjon.
6. Klikk Utforming.
7. Klikk Ny for å åpne nedtrekksdialogen.
8. I Navn-feltet skriver du inn Oppføring.
9. Klikk Legg til.
10. Klikk Ny for å åpne nedtrekksdialogen.
11. I Navn-feltet skriver du inn Firma.
12. Klikk Legg til.
    * Vi vil legge til en ny postliste i modellen vår. Denne listen vil vise (for ER-rapporter som bruker denne modellen som datakilde) innstillingene for valgte finansdimensjoner. Hver finansdimensjon vil bli presentert i denne listen som en post med aktuelle felt som representerer dimensjonens innstilling.  
13. Klikk Ny for å åpne nedtrekksdialogen.
14. Skriv inn Dimensjonsinnstilling i Navn-feltet.
15. Velg Postliste i Varetype-feltet.
16. Klikk Legg til.
17. Klikk Ny for å åpne nedtrekksdialogen.
18. I Navn-feltet skriver du inn Kode.
19. Velg Streng i Varetype-feltet.
20. Klikk Legg til.
21. Klikk Ny for å åpne nedtrekksdialogen.
22. I Navn-feltet skriver du inn Navn.
23. Klikk Legg til.
24. Velg Oppføring i treet.
25. Klikk Ny for å åpne nedtrekksdialogen.
26. I Navn-feltet skriver du inn Journal.
27. Velg Postliste i Varetype-feltet.
28. Klikk Legg til.
29. Klikk Ny for å åpne nedtrekksdialogen.
30. Skriv inn Parti i Navn-feltet.
31. Velg Streng i Varetype-feltet.
32. Klikk Legg til.
33. Klikk Ny for å åpne nedtrekksdialogen.
34. Skriv inn Transaksjon i Navn-feltet.
35. Velg Postliste i Varetype-feltet.
36. Klikk Legg til.
37. Klikk Ny for å åpne nedtrekksdialogen.
38. Skriv inn Dato i Navn-feltet.
39. Velg Dato i Varetype-feltet.
40. Klikk Legg til.
41. Klikk Ny for å åpne nedtrekksdialogen.
42. I Navn-feltet skriver du inn Debet.
43. Velg Faktisk i Varetype-feltet.
44. Klikk Legg til.
45. Klikk Ny for å åpne nedtrekksdialogen.
46. I Navn-feltet skriver du inn Kredit.
47. Klikk Legg til.
48. Klikk Ny for å åpne nedtrekksdialogen.
49. I Navn-feltet skriver du inn Valuta.
50. Velg Streng i Varetype-feltet.
51. Klikk Legg til.
52. Klikk Ny for å åpne nedtrekksdialogen.
53. I Navn-feltet skriver du inn Bilag.
54. Klikk Legg til.
55. Klikk Ny for å åpne nedtrekksdialogen.
56. Skriv inn Dimensjonsdata i Navn-feltet.
57. Velg Postliste i Varetype-feltet.
58. Klikk Legg til.
    * Vi la til en ny postliste i modellen vår. Denne listen vil vise (for ER-rapporter som bruker denne modellen som datakilde) verdiene for valgte finansdimensjoner. Hver finansdimensjon vil bli presentert i denne listen som en post med aktuelle felt som representerer dimensjonens verdier. Dimensjonsnavn blir også presentert i denne posten som et felt som skal brukes, om nødvendig, for utvalgsformål.  
59. Klikk Ny for å åpne nedtrekksdialogen.
60. I Navn-feltet skriver du inn Kode.
61. Velg Streng i Varetype-feltet.
62. Klikk Legg til.
63. Klikk Ny for å åpne nedtrekksdialogen.
64. Skriv inn Beskrivelse i Navn-feltet.
65. Klikk Legg til.
66. Klikk Ny for å åpne nedtrekksdialogen.
67. I Navn-feltet skriver du inn Navn.
68. Klikk Legg til.
69. Klikk Lagre.
70. Lukk siden.


