--- 
title: Delegere arbeidselementer i en arbeidsflyt
description: "Hvis du planlegger å være borte fra kontoret eller av andre grunner ikke er tilgjengelig til å behandle arbeidselementer, kan du delegere eller tilordne arbeidselementer til andre brukere."
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4765fec0cdce0e2f8859c979ff97d20aa6b20bfa
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a>Delegere arbeidselementer i en arbeidsflyt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Hvis du planlegger å være borte fra kontoret eller av andre grunner ikke er tilgjengelig til å behandle arbeidselementer, kan du delegere eller tilordne arbeidselementer til andre brukere. Dette hjelper deg med å konfigurere systemet slik at det automatisk delegerer arbeidsenhetene dine til en annen bruker.



Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="set-up-automatic-delegation"></a>Definere automatisk delegering
1. Gå til Felles > Oppsett > Brukeralternativer.
2. Klikk Arbeidsflyt-kategorien.
    * Kontroller at delen Delegering er utvidet.    Hvis du vil konfigurere systemet slik at det automatisk delegerer arbeidselementene dine til andre brukere, må du opprette delegeringsregler, som angir når bestemte typer arbeidselementer delegeres. Hvis du vil opprette en delegeringsregel, gjør du følgende:  
3. Klikk Legg til.
4. Velg et alternativ i Omfang-feltet.
    * Alle – deleger alle arbeidsenheter som er tilordnet til deg.    Modul – deleger bare arbeidselementene som er knyttet til en bestemt type arbeidsflyt. Hvis du velger dette alternativet, må du velge typen arbeidsflyt i Navn-feltet.    Arbeidsflyt – deleger bare arbeidselementene som er knyttet til en bestemt arbeidsflyt. Hvis du velger dette alternativet, må du velge arbeidsflyten i Navn-feltet.  
5. Velg brukeren som arbeidselementene skal delegeres til, i Deleger-feltet.
    * Bruk feltene Startdato/-klokkeslett og Sluttdato/-klokkeslett til å angi når du vil at arbeidselementer skal delegeres automatisk.  
6. Angi dato og klokkeslett i feltet Startdato/-klokkeslett.
7. Angi dato og klokkeslett i feltet Sluttdato/-klokkeslett.
8. Merk av for Aktivert for å aktivere denne delegeringsregelen.
    * Hvis du valgte Modul som omfanget, må du velge modulen i Navn-feltet.    Hvis du valgte Arbeidsflyt som omfanget, må du velge den bestemte arbeidsflyten som skal delegeres, i Navn-feltet.  
9. Angi en kommentar som forklarer hvorfor du delegerer arbeidselementene, i feltet Kommentar.


