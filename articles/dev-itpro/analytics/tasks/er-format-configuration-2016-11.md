--- 
title: Opprette en formatkonfigurasjon for elektronisk rapportering (ER)
description: "De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER)."
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
ms.openlocfilehash: c46b222cb12d0432609c47f89afc522e02c41ab6
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a>Opprette en formatkonfigurasjon for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER). Denne formatkonfigurasjonen definerer formatet for elektroniske dokumenter som skal brukes til behandling av betalinger. I dette eksemplet oppretter du en formatkonfigurasjon for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Tilordne modell til valgte datakilder.


## <a name="create-a-new-format-configuration"></a>Opprette en ny formatkonfigurasjon
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Rapporteringskonfigurasjoner.
3. Velg Betalinger (forenklet model) i treet.
4. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
5. I feltet Ny angir du Format basert på datamodell PaymentModel.
6. Skriv inn BACS (britisk fiktivt) i Navn-feltet.
    * BACS (britisk fiktivt)  
7. I Beskrivelse-feltet skriver du inn BACS-leverandørbetalingsformat (fiktivt Storbritannia).
    * BACS-leverandørbetalingsformat (fiktivt Storbritannia)  
    * Den aktive konfigurasjonsleverandøren angis automatisk her. Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen. Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.  
    * Du kan definere et bestemt format for elektronisk dokument. La dette feltet stå tomt hvis du vil velge et format under kjøring.  
8. Angi eller velg en verdi i feltet Definisjon av datamodell.
9. Klikk Opprett konfigurasjon.
    * En ny konfigurasjon er opprettet. Utkastversjonen kan brukes til å lagre utformingsformatet for behandling av elektroniske dokumenter.  

## <a name="design-format-of-electronic-document"></a>Designformat for elektronisk dokument
1. Klikk Utforming.
2. Klikk Legg til rot for å åpne nedtrekksdialogen.
3. Velg Felles\Fil i treet.
4. I Navn-feltet skriver du inn Xml.
    * XML  
5. I Koding-feltet skriver du inn UTF-8.
    * UTF-8  
6. Klikk OK.
7. Klikk Legg til for å åpne nedtrekksdialogen.
8. Velg XML\Element i treet.
9. I Navn-feltet skriver du inn Melding.
    * Melding  
10. Klikk OK.
11. Velg Xml\Melding i treet.
12. Klikk Legg til element.
13. I Navn-feltet skriver du inn ProcessingDate.
    * ProcessingDate  
14. Klikk OK.
15. Klikk Legg til element.
16. I Navn-feltet skriver du inn MessageId.
    * MessageId  
17. Klikk OK.
18. Klikk Legg til element.
19. Skriv inn Betalinger i Navn-feltet.
    * Betalinger  
20. Klikk OK.
21. Velg Xml\Melding\Betalinger i treet.
22. Klikk Legg til element.
23. I Navn-feltet skriver du inn Element.
    * Vare  
24. Klikk OK.
25. Velg Xml\Melding\Betalinger\Vare i treet.
26. Klikk Legg til for å åpne nedtrekksdialogen.
27. Velg XML\Attributt i treet.
28. I Navn-feltet skriver du inn ID.
    * ID  
29. Klikk OK.
30. Klikk Legg til for å åpne nedtrekksdialogen.
31. Velg XML\Element i treet.
32. I Navn-feltet skriver du inn Leverandør.
    * Leverandør  
33. Klikk OK.
34. Velg Xml\Melding\Betalinger\Vare\Leverandør i treet.
35. Klikk Legg til element.
36. I Navn-feltet skriver du inn Navn.
    * Navn  
37. Klikk OK.
38. Klikk Legg til element.
39. I Navn-feltet skriver du inn Bank.
    * Bank  
40. Klikk OK.
41. Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank i treet.
42. Klikk Legg til element.
43. Skriv inn RoutingNumber i feltet Navn.
    * RoutingNumber  
44. Klikk OK.
45. Klikk Legg til element.
46. Skriv inn AccountNumber i feltet Navn.
    * AccountNumber  
47. Klikk OK.
48. Velg Xml\Melding\Betalinger\Vare\Leverandør i treet.
49. Klikk Kopier.
50. Velg Xml\Melding\Betalinger\Vare i treet.
51. Klikk Lim inn.
52. I Navn-feltet skriver du inn Betaler.
    * Betaler  
53. Velg Xml\Melding\Betalinger\Vare i treet.
54. Klikk Legg til element.
55. I Navn-feltet skriver du inn Valuta.
    * Valuta  
56. Klikk OK.
57. Klikk Legg til element.
58. Skriv inn Beskrivelse i Navn-feltet.
    * beskrivelse  
59. Klikk OK.
60. Klikk Legg til element.
61. I Navn-feltet skriver du inn TransDate.
    * TransDate  
62. Klikk OK.
63. Klikk Legg til element.
64. I Navn-feltet skriver du inn Beløp.
    * Beløp  
65. Klikk OK.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Klargjøre formatkomponenter for tilordning til datamodellelementer
1. Velg Xml\Melding\ProcessingDate i treet.
2. Klikk Legg til for å åpne nedtrekksdialogen.
3. Velg Tekst\DateTime i treet.
4. Skriv inn åååå-MM-dd i Format-feltet.
    * åååå-MM-dd  
5. Klikk OK.
6. Velg Xml\Melding\Betalinger\Vare\TransDate i treet.
7. Klikk Legg til dato/klokkeslett.
8. Skriv inn åååå-MM-dd i Format-feltet.
    * åååå-MM-dd  
9. Velg Dato i feltet DateTime-type.
10. Klikk OK.
11. Velg Xml\Melding\MessageId i treet.
12. Klikk Legg til for å åpne nedtrekksdialogen.
13. Velg Tekst\Streng i treet.
14. Klikk OK.
15. Velg Xml\Melding\Betalinger\Vare\Leverandør\Navn i treet.
16. Klikk Legg til streng.
17. Klikk OK.
18. Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber i treet.
19. Klikk Legg til streng.
20. Klikk OK.
21. Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber i treet.
22. Klikk Legg til streng.
23. Klikk OK.
24. Velg Xml\Melding\Betalinger\Vare\Leverandør\Betaler\Navn i treet.
25. Klikk Legg til streng.
26. Klikk OK.
27. Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber i treet.
28. Klikk Legg til streng.
29. Klikk OK.
30. Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber i treet.
31. Klikk Legg til streng.
32. Klikk OK.
33. Velg Xml\Melding\Betalinger\Vare\Valuta i treet.
34. Klikk Legg til streng.
35. Klikk OK.
36. Velg Xml\Melding\Betalinger\Vare\Leverandør\Beskrivelse i treet.
37. Klikk Legg til streng.
38. Klikk OK.
39. Velg Xml\Melding\Betalinger\Vare\Beløp i treet.
40. Klikk Legg til streng.
41. Klikk OK.
42. Klikk Lagre.
43. Lukk siden.

