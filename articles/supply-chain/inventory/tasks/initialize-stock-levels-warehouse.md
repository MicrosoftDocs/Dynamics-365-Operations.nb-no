---
title: Initialisere lagernivåer i lageret
description: Denne prosedyren viser hvordan du får lagerbeholdningen oppdatert manuelt ved hjelp av en varetilgangsjournal.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f922620c7aeeafd8560316239875c1ec5486191
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145692"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Initialisere lagernivåer i lageret

[!include [banner](../../includes/banner.md)]

Denne prosedyren viser hvordan du får lagerbeholdningen oppdatert manuelt ved hjelp av en varetilgangsjournal. (Det er også mulig å oppdatere lagerbeholdningen ved å importere transaksjonene i data-enheter.) Du kan kjøre denne veiledningen i demonstrasjonsdataselskapet USMF der alle forutsetninger som journalnavn, vareoppsett, posteringsprofiler, og kontoer er tilgjengelige. Veiledningen foreslår bestemte verdier for varen og dimensjonene som brukes. Hvis du velger en annen vare, må du kanskje angi verdier for forskjellige dimensjoner.

1. Gå til Lagerstyring > Journaloppføringer > Varer > Bevegelse.
2. Klikk Ny.
3. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
4. Velg IMov.
    * Det er lurt å bruke forskjellige journalnavnmaler for forskjellige forretningsformål.  
5. Klikk koblingen i den valgte raden i listen.
6. Angi verdiene 140200 i Motkonto-feltet.
    * Dette er motkontoen som skal være standardkonto på journallinjene. Det er mulig å overstyre standarden for å tilordne forskjellige motkontoer per linje.  
7. Klikk OK.
8. Klikk Ny.
9. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
10. Velg vare A0001.
11. Klikk koblingen i den valgte raden i listen.
12. Klikk kategorien Lagerdimensjoner.
13. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
14. Velg område 1.
15. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
16. Velg lager 13.
17. Klikk koblingen i den valgte raden i listen.
18. Klikk rullegardinknappen i Lokasjon-feltet for å åpne oppslaget.
19. Velg lokasjon 13.
20. Angi et tall i feltet Antall.
21. Klikk Lagre.
22. Klikk Poster.
23. Merk av eller fjern merket i boksen Overfør alle posteringsfeil til en ny journal.
    * Hvis du aktiverer dette alternativet, kopieres eventuelle linjer som ikke kan posteres, til en ny journal. Du kan bruke informasjonen i loggen til å rette opp problemene og deretter postere linjene på nytt.  
24. Klikk OK.
25. Lukk siden.
26. Lukk siden.

