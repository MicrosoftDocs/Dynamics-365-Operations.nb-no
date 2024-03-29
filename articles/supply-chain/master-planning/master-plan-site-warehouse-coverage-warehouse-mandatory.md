---
title: Hovedplanlegging for område- og lagerdekning, lager obligatorisk
description: Denne artikkelen beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er obligatorisk.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcb2d41ff70714b6bc9c28f3e23ce95f5292f2e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740066"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Hovedplanlegging for område- og lagerdekning, lager obligatorisk

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er obligatorisk.

Dette hovedplanleggingsscenarioet omfatter følgende betingelser:

-   Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.
-   Lagerdimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.
-   Site- og lagerdimensjonene er angitt for dekningsplanlegging. Andre dimensjoner kan også være angitt for dekningsplanlegging. De berøres imidlertid ikke av multisite-funksjonaliteten.

Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår. Parameterne det refereres til i grafikken, og plasseringene, er følgende:
-   Lageret er satt til **Manuell**. Klikk på **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-hurtigfanen kan du se feltet **Manuelt**.
-   Varedekning er definert for varen. Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen og deretter i Handlingsrute i fanen **Plan** klikker du **Varedekning**.
-   Påfyllingsrelasjoner er definert for lageret. Klikk på **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-hurtigfanen kan du se feltgruppen **Hovedlager**.
-   Standard ordretype er satt til Produksjon, Bestilling eller Kanban. Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen og deretter i Handlingsrute i fanen **Plan** klikker du **Standard ordreinnstillinger**. I **Standard ordreinnstillinger**-skjemaet kan du se **Standard ordretype**.

![Behov for site- og lagerdekning, lager obligatorisk.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)
- [Hovedplanlegging for områdedekning, obligatorisk lager](master-plan-site-coverage-warehouse-mandatory.md)
- [Hovedplanlegging for områdedekning, lager ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)
- [Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Fastslå stykklisteversjonen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]