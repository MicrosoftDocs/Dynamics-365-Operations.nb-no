---
title: Planlegge ruter for frakttransport med flere stopp
description: "Denne artikkelen beskriver de ulike elementene som du bruker for å planlegge transportruter i Dynamics 365 for Finance and Operations."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: e7965c094f91bcbcad21ecfa599f133a6e84f4f7
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Planlegge ruter for frakttransport med flere stopp
<a id="plan-freight-transportation-routes-with-multiple-stops" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver de ulike elementene som du bruker for å planlegge transportruter i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

Du kan bruke ruteplaner og ruteveiledninger for komplekse transportruter som har flere stopp. Hvis samme rute skal brukes regelmessig, kan du definere en planlagt rute.

## Ruteplaner
<a id="route-plans" class="xliff"></a>
En ruteplan inneholder rutesegmenter som inneholder informasjon om stoppene er besøkt på ruten og transportørene som brukes for hvert segment. Du må definere stoppene på ruten som huber. En hub kan være en leverandør, et lager, en kunde eller bare en lokasjon for ny innlasting der du kan endre transportør. Du kan definere spotvurderinger for ulike gebyrer for hvert segment. Her er noen eksempler:

-   Gebyrene for reising til de angitte segmentene
-   Tillegg for en henting av varene
-   Gebyrer for levering av varene

Hver ruteplan må være tilknyttet en ruteveiledning.

## Ruteveiledninger
<a id="route-guides" class="xliff"></a>
En ruteveiledning definerer vilkårene for å sammenligne en last med en bestemt ruteplan. Du kan for eksempel angi en opprinnelseshub og en målhub, grenser for containervolum eller -vekt, og en transportør, tjenesten eller gruppe. Ruteveiledninger er tilgjengelige på siden **Arbeidsområde for vurderingsrute**, der lastene kan samsvares med ruter manuelt eller automatisk. Hvis ruteveiledningen er for en planlagt rute, er den også tilgjengelig på siden **Arbeidsområde for lastplanlegging**

## Planlagte ruter
<a id="scheduled-routes" class="xliff"></a>
En planlagt rute er en forhåndsdefinert ruteplan som har en tidsplan for leveringdatoene. Planlagte ruter og ikke-planlagte ruter varierer med hensyn til hvordan laster tilordnes. Hvis du tilordner en ikke-planlagt rute ved hjelp av Arbeidsområde for vurderingsrute, valideres bare lasten og ruteveiledningen. Hvis du tilordner en planlagt rute, vurderes også datoer og adresser fra ordrene og hubene, og det tas også hensyn til datoen på ruteplanen. Du trenger ikke å bruke siden Arbeidsområde for vurderingsrute for å tilordne laster manuelt til en planlagt rute. I stedet kan du bruke Arbeidsområde for lastplanlegging til å foreslå at lasten bygges opp på kundeadresser og leveringsdatoer fra ordrer for en bestemt planlagt rute. For planlagte ruter vil ruteplanen har fast opprinnelse og målhuber. Vanligvis er transportør og tjeneste den samme for alle segmenter, men de kan være forskjellige. Målhubene opprettes ved hjelp av postnumre for kundene som besøkes på ruten. Flere rutetidsplaner kan defineres for en ruteplan. Ruteplanen må være tilknyttet en ruteveiledning. For planlagte ruter kan imidlertid planen tilknyttes bare én ruteveiledning. Ruteplanen brukes bare til å opprette de faktiske rutene på siden **Ruteplan**. Du kan bruke standardmalen for last når du foreslår laster på Arbeidsområde for lastplanlegging.

## Arbeidsområde for lastplanlegging
<a id="load-building-workbench" class="xliff"></a>
Arbeidsområde for lastplanlegging bruker kundeadresser og leveringsdatoer fra salgsordrer og planlagte ruter som er tilgjengelige, for å foreslå en last. Verdiene fra ruten angis i arbeidsområdet som standard. Du kan imidlertid velge en fra-dato som er eldre enn fra-datoen på ruten. Når en last blir foreslått, sjekkes leveringsadresse og leveringsdato for alle åpne ordrer. Hvis postnummeret for leveringsadressen samsvarer med postnummeret for en hub i ruteplanen, og hvis leveringsdatoen er innenfor området som er valgt i vilkårene, foreslås salgsordren for lasten. Det tas også hensyn til kapasiteten i lastmalen. Bare én last foreslås om gangen. Hvis du har en salgsordre som ikke er inkludert, må du kanskje bruke en annen lastmal (for eksempel en lastmal for en større lastebil eller container) eller planlegge en ekstra levering.




