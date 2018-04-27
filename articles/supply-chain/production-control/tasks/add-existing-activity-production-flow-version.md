--- 
title: Legge til en eksisterende aktivitet i en produksjonsflytversjon
description: "Når du oppretter nye versjoner av produksjonsflyter, kan du velge å legge til aktiviteter som er opprettet for eldre versjoner, til den nye versjonen."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a74fb34db71ba4b539c1b6ede361329aaeb94920
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Legge til en eksisterende aktivitet i en produksjonsflytversjon

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Når du oppretter nye versjoner av produksjonsflyter, kan du velge å legge til aktiviteter som er opprettet for eldre versjoner, til den nye versjonen. Denne fremgangsmåten viser hvordan en ny versjon opprettes for en eksisterende produksjonsflyt, uten å kopiere aktivitetene. I det neste trinnet legges en eksisterende aktivitet til den nye versjonen. 

Denne oppgaven krever produksjonsflyt med versjon og aktiviteter som allerede er opprettet.


## <a name="create-a-new-production-flow-version"></a>Opprett en ny produksjonsflytversjon
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Rediger.
5. Merk den valgte raden i listen.
6. Angi dato og klokkeslett i feltet Utløpsdato.
    * Vær oppmerksom på at før du oppretter en ny produksjonsflytversjon, må du sjekke utløpsdatoen og -klokkeslettet for den aktive versjonen. Den nye versjonen opprettes med en gyldig startdato som knyttes til utløpsdatoen for den valgte versjonen.  
7. Klikk Legg til.
8. Velg Nei i Kopier fra versjon-feltet.
    * Velg Nei hvis du vil starte med en tom versjon hvis de fleste av aktivitetene i den kopierte versjonen vil bli erstattet av nye aktiviteter. Legg til de uendrede aktivitetene i Legg til eksisterende-funksjonen i aktivitetsskjemaet manuelt.  
9. Velg Nei i feltet Dupliser Kanban-regler.
    * Når aktivitetene ikke kopieres til den nye versjonen, er det ikke mulig å kopiere Kanban-reglene på tidspunktet for opprettelsen av den nye versjonen.   I stedet bruker du funksjonen Opprett ny Kanban senere i Kanban-regel-skjemaet for å erstatte Kanban-regler for den gamle produksjonsflytversjonen med Kanban-regler som bruker aktivitetene i den nye versjonen.  
10. Klikk OK.
11. Finn og velg ønsket post i listen.

## <a name="add-an-existing-activity"></a>Legge til en eksisterende aktivitet
1. Klikk Aktiviteter.
2. Klikk Legg til eksisterende for å åpne nedtrekksdialogen.
    * Finn og velg en eksisterende aktivitet som skal legges til den nye produksjonsflytversjonen.  Vær oppmerksom på at listen viser alle aktiviteter som er opprettet for denne produksjonsflyten for alle tidligere versjoner av flyten.  
3. Angi eller velg en verdi i feltet Aktivitet.
4. Klikk OK.


