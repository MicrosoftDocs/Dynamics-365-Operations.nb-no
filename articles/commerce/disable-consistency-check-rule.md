---
title: Deaktiver regler som brukes i transaksjonsvalideringsprosessen
description: Denne artikkelen beskriver funksjonaliteten for deaktivering av transaksjonsvalideringsregler i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884883"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Deaktiver regler som brukes i transaksjonsvalideringsprosessen

[!include [banner](../includes/banner.md)]

Forhandlere kan ha forretningsscenarioer og -prosesser som er unike for dem. Derfor gjelder ikke alle reglene som er inkludert i transaksjonsvalideringsprosessen, for alle forhandlere. Hvis du vil ha plass til forskjeller, tilbyr Microsoft Dynamics 365 Commerce funksjonalitet som kan brukes til å deaktivere reglene som ikke gjelder.

Hvis du vil vise en liste over regler som er tilgjengelige i transaksjonsvalideringsprosessen i miljøet ditt, og vise statusen for hver regel, kan du gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Handelsparametere** og velge fanen **Transaksjonsvalidering**. Alle aktiverte regler brukes til å validere transaksjoner under prosessen **Valider butikktransaksjoner** og må bestås for at transaksjoner skal samles inn og posteres på et transaksjonskontoutdrag.

Som standard er statusen for alle regler satt til **Aktivert**. Derfor brukes alle reglene til å validere transaksjoner før de kan hentes inn i handelstransaksjonsutdragene. Hvis du vil deaktivere en regel, endrer du statusen til **Deaktivert**. Deaktiverte regler tas ikke med når transaksjoner valideres under prosessen **Valider butikktransaksjoner**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
