---
title: ER Opprette en formatkonfigurasjon (november 2016)
description: De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 582e1a2baee805fe6770465edc7958954f638f1c
ms.sourcegitcommit: 29e19b6d91e5761178627ef2051f3385f5d7cfe5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/08/2019
ms.locfileid: "377555"
---
# <a name="er-create-a-format-configuration-november-2016"></a>ER Opprette en formatkonfigurasjon (november 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER). Denne formatkonfigurasjonen definerer formatet for elektroniske dokumenter som skal brukes til behandling av betalinger. I dette eksemplet oppretter du en formatkonfigurasjon for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Tilordne modell til valgte datakilder.


## <a name="create-a-new-format-configuration"></a>Opprette en ny formatkonfigurasjon
1. Gå til **Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering**.
2. Klikk på **Rapporteringskonfigurasjoner**.
3. Velg **Betalinger (forenklet model)** i treet.
4. Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.

 > [!NOTE]
 > Hvis du ikke ser **Opprett konfigurasjon**, må du aktivere utformingsmodus på siden **Parametere for elektronisk rapportering**. 
 
5. I **Ny**-feltet angir du **Format basert på datamodell PaymentModel**.
6. Skriv inn **BACS (britisk fiktivt)** i **Navn**-feltet.
7. I **Beskrivelse**-feltet skriver du inn **BACS-leverandørbetalingsformat (fiktivt Storbritannia)**.
    * Den aktive konfigurasjonsleverandøren angis automatisk her. Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen. Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.  
    * Du kan definere et bestemt format for elektronisk dokument. La dette feltet stå tomt hvis du vil velge et format under kjøring.  
8. Angi eller velg en verdi i feltet **Definisjon av datamodell**.
9. Klikk **Opprett konfigurasjon**. En ny konfigurasjon er opprettet. Utkastversjonen kan brukes til å lagre utformingsformatet for behandling av elektroniske dokumenter.  

## <a name="design-the-format-of-an-electronic-document"></a>Utforme formatet på et elektronisk dokument
1. Klikk **Utforming**.
2. Klikk på **Legg til rot** for å åpne nedtrekksdialogen.
3. Velg **Felles\Fil** i treet.
4. I **Navn**-feltet skriver du inn **Xml**.
5. I **Koding**-feltet skriver du inn **UTF-8**.
6. Klikk **OK**.
7. Klikk **Legg til**.
8. Velg **XML\Element** i treet.
9. I **Navn**-feltet skriver du inn **Melding**.
10. Klikk **OK**.
11. Velg **Xml\Melding** i treet.
12. Klikk på **Legg til element**.
13. I **Navn**-feltet skriver du inn **ProcessingDate**.
14. Klikk **OK**.
15. Klikk på **Legg til element**.
16. I Navn-feltet skriver du inn **MessageId**.
17. Klikk **OK**.
18. Klikk på **Legg til element**.
19. Skriv inn **Betalinger** i **Navn**-feltet.
20. Klikk **OK**.
21. Velg **Xml\Melding\Betalinger** i treet.
22. Klikk på **Legg til element**.
23. I **Navn**-feltet skriver du inn **Vare**.
24. Klikk **OK**.
25. Velg **Xml\Melding\Betalinger\Vare** i treet.
26. Klikk **Legg til**.
27. Velg **XML\Attributt** i treet.
28. I Navn-feltet skriver du inn **ID**.
29. Klikk **OK**.
30. Klikk **Legg til**.
31. Velg **XML\Element** i treet.
32. I Navn-feltet skriver du inn **Leverandør**.
33. Klikk **OK**.
34. Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.
35. Klikk på **Legg til element**.
36. I Navn-feltet skriver du inn **Navn**.
37. Klikk **OK**.
38. Klikk på **Legg til element**.
39. I **Navn**-feltet skriver du inn **Bank**.
40. Klikk **OK**.
41. Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank** i treet.
42. Klikk på **Legg til element**.
43. Skriv inn **RoutingNumber** i **Navn**-feltet.
44. Klikk **OK**.
45. Klikk på **Legg til element**.
46. Skriv inn **AccountNumber** i **Navn**-feltet.
47. Klikk **OK**.
48. Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.
49. Klikk **Kopier**.
50. Velg **Xml\Melding\Betalinger\Vare** i treet.
51. Klikk på **Lim inn**.
52. I **Navn**-feltet skriver du inn **Betaler**.
53. Velg **Xml\Melding\Betalinger\Vare** i treet.
54. Klikk på **Legg til element**.
55. I **Navn**-feltet skriver du inn **Valuta**.
56. Klikk **OK**.
57. Klikk på **Legg til element**.
58. Skriv inn **Beskrivelse** i **Navn**-feltet.
59. Klikk **OK**.
60. Klikk på **Legg til element**.
61. I Navn-feltet skriver du inn **TransDate**.
62. Klikk **OK**.
63. Klikk på **Legg til element**.
64. I Navn-feltet skriver du inn **Beløp**.
65. Klikk **OK**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Klargjøre formatkomponenter for tilordning til datamodellelementer
1. Velg **Xml\Melding\ProcessingDate** i treet.
2. Klikk på **Legg til** for å åpne nedtrekksdialogen.
3. Velg **Tekst\DateTime** i treet.
4. Skriv inn **åååå-MM-dd** i **Format**-feltet.
5. Klikk **OK**.
6. Velg **Xml\Melding\Betalinger\Vare\TransDate** i treet.
7. Klikk på **Legg til dato/klokkeslett**.
8. Skriv inn **åååå-MM-dd** i **Format**-feltet.
9. Velg **Dato** i feltet **Dato/klokkeslett**-type.
10. Klikk **OK**.
11. Velg **Xml\Melding\MessageId** i treet.
12. Klikk på **Legg til** for å åpne nedtrekksdialogen.
13. Velg **Tekst\Streng** i treet.
14. Klikk **OK**.
15. Velg **Xml\Melding\Betalinger\Vare\Leverandør\Navn** i treet.
16. Klikk på **Legg til streng**.
17. Klikk **OK**.
18. Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber** i treet.
19. Klikk på **Legg til streng**.
20. Klikk **OK**.
21. Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber** i treet.
22. Klikk på **Legg til streng**.
23. Klikk **OK**.
24. Velg **Xml\Melding\Betalinger\Vare\Betaler\Navn** i treet.
25. Klikk på **Legg til streng**.
26. Klikk **OK**.
27. Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber** i treet.
28. Klikk på **Legg til streng**.
29. Klikk **OK**.
30. Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber** i treet.
31. Klikk på **Legg til streng**.
32. Klikk **OK**.
33. Velg **Xml\Melding\Betalinger\Vare\Valuta** i treet.
34. Klikk på **Legg til streng**.
35. Klikk **OK**.
36. Velg **Xml\Melding\Betalinger\Vare\Beskrivelse** i treet.
37. Klikk på **Legg til streng**.
38. Klikk **OK**.
39. Velg **Xml\Melding\Betalinger\Vare\Beløp** i treet.
40. Klikk på **Legg til streng**.
41. Klikk **OK**.
42. Klikk **Lagre**.
43. Lukk siden.

