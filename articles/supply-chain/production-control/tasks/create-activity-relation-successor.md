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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 261bb1b99045cc78f0e74e1ed2ad7fa133d8ebe6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212348"
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
3. Klikk koblingen i den valgte raden i listen.
4. Merk den valgte raden i listen.
5. Velg en utkastversjon i listen.
    * Aktivitetsrelasjoner kan legges til i både utkast eller aktive versjoner av en produksjonsflyt.  

## <a name="open-the-activity-overview"></a>Åpne aktivitetsoversikten
1. Klikk Aktiviteter.
    * Legg merke til at skjemaet viser alle aktiviteter for produksjonsflyten som er fordelt til versjonen av produksjonsflytene som du arbeider i.  

## <a name="add-a-successor"></a>Legg til en etterfølgende aktivitet
1. Klikk Legg til etterfølgende aktivitet.
2. Klikk rullegardinknappen i feltet Aktivitet for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Merk av for Begrensning.
6. Angi et tall i feltet Begrensningsverdi.
    * Begrensningstiden er tiden som skal planlegges mellom den planlagte slutten av den foregående (forfallsdato og -klokkeslett) og den planlagte starten for den etterfølgende.  
7. Skriv inn en verdi i feltet Enheter.
8. Angi et tall i feltet Forhold for syklustid.
    * Hvis begge aktiviteter kjører på den samme takten, skal syklustidsforholdet være 1. Hvis den foregående aktiviteten kjøres med den etterfølgende aktiviteten Dobbel hastighet, skal forholdet være 2.   Syklustidforholdene brukes til å beregne de individuelle syklustidene for produksjonsflytaktivitetene.  
9. Klikk OK.
10. Lukk siden.
11. Klikk kategorien GridPanel.
12. Lukk siden.
13. Oppdater siden.

