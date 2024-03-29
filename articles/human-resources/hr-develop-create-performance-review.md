---
title: Opprette prestasjonsvurderinger
description: Denne artikkelen viser hvordan du oppretter en prestasjonsvurdering og beskriver formålet med hver del i vurderingen.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2de087f4e345ba826ddbe8a65f917476bd6894
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872188"
---
# <a name="create-performance-reviews"></a>Opprette prestasjonsvurderinger


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]


Denne artikkelen viser hvordan du oppretter en prestasjonsvurdering og beskriver formålet med hver del i vurderingen. Denne fremgangsmåten ble opprettet med demonstrasjonsdatafirmaet USMF.

1. Velg arbeidsområdet for **Ansattselvbetjening** på startsiden.
2. Klikk **Ny vurdering** for å opprette en ny vurdering.
3. Angi eller velg en verdi i **Vurderingstype**-feltet.
4. Angi eller velg en verdi i feltet **Ytelsesperiode**.
5. Angi en dato i **Sluttdato**-feltet.
6. Velg **OK**. Du kan også opprette en vurdering fra en mal. Dette er den beste måten å opprette en vurdering på fordi hver inndeling vil inneholde informasjonen du trenger for å starte en vurdering.  
7. Du kan vise eller skjule kategorier som vedleggskategorien:

    1. I handlingsruten velger du **Vis seksjoner** for å åpne dialogmenyen.
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
18. Velg **Legg til måling** for å åpne nedtrekksmenyen.
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
    - Hvis du vil vise denne delen, aktiverer du parameterinnstillingene for å vise ansattvurderinger på siden **Delte parametere for Human resources**.  

31. Velg fanen **Godkjenninger**. Hvis vurderingen bruker arbeidsflyt, vises godkjenningene bare etter at arbeidsflyten er fullført. Hvis det ikke brukes arbeidsflyt, er både arbeideren og lederen oppført her. Avmerkingsboksen **Obligatorisk** for **Godkjenninger** merkes på basis av innstillingene for vurderingstypen.  
32. Velg fanen **Generelt**.

    - Ytelsesperioden oppretter standard start- og sluttdatoer. Disse datoene kan redigeres.  
    - Statusene kontrollerer tilgangen til vurderingen. **Ikke startet**-statusen tillater alle å redigere vurderingen. **Pågår**-statusen lar bare den ansatte vise og redigere vurderingen. **Klar til vurdering** lar bare lederen vise og redigere vurderingen. Med **Endelig vurdering**-statusen kan begge ansatte og lederen vise og redigere gjennomgangen hvis alternativet **Tillat redigering i endelig vurdering** er valgt i gjennomgangstype. Statusen **Fullført** og **Annullert** gjør at vurderingen blir skrivebeskyttet. Hvis en gjennomgang blir **Avvist** og sendes tilbake til den ansatte, kan både den ansatte og den overordnede utføre nødvendige endringer, slik at den ansatte kan sende på nytt.

33. Skriv inn en verdi i feltet **Oversikt**.
34. Velg fanen **Gjennomgang**. Etter hvert som vurderingen endrer status, kan den ansatte og lederen legge til kommentarer for hvert mål eller hver kompetanse.  
35. Velg kategorien **Godkjenninger**. Arbeideren og sjefen kan godkjenne gjennomgangen. Når alle nødvendige godkjenninger er foretatt, endres statusen til **Fullført**, og da kan det ikke gjøres flere endringer.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
