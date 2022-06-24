---
title: ER Opprette en formatkonfigurasjon (november 2016)
description: Denne artikkelen forklarer hvordan du oppretter en formatkonfigurasjon for elektronisk rapportering (ER).
author: NickSelin
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2617f33293c38b7f1aaa61fda7d8de06711c6727
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902661"
---
# <a name="er-create-a-format-configuration-november-2016"></a>ER Opprette en formatkonfigurasjon (november 2016)

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER). Denne formatkonfigurasjonen definerer formatet for elektroniske dokumenter som skal brukes til behandling av betalinger. I dette eksemplet oppretter du en formatkonfigurasjon for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Tilordne modell til valgte datakilder.


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
9. Klikk på **Opprett konfigurasjon**. En ny konfigurasjon er opprettet. Utkastversjonen kan brukes til å lagre utformingsformatet for behandling av elektroniske dokumenter.  

## <a name="design-the-format-of-an-electronic-document"></a>Utforme formatet på et elektronisk dokument
1. Klikk på **Utforming**.
2. Klikk på **Legg til rot** for å åpne nedtrekksdialogen.
3. Velg **Felles\Fil** i treet.
4. I **Navn**-feltet skriver du inn **Xml**.
5. I **Koding**-feltet skriver du inn **UTF-8**.
6. Klikk på **OK**.
7. Klikk på **Legg til**.
8. Velg **XML\Element** i treet.
9. I **Navn**-feltet skriver du inn **Melding**.
10. Klikk på **OK**.
11. Velg **Xml\Melding** i treet.
12. Klikk på **Legg til element**.
13. I **Navn**-feltet skriver du inn **ProcessingDate**.
14. Klikk på **OK**.
15. Klikk på **Legg til element**.
16. I Navn-feltet skriver du inn **MessageId**.
17. Klikk på **OK**.
18. Klikk på **Legg til element**.
19. Skriv inn **Betalinger** i **Navn**-feltet.
20. Klikk på **OK**.
21. Velg **Xml\Melding\Betalinger** i treet.
22. Klikk på **Legg til element**.
23. I **Navn**-feltet skriver du inn **Vare**.
24. Klikk på **OK**.
25. Velg **Xml\Melding\Betalinger\Vare** i treet.
26. Klikk på **Legg til**.
27. Velg **XML\Attributt** i treet.
28. I Navn-feltet skriver du inn **ID**.
29. Klikk på **OK**.
30. Klikk på **Legg til**.
31. Velg **XML\Element** i treet.
32. I Navn-feltet skriver du inn **Leverandør**.
33. Klikk på **OK**.
34. Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.
35. Klikk på **Legg til element**.
36. I Navn-feltet skriver du inn **Navn**.
37. Klikk på **OK**.
38. Klikk på **Legg til element**.
39. I **Navn**-feltet skriver du inn **Bank**.
40. Klikk på **OK**.
41. Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank** i treet.
42. Klikk på **Legg til element**.
43. Skriv inn **RoutingNumber** i **Navn**-feltet.
44. Klikk på **OK**.
45. Klikk på **Legg til element**.
46. Skriv inn **AccountNumber** i **Navn**-feltet.
47. Klikk på **OK**.
48. Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.
49. Klikk på **Kopier**.
50. Velg **Xml\Melding\Betalinger\Vare** i treet.
51. Klikk på **Lim inn**.
52. I **Navn**-feltet skriver du inn **Betaler**.
53. Velg **Xml\Melding\Betalinger\Vare** i treet.
54. Klikk på **Legg til element**.
55. I **Navn**-feltet skriver du inn **Valuta**.
56. Klikk på **OK**.
57. Klikk på **Legg til element**.
58. Skriv inn **Beskrivelse** i **Navn**-feltet.
59. Klikk på **OK**.
60. Klikk på **Legg til element**.
61. I Navn-feltet skriver du inn **TransDate**.
62. Klikk på **OK**.
63. Klikk på **Legg til element**.
64. I Navn-feltet skriver du inn **Beløp**.
65. Klikk på **OK**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Klargjøre formatkomponenter for tilordning til datamodellelementer
1. Velg **Xml\Melding\ProcessingDate** i treet.
2. Klikk på **Legg til** for å åpne nedtrekksdialogen.
3. Velg **Tekst\DateTime** i treet.
4. Skriv inn **åååå-MM-dd** i **Format**-feltet.
5. Klikk på **OK**.
6. Velg **Xml\Melding\Betalinger\Vare\TransDate** i treet.
7. Klikk på **Legg til dato/klokkeslett**.
8. Skriv inn **åååå-MM-dd** i **Format**-feltet.
9. Velg **Dato** i feltet **Dato/klokkeslett**-type.
10. Klikk på **OK**.
11. Velg **Xml\Melding\MessageId** i treet.
12. Klikk på **Legg til** for å åpne nedtrekksdialogen.
13. Velg **Tekst\Streng** i treet.
14. Klikk på **OK**.
15. Velg **Xml\Melding\Betalinger\Vare\Leverandør\Navn** i treet.
16. Klikk på **Legg til streng**.
17. Klikk på **OK**.
18. Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber** i treet.
19. Klikk på **Legg til streng**.
20. Klikk på **OK**.
21. Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber** i treet.
22. Klikk på **Legg til streng**.
23. Klikk på **OK**.
24. Velg **Xml\Melding\Betalinger\Vare\Betaler\Navn** i treet.
25. Klikk på **Legg til streng**.
26. Klikk på **OK**.
27. Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber** i treet.
28. Klikk på **Legg til streng**.
29. Klikk på **OK**.
30. Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber** i treet.
31. Klikk på **Legg til streng**.
32. Klikk på **OK**.
33. Velg **Xml\Melding\Betalinger\Vare\Valuta** i treet.
34. Klikk på **Legg til streng**.
35. Klikk på **OK**.
36. Velg **Xml\Melding\Betalinger\Vare\Beskrivelse** i treet.
37. Klikk på **Legg til streng**.
38. Klikk på **OK**.
39. Velg **Xml\Melding\Betalinger\Vare\Beløp** i treet.
40. Klikk på **Legg til streng**.
41. Klikk på **OK**.
42. Klikk på **Lagre**.
43. Lukk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]