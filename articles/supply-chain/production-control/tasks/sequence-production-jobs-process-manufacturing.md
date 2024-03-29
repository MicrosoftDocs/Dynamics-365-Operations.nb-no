---
title: Sekvensiere produksjonsjobber for prosessproduksjon
description: Denne fremgangsmåten bruker malingsprodukter som eksempel for å vise hvordan du sorterer planlagte ordrer i henhold til prioriteten for farge og pakkestørrelse.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e54cfa60fa9efd511aef8c074484b9b1a738e8cb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572751"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Sekvensiere produksjonsjobber for prosessproduksjon

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten bruker malingsprodukter som eksempel for å vise hvordan du sorterer planlagte ordrer i henhold til prioriteten for farge og pakkestørrelse. Demonstrasjonsdatafirmaet USPI brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for produksjonsplanleggeren.


## <a name="run-master-planning-for-uspi"></a>Kjøre hovedplanlegging for USPI
1. Gå til Hovedplanlegging > Hovedplanlegging > Kjør > Hovedplanlegging.
2. Klikk på rullegardinknappen i feltet Hovedplan for å åpne oppslaget.
3. Klikk på koblingen i den valgte raden i listen.
    * Velg MasterPlan.  
4. Klikk på OK.
    * Dette starter hovedplanlegging, inkludert sekvensprosessen. Denne prosessen kan ta noen minutter.  

## <a name="view-planned-orders-for-the-paint-products"></a>Vise planlagte bestillinger for malingsprodukter
1. Gå til Hovedplanlegging > Hovedplanlegging > Planlagte bestillinger.
2. Vis faktaboks for varedetaljer.
3. Vis faktaboks for Tidsplandetaljer.
4. Klikk på rullegardinknappen i Plan-feltet for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
    * Velg MasterPlan.  
6. Klikk på koblingen i den valgte raden i listen.
7. Bruk hurtigfilteret til å filtrere på feltet Varenummer med verdien P300.
    * Lås opp for å gå til høyre for å vise ordredato og leveringsdato. Legg merke til at disse varene har ordredatoen I dag, og leveringsdatoene for de planlagte ordrene er ikke i rekkefølge etter prioritet for farge og pakkestørrelse, som vist i produktnavnet. Du kan holder musepekeren over et varenummer for å se varenavn og prioritet.  

## <a name="sequence-planned-orders-for-paint"></a>Sekvens for planlagte ordre for maling
1. Lukk siden.
2. Gå til Hovedplanlegging > Hovedplanlegging > Sekvenserte planlagte ordrer.
3. Vis faktaboks for varedetaljer.
4. Vis faktaboks for Tidsplandetaljer.
    * Obs!  Her ser du at startdato/-klokkeslett for de planlagte ordrene er i rekkefølge i henhold til farge og pakkestørrelse i en tidsperiode på 28 dager. Disse periodene er definert av et tall i feltet Kampanje. Skjemaet Sekvensert planlagt ordre fungerer som det vanlige planlagte bestillingsskjemaet, og produksjonsplanleggeren kan bekrefte planlagte ordre her.  
5. Merk alle rader.
6. Klikk på Godta.
    * Dette vil oppdatere de planlagte ordrene med den valgte sekvenshandlingen Utsett eller Forskudd.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Kontroller rekkefølgen for de planlagte ordrene
1. Lukk siden.
2. Gå til Hovedplanlegging > Hovedplanlegging > Planlagte bestillinger.
3. Vis faktaboks for varedetaljer.
4. Vis faktaboks for Tidsplandetaljer.
5. Klikk på rullegardinknappen i Plan-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
    * Velg MasterPlan.  
7. Klikk på koblingen i den valgte raden i listen.
8. Bruk hurtigfilteret til å filtrere på feltet Varenummer med verdien P300.
    * Legg merke til at ordrene nå er i rekkefølge i henhold til prioriteten for farge og størrelse, og de planlagte ordrene starter på den tidligste ordredatoen og leveringsdatoen. Valider Ordredato-kolonnen eller Startdato i faktaboksen Tidsplandetaljer.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]