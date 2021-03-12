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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e012850a390f373088e758418b68c7eaae7ad53e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973991"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Definere gebyrer for hubtilbehør og tilbehørsmaler

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør. Fremgangsmåten bruker USMF-datasettet. Dette oppsettet utføres vanligvis av en transportkoordinator.


## <a name="set-up-a-hub-master"></a>Definere en hubmal
1. Gå til Transportstyring > Oppsett > Vurdering > Tilbehørsmaler.
2. Klikk på Ny.
3. Angi en verdi i Tilbehørsmal-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Velg Hub i Tilbehørstype-feltet.
6. Klikk på Lagre.
7. Lukk siden.

## <a name="set-up-a-hub-accessorial-charge"></a>Definer et gebyr for hubtilbehør
1. Gå til Transportstyring > Oppsett > Vurdering > Gebyrer for hubtilbehøret.
2. Klikk på Ny.
3. Skriv inn en verdi i feltet ID for hubtilbehør.
4. Klikk på rullegardinknappen i Hub-feltet for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
6. Velg et alternativ i feltet Hubposisjon.
    * Du kan opprette tillegget som en henting eller levering. Avhengig av valget gjelder tillegget for det tilsvarende transportsegmentet i din rute.  
7. Klikk på rullegardinknappen i feltet Tilbehørsmal for å åpne oppslaget.
8. Klikk på koblingen i den valgte raden i listen.
    * Velg malen du nettopp opprettet.  
9. Klikk på Lagre.
10. Lukk siden.

