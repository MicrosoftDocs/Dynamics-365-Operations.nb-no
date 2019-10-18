---
title: Opprette et lukket spørsmål
description: Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e4f9697fc00798d917db6f7f50d7e3b8739233
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179330"
---
# <a name="create-a-closed-ended-question"></a>Opprette et lukket spørsmål

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

