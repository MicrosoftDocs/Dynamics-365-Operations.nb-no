---
title: Opprette prosessaktiviteter for lean manufacturing
description: Opprett en prosessaktivitet for lean manufacturing.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd505446456791b26850d676722b6676b50dca4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981212"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>Opprette prosessaktiviteter for lean manufacturing

[!include [banner](../../includes/banner.md)]

Opprett en prosessaktivitet for lean manufacturing. 

Forutsetninger: 

1. En produksjonsflyt og versjon som ikke er aktiv, må opprettes.

2. En arbeidscelle må opprettes.


## <a name="find-the-production-flow-version"></a>Finne produksjonsflytversjonen
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
3. Klikk på koblingen i den valgte raden i listen.

## <a name="create-a-new-activity"></a>Opprette en ny aktivitet
1. Klikk på Aktiviteter.
    * Kontroller at den valgte produksjonsflyten har en versjon i utkast, og velg den versjonen.  
2. Klikk på Opprett ny planaktivitet.
3. Klikk på Neste.
4. Skriv inn en verdi i Navn-feltet.
5. Skriv inn en verdi i Navn-feltet.
    * Legg merke til at navnet må være unikt for en gitt produksjonsflyt for alle versjoner.  
6. Angi et tall i feltet Prosessantall.
    * Vær oppmerksom på at uansett hvilket jobbantall som blir behandlet, er dette det minste antallet per jobb for å beregne kostnaden for arbeid. Hvis jobbantall avviker fra dette antallet, vil arbeidskostnadsavvik opprettes.  
7. Klikk på Neste.

## <a name="select-the-work-cell"></a>Velge arbeidscellen
1. Klikk på rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.
2. Klikk på koblingen i den valgte raden i listen.

## <a name="define-the-inventory-updates"></a>Definere beholdningsoppdateringene
1. Merk av eller fjern merket i boksen Oppdater beholdningsmottak.
    * Hvis Oppdater beholdning = Nei, kan du definere aktiviteten for å motta et halvfabrikata (aktiviteten når ikke det neste nivået i stykklisten).    Du kan også velge å bruke halvfabrikata.  

## <a name="define-the-picking-activities"></a>Definere plukkaktivitetene
1. Klikk på Neste.
2. Merk den valgte raden i listen.
    * En standard plukkaktivitet opprettes for innleveringsstedet for den valgte arbeidscellen.  
3. Klikk på Legg til.
    * Du kan opprette flere plukkaktivitetene for bestemte produkter, som ikke er oppsamlet på innleveringsaktiviteten for arbeidscellen.  
4. Finn og velg ønsket post i listen.
5. Skriv inn en verdi i Varenummer-feltet.
6. Klikk på rullegardinknappen i Lager-feltet for å åpne oppslaget.
    * Med denne definisjonen plukkes alt materiale som forbrukes i aktiviteten fra standard innleveringslager og -lokasjon, med unntak av varen som er definert i den andre plukkaktiviteten. Denne varen plukkes fra et annet lager og en annen lokasjon.  
7. Finn og velg ønsket post i listen.
8. Klikk på koblingen i den valgte raden i listen.
9. Merk av eller fjern merket i boksen Registrer svinn.
10. Klikk på Neste.

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

