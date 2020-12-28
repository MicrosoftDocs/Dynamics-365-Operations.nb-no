---
title: Definere produksjonsflytmodeller
description: Produksjonsflytmodeller beskrive hvordan kapasiteten for arbeidsceller for lean manufacturing er beregnet og opprettholdt.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlowModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 511c466d6019cb182c9ada0b02172b8eeb3725e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434109"
---
# <a name="define-production-flow-models"></a>Definere produksjonsflytmodeller

[!include [banner](../../includes/banner.md)]

Produksjonsflytmodeller beskrive hvordan kapasiteten for arbeidsceller for lean manufacturing er beregnet og opprettholdt. Definisjonen av en Produksjonsflytmodell er derfor en forutsetning for definisjon av arbeidsceller. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="define-a-production-flow-model"></a>Definer en produksjonsflytmodell. 
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflytmodeller.
2. Klikk Ny.
3. Angi en ID for produksjonsflytmodellen i feltet Produksjonsflytmodell.
4. Velg et alternativ i Modelltype-feltet.
    * Det finnes to modelltyper: gjennomstrømmingstype og type for timer. For gjennomstrømmingstype vil kapasiteten i arbeidsceller som bruker denne produksjonsflytmodellen, bli uttrykt og beregnet i produktantall. For type for timer vil kapasiteten i arbeidsceller som bruker denne produksjonsflytmodellen, bli uttrykt og beregnet i timer. Legg merke til at denne egenskapen ikke kan endres for en eksisterende produksjonsflytmodell. Når en arbeidscelle har kapasitetsreservasjoner, kan ikke produksjonsflytmodelltypen endres.  
5. Skriv inn antallet dager i EPE-syklusen.
    * Intervallet beskriver perioden når hver del som produseres av en produksjonsflyt eller arbeidscelle, vil bli produsert minst én gang. Jo kortere EPE-syklus, jo mer fleksibel er produksjonsprosessen. Hvis EPE-syklus = 0, kan alt behov produseres på samme dag. EPE-syklus brukes til å planlegge lean-prosessjobber. Når du planlegger en jobb i en arbeidscelle med EPE-syklus = 5, vil planleggingsprosessen se etter kapasitet i arbeidscellen ved forfallsdato – EPE-syklus (5 dager foran forfallsdatoen) for å sikre at produktet kan produseres i denne syklusen. Leveringstid for lager for et produkt er vanligvis lik eller større enn EPE-syklusen for den relaterte produksjonsprosessen.  
6. Velg et alternativ i feltet Type planleggingsperiode.
    * Når en arbeidscelle har kapasitetsreservasjoner, kan ikke typen planleggingsperiode endres. Du kan bare velge produksjonsflytmodeller med samme periodetype for denne gitte arbeidscellen.  
7. I feltet Horisont for tidsplanlegging angir du et tall.
    * Planleggingshorisonten beskriver hvor mange dager kapasitetsreservasjoner kan utføres for de relaterte arbeidscellene. I horisonten for tidsplanlegging angir du antallet dager.   Kanban-prosessjobber som faller utenfor denne perioden, planlegges ikke med automatisk planlegging. Horisonten for tidsplanlegging er vanligvis to ganger gjennomsnittlig leveringstid for beholdning for produktene som produseres i en produksjonsflyt eller arbeidscelle. EPE-syklus må ikke være mer enn halvparten planleggingshorisonten.     
8. Velg et alternativ i feltet Reaksjon på kapasitetsmangel.
    * Alternativene omfatter: Utsett – utsetter fullstendig behovet for planleggingshendelsen på neste tilgjengelige produksjonsdag, med tilgjengelig kapasitet. Avbryt – Avslutter automatisk planlegging for planleggingshendelsen og lar de relaterte jobbene være uplanlagt.   Legg til for ønsket dag - planlegg de ønskede jobbene for den ønskede perioden. Dette overbelaster cellen for denne dagen og krever at planleggeren ser gjennom og foretar en manuell samhandling.   Distribuer til tilgjengelig perioder - distribuer de ulike jobbene for planleggingshendelsen til alle tilgjengelige produksjonsdager, med start fra den første tilgjengelige dagen. Minste distribusjonsantall er kanban-jobbantallet. Distribusjonen tilordner minste planleggingsantall (kanban-antall) til hver dag med nok tilgjengelig gjennomstrømning.  

