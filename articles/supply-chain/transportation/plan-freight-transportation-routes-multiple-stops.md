---
title: Planlegge ruter for frakttransport med flere stopp
description: Denne artikkelen beskriver de ulike elementene som du bruker for å planlegge transportruter i Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate, TMSRouteSchedule, TMSRouteRateDetail
audience: Application User
ms.reviewer: kamaybac
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e3d316b5bed67e84fdd5cec8b518069c053436d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671598"
---
# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Planlegge ruter for frakttransport med flere stopp

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver de ulike elementene som du bruker for å planlegge transportruter i Dynamics 365 Supply Chain Management.

Du kan bruke ruteplaner og ruteveiledninger for komplekse transportruter som har flere stopp. Hvis samme rute skal brukes regelmessig, kan du definere en planlagt rute.

## <a name="route-plans"></a>Ruteplaner
En ruteplan inneholder rutesegmenter som inneholder informasjon om stoppene er besøkt på ruten og transportørene som brukes for hvert segment. Du må definere stoppene på ruten som huber. En hub kan være en leverandør, et lager, en kunde eller bare en lokasjon for ny innlasting der du kan endre transportør. Du kan definere spotvurderinger for ulike gebyrer for hvert segment. Her er noen eksempler:

-   Gebyrene for reising til de angitte segmentene
-   Tillegg for en henting av varene
-   Gebyrer for levering av varene

Hver ruteplan må være tilknyttet en ruteveiledning.

## <a name="route-guides"></a>Ruteveiledninger
En ruteveiledning definerer vilkårene for å sammenligne en last med en bestemt ruteplan. Du kan for eksempel angi en opprinnelseshub og en målhub, grenser for containervolum eller -vekt, og en transportør, tjenesten eller gruppe. Ruteveiledninger er tilgjengelige på siden **Arbeidsområde for vurderingsrute**, der lastene kan samsvares med ruter manuelt eller automatisk. Hvis ruteveiledningen er for en planlagt rute, er den også tilgjengelig på siden **Arbeidsområde for lastplanlegging**

## <a name="scheduled-routes"></a>Planlagte ruter
En planlagt rute er en forhåndsdefinert ruteplan som har en tidsplan for leveringdatoene. Planlagte ruter og ikke-planlagte ruter varierer med hensyn til hvordan laster tilordnes. Hvis du tilordner en ikke-planlagt rute ved hjelp av Arbeidsområde for vurderingsrute, valideres bare lasten og ruteveiledningen. Hvis du tilordner en planlagt rute, vurderes også datoer og adresser fra ordrene og hubene, og det tas også hensyn til datoen på ruteplanen. Du trenger ikke å bruke siden Arbeidsområde for vurderingsrute for å tilordne laster manuelt til en planlagt rute. I stedet kan du bruke Arbeidsområde for lastplanlegging til å foreslå at lasten bygges opp på kundeadresser og leveringsdatoer fra ordrer for en bestemt planlagt rute. For planlagte ruter vil ruteplanen har fast opprinnelse og målhuber. Vanligvis er transportør og tjeneste den samme for alle segmenter, men de kan være forskjellige. Målhubene opprettes ved hjelp av postnumre for kundene som besøkes på ruten. Flere rutetidsplaner kan defineres for en ruteplan. Ruteplanen må være tilknyttet en ruteveiledning. For planlagte ruter kan imidlertid planen tilknyttes bare én ruteveiledning. Ruteplanen brukes bare til å opprette de faktiske rutene på siden **Ruteplan**. Du kan bruke standardmalen for last når du foreslår laster på Arbeidsområde for lastplanlegging.

## <a name="load-building-workbench"></a>Arbeidsområde for lastplanlegging
Arbeidsområde for lastplanlegging bruker kundeadresser og leveringsdatoer fra salgsordrer og planlagte ruter som er tilgjengelige, for å foreslå en last. Verdiene fra ruten angis i arbeidsområdet som standard. Du kan imidlertid velge en fra-dato som er eldre enn fra-datoen på ruten. Når en last blir foreslått, sjekkes leveringsadresse og leveringsdato for alle åpne ordrer. Hvis postnummeret for leveringsadressen samsvarer med postnummeret for en hub i ruteplanen, og hvis leveringsdatoen er innenfor området som er valgt i vilkårene, foreslås salgsordren for lasten. Det tas også hensyn til kapasiteten i lastmalen. Bare én last foreslås om gangen. Hvis du har en salgsordre som ikke er inkludert, må du kanskje bruke en annen lastmal (for eksempel en lastmal for en større lastebil eller container) eller planlegge en ekstra levering.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]