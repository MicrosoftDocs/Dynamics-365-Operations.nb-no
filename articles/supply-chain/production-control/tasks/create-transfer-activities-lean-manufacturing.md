---
title: Opprette overføringsaktiviteter for lean manufacturing
description: Opprett en overføringsaktivitet for lean manufacturing.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36f79ef189924b0f3bd38cb764e73c6a0793353e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "331213"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Opprette overføringsaktiviteter for lean manufacturing

[!include [task guide banner](../../includes/task-guide-banner.md)]

Opprett en overføringsaktivitet for lean manufacturing. 

Forutsetninger: 

1. En produksjonsflyt og versjon som ikke er aktiv, må opprettes.

2. Fra- og Til- lager og -lokasjoner må opprettes. Arbeidscellen som skal etterfylles eller som er etterfylt, kan eventuelt opprettes.


## <a name="find-the-production-flow-version"></a>Finne produksjonsflytversjonen
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
    * Legg merke til at produksjonsflyten må ha en versjon i utkaststatus.  
3. Klikk koblingen i den valgte raden i listen.

## <a name="create-a-new-activity"></a>Opprette en ny aktivitet
1. Klikk Aktiviteter.
    * Kontroller at den valgte produksjonsflyten har en versjon i utkast, og velg den versjonen.  
2. Klikk Opprett ny planaktivitet.
3. Klikk Neste.
4. Skriv inn en verdi i Navn-feltet.
5. Velg Overføring i Aktivitetstype-feltet.
6. Angi et tall i feltet Prosessantall.
7. Klikk Neste.

## <a name="select-the-work-cells"></a>Velge arbeidscellene
1. Klikk rullegardinknappen i feltet Etterfyller for å åpne oppslaget.
    * Når du skal bruke utleveringsstedet for arbeidscellen som fra-lokasjon i overføringsaktiviteten, velger du en arbeidscelle. Det samme kan gjøres med den etterfylte arbeidscellen, som angir mållokasjonen for overføringsaktiviteten.  
2. Klikk koblingen i den valgte raden i listen.

## <a name="define-the-inventory-updates"></a>Definere beholdningsoppdateringene
1. Velg et alternativ i Produkttype-feltet.
    * Legg merke til at en overføring ikke endrer typen produkt. Du kan overføre ferdige produkter eller halvfabrikata (overføring mellom to aktiviteter i en produksjonsflyt og eventuelt en kanban-flyt).     Når du overfører ferdige produkter, kan du velge om plukking eller mottak resulterer i en lagertransaksjon.  

## <a name="define-the-transfer-locations"></a>Definere overføringslokasjonene
1. Klikk Neste.
2. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Klikk rullegardinknappen i Lokasjon-feltet for å åpne oppslaget.
6. Klikk koblingen i den valgte raden i listen.
7. I Fraktet av-feltet velger du "Speditør".
    * Alternativene omfatter: Speditør - organisasjonen betjener forsendelseslageret, Mottaker - organisasjonen betjener mottakslageret, Transportør - en tredjepartsleverandør. Hvis driftsorganisasjonen en leverandør, krever overføringsaktiviteten en utsettingsavtale.  
8. Klikk Neste.

## <a name="define-the-activity-times"></a>Definere aktivitetstidene
1. Finn og velg ønsket post i listen.
    * Definisjonen av en kjøretid er nødvendig. Kjøretiden brukes til å beregne kostnad og produksjonstidene for kanban-jobber. Kjøretider brukes ikke til å beregne kapasitetsbelastning og forbruk, som beregnes fra syklustid, som er avledet fra oppgaven for produksjonsflytversjonen.  
2. Angi et tall i feltet Tid.
3. Skriv inn en verdi i feltet Enhet.
4. Velg tidsenheten.
5. Angi et tall i feltet Per antall.
6. Finn og velg ønsket post i listen.
    * Køtider er valgfrie.  
7. Angi et tall i feltet Tid.
8. Skriv inn en verdi i feltet Enhet.
9. Velg tidsenheten.
10. Angi et tall i feltet Per antall.
11. Klikk Neste.
12. Klikk Finish.
13. Lukk siden.

