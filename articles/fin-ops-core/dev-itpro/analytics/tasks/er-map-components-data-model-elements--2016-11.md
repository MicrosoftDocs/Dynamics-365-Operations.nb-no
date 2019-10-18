---
title: ER Tilordne komponenter i det opprettede formatet til datamodellelementer (november 2016)
description: Følgende prosedyre viser hvordan en bruker med rollen systemansvarlig eller utvikler av elektronisk rapportering kan tilordne datamodellelementer til komponenter i den opprettede konfigurasjonen for elektronisk rapportering (ER), som definerer et elektronisk dokumentformat for forretningsområdet for betalinger.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a033853be17d6013daa5550ca9c061198bb0330
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184744"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>ER Tilordne komponenter i det opprettede formatet til datamodellelementer (november 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende prosedyre viser hvordan en bruker med rollen systemansvarlig eller utvikler av elektronisk rapportering kan tilordne datamodellelementer til komponenter i den opprettede konfigurasjonen for elektronisk rapportering (ER), som definerer et elektronisk dokumentformat for forretningsområdet for betalinger. Dette formatet brukes senere til å generere elektroniske dokumenter for behandling av betalinger. I dette eksemplet skal du opprette en formatkonfigurasjon for eksempelfirmaet "Litware, Inc". Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles for alle firmaer. For å fullføre disse trinnene må du først fullføre trinnene i oppgaveveiledningen "Opprette en formatkonfigurasjon".


## <a name="select-a-format-configuration"></a>Velge en formatkonfigurasjon
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Rapporteringskonfigurasjoner.
3. Vis Betalinger (forenklet model) i treet.
4. Velg Betalinger (forenklet model)\BBS (Storbritannia fiktiv) i treet.
5. Klikk Utforming.

## <a name="map-format-components-to-data-model-elements"></a>Tilordne formatkomponenter til datamodellelementer
1. Klikk Vis/skjul.
2. Klikk kategorien Tilordning.
3. Utvid noden 'model' i treet.
4. Velg Xml\Melding\ProcessingDate\DateTime i treet.
5. Velg modell\ProcessingDateTime i treet.
6. Klikk Bind.
7. Velg Xml\Melding\MessageId\Streng i treet.
8. Velg modell\MessageIdentification i treet.
9. Klikk Bind.
10. Utvid modell\Betalinger i treet.
11. Velg Xml\Melding\Betalinger\Vare\Beløp\Streng i treet.
12. Velg modell\Betalinger\InstructedAmount i treet.
13. Klikk Bind.
14. Velg Xml\Melding\Betalinger\Vare\TransDate\DateTime i treet.
15. Velg modell\Betalinger\TransactionDate i treet.
16. Klikk Bind.
17. Velg Xml\Melding\Betalinger\Vare\Beskrivelse\Streng i treet.
18. Velg modell\Betalinger\Beskrivelse i treet.
19. Klikk Bind.
20. Velg Xml\Melding\Betalinger\Vare\Beløp\Valuta\Streng i treet.
21. Velg model\Payments\Currency i treet.
22. Klikk Bind.
23. Velg Xml\Melding\Betalinger\Vare\Id i treet.
24. Velg modell\Betalinger\End2EndID i treet.
25. Klikk Bind.
26. Utvid modell\Betalinger\Kreditor i treet.
27. Utvid modell\Betalinger\Kreditor\Konto i treet.
28. Utvid modell\Betalinger\Kreditor\Agent i treet.
29. Velg Xml\Melding\Betalinger\Vare\Leverandør\Navn\Streng i treet.
30. I treet velger du modell\Betalinger\Kreditor\Navn.
31. Klikk Bind.
32. Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber\String i treet.
33. I treet velger du modell\Betalinger\Kreditor\Agent\RoutingNumber.
34. Klikk Bind.
35. Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber\Streng i treet.
36. I treet velger du modell\Betalinger\Kreditor\Konto\Nummer.
37. Klikk Bind.
38. Velg Xml\Melding\Betalinger\Vare\Betaler\Navn\Streng i treet.
39. Utvid modell\Betalinger\Debitor i treet.
40. Utvid modell\Betalinger\Debitor\Konto i treet.
41. Utvid modell\Betalinger\Debitor\Agent i treet.
42. I treet velger du modell\Betalinger\Debitor\Navn.
43. Klikk Bind.
44. Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber\Streng i treet.
45. Velg modell\Betalinger\Debitor\Agent\RoutingNumber i treet.
46. Klikk Bind.
47. Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber\Streng i treet.
48. I treet velger du modell\Betalinger\Debitor\Konto\Nummer.
49. Klikk Bind.
50. Velg Xml\Melding\Betalinger\Vare i treet.
51. Velg modell\Betalinger i treet.
52. Klikk Bind.
53. Klikk Lagre.

## <a name="validate-format-mapping"></a>Validere formattilordning
1. Klikk Valider.
    * Valider den nye tilordningen for å sikre at alle bindinger er i orden.  
2. Lukk siden.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Endre status for gjeldende versjon av formatkonfigurasjon
    * I de neste trinnene endrer du statusen for formatkonfigurasjonen fra Utkast til Fullført for å gjøre den tilgjengelig for generering av betalingsdokumenter.  
1. Klikk Endre status.
2. Klikk Fullført.
3. Skriv inn en verdi i feltet Beskrivelse.
    * For eksempel versjon 1.  
4. Klikk OK.
5. Velg den fullførte versjonen av den gjeldende konfigurasjonen.
    * Legg merke til at konfigurasjonen er lagret som fullført versjon 1.1. Dette er versjon 1 av formatet, som er basert på versjon 1 av datamodellen.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Definere gyldighetsdato for fullført versjon av format
    * Du kan konfigurere hver formatversjon som tilgjengelig for bruk fra en bestemt dato. Når mer enn én formatversjon er aktiv på en bestemt dato, velges det nyeste formatet (basert på versjonsnummeret) for bruk. Datoverdien for økten brukes for valg av riktig versjon.  

## <a name="restrict-access-to-created-format-from-companies"></a>Begrense tilgang til formatet som er opprettet fra firmaer
1. Utvid delen ISO-land-/områdekoder.
    * Hver formattilgang kan begrenses ved å identifisere bestemte land/regioner der et format er tilgjengelig. Når listen over land/områder for et bestemt format er tomt, kan dette formatet brukes i et hvilket som helst firma. Når det settes noen ISO-land-/områdekoder i denne listen over land/regioner, kan formatet bare brukes i firmaer hvis den primære adressen er i landet/regionen.  

