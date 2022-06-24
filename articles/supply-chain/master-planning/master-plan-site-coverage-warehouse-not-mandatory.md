---
title: Hovedplanlegging for områdedekning, lager ikke obligatorisk
description: Denne artikkelen beskriver hvordan en vare som har et områdedimensjonssett for dekning planlegges.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 327bb259cc108f1fad068c847441229dcaee7ff1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859234"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Hovedplanlegging for områdedekning, lager ikke obligatorisk

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan en vare som har et områdedimensjonssett for dekning planlegges.

Dette hovedplanleggingsscenariet omfatter følgende betingelser:

-   Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.
-   Lagerdimensjonen er ikke satt til obligatorisk. Lageret kan være kjent, men det brukes ikke i hovedplanleggingsberegningen.
-   Sitedimensjonen er angitt for dekningsplanlegging.
-   Lagerdimensjonen er ikke angitt for dekningsplanlegging. Derfor samles tilbud og etterspørsel etter område, og kanskje også andre dekningsplanlagte dimensjoner.

Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår. Parameterne det refereres til i grafikken, og plasseringene, er følgende:
-   Varedekning er definert for varen. Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen, og klikk deretter **Plan &gt; Varedekning**.
-   Påfyllingsrelasjoner er definert for lageret. Klikk på **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-fanen kan du se feltgruppen **Hovedlager**.
-   Standard ordretype er satt til Produksjon, Bestilling eller Kanban. Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen, og klikk deretter **Plan &gt; Standard ordreinnstillinger**. I **Standard ordreinnstillinger**-skjemaet kan du se feltet **Standard ordretype**.

![Behov for sitedekning, lager ikke obligatorisk.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)

[Hovedplanlegging for område- og lagerdekning, lager obligatorisk](master-plan-site-coverage-warehouse-mandatory.md)

[Hovedplanlegging for områdedekning, obligatorisk lager](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hovedplanlegging for områdedekning, lager ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Fastslå stykklisteversjonen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]