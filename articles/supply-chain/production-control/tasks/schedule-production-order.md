---
title: Planlegge en produksjonsordre
description: Denne prosedyren viser hvordan du planlegger en produksjonsordre.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93ec5bd6984dd1a8f970834070fd77873078b3b0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237137"
---
# <a name="schedule-a-production-order"></a>Planlegge en produksjonsordre

[!include [banner](../../includes/banner.md)]

Denne prosedyren viser hvordan du planlegger en produksjonsordre. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den tredje prosedyren av sju som forklarer livssyklusen for produksjonsordren.


## <a name="schedule-a-production-order"></a>Planlegge en produksjonsordre
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
    * Velg en produksjonsordre med statusen Estimert.  
2. Klikk på Planlegg i handlingsruten.
3. Klikk på Planlegg jobber.
    * Parameterne for planlegging er definert på denne siden. Du kan definere parameterne for bestemte brukere eller alle brukere.  
4. Velg Fremover fra i dag i Planleggingsretning-feltet.
5. Angi en dato i Planleggingsdato-feltet.
6. Merk av for eller fjern merket for Begrenset kapasitet.
7. Merk av for eller fjern merket for Begrenset materiale.
8. Klikk på OK.

## <a name="view-the-scheduling-results"></a>Vise planleggingsresultatene
1. Klikk på Produksjonsordre i handlingsruten.
2. Klikk på Alle jobber.
    * Denne siden viser planlagte jobber som du nettopp har generert.  
3. Vis eller skjul Planlegging-delen.
    * Du kan vise planlagt dato og klokkeslett på hurtigfanen Planlegging.  
4. Klikk på Forespørsler.
5. Klikk på Kapasitetsbelastning.
    * Kapasitetsbelastning-siden viser kapasiteten som er reservert gjennom finplanlegging, totalt antall timer som er reservert for ressursen nå, og gjenværende antall timer som er tilgjengelig for finplanlegging av ressursen.  
6. Lukk siden.
7. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]