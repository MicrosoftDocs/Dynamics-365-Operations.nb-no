---
title: Synkronisere med prissettingsmotoren i Dynamics 365 Supply Chain Management ved forespørsel
description: Dette emnet beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Supply Chain Management fra Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173183"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>Synkronisere med prissettingsmotoren i Dynamics 365 Supply Chain Management ved forespørsel

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management inkluderer en prissettingsmotor som håndterer forretningsavtaler, prislister, fordelsprogrammer, kampanjer og rabatter. Prissettingsmotoren bruker komplekse regler til å bestemme den beste prisen for et gitt tilbud eller ordre. Når du bruker dobbel skriving, bruker du enten statisk prissetting eller prissettingsmotoren fra Dynamics 365 Supply Chain Management på tilbuds- og ordresider i Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Bruk prissettingsmotoren fra Supply Chain Management i Sales

1. I Sales går du til **Salg \> Ordrer**.
2. Velg **Ny** for å opprette en ny ordre, eller velg en eksisterende ordre i **Mine ordrer**-listen.
3. Legg til en ny ordrelinje.
4. Hvis du oppretter en ny ordre, velger du **Prisordre** i handlingsruten. Hvis du oppdaterer en eksisterende ordre, velger du **Beregn på nytt** i handlingsruten.

    Følgende felt fylles ut automatisk:

    + Detaljbeløp
    + Rabatt-%
    + Rabatt
    + Beløp før frakt
    + Fraktbeløp
    + Total avgift
    + Totalbeløp

## <a name="how-it-works"></a>Hvordan det fungerer

Når du velger **Prisordre** i Sales, kalles **Summer**-funksjonen i kategorien **Salgsordre \> Vis** i Supply Chain Management for den tilknyttede salgsordren. Verdiene i ordretotalen i Sales brukes til å fylle ut de tilsvarende feltene i Supply Chain Management.

Når salgsordretotalen beregnes i Supply Chain Management, evaluerer beregningen de eksisterende forretningsavtalene og salgsavtalene for kunden og produktene som er oppført i salgsordren. Denne informasjonen brukes til å beregne totalene. Når **Prisordre** er valgt, gjenspeiler Sale automatisk alle oppsett som er utført i Supply Chain Management.

## <a name="limitations"></a>Begrensninger

Når feltene i Sale er fylt ut, gjelder følgende begrensninger:

+ Oppsettet av gebyrer og gebyrfordelinger i Supply Chain Management replikeres ikke i Sales.
+ Prissetting tar ikke hensyn til spesielle detaljhandelpriser som er angitt i **Detaljhandelskanal**-feltet på salgsordrelinje-siden i Supply Chain Management.
+ Rabatter som er definert i delen **Handelsrabattbehandling** i Supply Chain Management, vurderes ikke.