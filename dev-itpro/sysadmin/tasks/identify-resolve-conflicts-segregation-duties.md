--- 
title: "Identifisere og løse konflikter i arbeidsdeling"
description: "Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: fdc0bbd0a239c8d7719271445a4d6a5323e87aad
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identifisere og løse konflikter i arbeidsdeling

[!include[task guide banner](../../includes/task-guide-banner.md)]

Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere. Dette konseptet kalles arbeidsdeling. Når definisjonen av en sikkerhetsrolle eller rolletildelingene til en bruker bryter reglene, logges konflikten. Alle konflikter må løses av administratoren. Fullfør fremgangsmåten nedenfor for å identifisere og løse konflikter. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Bekrefte om brukerrolletilordninger samsvarer med nye regler for arbeidsdeling
1. Gå til Systemadministrasjon > Sikkerhet > Arbeidsdeling > Bekreft overholdelse av brukerrolletilordninger.
2. Klikk OK.
    * En varsling viser resultatet av valideringen.     Hvis det oppstår en konflikt, kan du åpne siden Brukere og endre brukerens rolletilordninger. Konflikter er også logget på siden Arbeidsdelingskonflikter.     Hvis du vil kjøre bekreftelsesprosessen som en satsvis jobb, velg Satsvis behandling, og deretter angir du partiparameterne. Når den satsvise jobben er kjørt, kan du vise konfliktene på siden Arbeidsdelingskonflikter.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Vise og løse tilordninger av brukerroller i konflikt
1. Gå til Systemadministrasjon > Sikkerhet > Arbeidsdeling > Arbeidsdelingskonflikter.
    * Velg en konflikt, og klikk deretter en av følgende knapper: Avslå tilordning – Avslå tilordningen av brukeren til den ekstra sikkerhetsrollen. Hvis du nekter en automatisk rolletilordning, merkes brukeren som utelatt fra rollen. Den ekskluderte brukeren har ikke tilgangen som er knyttet til rollen, og brukeren kan ikke tilordnes til rollen før administratoren fjerner utelatelsen.     Tillat tilordning – overstyr konflikten, og la brukeren bli tilordnet til begge sikkerhetsroller. Hvis du overstyrer en konflikt, må du angi en årsak i feltet Årsak til overstyring.  
2. Lukk siden.
3. Gå til Systemadministrasjon > Sikkerhet > Arbeidsdeling > Uløste konflikter for arbeidsdeling.
    * Velg en konflikt, og klikk deretter en av følgende knapper: Avslå tilordning – Avslå tilordningen av brukeren til den ekstra sikkerhetsrollen. Hvis du nekter en automatisk rolletilordning, merkes brukeren som utelatt fra rollen. Den ekskluderte brukeren har ikke tilgangen som er knyttet til rollen, og brukeren kan ikke tilordnes til rollen før administratoren fjerner utelatelsen.     Tillat tilordning – overstyr konflikten, og la brukeren bli tilordnet til begge sikkerhetsroller. Hvis du overstyrer en konflikt, må du angi en årsak i feltet Årsak til overstyring.    
4. Lukk siden.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Verifisere om eksisterende roller overholder nye regler for arbeidsdeling
1. Gå til Systemadministrasjon > Sikkerhet > Arbeidsdeling > Arbeidsdelingsregler.
    * Velg en regel.  
2. Klikk Valider plikter og roller.
    * Hvis noen eksisterende roller bryter en valgt regel, vises en melding som inneholder navnet på rollen og navnene på pliktene som er i konflikt med hverandre. Administratoren må angi reduksjonen for sikkerhetsrisikoen eller endre rollen slik at den ikke er et brudd på regler for arbeidsdeling.     Hvis ingen roller bryter en valgt regel, får du en melding som angir at alle roller er i samsvar.  


