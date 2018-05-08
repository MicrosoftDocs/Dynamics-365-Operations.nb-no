--- 
title: Sekvensiere produksjonsjobber for prosessproduksjon
description: "Denne fremgangsmåten bruker malingsprodukter som eksempel for å vise hvordan du sorterer planlagte ordrer i henhold til prioriteten for farge og pakkestørrelse."
author: ChristianRytt
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 87e35de4744a0728cd41192b4afc750b575a1324
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Sekvensiere produksjonsjobber for prosessproduksjon

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten bruker malingsprodukter som eksempel for å vise hvordan du sorterer planlagte ordrer i henhold til prioriteten for farge og pakkestørrelse. Demonstrasjonsdatafirmaet USPI brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for produksjonsplanleggeren.


## <a name="run-master-planning-for-uspi"></a>Kjøre hovedplanlegging for USPI
1. Gå til Hovedplanlegging > Hovedplanlegging > Kjør > Hovedplanlegging.
2. Klikk rullegardinknappen i feltet Hovedplan for å åpne oppslaget.
3. Klikk koblingen i den valgte raden i listen.
    * Velg MasterPlan.  
4. Klikk OK.
    * Dette starter hovedplanlegging, inkludert sekvensprosessen. Denne prosessen kan ta noen minutter.  

## <a name="view-planned-orders-for-the-paint-products"></a>Vise planlagte bestillinger for malingsprodukter
1. Gå til Hovedplanlegging > Hovedplanlegging > Planlagte bestillinger.
2. Vis faktaboks for varedetaljer.
3. Vis faktaboks for Tidsplandetaljer.
4. Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
    * Velg MasterPlan.  
6. Klikk koblingen i den valgte raden i listen.
7. Bruk hurtigfilteret til å filtrere på feltet Varenummer med verdien P300.
    * Lås opp for å gå til høyre for å vise ordredato og leveringsdato. Legg merke til at disse varene har ordredatoen I dag, og leveringsdatoene for de planlagte ordrene er ikke i rekkefølge etter prioritet for farge og pakkestørrelse, som vist i produktnavnet. Du kan holder musepekeren over et varenummer for å se varenavn og prioritet.  

## <a name="sequence-planned-orders-for-paint"></a>Sekvens for planlagte ordre for maling
1. Lukk siden.
2. Gå til Hovedplanlegging > Hovedplanlegging > Sekvenserte planlagte ordrer.
3. Vis faktaboks for varedetaljer.
4. Vis faktaboks for Tidsplandetaljer.
    * Obs!  Her ser du at startdato/-klokkeslett for de planlagte ordrene er i rekkefølge i henhold til farge og pakkestørrelse i en tidsperiode på 28 dager. Disse periodene er definert av et tall i feltet Kampanje. Skjemaet Sekvensert planlagt ordre fungerer som det vanlige planlagte bestillingsskjemaet, og produksjonsplanleggeren kan bekrefte planlagte ordre her.  
5. Merk alle rader.
6. Klikk Godta.
    * Dette vil oppdatere de planlagte ordrene med den valgte sekvenshandlingen Utsett eller Forskudd.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Kontroller rekkefølgen for de planlagte ordrene
1. Lukk siden.
2. Gå til Hovedplanlegging > Hovedplanlegging > Planlagte bestillinger.
3. Vis faktaboks for varedetaljer.
4. Vis faktaboks for Tidsplandetaljer.
5. Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
    * Velg MasterPlan.  
7. Klikk koblingen i den valgte raden i listen.
8. Bruk hurtigfilteret til å filtrere på feltet Varenummer med verdien P300.
    * Legg merke til at ordrene nå er i rekkefølge i henhold til prioriteten for farge og størrelse, og de planlagte ordrene starter på den tidligste ordredatoen og leveringsdatoen. Valider Ordredato-kolonnen eller Startdato i faktaboksen Tidsplandetaljer.  


