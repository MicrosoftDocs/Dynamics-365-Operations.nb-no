---
title: Hovedplanlegging for område- og lagerdekning, lager obligatorisk
description: Denne artikkelen beskriver hvordan en vare som har en dekningsdimensjon planlegges. Lager er en obligatorisk dimensjon.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6e9cb9362fcafab5738e0a1887366e5fd1efbab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863976"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Hovedplanlegging for område- og lagerdekning, lager obligatorisk

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan en vare som har en dekningsdimensjon planlegges. Lager er en obligatorisk dimensjon.

Dette hovedplanleggingsscenariet omfatter følgende betingelser:

-   Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen. Denne innstillingen kan ikke endres.
-   Lagerdimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.
-   Sitedimensjonen er angitt for dekningsplanlegging. Andre dimensjoner kan også være angitt for dekningsplanlegging. De berøres imidlertid ikke av multisite-funksjonaliteten.
-   Lagerdimensjonen er ikke angitt for dekningsplanlegging. Derfor samles tilbud og etterspørsel etter område, og kanskje også andre dekningsplanlagte dimensjoner.

Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår. Parameterne det refereres til i grafikken, og plasseringene, er følgende:
-   Varedekning er definert for varen. Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen, og klikk deretter **Plan &gt; Varedekning**.
-   Påfyllingsrelasjoner er definert for lageret. Klikk på **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**. På **Hovedplanlegging**-fanen kan du se feltgruppen **Hovedlager**.
-   Standard ordretype er satt til Produksjon, Bestilling eller Kanban. Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg varen, og klikk deretter **Plan &gt; Standard ordreinnstillinger**. I **Standard ordreinnstillinger**-skjemaet kan du se **Standard ordretype**.

![Behov for sitedekning, lager obligatorisk.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)

[Hovedplanlegging for område- og lagerdekning, lager obligatorisk](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hovedplanlegging for områdedekning, obligatorisk lager](master-plan-site-coverage-warehouse-mandatory.md)

[Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Fastslå stykklisteversjonen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]