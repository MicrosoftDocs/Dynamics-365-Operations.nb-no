--- 
title: Opprette driftstidsmaler
description: "Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff1978f127a014e75619a4bbbb9b6ff3a3ad7c7a
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-working-time-templates"></a>Opprette driftstidsmaler

[!include[task guide banner](../../includes/task-guide-banner.md)]

Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode. Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.

1. Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.
2. Klikk Driftstidsmaler.

## <a name="create-working-time-template"></a>Opprette driftstidsmal
1. Klikk Ny.
2. Skriv inn en verdi i feltet Driftstidsmal.
3. Skriv inn en verdi i Navn-feltet.
4. Utvid delen Mandag.
5. Klikk Legg til.
6. Angi et klokkeslett i feltet Fra.
    * Angi tidspunktet når arbeidet begynner om morgenen.  
7. Angi et klokkeslett i feltet Til.
    * Angi tidspunktet når arbeidere tar lunsjpause.  
8. Klikk Legg til.
9. Angi et klokkeslett i feltet Fra.
    * Angi tidspunktet når arbeidet fortsetter etter lunsj.  
10. Angi et klokkeslett i feltet Til.
    * Angi slutten på arbeidsdagen.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikere arbeidstider til alle ukedager
1. Klikk Kopier dag.
    * Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.  
2. Klikk OK.
3. Klikk Kopier dag.
    * Kopier arbeidstidsdefinisjonene fra mandag til onsdag.  
4. Velg et alternativ i feltet Til ukedag.
5. Klikk OK.
6. Klikk Kopier dag.
    * Kopier arbeidstidsdefinisjonene fra mandag til torsdag.  
7. Velg et alternativ i feltet Til ukedag.
8. Klikk OK.
9. Klikk Kopier dag.
    * Kopier arbeidstidsdefinisjonene fra mandag til fredag.  
10. Velg et alternativ i feltet Til ukedag.
11. Klikk OK.

## <a name="define-time-slots-for-special-operations"></a>Definere tidsrom for spesielle operasjoner
1. Utvid delen Fredag.
2. Finn og velg ønsket post i listen.
3. Angi eller velg en verdi i feltet Egenskap.
4. Finn og velg ønsket post i listen.
5. Angi eller velg en verdi i feltet Egenskap.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Merke helgedager som lukket for plukking
1. Utvid delen Lørdag.
2. Velg Ja i feltet Lukket for plukk.
3. Utvid delen Søndag.
4. Velg Ja i feltet Lukket for plukk.

