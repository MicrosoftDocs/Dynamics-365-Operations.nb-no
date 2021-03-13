---
title: Initialisere lagernivåer i lageret
description: Denne prosedyren viser hvordan du får lagerbeholdningen oppdatert manuelt ved hjelp av en varetilgangsjournal.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6934fc8142a589532cbd9d360ca0f8276456b20e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011555"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Initialisere lagernivåer i lageret

[!include [banner](../../includes/banner.md)]

Denne prosedyren viser hvordan du får lagerbeholdningen oppdatert manuelt ved hjelp av en varetilgangsjournal. (Det er også mulig å oppdatere lagerbeholdningen ved å importere transaksjonene i data-enheter.) Du kan kjøre denne veiledningen i demonstrasjonsdataselskapet USMF der alle forutsetninger som journalnavn, vareoppsett, posteringsprofiler, og kontoer er tilgjengelige. Veiledningen foreslår bestemte verdier for varen og dimensjonene som brukes. Hvis du velger en annen vare, må du kanskje angi verdier for forskjellige dimensjoner.

1. Gå til Lagerstyring > Journaloppføringer > Varer > Bevegelse.
2. Klikk på Ny.
3. Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.
4. Velg IMov.
    * Det er lurt å bruke forskjellige journalnavnmaler for forskjellige forretningsformål.  
5. Klikk på koblingen i den valgte raden i listen.
6. Angi verdiene 140200 i Motkonto-feltet.
    * Dette er motkontoen som skal være standardkonto på journallinjene. Det er mulig å overstyre standarden for å tilordne forskjellige motkontoer per linje.  
7. Klikk på OK.
8. Klikk på Ny.
9. Klikk på rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
10. Velg vare A0001.
11. Klikk på koblingen i den valgte raden i listen.
12. Klikk på fanen Lagerdimensjoner.
13. Klikk på rullegardinknappen i Område-feltet for å åpne oppslaget.
14. Velg område 1.
15. Klikk på rullegardinknappen i Lager-feltet for å åpne oppslaget.
16. Velg lager 13.
17. Klikk på koblingen i den valgte raden i listen.
18. Klikk på rullegardinknappen i Lokasjon-feltet for å åpne oppslaget.
19. Velg lokasjon 13.
20. Angi et tall i feltet Antall.
21. Klikk på Lagre.
22. Klikk på Poster.
23. Merk av eller fjern merket i boksen Overfør alle posteringsfeil til en ny journal.
    * Hvis du aktiverer dette alternativet, kopieres eventuelle linjer som ikke kan posteres, til en ny journal. Du kan bruke informasjonen i loggen til å rette opp problemene og deretter postere linjene på nytt.  
24. Klikk på OK.
25. Lukk siden.
26. Lukk siden.

