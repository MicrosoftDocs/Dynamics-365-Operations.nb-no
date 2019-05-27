---
title: Opprette en ny Kanban-regel
description: Denne prosedyren fokuserer på å erstatte en eksisterende kanban-regel med en ny kanban-regel på en bestemt dato.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8a9367d4796999857e473bcbe36a709d534f3b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564069"
---
# <a name="create-a-replacement-kanban-rule"></a>Opprette en ny Kanban-regel

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på å erstatte en eksisterende kanban-regel med en ny kanban-regel på en bestemt dato. Dette er nyttig når endringer i reglene for produksjonsflyt eller etterfylling må koordineres og planlegges. USMF-demodatafirmaet brukes til å opprette denne prosedyren. Denne fremgangsmåten er ment for prosessingeniøren eller verdistrømlederen når de klargjør produksjon for en endret produksjonsflyt eller en ny etterfyllingsregel. Denne oppgaven kanban-regel 000022 med en ny regel og øker det maksimale antallet fra 48-100 for den nye regelen.


## <a name="select-a-kanban-rule-to-replace"></a>Velge en kanban-regel å erstatte
1. Gå til Kanban-regler.
2. Finn og velg ønsket post i listen.
    * Velg Kanban-regel 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Opprette en ny Kanban-regel
1. Klikk Erstatt Kanban-regel.
2. Angi dato og klokkeslett i feltet Gyldighetsdato.
    * Velg en dato i fremtiden, for eksempel én uke fra nå. Dette er datoen og klokkeslettet da den nye kanban-regelen blir aktiv og erstatter den gamle kanban-regelen.  
    * Hvis kanban-regelen endrer banen i produksjonsflyten, kan du velge en annen aktivitet.  I denne fremgangsmåten beholder vi aktiviteten uendret.  
3. Klikk OK.
    * Legg merke til at det opprettes en ny kanban-regel som erstatter kanban-regel 000022.  
    * Gyldighetsdatoen angis i henhold til datoen som velges når du erstatter kanban-regelen.  
4. Finn og velg ønsket post i listen.
    * Velg den erstattede kanban-regelen 000022.  
    * Legg merke til at den erstattede kanban-regelen har samme dato som utløpsdatoen fordi dette er datoen den utløper.  
5. Velg rad 1 i listen.
    * Velg den nye kanban-regelen øverst i listen. Dette er Kanban-regelen med det høyeste kanban-regelnummeret.  
6. Klikk koblingen i den valgte raden i listen.
    * Klikk kanban-regelnummeret for å åpne kanban-regelen.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Endre maksimalt antall for den nye kanban-regelen
1. Sett Maksimalt antall til 100.
    * Vis hurtigfanen Antall hvis du vil vise Maksimalt antall-feltet. Hvis du endrer det maksimale antallet til 100, kan opptil 100 Kanbaner behandles.    Dette er det siste trinnet i oppgaven.  

