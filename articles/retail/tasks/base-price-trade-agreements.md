--- 
title: Opprette kanalspesifikke forretningsavtaler
description: "Denne prosedyren hjelper med å opprette kanalspesifikke salgsprisforretningsavtaler."
author: josaw1
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 4cc797d2e23f0c7b14564415de6153ac0894c727
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="create-channel-specific-trade-agreements"></a>Opprette kanalspesifikke forretningsavtaler

[!include [task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren hjelper med å opprette kanalspesifikke salgsprisforretningsavtaler. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.

1. Gå til Detaljhandel og handel > Priser og rabatter > Prisgrupper > Alle prisgrupper.
    * Prisgrupper er måten forretningsavtaler tilordnes til bestemte kanaler på. Kanalspesifikke priser blir mulig ved å bruke prisgrupper for å tilordne forretningsavtaler til en kanal.  
2. Klikk Ny.
3. Skriv inn en verdi i feltet Prisgrupper.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk Lagre.
6. Lukk siden.
7. Gå til Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelsbutikker.
8. Velg New York i listen.
9. Klikk Butikk i handlingsruten.
10. Klikk Prisgrupper.
11. Klikk Ny.
12. Klikk rullegardinknappen i Prisgrupper-feltet for å åpne oppslaget.
13. Finn og velg ønsket post i listen.
14. Klikk Lagre.
15. Lukk siden.
16. Lukk siden.
17. Gå til Detaljhandel og handel > Produkter og kategorier > Utgitte produkter etter kategori.
18. Klikk koblingen i den valgte raden i listen.
19. Klikk Rediger
20. Aktiver/deaktiver utvidelsen av delen Selg.
21. Angi et tall i Pris-feltet
    * Denne prisen brukes hvis det ikke blir funnet en gjeldende forretningsavtale.  
22. Klikk Lagre.
23. Klikk Selg i handlingsruten.
24. Klikk Opprett forretningsavtaler.
25. Klikk Ny.
26. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
27. Velg Detaljhandel i listen.
    * I demonstrasjonsdataene har journalnavnet Detaljhandel standardrelasjonen Pris (salg). Det betyr at alle nye linjer som opprettes, bruker salgsprisforretningsavtaler som standard.  
28. Klikk Linjer.
29. Velg Gruppe i Kontokode-feltet.
30. Klikk rullegardinknappen i feltet Kontovalg for å åpne oppslaget.
31. Finn og velg ønsket post i listen.
    * Dette fullfører koblingen fra kanal til prisgruppe til forretningsavtale.  
32. Skriv inn en verdi i Varerelasjon-feltet.
33. Angi en verdi i feltet Beløp i valuta.
34. Merk av eller fjern merket for Søk etter neste.
    * Når Søk etter neste settes til Ja, fortsetter prissettingsmotoren å søke etter gjeldende forretningsavtaler med en lavere salgspris. Når Søk etter neste settes til Nei, slutter motoren å søke og bruker forretningsavtalen.  
35. Klikk Poster.
36. Klikk OK.
37. Lukk siden.
38. Klikk Selg i handlingsruten.
39. Klikk Salgspris.


