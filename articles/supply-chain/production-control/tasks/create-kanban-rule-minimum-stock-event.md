---
title: Opprette en Kanban-regel ved hjelp av en hendelse for minste beholdning
description: Denne fremgangsmåten fokuserer på oppsettet for å opprette en Kanban-regel som bruker en minste beholdning-hendelse for å sikre at et bestemt produkt alltid er tilgjengelig på em bestemt lokasjon.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19b4f80c6afa2634c469a23dfcd8dd8f151dd6cc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998709"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Opprette en Kanban-regel ved hjelp av en hendelse for minste beholdning

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten fokuserer på oppsettet for å opprette en Kanban-regel som bruker en minste beholdning-hendelse for å sikre at et bestemt produkt alltid er tilgjengelig på em bestemt lokasjon. Det opprettes en Kanban-regel for å overføre materiale til lokasjonen når lagernivået faller under 200 enheter. Ved å kjøre Behandling av utligningshendelse, opprettes de nødvendige Kanbanene. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven. Denne oppgaven er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt i et lean-miljø.


## <a name="create-a-new-kanban-rule"></a>Opprett en ny Kanban-regel
1. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
2. Klikk på Ny.
3. Velg Uttak i Type-feltet.
    * Denne typen brukes til å opprette Kanbaner for overføring.  
4. Velg Hendelse i feltet Etterfyllingsstrategi.
    * Hendelsesstrategien brukes for å opprette overføringen av Kanbaner basert på en hendelse. Senere i fremgangsmåten utløser du Kanbaner for overføring ved hjelp av lageretterfylling.  
5. Angi eller velg en verdi i feltet Første planaktivitet.
    * Angi eller velg ReplenishSpeakerComponents. Denne overføringsaktiviteten har mottakslager (utdata), og lokasjon 12, noe som innebærer at materialer vil bli flyttet til lokasjon 12 i lager 12.  
6. Vis delen Detaljer.
7. Angi eller velg en verdi i feltet Produkt.
    * Velg M0007.  
8. Utvid delen Hendelser.
9. Velg Parti i feltet Hendelse for lageretterfylling.
    * Dette oppretter Kanbaner for å oppfylle materialbehov på den tilknyttede plasseringen under behandling av utligningshendelse.  

## <a name="set-the-minimum-quantity-for-the-item"></a>Sette minimumsantallet for varen
1. Klikk på for å følge koblingen i Produkt-feltet.
2. Klikk på for å følge koblingen i Varenummer-feltet.
3. Vis Produktbilde-faktaboksen.
4. Klikk på Plan i handlingsruten.
5. Klikk på Varedekning.
6. Klikk på Ny.
7. Merk den valgte raden i listen.
8. Angi eller velg en verdi i feltet Lager.
    * Sett Lager til 12.  
9. Sett Minimum til 200.

## <a name="run-the-batch-event-creation-job"></a>Kjøre den satsvise jobben for oppretting av hendelse
1. Gå til Produksjonskontroll > Periodiske oppgaver > Satsvis behandling av Kanban-jobb > Behandling av utligningshendelse.
2. Klikk på OK.
3. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
4. Klikk på koblingen i den valgte raden i listen.
    * Velg Kanban-regelen som du opprettet tidligere.  
5. Vis delen Kanbaner.
    * Legg merke til at en Kanban ble opprettet for å overføre det nødvendige materialet til lager 12.  

