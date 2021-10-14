---
title: Opprette aktivitetsrelasjon - Etterfølger
description: Flyten av aktiviteter i en lean produksjonsflyt er dokumentert gjennom aktivitetsrelasjoner.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cee0c75de1fee24cfb6df018de62ece102c96cc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579214"
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