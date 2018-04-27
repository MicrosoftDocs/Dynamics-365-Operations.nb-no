--- 
title: "Opprette et lukket spørsmål"
description: "Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fdfac92b80774adb8376d5c2e945d063173188c8
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-closed-ended-question"></a>Opprette et lukket spørsmål

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant. Du må først opprette svargruppen med svar, og deretter opprette spørsmålet som bruker svargruppen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-an-answer-group"></a>Opprette en svargruppe
1. Gå til Spørreskjema > Utform > Svargrupper.
2. Klikk Ny.
3. Skriv inn en verdi i Svargruppe-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
    * Bruk funksjonen Tilfeldig rekkefølge til å plassere svarene tilfeldig i en annen rekkefølge hver gang svargruppen brukes for et spørsmål.  
5. Klikk Svar.
6. Klikk Ny.
    * Sekvensnummeret styrer rekkefølgen som svar vises i, med mindre Tilfeldig rekkefølge velges for svargruppen.  
    * Poeng kan tildeles til svarene for bruk i poengberegning for spørreskjemaet.  
7. Angi et tall i Poeng-feltet.
    * Det riktige svaret kan merkes for å indikere at det valgte svaret er riktig. Dette kan brukes for poengberegning for spørreskjemaet.  
8. Skriv inn en verdi i Svar-feltet.
    * Fortsett å opprette svaralternativer for svargruppen.  
9. Klikk Ny.
10. Angi et tall i Poeng-feltet.
11. Skriv inn en verdi i Svar-feltet.
12. Klikk Ny.
13. Angi et tall i Poeng-feltet.
14. Skriv inn en verdi i Svar-feltet.
15. Klikk Ny.
16. Angi et tall i Poeng-feltet.
17. Skriv inn en verdi i Svar-feltet.
18. Klikk Ny.
19. Angi et tall i Poeng-feltet.
20. Skriv inn en verdi i Svar-feltet.
21. Lukk siden.
22. Lukk siden.

## <a name="create-the-question"></a>Opprette spørsmålet
1. Gå til Spørreskjema > Utform > Spørsmål.
2. Klikk Ny.
3. Bruk Type-feltet til å gruppere relaterte spørsmål.
    * Du kan bruke inndatatyper for avmerkingsboks, alternativknapp eller kombinasjonsboks for lukkede spørsmål.  
4. Velg et alternativ i Inndatatype-feltet.
5. Angi eller velg en verdi i Svargruppe-feltet.
6. Skriv inn en verdi i Tekst-feltet.


