---
title: Definere gebyrer for hubtilbehør og tilbehørsmaler
description: Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e67992c9e744b6337cf4921e06cc7886dead8021102d263022f67940c3e7669b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720138"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]