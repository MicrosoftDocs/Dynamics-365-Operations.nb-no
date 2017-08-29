---
title: "Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk"
description: "Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er ikke obligatorisk."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ec5150abd297a7c00ac180db581adb30bef65b3f
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er ikke obligatorisk.

Dette hovedplanleggingsscenariet omfatter følgende betingelser:

-   Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen. Denne innstillingen kan ikke endres.
-   Lagerdimensjonen er ikke satt til obligatorisk. Lageret kan være kjent, men det brukes ikke i hovedplanleggingsberegningen.
-   Site- og lagerdimensjonene er angitt for dekningsplanlegging. Andre dimensjoner kan også være angitt for dekningsplanlegging. De berøres imidlertid ikke av multisite-funksjonaliteten.

Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår. Parameterne det refereres til i grafikken, og plasseringene, er følgende:
-   Lageret er satt til Manuell. Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-hurtigkategorien kan du se feltet **Manuelt**.
-   Varedekning er definert for varen. Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen og deretter i Handlingsrute i kategorien **Plan** klikker du **Varedekning**.
-   Påfyllingsrelasjoner er definert for lageret. Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-hurtigkategorien kan du se feltgruppen **Hovedlager**.
-   Standard ordretype er satt til Produksjon, Bestilling eller Kanban. Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen og deretter i Handlingsrute i kategorien **Plan** klikker du **Standard ordreinnstillinger**. I **Standard ordreinnstillinger**-skjemaet kan du se **Standard ordretype**.

![Behov for site og lager, ikke lager](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>Se også
--------

[Hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)

[Hovedplanlegging – område- og lagerdekning, lager obligatorisk](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hovedplanlegging – område- og lagerdekning, lager obligatorisk](master-plan-site-coverage-warehouse-mandatory.md)

[Hovedplanlegging – område- og lagerdekning, lager ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)

[Hovedplanlegging – hvordan stykklisteversjon fastsettes](master-plan-bom-version-determined.md)




