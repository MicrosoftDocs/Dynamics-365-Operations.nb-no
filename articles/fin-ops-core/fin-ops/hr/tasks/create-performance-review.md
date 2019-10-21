---
title: Opprette prestasjonsvurderinger
description: Dette emnet viser hvordan du oppretter en prestasjonsvurdering og beskriver formålet med hver del i vurderingen.
author: andreabichsel
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3583f974d1768e0efefb80f0ad8aa011669c1301
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179327"
---
# <a name="create-performance-reviews"></a>Opprette prestasjonsvurderinger

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet viser hvordan du oppretter en prestasjonsvurdering og beskriver formålet med hver del i vurderingen. Denne fremgangsmåten ble opprettet med demonstrasjonsdatafirmaet USMF.

1. Velg arbeidsområdet for **Ansattselvbetjening** på startsiden.
2. Klikk **Ny vurdering** for å opprette en ny vurdering.
3. Angi eller velg en verdi i **Vurderingstype**-feltet.
4. Angi eller velg en verdi i feltet **Ytelsesperiode**.
5. Angi en dato i **Sluttdato**-feltet.
6. Velg **OK**. Du kan også opprette en vurdering fra en mal. Dette er den beste måten å opprette en vurdering på fordi hver inndeling vil inneholde informasjonen du trenger for å starte en vurdering.  
7. Du kan vise eller skjule kategorier som vedleggskategorien:

    1. I handlingsruten velger du **Vis seksjoner** for å åpne nedtrekksdialogen.
    1. Velg **Ja** eller **Nei** i **Vis vedlegg**-feltet for å vise eller skjule vedleggskategorien.
    1. Velg **Lagre**.

8. Velg **Legg til mål i vurderingen** for å legge til et mål. Når du er ferdig, velg **OK**.
9. Velg **Legg til kompetanse** for å åpne nedtrekksdialogen.
10. Skriv inn en verdi i **Tittel**-feltet.
11. I **Beskrivelse**-feltet skriver du inn `Increase customer skills by working with the support team`.
12. Velg **OK**.
13. Velg **Skjul alle**.
14. Velg **Vis alle**.
15. Velg **Legg til kommentar**.
16. Velg **Poster**.
17. Velg kategorien **Målinger**.
18. Velg **Legg til måling** for å åpne nedtrekksdialogen.
19. Angi eller velg en verdi i feltet **Måling**.
26. Angi et tall i **Målbeløp**-feltet.
20. Velg **OK**.
21. Velg fanen **Aktiviteter**.
22. Velg **Legg til**.
23. Skriv inn en verdi i **Tittel**-feltet.
24. Skriv inn en verdi i **Beskrivelse**-feltet.
25. Angi en dato i **Startdato**-feltet.
26. Angi en dato i **Fullført dato**-feltet.
27. Velg **Ja** i **Utviklingsplan**-feltet.
28. Skriv inn en verdi i feltet **Nøkkelord**.
29. Velg **Lagre**.
30. Velg kategorien **Vurderinger**.  

    - I **Vurderingsdetaljer**-hurtigfanen kan ansatte vurdere seg selv og lederen vurdere den ansatte. Hvis det brukes vekter, beregnes vektverdien av poengsummene automatisk.  
    - Hvis du vil se denne delen, kan du aktivere parameterinnstillingene til å vise ansattvurderinger.  

31. Velg fanen **Godkjenninger**. Hvis vurderingen bruker arbeidsflyt, vises godkjenningene bare etter at arbeidsflyten er fullført. Hvis det ikke brukes arbeidsflyt, er både arbeideren og lederen oppført her. Avmerkingsboksen for nødvendig merkes på basis av innstillingene for vurderingstypen.  
32. Velg kategorien **Generelt**.

    - Ytelsesperioden oppretter standard start- og sluttdatoer. Disse datoene kan redigeres.  
    - Statusene kontrollerer tilgangen til vurderingen. **Ikke startet**-statusen tillater alle å redigere vurderingen. **Pågår**-statusen lar bare den ansatte vise og redigere vurderingen. Klar til vurdering lar bare lederen vise og redigere vurderingen. Endelig vurdering-statusen lar både den ansatte og lederen vise vurderingen og også redigere den hvis dette er angitt for vurderingstypen. Statusen **Fullført**, **Avvist** og **Annullert** gjør at vurderingen blir skrivebeskyttet.  

33. Skriv inn en verdi i feltet **Oversikt**.
34. Velg fanen **Gjennomgang**. Etter hvert som vurderingen endrer status, kan den ansatte og lederen legge til kommentarer for hvert mål eller hver kompetanse.  
35. Velg kategorien **Godkjenninger**. Arbeideren og sjefen kan godkjenne gjennomgangen. Når alle nødvendige godkjenninger er foretatt, endres statusen til **Fullført**, og da kan det ikke gjøres flere endringer.  
