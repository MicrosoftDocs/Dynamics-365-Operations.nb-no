---
title: Opprette driftstidsmaler
description: Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130a21d08e4e720f8bf803a5d4b03d315cefc26f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580678"
---
# <a name="create-working-time-templates"></a>Opprette driftstidsmaler

[!include [banner](../../includes/banner.md)]

Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode. Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.

1. Gå til **Arbeidsområder > Administrasjon av livssyklus for ressurs**.
1. Velg **Driftstidsmaler**.

## <a name="create-working-time-template"></a>Opprette driftstidsmal

1. Velg **Ny**.
1. I feltet **Driftstidsmal** skriver du inn en verdi.
1. Skriv inn en verdi i **Navn**-feltet.
1. Utvid delen **Mandag**.
1. Velg **Legg til**.
1. Angi et klokkeslett i feltet **Fra**.
    * Angi tidspunktet når arbeidet begynner om morgenen.  
1. Angi et klokkeslett i feltet **Til**.
    * Angi tidspunktet når arbeidere tar lunsjpause.  
1. Velg **Legg til**.
1. Angi et klokkeslett i feltet **Fra**.
    * Angi tidspunktet når arbeidet fortsetter etter lunsj.  
1. Angi et klokkeslett i feltet **Til**.
    * Angi slutten på arbeidsdagen.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikere arbeidstider til alle ukedager

1. Velg **Kopier dag**.
    * Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.  
1. Velg **OK**.
1. Velg **Kopier dag**.
    * Kopier arbeidstidsdefinisjonene fra mandag til onsdag.  
1. Velg et alternativ i feltet **Til ukedag**.
1. Velg **OK**.
1. Velg **Kopier dag**.
    * Kopier arbeidstidsdefinisjonene fra mandag til torsdag.  
1. Velg et alternativ i feltet **Til ukedag**.
1. Velg **OK**.
1. Velg **Kopier dag**.
    * Kopier arbeidstidsdefinisjonene fra mandag til fredag.  
1. Velg et alternativ i feltet **Til ukedag**.
1. Velg **OK**.

## <a name="define-time-slots-for-special-operations"></a>Definere tidsrom for spesielle operasjoner

1. Utvid delen **Fredag**.
1. Finn og velg ønsket post i listen.
1. Angi eller velg en verdi i feltet **Egenskap**.
1. Finn og velg ønsket post i listen.
1. Angi eller velg en verdi i feltet **Egenskap**.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Merke helgedager som lukket for plukking

1. Utvid delen **Lørdag**.
1. Velg *Ja* i feltet **Lukket for plukk**.
1. Utvid delen **Søndag**.
1. Velg *Ja* i feltet **Lukket for plukk**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]