--- 
title: "Oversikt over leverandørbetaling"
description: "Denne oppgaveveiledningen leder deg gjennom forskjellige metoder som brukes til å opprette leverandørbetalinger, inkludert hvordan du bruker et betalingsforslag eller angir en engangsbetaling manuelt."
author: kweekley
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: e9a94231f755ff23bb442d62e90daff8f2d1f4fb
ms.contentlocale: nb-no
ms.lasthandoff: 10/30/2017

---
# <a name="vendor-payment-overview"></a>Oversikt over leverandørbetaling

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen leder deg gjennom forskjellige metoder som brukes til å opprette leverandørbetalinger, inkludert hvordan du bruker et betalingsforslag eller angir en engangsbetaling manuelt. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.

1. Gå til Leverandører > Betalinger > Betalingsjournal.
2. Klikk Ny.
3. Velg betalingsjournalen som leverandørbetalingene skal lagres i. 
4. Velg journalen, eller angi den manuelt.
5. Klikk Linjer.
6. Klikk Betalingsforslag.
7. Klikk Opprett betalingsforslag.
    * Betalingsforslaget er en spørring som brukes til å velge fakturaer for betaling. Du kan redigere listen over fakturaer som skal betales før du oppretter eller genererer leverandørbetalingene.  
8. Velg fakturaer for betaling etter forfallsdato, kontantrabatt, eller begge deler. 
9. Angi datoen for sammenligning med forfalt dato eller kontantrabatten. 
10. Valgfritt: Angi en betalingsdato som brukes for alle betalinger.
    * Datoen som er angitt her, blir den betalingsdatoen for alle fakturaer som er opprettet, uavhengig av forfallsdatoen eller kontantrabattdatoen.  
11. Valgfritt: Angi en minste betalingsdato som kan brukes som betalingsdato.
    * Den minste betalingsdatoen vil være den tidligste datoen som brukes ved opprettelse av betalinger. Hvis for eksempel en faktura har en forfallsdato etter den minste betalingsdatoen, blir forfallsdato betalingsdatoen i stedet for den minste betalingsdatoen for å betale fakturaen på den seneste mulige datoen.  
12. Angi flere spørringsbegrensninger under Poster som skal inkluderes.
    * Filteret brukes ofte til å begrense fakturaene som velges for betaling etter leverandørgruppe eller betalingsmåte. Du kan for eksempel legge til et filter for å betale bare fakturaer med sjekk i denne lønnskjøringen.  
13. Angi flere standarder for spørringsbegrensning eller betaling. 
    * De ekstra parameterne kan brukes til å definere betalingsvalutaen, eller for å aktivere sentralisert betaling for denne lønnskjøringen.  
14. Klikk OK.
    * Når du klikker OK, vises resultatene av spørringen. Hvis du ikke vil forhåndsvise listen over fakturaene som er valgt for betaling, kan du gå tilbake til hurtigkategorien Parametere og endre innstillingen Opprett betalinger uten forhåndsvisning av faktura = Ja.  
15. Velg knappen Vis betalingsoversikt for å vise betalingene som skal opprettes for leverandøren på fakturaen som er valgt.
16. Velg Skjul betalingsoversikt for å skjule betalingene. 
17. Klikk Opprett betalinger.
    * Før du velger Opprett betalinger, kan du høyreklikke i rutenettet og eksportere en liste over fakturaene til Excel. Knappen Opprett betalinger oppretter leverandørbetalingene i betalingsjournalen.  
18. Skann betalingene og kontroller at betalingsmåten er definert for alle betalinger. 
    * Hvis du genererer betalingene, for eksempel skrive ut en sjekk eller opprette en elektronisk betaling, må betalingsmåten defineres. Betalingsmåten vil også angi standard bankkonto som betalingen skal skje fra.  
19. Klikk Ny for å opprette en engangsbetaling.
    * En engangsbetaling kan legges til i en betalingsjournal når som helst før postering. Dette gjøres ved å klikke Ny og legge til betalingsinformasjonen manuelt, i stedet for å bruke betalingsforslaget.  
20. Velg leverandøren som betalingen skal utføres til.
21. Hvis det finnes en faktura å betale, velger du Utlign transaksjoner for å velge fakturaen for betaling.
    * Hvis dette er en forskuddsbetaling, er dette trinnet valgfritt. Du kan opprette betalingen uten å merke noen fakturaer.  
22. Merk alle fakturaer som skal betales.
    * Hvis du bruker Utlign transaksjoner til å velge fakturaer for betaling, beregnes betalingsbeløpet automatisk basert på hvilke fakturaer du merker for betaling og hvilket beløp du angir i Beløp som skal utlignes.  
23. Klikk OK.
24. Hvis du vil slette en betaling, merker du raden.
25. Klikk Slett.
    * Hvis du sletter en betaling, slettes bare betalingen. Alle fakturaer som er merket for betaling vil fremdeles være tilgjengelig for betaling med en annen betaling.  
26. Klikk Ja.
27. Velg Generer betaling for å skrive ut sjekker eller opprette den elektroniske betalingsfilen.
28. Velg betalingsmåten som du vil generere.
    * Betalingsjournalen kan inneholde betalinger for både sjekker og elektroniske betalinger, men du kan bare generere en betalingstype om gangen.  
29. Velg bankkontoen som du vil generere betalingene fra.
30. Klikk OK.
    * Betalinger genereres bare for betalinger som samsvarer med betalingsmåten og bankkontoen du valgte.  
31. Hvis du genererer sjekker, velger du Dokument for å sikre riktig utskriftsmål for sjekkene.
32. Klikk OK.
33. Klikk OK for å generere betalingene.
34. Klikk Poster hvis alle betalingene er godkjent og generert. 


