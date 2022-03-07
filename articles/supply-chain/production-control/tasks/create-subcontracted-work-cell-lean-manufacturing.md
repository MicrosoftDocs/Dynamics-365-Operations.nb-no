---
title: Opprette en arbeidscelle for underleveranse for lean manufacturing
description: For å modellere underleveransearbeidet for lean manufacturing må du opprette en arbeidscelle som er knyttet til leverandøren som har arbeidet.
author: cvocph
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acb0adf3e53830f951ae6d1faefd3f30aa3a445e28dc1a08b76a408bdf9af810
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744684"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Opprette en arbeidscelle for underleveranse for lean manufacturing

[!include [banner](../../includes/banner.md)]

For å modellere underleveransearbeidet for lean manufacturing må du opprette en arbeidscelle som er knyttet til leverandøren som har arbeidet. En arbeidscelle for underleveranse er knyttet til leverandøren via tilknytningen for en ressurs av typen leverandør. Hvis du spiller dette opptaket i USMF-demofirmaet, kan du velge leverandørkonto ID 1002 og område 1.


## <a name="create-a-vendor-resource"></a>Opprette en leverandørressurs
1. Gå til Ressurser.
2. Klikk på Ny.
3. Skriv inn en verdi i Ressurs-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg 'Leverandør' i Type-feltet.
6. Klikk på rullegardinknappen i feltet Leverandør for å åpne oppslaget.

## <a name="create-the-resource-group"></a>Opprette ressursgruppen
1. Gå til Ressursgrupper.
2. Klikk på Ny.
3. Skriv inn en verdi i Ressursgruppe-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk på rullegardinknappen i Område-feltet for å åpne oppslaget.
    * Velg området som arbeidscellen skal tilordnes til. I teorien kan et område representere ett enkelt område som styres av en leverandør. Imidlertid tildeles i de fleste tilfeller underleveranseressurser bare til området som bestiller arbeidet fra underleverandøren. Legg merke til at inngående og utgående lagre fra arbeidsceller til underleverandører må være i samme område.  
6. Skriv inn en verdi i Område-feltet.
7. @SysTaskRecorder:_RequestClose
8. Merk av eller fjern merket i avmerkingsboksen Arbeidscelle.
9. Klikk på rullegardinknappen i feltet Innleveringslager for å åpne oppslaget.
    * Velg lageret og lokasjonen som brukes til å klargjøre materialet for den leverandøradministrerte arbeidscellen. Lager og lokasjon er utformet ved hjelp av et eget lager per leverandør og ett sted per arbeidscellen i mange tilfeller.  
10. Klikk på rullegardinknappen i feltet Innleveringssted for å åpne oppslaget.
11. Klikk på rullegardinknappen i feltet Utleveringslager for å åpne oppslaget.
    * Definer lager og lokasjonen der materialet posteres ved postering av aktiviteter i underleveranser for arbeidscellen. Lager og lokasjon kan være på leverandørområdet for hvis leverandøren rapporterer kanban-jobbene. Lager og lokasjon kan også være mottar plasseringen som er knyttet til det neste trinnet i produksjonsflyten.  
12. Klikk på rullegardinknappen i feltet Utleveringssted for å åpne oppslaget.
13. Vis eller skjul delen Kalendere.
14. Klikk på Legg til.
15. Klikk på rullegardinknappen i Kalender-feltet for å åpne oppslaget.
    * Tilknytt arbeidstidskalenderen for arbeidscellen til ressursgruppen. For kritiske ressurser anbefaler vi at du definerer bestemte kalendere som representerer nøyaktig arbeidstidene og tilknyttede kapasitet på webområdet arbeid cellen eller leverandør.  
16. Vis eller skjul delen Ressurser.
17. Klikk på Legg til.
    * En ressursgruppe for underleveranse må ha en tilknyttet ressurs av typen Leverandør, som kobler ressursgruppen til kundens leverandørkonto.  
18. Klikk på rullegardinknappen i feltet Ressurser for å åpne oppslaget.
    * Velg eller angi leverandørressursen som du opprettet i den forrige delaktiviteten.  
19. Vis eller skjul delen Arbeidscellekapasitet.
20. Klikk på Legg til.
    * En arbeidscelle må ha en definert kapasitet. I dette eksemplet oppretter vi en gjennomstrømningskapasitet på 100 enheter per standard arbeidsdag.  
21. Klikk på rullegardinknappen i feltet Produksjonsflytmodell for å åpne oppslaget.
22. Velg et alternativ i Kapasitetsperiode-feltet.
23. Angi et nummer i feltet Gjennomsnittlig gjennomstrømningsantall.
24. Klikk på rullegardinknappen i feltet Enhet for å åpne oppslaget.
25. ResolveChanges enheten.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]