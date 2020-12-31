---
title: Oversikt over leverandørbetaling
description: Denne oppgaveveiledningen leder deg gjennom forskjellige metoder som brukes til å opprette leverandørbetalinger, inkludert hvordan du bruker et betalingsforslag eller angir en engangsbetaling manuelt.
author: kweekley
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19cea683058f7fb757ac3a99541959ba06df1963
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446431"
---
# <a name="vendor-payment-overview"></a>Oversikt over leverandørbetaling

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen leder deg gjennom forskjellige metoder som brukes til å opprette leverandørbetalinger, inkludert hvordan du bruker et betalingsforslag eller angir en engangsbetaling manuelt. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.

1. Gå til **Navigasjonsrute > Moduler > Leverandører > Betalinger > Betalingsjournal**.
2. Klikk på **Ny**.
3. Velg betalingsjournalen som leverandørbetalingene skal lagres i. 
4. Velg journalen, eller angi den manuelt.
5. Klikk **Linjer**.
6. Klikk på **Betalingsforslag** i **handlingsruten**.
7. Klikk på **Opprett betalingsforslag**. Betalingsforslaget er en spørring som brukes til å velge fakturaer for betaling. Du kan redigere listen over fakturaer som skal betales før du oppretter eller genererer leverandørbetalingene.
8. Velg fakturaer for betaling etter forfallsdato, kontantrabatt, eller begge deler. 
9. Angi datoen for sammenligning med forfalt dato eller kontantrabatten. 
10. Valgfritt: Angi en betalingsdato som brukes for alle betalinger. Datoen som er angitt her, blir den betalingsdatoen for alle fakturaer som er opprettet, uavhengig av forfallsdatoen eller kontantrabattdatoen.  
11. Valgfritt: Angi en minste betalingsdato som kan brukes som betalingsdato. Den minste betalingsdatoen vil være den tidligste datoen som brukes ved opprettelse av betalinger. Hvis for eksempel en faktura har en forfallsdato etter den minste betalingsdatoen, blir forfallsdato betalingsdatoen i stedet for den minste betalingsdatoen for å betale fakturaen på den seneste mulige datoen.
12. Angi flere spørringsbegrensninger under delen **Poster som skal inkluderes**. Filteret brukes ofte til å begrense fakturaene som velges for betaling etter leverandørgruppe eller betalingsmåte. Du kan for eksempel legge til et filter for å betale bare fakturaer med sjekk i denne lønnskjøringen.
13. Angi flere standarder for spørringsbegrensning eller betaling. De ekstra parameterne kan brukes til å definere betalingsvalutaen, eller for å aktivere sentralisert betaling for denne lønnskjøringen.  
14. Klikk **OK**. Når du klikker på **OK**, vises resultatene av spørringen. Hvis du ikke vil forhåndsvise listen over fakturaene som er valgt for betaling, kan du gå tilbake til hurtigkategorien **Parametere** og endre innstillingen **Opprett betalinger uten forhåndsvisning av faktura** til Ja.  
15. Velg knappen **Vis betalingsoversikt** for å vise betalingene som skal opprettes for leverandøren på fakturaen som er valgt.
16. Velg **Skjul betalingsoversikt** for å skjule betalingene. 
17. Klikk **Opprett betalinger**. Før du velger **Opprett betalinger**, kan du høyreklikke i rutenettet og eksportere en liste over fakturaene til Excel. Knappen **Opprett betalinger** oppretter leverandørbetalingene i betalingsjournalen.  
18. Skann betalingene og kontroller at betalingsmåten er definert for alle betalinger. Hvis du genererer betalingene, for eksempel skrive ut en sjekk eller opprette en elektronisk betaling, må betalingsmåten defineres. Betalingsmåten vil også angi standard bankkonto som betalingen skal skje fra.  
19. Klikk på **Ny** for å opprette en engangsbetaling. En engangsbetaling kan legges til i en betalingsjournal når som helst før postering. Dette gjøres ved å klikke på **Ny** og legge til betalingsinformasjonen manuelt, i stedet for å bruke **Betalingsforslag**.  
20. Velg leverandøren som betalingen skal utføres til.
21. Hvis det finnes en faktura å betale, velger du **Utlign transaksjoner** for å velge fakturaen for betaling. Hvis dette er en forskuddsbetaling, er dette trinnet valgfritt. Du kan opprette betalingen uten å merke noen fakturaer. 
22. Merk alle fakturaer som skal betales. Hvis du bruker **Utlign transaksjoner** til å velge fakturaer for betaling, beregnes betalingsbeløpet automatisk basert på hvilke fakturaer du merker for betaling og hvilket beløp du angir i **Beløp som skal utlignes**.
23. Klikk **OK**.
24. Hvis du vil slette en betaling, merker du raden.
25. Klikk **Slett**. Hvis du sletter en betaling, slettes bare betalingen. Alle fakturaer som er merket for betaling vil fremdeles være tilgjengelig for betaling med en annen betaling.
26. Klikk **Ja**.
27. Velg **Generer betaling** for å skrive ut sjekker eller opprette den elektroniske betalingsfilen.
28. Velg betalingsmåten som du vil generere. Betalingsjournalen kan inneholde betalinger for både sjekker og elektroniske betalinger, men du kan bare generere en betalingstype om gangen.
29. Velg bankkontoen som du vil generere betalingene fra.
30. Klikk **OK**. Betalinger genereres bare for betalinger som samsvarer med valgt **Betalingsmåte** og **Bankkonto**.
31. Hvis du genererer **Sjekker**, velger du **Dokument** for å sikre riktig utskriftsmål for sjekkene.
32. Klikk **OK**.
33. Klikk på **OK** for å generere betalingene.
34. Klikk på **Poster** hvis alle betalingene er godkjent og generert. 

