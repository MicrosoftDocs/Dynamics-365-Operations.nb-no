---
title: Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk
description: Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er ikke obligatorisk.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6d163a0a9fc98442f8717972445a1de6d35ca1c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573735"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er ikke obligatorisk.

Dette hovedplanleggingsscenarioet omfatter følgende betingelser:

-   Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen. Denne innstillingen kan ikke endres.
-   Lagerdimensjonen er ikke satt til obligatorisk. Lageret kan være kjent, men det brukes ikke i hovedplanleggingsberegningen.
-   Site- og lagerdimensjonene er angitt for dekningsplanlegging. Andre dimensjoner kan også være angitt for dekningsplanlegging. De berøres imidlertid ikke av multisite-funksjonaliteten.

Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår. Parameterne det refereres til i grafikken, og plasseringene, er følgende:
-   Lageret er satt til Manuell. Klikk på **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-hurtigfanen kan du se feltet **Manuelt**.
-   Varedekning er definert for varen. Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen og deretter i Handlingsrute i fanen **Plan** klikker du **Varedekning**.
-   Påfyllingsrelasjoner er definert for lageret. Klikk på **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-hurtigfanen kan du se feltgruppen **Hovedlager**.
-   Standard ordretype er satt til Produksjon, Bestilling eller Kanban. Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen og deretter i Handlingsrute i fanen **Plan** klikker du **Standard ordreinnstillinger**. I **Standard ordreinnstillinger**-skjemaet kan du se **Standard ordretype**.

![Behov for site og lager, ikke lager.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)

[Hovedplanlegging for områdedekning, obligatorisk lager](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hovedplanlegging for område- og lagerdekning, lager obligatorisk](master-plan-site-coverage-warehouse-mandatory.md)

[Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)

[Fastslå stykklisteversjonen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]