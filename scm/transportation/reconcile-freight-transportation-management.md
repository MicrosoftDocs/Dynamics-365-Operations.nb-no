---
title: Avstemme frakt i transportstyring
description: Denne artikkelen beskriver fraktavstemmingsprosessen.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ab7d21d7a75e2c954831a254bb339d9cf5746d9d
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Avstemme frakt i transportstyring
<a id="reconcile-freight-in-transportation-management" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver fraktavstemmingsprosessen.

Fraktavstemming kan gjøres manuelt, eller det kan settes opp til å skje automatisk. Hvis du vil bruke automatisk fraktavstemming, må du opprette en revisjonsstandard der du kan definere kriteriene som bestemmer hvilke fraktbrev som sammenlignes automatisk.

## Fraktavstemmingsprosessen
<a id="the-freight-reconciliation-process" class="xliff"></a>
Fraktsatser beregnes av satsmotoren som er tilknyttet med den aktuelle transportøren. Når en last er bekreftet, genereres et fraktbrev og fraktsatser overføres til den. Fraktsatsene fordeles som tillegg til det aktuelle kildedokumentet (bestilling, salgsordre, og/eller overføringsordre), avhengig av oppsettet som brukes for den vanlige faktureringsprosessen. Fraktavstemmingsprosessen (som også kalles kontrollprosessen) kan starte så snart fraktfakturaen mottas fra transportøren. Fakturaen kan mottas elektronisk eller på papir. Hvis fakturaen mottas på papir, kan du generere en elektronisk faktura ved hjelp av fraktbrevet som mal. 

[![Fraktavstemmingsprosessen](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## Manuell avstemming
<a id="manual-reconciliation" class="xliff"></a>
Hvis du er avstemmer frakt manuelt, må du sammenligne hver fakturalinje med fraktbrevlinjen eller -linjene for lasten som skal faktureres. Du gjør dette på siden **Samsvare fraktbrev og faktura**. Hvis beløpet på fakturalinjen ikke samsvarer med hvor fraktbrevbeløpet, må du velge en avstemmingsårsak for forskjellen. Hvis det er flere årsaker til avstemming, kan du dele de ikke-samsvarte beløpene på tvers av dem. Årsaken til avstemming bestemmer hvordan differansebeløpene posteres i Finans. Når avstemmingen av hele fakturabeløpet er gjort rede for, sendes sendt til godkjenning, og deretter posteres journalen. Illustrasjonen nedenfor viser hvordan du genererer en fraktfaktura og utfører fraktavstemming i Microsoft Dynamics 365 for Finance and Operations. 
[![Fraktavstemmingsoppgaver i Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## Automatisk avstemming
<a id="automatic-reconciliation" class="xliff"></a>
Hvis du vil bruke automatisk avstemming, må du angi tidsplanen for avstemming og fakturaene og transportørene som skal brukes. Treff for fakturalinjer og fraktbrev gjøres i henhold til oppsettet av typen revisjonsstandard og fraktbrev. Når du har kjørt automatisk avstemming, må du håndtere alle fakturaer som systemet ikke kan samsvare. Du må behandle disse fakturaene manuelt før du kan bokføre alle fakturaene for betaling.




