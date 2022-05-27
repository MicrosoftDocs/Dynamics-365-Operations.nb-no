---
title: Vedlikeholde informasjon om ansattskade og -sykdom
description: Denne oppgaven beskriver hvordan du oppretter et skade- eller sykdomstilfelle.
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36c25626bcc828a2d341d4ce4c9fe8fdcd4e6583
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688552"
---
# <a name="maintain-employee-injury-and-illness-information"></a>Vedlikeholde informasjon om ansattskade og -sykdom


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Det anbefales at du fullfører hele oppgaveveiledningen Oppsett for skade og sykdom først, ettersom noe av oppsettsinformasjonen brukes her. 



Oppgaveveiledningen beskriver de grunnleggende trinnene for oppretting av en skade- eller sykdomssak. I tillegg til detaljene for skaden eller sykdommen, spores en saksstatus. Som standard har saker statusen **Åpen**. Du kan administrere statusen ved å bruke menyelementet **Saksstatus** øverst på siden.

1. Gå til **Personale \> Arbeidere \> Skade og sykdom \> Ulykkes- eller sykdomstilfeller**.
2. Velg **Ny**.
3. I **Saksbeskrivelse**-feltet angir du en verdi (for eksempel **Håndleddskade**).
4. I **Arbeider**-feltet angir eller velger du en verdi (for eksempel **Ana Bowman**).
5. I feltet **Dato og klokkeslett for tilfellet** angir du en dato og et klokkeslett (for eksempel 20. januar 2016, klokken 10:00).
6. Angi eller velg en verdi i feltet **Skade- eller sykdomstype** (for eksempel **Brudd**).
7. Angi eller velg en verdi i **Kroppsdel**-feltet (for eksempel **Håndledd**).
8. Angi eller velg en verdi i **Utfallstype**-feltet (for eksempel **Terapi**).
9. Angi dato og klokkeslett i feltet **Dato og klokkeslett rapportert**.

    Datoen og klokkeslettet for rapporteringen må være senere enn datoen og klokkeslettet for hendelsen.

10. Angi eller velg en verdi i feltet **Person som rapporterte sak**, (for eksempel **Ana Bowman**).

    Den angitte personen kan være en ansatt eller et annet vitne til hendelsen.

11. I **Tilfelle**-delen, i feltet **Hvor tilfellet inntraff**, angir du en verdi (for eksempel **Lager**).
12. I feltet **På arbeidsstedet** velger du **Ja** hvis tilfellet inntraff på arbeidsstedet.
13. I feltet **Dato og klokkeslett for arbeidsstart** angir du datoen og klokkeslettet da den berørte personen begynte å arbeide, før tilfellet inntraff.
14. I feltet **Jobb eller oppgave for ansatt** angir du jobben eller oppgaven som arbeideren utførte da tilfellet inntraff (for eksempel **Laste bokser**). 
15. I feltet **Årsak til tilfelle** angir du årsaken til tilfellet (for eksempel **Skled på vått gulv**).
16. Angi eller velg en verdi i **Alvorlighetsnivå**-feltet.
17. I feltet **Handling som må iverksettes**, angir du en verdi (for eksempel **Rydde opp søl umiddelbart**).
18. I feltet **Dager forventet borte fra arbeid** angir du antall dager personen forventes å være borte fra arbeid.

    Når personen kommer tilbake på jobb, oppdaterer du feltet **Dager borte fra arbeid** med det faktiske antallet dager personen hadde fravær.

19. I delen **Skade- eller sykdomskostnader** velger du **Legg til**.
20. Angi en dato i **Dato**-feltet.
21. Angi eller velg en verdi i **Kostnadstype**-feltet (for eksempel **Terapi**).

    Du kan også skrive inn i et beløp og legge ved relevant dokumentasjon til kostnaden (for eksempel fakturaer og legens merknader).

22. Velg **Legg til**.
23. Angi en dato i **Dato**-feltet.
24. Angi eller velg en verdi i **Kostnadstype**-feltet (for eksempel **Lege**).
25. I delen **Skade- eller sykdomsbehandlinger** velger du **Legg til**.
26. Angi dato og klokkeslett i **Behandlingsdato**-feltet.
27. Angi eller velg en verdi i **Behandlingstype**-feltet (for eksempel **Skinne**).
28. Valgfritt: Angi angi **Ja** for delen **Sykebesøk på intensivavdeling**.
29. Angi eller velg en verdi i **Behandlingskommentarer**-feltet (for eksempel **Skinne i 2 uker**).
30. I feltet **Navn på lege** angir du en verdi (for eksempel **Dr. Anderson**).
31. I feltet **Behandlingsfasilitet og -sted** skriver du inn en verdi (for eksempel **Almegt. legevakt**).
32. I **Behandlingsdetaljer**-feltet angir du en verdi (for eksempel **Røntgenbilder bekrefter brudd, bruk skinne**).
33. Velg **Lagre**.

Saksstatusen kan oppdateres når som helst. Hvis behandlingen av skaden eller sykdommen pågår, setter du statusen til **Pågår**. Når du har lukket hendelsen, kan du bare legge til eller fjerne kostnader, behandlinger eller arkiveringer som er knyttet til hendelsen. Hvis du vil endre annen informasjon, må du åpne saken på nytt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
