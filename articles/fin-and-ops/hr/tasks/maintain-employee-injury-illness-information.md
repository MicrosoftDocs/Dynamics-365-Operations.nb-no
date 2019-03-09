---
title: Vedlikeholde informasjon om ansattskade og -sykdom
description: Vi anbefaler at du fullfører hele oppgaveveiledningen Oppsett for skade og sykdom først, ettersom noe av oppsettsinformasjonen brukes her.
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03d1e7f7b648e65cbe628aa4ff8b39dfa03ce96b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "332616"
---
# <a name="maintain-employee-injury-and-illness-information"></a>Vedlikeholde informasjon om ansattskade og -sykdom

[!include [task guide banner](../../includes/task-guide-banner.md)]

Vi anbefaler at du fullfører hele oppgaveveiledningen Oppsett for skade og sykdom først, ettersom noe av oppsettsinformasjonen brukes her. 



Oppgaveveiledningen dekker de grunnleggende trinnene for oppretting av en skade- eller sykdomssak. I tillegg til å spore detaljene for skaden eller sykdommen, finner du en saksstatus som også spores.  Saksstandardene med statusen Åpen.  Statusene kan administreres fra menyelementet Saksstatus på programlinjen øverst i skjemaet.

1. Gå til Personale > Arbeidere > Skade og sykdom > Ulykkes- eller sykdomstilfeller.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Saksbeskrivelse.
    * Eksempel: Håndleddskade  
4. Angi eller velg en verdi i Arbeider-feltet.
    * Eksempel: Ahmed Barnett  
5. Angi dato og klokkeslett i feltet Dato og klokkeslett for tilfellet.
    * Eksempel: 20.01.2016 10:00:00  
6. Angi eller velg en verdi i feltet Skade- eller sykdomstype.
    * Eksempel: Brudd  
7. Angi eller velg en verdi i Kroppsdel-feltet.
    * Eksempel: Håndledd  
8. Angi eller velg en verdi i Utfallstype-feltet.
    * Eksempel: Psykolog  
9. Angi dato og klokkeslett i feltet Dato og klokkeslett rapportert.
    * Datoen og klokkeslettet som rapporteres, må være senere enn datoen og klokkeslettet for hendelsen.  
10. Angi eller velg en verdi i feltet Person som rapporterte sak.
    * Dette kan være en ansatt eller et annet vitne til hendelsen.  Eksempel: Ahmed Barnett  
11. Utvid Tilfelle-delen.
12. Angi en verdi i feltet Hvor tilfellet inntraff.
    * Eksempel: Lager  
13. Velg Ja i feltet På arbeidsstedet.
    * Hvis hendelsen inntraff på arbeidsstedet, velger du ja.  
14. Angi dato og klokkeslett i feltet Dato og klokkeslett for arbeidsstart.
    * Angi datoen og klokkeslettet som den påvirkede personen startet arbeidet på, før den inntrufne hendelsen.  
15. Angi en verdi i feltet Jobb eller oppgave for ansatt.
    * Angi jobben eller oppgaven som arbeideren utførte da hendelsen oppstod.  Eksempel: Laste bokser  
16. Skriv inn en verdi i feltet Årsak til tilfelle.
    * Angi årsaken til hendelsen.  Eksempel: Skled på vått gulv  
17. Angi eller velg en verdi i Alvorlighetsnivå-feltet.
18. Angi en verdi i feltet Handling som må iverksettes.
    * Eksempel: Rydde opp søl umiddelbart  
19. Angi en verdi i feltet Dager forventet borte fra arbeid.
    * Angi hvor mange dager som personen er forventet å være borte fra arbeid.  Når personen kommer tilbake på jobb, oppdaterer du feltet Dager borte fra arbeid med faktisk antall fraværsdager.  
20. Utvid delen Skade- eller sykdomskostnader.
21. Klikk Legg til.
22. Angi en dato i Dato-feltet.
23. Angi eller velg en verdi i Kostnadstype-feltet.
    * Eksempel: Terapi Du kan også skrive inn i et beløp og legge ved relevant dokumentasjon til kostnaden, for eksempel fakturaer og legens merknader.  
24. Klikk Legg til.
25. Angi en dato i Dato-feltet.
26. Angi eller velg en verdi i Kostnadstype-feltet.
    * Eksempel: Lege  
27. Utvid delen Skade- eller sykdomsbehandlinger.
28. Klikk Legg til.
29. Angi dato og klokkeslett i Behandlingsdato-feltet.
30. Angi eller velg en verdi i Behandlingstype-feltet.
    * Eksempel: Skinne  
31. Du kan også angi Ja for delen Sykebesøk på intensivavdeling.
32. Skriv inn en verdi i Behandlingskommentarer-feltet.
    * Eksempel: Skinne i to uker  
33. Skriv inn en verdi i feltet Navn på lege.
    * Eksempel: Dr. Anderson  
34. Angi en verdi i feltet Behandlingsfasilitet og -sted.
    * Eksempel: Almegt. legevakt  
35. Skriv inn en verdi i Behandlingsdetaljer-feltet.
    * Eksempel: Røntgenbilder bekrefter brudd, bruk skinne  
36. Klikk Lagre.
    * Saksstatusen kan oppdateres når som helst.  Sett saken til arbeid pågår hvis behandlingen av skaden eller sykdommen pågår.  Når du lukker hendelsen, kan du bare legge til eller fjerne kostnader, behandlinger eller arkiveringer knyttet til hendelsen.  Hvis du vil endre annen informasjon, åpner du saken på nytt.  

