---
title: Synkronisere med prismotoren for Supply Chain Management ved behov
description: Dette emnet beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Supply Chain Management fra Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c9f94ec35ebed5a14252377fb543de09cb994ffd
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416186"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Synkronisere med prismotoren for Supply Chain Management ved behov

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management inkluderer en prissettingsmotor som håndterer forretningsavtaler, prislister, fordelsprogrammer, kampanjer og rabatter. Prissettingsmotoren bruker komplekse regler til å bestemme den beste prisen for et gitt tilbud eller ordre. Når du bruker dobbel skriving, bruker du enten statisk prissetting eller prissettingsmotoren fra Dynamics 365 Supply Chain Management på tilbuds- og ordresider i Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Bruk prissettingsmotoren fra Supply Chain Management i Sales

1. I Sales går du til **Salg \> Ordrer**.
2. Velg **Ny** for å opprette en ny ordre, eller velg en eksisterende ordre i **Mine ordrer**-listen.
3. Legg til en ny ordrelinje.
4. Hvis du oppretter en ny ordre, velger du **Prisordre** i handlingsruten. Hvis du oppdaterer en eksisterende ordre, velger du **Beregn på nytt** i handlingsruten.

    Følgende kolonner fylles ut automatisk:

    + Detaljbeløp
    + Rabatt-%
    + Rabatt
    + Beløp før frakt
    + Fraktbeløp
    + Total avgift
    + Totalbeløp
    
5. For å sikre at systemet vurderer handels- og salgsavtaler for å beregne prisen:
    1. Gå til Supply Chain Management-miljøet.
    2. Gå til **Kunder \> Oppsett \> Kundeparametere**.
    3. Velg fanen **Priser** i sidenavigasjonsfeltet.
    4. Fjern merket for **Manuell registrering** under hurtigfanen **Evaluering av handelssavtale**.

## <a name="how-it-works"></a>Hvordan det fungerer

Når du velger **Prisordre** i Sales, kalles **Summer**-funksjonen i fanen **Salgsordre \> Vis** i Supply Chain Management for den tilknyttede salgsordren. Verdiene i ordretotalen i Sales brukes til å fylle ut de tilsvarende kolonnene i Supply Chain Management.

Når salgsordretotalen beregnes i Supply Chain Management, evaluerer beregningen de eksisterende forretningsavtalene og salgsavtalene for kunden og produktene som er oppført i salgsordren. Denne informasjonen brukes til å beregne totalene. Når **Prisordre** er valgt, gjenspeiler Sale automatisk alle oppsett som er utført i Supply Chain Management.

## <a name="limitations"></a>Begrensninger

Når kolonnene i Sales fylles ut, gjelder følgende begrensninger:

+ Oppsettet av gebyrer og gebyrfordelinger i Supply Chain Management replikeres ikke i Sales.
+ Prissetting tar ikke hensyn til spesielle detaljhandelpriser som er angitt i **Detaljhandelskanal**-kolonnen på salgsordrelinje-siden i Supply Chain Management.
+ Rabatter som er definert i delen **Handelsrabattbehandling** i Supply Chain Management, vurderes ikke.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]