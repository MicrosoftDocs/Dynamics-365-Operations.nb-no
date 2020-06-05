---
title: Hovedplanlegging for område- og lagerdekning, lager obligatorisk
description: Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er obligatorisk.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a07a4588d042af53d6281afc174ff58ecf24ca06
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383349"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Hovedplanlegging for område- og lagerdekning, lager obligatorisk

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er obligatorisk.

Dette hovedplanleggingsscenarioet omfatter følgende betingelser:

-   Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.
-   Lagerdimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.
-   Site- og lagerdimensjonene er angitt for dekningsplanlegging. Andre dimensjoner kan også være angitt for dekningsplanlegging. De berøres imidlertid ikke av multisite-funksjonaliteten.

Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår. Parameterne det refereres til i grafikken, og plasseringene, er følgende:
-   Lageret er satt til **Manuell**. Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-hurtigkategorien kan du se feltet **Manuelt**.
-   Varedekning er definert for varen. Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen og deretter i Handlingsrute i kategorien **Plan** klikker du **Varedekning**.
-   Påfyllingsrelasjoner er definert for lageret. Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-hurtigkategorien kan du se feltgruppen **Hovedlager**.
-   Standard ordretype er satt til Produksjon, Bestilling eller Kanban. Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen og deretter i Handlingsrute i kategorien **Plan** klikker du **Standard ordreinnstillinger**. I **Standard ordreinnstillinger**-skjemaet kan du se **Standard ordretype**.

![Behov for site- og lagerdekning, lager obligatorisk](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a>Tilleggsressurser
--------

[Oversikt over hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)

[Hovedplanlegging for områdedekning, obligatorisk lager](master-plan-site-coverage-warehouse-mandatory.md)

[Hovedplanlegging for områdedekning, lager ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)

[Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Fastslå stykklisteversjonen](master-plan-bom-version-determined.md)



