---
title: Aktivavisning
description: Dette emnet beskriver aktivavisning i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63e5ec5b2a47706763df8105932d722986535a9b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783487"
---
# <a name="asset-view"></a>Aktivavisning

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emnet beskriver aktivavisning i Aktivastyring. Siden **Aktivavisning** viser aktive aktiva og arbeidssteder i en trevisning. Derfor kan du enkelt få en oversikt over aktivarelasjoner til arbeidssteder. I tillegg kan du vise detaljert informasjon om arbeidssteder, aktiva og tilknyttede stykklister. Du kan også få en rask oversikt over aktive vedlikeholdsanmodninger og arbeidsordrer som er knyttet til et aktivum.

1. Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Aktivavisning**.
2. Hvis du vil endre visningen som vises på siden, velger du en ny verdi i **Visning**-feltet.

    > [!NOTE]
    > Standardvisningen som vises når du åpner siden **Aktivavisning**, avhenger av verdien som er valgt i **Visning**-feltet i kategorien **Aktiva** på siden **Parametere i Aktivastyring** (**Aktivastyring** \> **Oppsett** \> **Parametere i Aktivastyring**).

Hurtigfanen på høyre side av siden viser detaljer om den valgte visningen.

Brødsmulesporet som vises over trevisningen, viser det gjeldende merkede området i trevisningen. Dette brødsmulesporet bruker følgende format:

ID for arbeidssted / ID for arbeidssted (hvis det er flere arbeidssteder) \> Aktiva-ID / Aktiva-ID (hvis det er flere aktiva) – Varenummer.

Hvis du har valgt et aktivum i trevisningen, kan du velge **Aktive forespørsler** eller **Aktive arbeidsordrer** for å vise vedlikeholdsanmodningene eller arbeidsordrene som er relatert til aktivumet. Du kan også velge **Åpne** \> **Arbeidssted**, **Aktiva** eller **Stykkliste for aktiva** for å åpne den tilknyttede visningen.

Alternativet **Arbeidssteder for aktiva** som du kan velge i **Visning**-feltet, er også tilgjengelig i alle aktivaoppslag der du kan velge et aktivum. Trevisningen vises i kategorien **Aktivavisning**, der du for eksempel [oppretter et aktivum](../objects/create-an-object.md), oppretter en vedlikeholdsanmodning eller oppretter en arbeidsordre.
