--- 
title: "Initialisere lagernivåer i lageret"
description: "Denne prosedyren viser hvordan du får lagerbeholdningen oppdatert manuelt ved hjelp av en varetilgangsjournal."
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45c93febbbc4ea78fe2b87735ed96fd773605d96
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Initialisere lagernivåer i lageret

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


