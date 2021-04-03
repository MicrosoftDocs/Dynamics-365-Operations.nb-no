---
title: Opprette aktivitetsrelasjon - Etterfølger
description: Flyten av aktiviteter i en lean produksjonsflyt er dokumentert gjennom aktivitetsrelasjoner.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f10ecb8e579975327440ede6ea383226645c8cf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255307"
---
# <a name="create-activity-relation---successor"></a>Opprette aktivitetsrelasjon - Etterfølger

[!include [banner](../../includes/banner.md)]

Flyten av aktiviteter i en lean produksjonsflyt er dokumentert gjennom aktivitetsrelasjoner. Denne registreringen viser hvordan du oppretter en aktivitetsrelasjon.

Forutsetninger:

- En produksjonsflyt og versjon i utkastmodus. 

- To aktiviteter som kommer etter hverandre i produksjonsflyten er opprettet, men ikke er tilknyttet.


## <a name="find-the-production-flow-version"></a>Finne produksjonsflytversjonen 
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
3. Klikk på koblingen i den valgte raden i listen.
4. Merk den valgte raden i listen.
5. Velg en utkastversjon i listen.
    * Aktivitetsrelasjoner kan legges til i både utkast eller aktive versjoner av en produksjonsflyt.  

## <a name="open-the-activity-overview"></a>Åpne aktivitetsoversikten
1. Klikk på Aktiviteter.
    * Legg merke til at skjemaet viser alle aktiviteter for produksjonsflyten som er fordelt til versjonen av produksjonsflytene som du arbeider i.  

## <a name="add-a-successor"></a>Legg til en etterfølgende aktivitet
1. Klikk på Legg til etterfølgende aktivitet.
2. Klikk på rullegardinknappen i feltet Aktivitet for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk på koblingen i den valgte raden i listen.
5. Merk av for Begrensning.
6. Angi et tall i feltet Begrensningsverdi.
    * Begrensningstiden er tiden som skal planlegges mellom den planlagte slutten av den foregående (forfallsdato og -klokkeslett) og den planlagte starten for den etterfølgende.  
7. Skriv inn en verdi i feltet Enheter.
8. Angi et tall i feltet Forhold for syklustid.
    * Hvis begge aktiviteter kjører på den samme takten, skal syklustidsforholdet være 1. Hvis den foregående aktiviteten kjøres med den etterfølgende aktiviteten Dobbel hastighet, skal forholdet være 2.   Syklustidforholdene brukes til å beregne de individuelle syklustidene for produksjonsflytaktivitetene.  
9. Klikk på OK.
10. Lukk siden.
11. Klikk på fanen GridPanel.
12. Lukk siden.
13. Oppdater siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]