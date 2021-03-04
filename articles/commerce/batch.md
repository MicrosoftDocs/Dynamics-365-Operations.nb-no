---
title: Forbedret håndtering av varer med partisporing
description: Dette emnet beskriver forbedringene som er gjort i håndteringen av partier for varer med partisporing under posteringsprosessen for utdrag.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: ef946df30c68373b83660fce98b472dc94b42719
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989599"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Forbedret håndtering av varer med partisporing


[!include [banner](includes/banner.md)]


På salgsstedet kan ikke partinumre registreres for varer med partisporing på salgstidspunktet. For bestemte konfigurasjoner imidlertid, når salg posteres på hovedkontoret via kundeordrer eller utdragspostering, forventer Microsoft Dynamics-systemet at det finnes gyldige partinumre for varer med partisporing, og at de skal brukes under faktureringen.

Hvis det finnes gyldige partinumre for produktene, brukes de i kundeordrefaktureringen og salgsordrefaktureringen fra utdragspostering. Ellers kan ikke kundeordrefaktureringen postere, og salgsstedsbrukeren får en feilmelding. Utdragspostering går deretter inn i en feiltilstand. Denne feiltilstanden forekommer selv om negativ beholdning er aktivert for produktene.

Når negativ beholdning er aktivert for varer med partisporing, sikrer forbedringene som er gjort i Retail versjon 10.0.4 og senere, at kundeordrefakturering og salgsordrefakturering via utdragspostering ikke blokkeres for disse varene hvis beholdningen er 0 (null) eller det ikke finnes et partinummer. Den nye funksjonaliteten bruker en standard parti-ID for salgslinjene når partinumre ikke er tilgjengelige.

Hvis du vil definere standard parti-ID som brukes for kundeordrer, angir du feltet **Standard parti-ID** i hurtigfanen **Ordre** i fanen **Kundeordrer** på siden **Handelsparametere**.

Hvis du vil definere standard parti-ID som brukes for salgsordrefakturering via utdragspostering, angir du feltet **Standard parti-ID** i hurtigfanen **Lageroppdatering** i fanen **Postering** på siden **Handelsparametere**.

> [!NOTE]
> Denne funksjonaliteten er bare tilgjengelig når avanserte lageraktiviteter er aktivert for det spesifikke butikklageret og varene. I en senere versjon vil funksjonaliteten også støttes for scenarioer der avansert lagerstyring ikke brukes.

> [!NOTE]
> Støtte for forbedret håndtering av satsvise varer under utdragspostering for ikke-avanserte lagerstyringsscenarier ble innført i Retail versjon 10.0.5.


[!INCLUDE[footer-include](../includes/footer-banner.md)]