---
title: Opprette overføringsaktiviteter for lean manufacturing
description: Opprett en overføringsaktivitet for lean manufacturing.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eee0fd510639f2dad78fecb6395c0e31154db6b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568045"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Opprette overføringsaktiviteter for lean manufacturing

[!include [banner](../../includes/banner.md)]

Opprett en overføringsaktivitet for lean manufacturing. 

Forutsetninger: 

1. En produksjonsflyt og versjon som ikke er aktiv, må opprettes.

2. Fra- og Til- lager og -lokasjoner må opprettes. Arbeidscellen som skal etterfylles eller som er etterfylt, kan eventuelt opprettes.


## <a name="find-the-production-flow-version"></a>Finne produksjonsflytversjonen
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
    * Legg merke til at produksjonsflyten må ha en versjon i utkaststatus.  
3. Klikk på koblingen i den valgte raden i listen.

## <a name="create-a-new-activity"></a>Opprette en ny aktivitet
1. Klikk på Aktiviteter.
    * Kontroller at den valgte produksjonsflyten har en versjon i utkast, og velg den versjonen.  
2. Klikk på Opprett ny planaktivitet.
3. Klikk på Neste.
4. Skriv inn en verdi i Navn-feltet.
5. Velg Overføring i Aktivitetstype-feltet.
6. Angi et tall i feltet Prosessantall.
7. Klikk på Neste.

## <a name="select-the-work-cells"></a>Velge arbeidscellene
1. Klikk på rullegardinknappen i feltet Etterfyller for å åpne oppslaget.
    * Når du skal bruke utleveringsstedet for arbeidscellen som fra-lokasjon i overføringsaktiviteten, velger du en arbeidscelle. Det samme kan gjøres med den etterfylte arbeidscellen, som angir mållokasjonen for overføringsaktiviteten.  
2. Klikk på koblingen i den valgte raden i listen.

## <a name="define-the-inventory-updates"></a>Definere beholdningsoppdateringene
1. Velg et alternativ i Produkttype-feltet.
    * Legg merke til at en overføring ikke endrer typen produkt. Du kan overføre ferdige produkter eller halvfabrikata (overføring mellom to aktiviteter i en produksjonsflyt og eventuelt en kanban-flyt).     Når du overfører ferdige produkter, kan du velge om plukking eller mottak resulterer i en lagertransaksjon.  

## <a name="define-the-transfer-locations"></a>Definere overføringslokasjonene
1. Klikk på Neste.
2. Klikk på rullegardinknappen i Lager-feltet for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk på koblingen i den valgte raden i listen.
5. Klikk på rullegardinknappen i Lokasjon-feltet for å åpne oppslaget.
6. Klikk på koblingen i den valgte raden i listen.
7. I Fraktet av-feltet velger du "Speditør".
    * Alternativene omfatter: Speditør - organisasjonen betjener forsendelseslageret, Mottaker - organisasjonen betjener mottakslageret, Transportør - en tredjepartsleverandør. Hvis driftsorganisasjonen en leverandør, krever overføringsaktiviteten en utsettingsavtale.  
8. Klikk på Neste.

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
11. Klikk på Neste.
12. Klikk på Finish.
13. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]