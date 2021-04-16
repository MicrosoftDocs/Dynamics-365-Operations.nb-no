---
title: Opprette driftstidsmaler
description: Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1885aba11b5c6878cc9dca615cea98b77b4df63f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811588"
---
# <a name="create-working-time-templates"></a>Opprette driftstidsmaler

[!include [banner](../../includes/banner.md)]

Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode. Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.

1. Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.
2. Klikk på Driftstidsmaler.

## <a name="create-working-time-template"></a>Opprette driftstidsmal
1. Klikk på Ny.
2. Skriv inn en verdi i feltet Driftstidsmal.
3. Skriv inn en verdi i Navn-feltet.
4. Utvid delen Mandag.
5. Klikk på Legg til.
6. Angi et klokkeslett i feltet Fra.
    * Angi tidspunktet når arbeidet begynner om morgenen.  
7. Angi et klokkeslett i feltet Til.
    * Angi tidspunktet når arbeidere tar lunsjpause.  
8. Klikk på Legg til.
9. Angi et klokkeslett i feltet Fra.
    * Angi tidspunktet når arbeidet fortsetter etter lunsj.  
10. Angi et klokkeslett i feltet Til.
    * Angi slutten på arbeidsdagen.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikere arbeidstider til alle ukedager
1. Klikk på Kopier dag.
    * Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.  
2. Klikk på OK.
3. Klikk på Kopier dag.
    * Kopier arbeidstidsdefinisjonene fra mandag til onsdag.  
4. Velg et alternativ i feltet Til ukedag.
5. Klikk på OK.
6. Klikk på Kopier dag.
    * Kopier arbeidstidsdefinisjonene fra mandag til torsdag.  
7. Velg et alternativ i feltet Til ukedag.
8. Klikk på OK.
9. Klikk på Kopier dag.
    * Kopier arbeidstidsdefinisjonene fra mandag til fredag.  
10. Velg et alternativ i feltet Til ukedag.
11. Klikk på OK.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]