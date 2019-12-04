---
title: Hovedplanlegging for områdedekning, lager ikke obligatorisk
description: Dette emnet beskriver hvordan en vare som har et områdedimensjonssett for dekning planlegges.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43989f95764a60dc7f5662ef74c005c5fddaa275
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813737"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Hovedplanlegging for områdedekning, lager ikke obligatorisk

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan en vare som har et områdedimensjonssett for dekning planlegges.

Dette hovedplanleggingsscenariet omfatter følgende betingelser:

-   Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.
-   Lagerdimensjonen er ikke satt til obligatorisk. Lageret kan være kjent, men det brukes ikke i hovedplanleggingsberegningen.
-   Sitedimensjonen er angitt for dekningsplanlegging.
-   Lagerdimensjonen er ikke angitt for dekningsplanlegging. Derfor samles tilbud og etterspørsel etter område, og kanskje også andre dekningsplanlagte dimensjoner.

Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår. Parameterne det refereres til i grafikken, og plasseringene, er følgende:
-   Varedekning er definert for varen. Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen, og klikk deretter **Plan &gt; Varedekning**.
-   Påfyllingsrelasjoner er definert for lageret. Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-fanen kan du se feltgruppen **Hovedlager**.
-   Standard ordretype er satt til Produksjon, Bestilling eller Kanban. Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen, og klikk deretter **Plan &gt; Standard ordreinnstillinger**. I **Standard ordreinnstillinger**-skjemaet kan du se feltet **Standard ordretype**.

![Behov for sitedekning, lager ikke obligatorisk    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a>Tilleggsressurser
--------

[Oversikt over hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)

[Hovedplanlegging for område- og lagerdekning, lager obligatorisk](master-plan-site-coverage-warehouse-mandatory.md)

[Hovedplanlegging for områdedekning, obligatorisk lager](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hovedplanlegging for områdedekning, lager ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Fastslå stykklisteversjonen](master-plan-bom-version-determined.md)



