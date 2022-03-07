---
title: Opprette et lukket spørsmål
description: Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3b90bb2a4981f32feb10ee1192e9c4d2e604e7a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071566"
---
# <a name="create-a-closed-ended-question"></a>Opprette et lukket spørsmål


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant. Du må først opprette svargruppen med svar, og deretter opprette spørsmålet som bruker svargruppen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-an-answer-group"></a>Opprette en svargruppe
1. Gå til **Spørreskjema** > **Utform** > **Svargrupper**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Svargruppe**-feltet.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
    * Bruk funksjonen **Tilfeldig rekkefølge** til å plassere svarene tilfeldig i en annen rekkefølge hver gang svargruppen brukes for et spørsmål.  
5. Klikk **Svar**.
6. Klikk på **Ny**.
    * Sekvensnummeret styrer rekkefølgen som svar vises i, med mindre **Tilfeldig rekkefølge** velges for **svargruppen**.  
    * Poeng kan tildeles til svarene for bruk i poengberegning for spørreskjemaet.  
7. Angi et tall i **Poeng**-feltet.
    * Det riktige svaret kan merkes for å indikere at det valgte svaret er riktig. Dette kan brukes for poengberegning for spørreskjemaet.  
8. Skriv inn en verdi i **Svar**-feltet.
    * Fortsett å opprette svaralternativer for svargruppen.  
9. Klikk på **Ny**.
10. Angi et tall i **Poeng**-feltet.
11. Skriv inn en verdi i **Svar**-feltet.
12. Klikk på **Ny**.
13. Angi et tall i **Poeng**-feltet.
14. Skriv inn en verdi i **Svar**-feltet.
15. Klikk på **Ny**.
16. Angi et tall i **Poeng**-feltet.
17. Skriv inn en verdi i **Svar**-feltet.
18. Klikk på **Ny**.
19. Angi et tall i **Poeng**-feltet.
20. Skriv inn en verdi i **Svar**-feltet.
21. Lukk siden.
22. Lukk siden.

## <a name="create-the-question"></a>Opprette spørsmålet
1. Gå til **Spørreskjema** > **Utform** > **Spørsmål**.
2. Klikk på **Ny**.
3. Bruk **Type**-feltet til å gruppere relaterte spørsmål.
    * Du kan bruke inndatatypene **Avmerkingsboks**, **Alternativknapp** eller **Kombinasjonsboks** for lukkede spørsmål.  
4. Velg et alternativ i **Inndatatype**-feltet.
5. Angi eller velg en verdi i **Svargruppe**-feltet.
6. Skriv inn en verdi i **Tekst**-feltet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
