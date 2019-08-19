---
title: Opprette en Kanban-regel for flere aktiviteter
description: Denne fremgangsmåten viser hvordan du oppretter en Kanban-regel som inkluderer flere aktiviteter fra en produksjonsflyt.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c7be4e9da6f3dbaf2683c0dba78e0e780628f4b2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838661"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Opprette en Kanban-regel for flere aktiviteter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en Kanban-regel som inkluderer flere aktiviteter fra en produksjonsflyt. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven. Denne oppgaven er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt i et lean-miljø.


## <a name="create-a-new-kanban-rule"></a>Opprett en ny Kanban-regel
1. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
2. Klikk Ny.
3. Velg Planlagt i feltet Etterfyllingsstrategi.
4. Angi eller velg en verdi i feltet Første planaktivitet.
    * Velg SpeakerAssemblyAndPolish.  
5. Merk av for Flere aktiviteter.
    * Formålet er å inkludere flere enn én aktivitet i Kanban-regelen. Du kan velge en bane i produksjonsflyten når du velger den siste planaktiviteten.  
6. Angi eller velg en verdi i feltet Siste planaktivitet.
    * Velg SpeakerTestAndPackaging. Når du har valgt verdien, åpnes en side automatisk. Velg Kanban-flyten SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. Klikk OK.  
7. Vis delen Detaljer.
8. Angi eller velg en verdi i feltet Produkt.
    * Velg vare L0006.  

## <a name="create-kanban-and-view-jobs"></a>Opprette Kanban og vise jobber
1. Vis delen Kanbaner.
2. Klikk Legg til.
3. Skriv inn 1 i feltet Antall nye Kanbaner.
    * Dette oppretter én Kanban.  
4. Sett Produktantall til 3.
    * Kanbanen behandler tre produkter.  
5. Angi dato og klokkeslett i feltet Forfallsdato/-klokkeslett.
    * Du kan angi I dag.  
6. Klikk Opprett.
7. Klikk Detaljer.
    * Legg merke til at Kanbanen har to prosessjobber fra produksjonsflyten. Den første er SpeakerAssemblyAndPolish, og den andre er SpeakerTestAndPackaging.  
    * Dette er det siste trinnet!  

