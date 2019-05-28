---
title: " Definere fordelsprogrammer"
description: Denne prosedyren viser hvordan du konfigurerer et fordelsprogram med to fordelslag.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e57bb9c9e3348f2a9853dfda1351a8a75261beb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560766"
---
# <a name="define-loyalty-programs"></a> Definere fordelsprogrammer

[!include [task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du konfigurerer et fordelsprogram med to fordelslag. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.

1. Gå til Detaljhandel og handel > .. > Fordelsprogrammer.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk Legg til linje.
6. Angi et nummer i Nivå-feltet.
7. Angi et navn på fordelslaget i Lag-feltet.
8. Skriv inn en verdi i Beskrivelse-feltet.
9. Klikk rullegardinknappen i feltet Datointervall for å åpne oppslaget.
    * Dette datointervallet må være frem i tid. Hvis datointervallet som er valgt for gullnivå, for eksempel er en periode på ett år, kan kunder som kvalifiserer for gullnivået motta fordelene som er tilordnet gullnivået, i ett år. Hvis kunder kvalifiserer seg for gullnivået på nytt mens de er på dette nivået, utsettes utløpsdatoen for nivået med enda et år fra den dagen de kvalifiserer seg på nytt.  
10. Klikk koblingen i den valgte raden i listen.
11. Klikk Legg til linje.
12. Angi et nummer i Nivå-feltet.
13. Angi et navn på fordelslaget i Lag-feltet.
14. Skriv inn en verdi i Beskrivelse-feltet.
15. Klikk rullegardinknappen i feltet Datointervall for å åpne oppslaget.
16. Klikk koblingen i den valgte raden i listen.
17. Klikk Lagre.
18. Finn og velg ønsket post i listen.
    * Lagregler definerer det minste antallet fordelspoeng som må være opptjent i en tidsperiode for å kvalifisere for laget.  
19. Aktiver/deaktiver utvidelsen av delen Regler for lag.
20. Klikk Ny.
    * Du kan ha mer enn én lagregel per lag. Du kan for eksempel har tre ulike kriterier for å oppnå et lag: ved å bruke 500 kroner på én måned, ved å bruke 1000 kroner over ett år og ved å ha 20 transaksjoner på ett år. Hvis du vil gjøre dette, må du opprette tre lagregler.  
21. Klikk rullegardinknappen i feltet Fordelspoeng for å åpne oppslaget.
    * Dette bør være fordelspoeng som ikke kan innløses.  
22. Klikk koblingen i den valgte raden i listen.
23. Angi et nummer i feltet Minimalt antall utstedte poeng.
    * For det laveste nivålaget angir du 0 hvis alle kunder kvalifiserer seg bare ved å delta i programmet.  
24. Klikk rullegardinknappen i feltet Datointervall for evaluering for å åpne oppslaget.
    * Dette datointervallet må strekke seg bakover i tid. Bare poeng som opptjenes i dette datointervallet skal telles mot en oppnåelse av verdien for minimalt antall utstedte poeng.  
25. Klikk koblingen i den valgte raden i listen.
26. Klikk Lagre.
27. Finn og velg ønsket post i listen.
28. Klikk Ny.
29. Klikk rullegardinknappen i feltet Fordelspoeng for å åpne oppslaget.
30. Klikk koblingen i den valgte raden i listen.
31. Angi et nummer i feltet Minimalt antall utstedte poeng.
32. Klikk rullegardinknappen i feltet Datointervall for evaluering for å åpne oppslaget.
    * Dette datointervallet må strekke seg bakover i tid.  
33. Klikk koblingen i den valgte raden i listen.
34. Klikk Lagre.
35. Klikk Prisgrupper.
    * Hvis du vil gi lojale kunder rabatter, må du tilordne én eller flere prisgrupper til fordelsprogrammet og tilordne prisgruppene til rabatter. Det er lurt ikke å blande prisgrupper på tvers av forskjellige typer rabattenheter.  Ikke bruk for eksempel den samme prisgruppen for en fordelsrabatt og en kanalrabatt.  
36. Klikk rullegardinknappen i Prisgruppe-feltet for å åpne oppslaget.
    * Prisgruppekoblingen øverst på siden er til fordelsprogrammet. Prisgruppekoblingen i hurtigfanen Programnivåer er bare for et bestemt fordelslag.  
37. Klikk koblingen i den valgte raden i listen.
38. Klikk Lagre.
39. Lukk siden.
40. Klikk Lagre.

