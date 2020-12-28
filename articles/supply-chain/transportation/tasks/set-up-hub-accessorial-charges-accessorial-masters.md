---
title: Definere gebyrer for hubtilbehør og tilbehørsmaler
description: Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad89afe0a21261c57311c439153b969d837748e4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434869"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Definere gebyrer for hubtilbehør og tilbehørsmaler

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør. Fremgangsmåten bruker USMF-datasettet. Dette oppsettet utføres vanligvis av en transportkoordinator.


## <a name="set-up-a-hub-master"></a>Definere en hubmal
1. Gå til Transportstyring > Oppsett > Vurdering > Tilbehørsmaler.
2. Klikk Ny.
3. Angi en verdi i Tilbehørsmal-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Velg Hub i Tilbehørstype-feltet.
6. Klikk Lagre.
7. Lukk siden.

## <a name="set-up-a-hub-accessorial-charge"></a>Definer et gebyr for hubtilbehør
1. Gå til Transportstyring > Oppsett > Vurdering > Gebyrer for hubtilbehøret.
2. Klikk Ny.
3. Skriv inn en verdi i feltet ID for hubtilbehør.
4. Klikk rullegardinknappen i Hub-feltet for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
6. Velg et alternativ i feltet Hubposisjon.
    * Du kan opprette tillegget som en henting eller levering. Avhengig av valget gjelder tillegget for det tilsvarende transportsegmentet i din rute.  
7. Klikk rullegardinknappen i feltet Tilbehørsmal for å åpne oppslaget.
8. Klikk koblingen i den valgte raden i listen.
    * Velg malen du nettopp opprettet.  
9. Klikk Lagre.
10. Lukk siden.

