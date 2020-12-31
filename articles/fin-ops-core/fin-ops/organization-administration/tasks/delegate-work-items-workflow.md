---
title: Delegere arbeidselementer i en arbeidsflyt
description: Hvis du planlegger å være borte fra kontoret eller av andre grunner ikke er tilgjengelig til å behandle arbeidselementer, kan du delegere eller tilordne arbeidselementer til andre brukere.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4b9abff57386fda61e3a83b0b8f18e533c8758c
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694647"
---
# <a name="delegate-work-items-in-a-workflow"></a>Delegere arbeidselementer i en arbeidsflyt

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Delegere et arbeidselement manuelt

For å delegere et individuelt arbeidselement, velg **Deleger**-alternativet på **Arbeidsflyt**-menyen, og angi deretter brukeren det skal delegeres til, sammen med en kommentar. Dette vil tilordne arbeidselementet til denne brukeren, slik at vedkommende kan fullføre det.

## <a name="manually-delegate-multiple-work-items"></a>Delegere flere arbeidselementer manuelt

Flere arbeidselementer kan delegeres sammen fra **Arbeidselementer som tilordnet til meg**-siden. Følgende arbeidsflyttyper er berettiget til massedelegering: arbeidsflyt for godkjenning av kjøpsavtale, bestillingsarbeidsflyt, innkjøpsrekvisisjonsgjennomgang og leverandørfakturaarbeidsflyt. **Deleger flere arbeidselementer**-funksjonen er deaktivert som standard, og kan aktiveres i **Arbeidsområder > Funksjonsstyring**. Ta kontakt med systemansvarlig for å få hjelp til å aktivere denne funksjonen.
1.  Gå til **Felles > Felles > Arbeidselementer > Arbeidselementer som er tilordnet til meg**.
2.  Velg arbeidselementene som skal delegeres.
3.  Klikk på **Deleger arbeidselementer**-menyen.
4.  Velg brukeren som arbeidselementene skal delegeres til, i **Bruker**-feltet.
5.  Angi en kommentar som forklarer hvorfor du delegerer arbeidselementene, i feltet **Kommentar**.
6.  Klikk på **Deleger arbeidselementer**-knappen for å fullføre arbeidselementdelegeringen.

## <a name="automatically-delegate-work-items"></a>Automatisk delegere arbeidselementer

Hvis du planlegger å være borte fra kontoret eller å ikke være tilgjengelig for jobb med arbeidselementer i en bestemt tidsperiode, kan du automatisk delegere nye arbeidselementer til andre brukere ved hjelp av siden **Brukeralternativer**.

### <a name="set-up-automatic-delegation"></a>Definere automatisk delegering
1. Gå til **Felles > Oppsett > Brukeralternativer**.
2. Klikk på kategorien **Arbeidsflyt**. Kontroller at Delegering-delen er utvidet. Hvis du vil konfigurere systemet slik at det automatisk delegerer arbeidselementene dine til andre brukere, må du opprette delegeringsregler, som angir når bestemte typer arbeidselementer delegeres. Hvis du vil opprette en delegeringsregel, gjør du følgende:  
3. Klikk **Legg til**.
4. Velg et alternativ i **Omfang**-feltet:
    - Alle – deleger alle arbeidsenheter som er tilordnet til deg.
    - Modul – deleger bare arbeidselementene som er knyttet til en bestemt type arbeidsflyt. Hvis du velger dette alternativet, må du velge typen arbeidsflyt i **Navn**-feltet.
    - Arbeidsflyt – deleger bare arbeidselementene som er knyttet til en bestemt arbeidsflyt. Hvis du velger dette alternativet, må du velge arbeidsflyten i **Navn**-feltet.  
5. I **Navn**-feltet:
    - For **Modul**-området velger du målmodulen.
    - For **Arbeidsflyt**-området velger du målarbeidsflyten.
6. Velg brukeren som arbeidselementene skal delegeres til, i **Deleger**-feltet. Bruk feltene **Startdato/-klokkeslett** og **Sluttdato/-klokkeslett** til å angi når du vil at arbeidselementer skal delegeres automatisk.  
7. Angi dato og klokkeslett i feltet **Startdato/-klokkeslett**.
8. Angi dato og klokkeslett i feltet **Sluttdato/-klokkeslett**.
9. Merk av for **Aktivert** for å aktivere denne delegeringsregelen. 
10. Angi en kommentar som forklarer hvorfor du delegerer arbeidselementene, i feltet **Kommentar**.
