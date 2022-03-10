---
title: Deaktiver regler som brukes i transaksjonsvalideringsprosessen
description: Dette emnet beskriver funksjonaliteten for deaktivering av transaksjonsvalideringsregler i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919533"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Deaktiver regler som brukes i transaksjonsvalideringsprosessen

[!include [banner](../includes/banner.md)]

Forhandlere kan ha forretningsscenarioer og -prosesser som er unike for dem. Derfor gjelder ikke alle reglene som er inkludert i transaksjonsvalideringsprosessen, for alle forhandlere. Hvis du vil ha plass til forskjeller, tilbyr Microsoft Dynamics 365 Commerce funksjonalitet som kan brukes til å deaktivere reglene som ikke gjelder.

Hvis du vil vise en liste over regler som er tilgjengelige i transaksjonsvalideringsprosessen i miljøet ditt, og vise statusen for hver regel, kan du gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Handelsparametere** og velge fanen **Transaksjonsvalidering**. Alle aktiverte regler brukes til å validere transaksjoner under prosessen **Valider butikktransaksjoner** og må bestås for at transaksjoner skal samles inn og posteres på et transaksjonskontoutdrag.

Som standard er statusen for alle regler satt til **Aktivert**. Derfor brukes alle reglene til å validere transaksjoner før de kan hentes inn i handelstransaksjonsutdragene. Hvis du vil deaktivere en regel, endrer du statusen til **Deaktivert**. Deaktiverte regler tas ikke med når transaksjoner valideres under prosessen **Valider butikktransaksjoner**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
