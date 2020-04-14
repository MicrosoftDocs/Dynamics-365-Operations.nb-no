---
title: ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bbbc81eaf8c13e8d13e30a0276e38453e07ead9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142530"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a>ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 2: Modelltilordning).


## <a name="design-a-report-to-present-financial-dimensions"></a>Utforme en rapport for å presentere finansdimensjoner
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Velg Eksempelmodell for finansdimensjoner i treet.
3. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
4. I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.
    * Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.  
5. Skriv inn Finansjournalrapport i Navn-feltet.
6. Velg Oppføring i Definisjon av datamodell-feltet.
7. Klikk Opprett konfigurasjon.
8. Klikk Utforming.
9. Klikk Legg til rot for å åpne nedtrekksdialogen.
10. Velg XML\Element i treet.
11. Skriv inn Rot i Navn-feltet.
12. Klikk OK.
13. Klikk Legg til for å åpne nedtrekksdialogen.
14. Velg XML\Attributt i treet.
15. I Navn-feltet skriver du inn Firma.
16. Klikk OK.
17. Klikk Legg til for å åpne nedtrekksdialogen.
18. Velg XML\Element i treet.
19. I Navn-feltet skriver du inn Journal.
20. Klikk OK.
21. Velg Rot: XML-element\Journal: XML-element i treet.
22. Klikk Legg til for å åpne nedtrekksdialogen.
23. Velg XML\Attributt i treet.
24. Skriv inn Parti i Navn-feltet.
25. Klikk OK.
26. Klikk Legg til for å åpne nedtrekksdialogen.
27. Velg XML\Element i treet.
28. Skriv inn Transaksjon i Navn-feltet.
29. Klikk OK.
30. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.
31. Klikk Legg til for å åpne nedtrekksdialogen.
32. Velg XML\Attributt i treet.
33. I Navn-feltet skriver du inn Bilag.
34. Klikk OK.
35. Klikk Legg til attributt.
36. Skriv inn Dato i Navn-feltet.
37. Klikk OK.
38. Klikk Legg til attributt.
39. I Navn-feltet skriver du inn Valuta.
40. Klikk OK.
41. Klikk Legg til attributt.
42. Skriv inn Dt i Navn-feltet.
43. Klikk OK.
44. Klikk Legg til attributt.
45. Skriv inn Kt i Navn-feltet.
46. Klikk OK.
47. Klikk Legg til for å åpne nedtrekksdialogen.
48. Velg XML\Element i treet.
49. Skriv inn Dimensjoner i Navn-feltet.
50. Klikk OK.
51. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.
52. Klikk Legg til for å åpne nedtrekksdialogen.
53. Velg XML\Attributt i treet.
54. I Navn-feltet skriver du inn Kode.
55. Klikk OK.
56. Klikk Legg til attributt.
57. Skriv inn Verdi i Navn-feltet.
58. Klikk OK.
59. Klikk Legg til attributt.
60. Skriv inn Beskr i Navn-feltet.
61. Klikk OK.

## <a name="map-report-elements-to-data-sources"></a>Tilordne rapportelementer til datakilder
1. Klikk kategorien Tilordning.
2. Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.
3. Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.
4. Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.
5. Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.
6. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Beskr: XML-attributt i treet.
7. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Beskrivelse: Streng i treet.
8. Klikk Bind.
9. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Verdi: XML-attributt i treet.
10. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.
11. Klikk Bind.
12. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Kode: XML-attributt i treet.
13. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Navn: Streng i treet.
14. Klikk Bind.
15. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.
16. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.
17. Klikk Bind.
18. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Kt: XML-attributt i treet.
19. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.
20. Klikk Bind.
21. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dt: XML-attributt i treet.
22. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.
23. Klikk Bind.
24. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Valuta: XML-attributt i treet.
25. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.
26. Klikk Bind.
27. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dato: XML-attributt i treet.
28. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.
29. Klikk Bind.
30. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Bilag: XML-attributt i treet.
31. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.
32. Klikk Bind.
33. Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.
34. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.
35. Klikk Bind.
36. Velg Rot: XML-element\Journal: XML-element\Parti: XML-attributt i treet.
37. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.
38. Klikk Bind.
39. Velg Rot: XML-element\Journal: XML-element i treet.
40. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.
41. Klikk Bind.
42. Velg Rot: XML-element\Firma: XML-attributt i treet.
43. Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.
44. Klikk Bind.
45. Klikk Lagre.
46. Lukk siden.

