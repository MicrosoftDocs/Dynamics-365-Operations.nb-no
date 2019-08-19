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
# <a name="asset-view"></a><span data-ttu-id="6dcbc-103">Aktivavisning</span><span class="sxs-lookup"><span data-stu-id="6dcbc-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6dcbc-104">Dette emnet beskriver aktivavisning i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="6dcbc-105">Siden **Aktivavisning** viser aktive aktiva og arbeidssteder i en trevisning.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="6dcbc-106">Derfor kan du enkelt få en oversikt over aktivarelasjoner til arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="6dcbc-107">I tillegg kan du vise detaljert informasjon om arbeidssteder, aktiva og tilknyttede stykklister.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="6dcbc-108">Du kan også få en rask oversikt over aktive vedlikeholdsanmodninger og arbeidsordrer som er knyttet til et aktivum.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="6dcbc-109">Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Aktivavisning**.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="6dcbc-110">Hvis du vil endre visningen som vises på siden, velger du en ny verdi i **Visning**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6dcbc-111">Standardvisningen som vises når du åpner siden **Aktivavisning**, avhenger av verdien som er valgt i **Visning**-feltet i kategorien **Aktiva** på siden **Parametere i Aktivastyring** (**Aktivastyring** \> **Oppsett** \> **Parametere i Aktivastyring**).</span><span class="sxs-lookup"><span data-stu-id="6dcbc-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="6dcbc-112">Hurtigfanen på høyre side av siden viser detaljer om den valgte visningen.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="6dcbc-113">Brødsmulesporet som vises over trevisningen, viser det gjeldende merkede området i trevisningen.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="6dcbc-114">Dette brødsmulesporet bruker følgende format:</span><span class="sxs-lookup"><span data-stu-id="6dcbc-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="6dcbc-115">ID for arbeidssted / ID for arbeidssted (hvis det er flere arbeidssteder) \> Aktiva-ID / Aktiva-ID (hvis det er flere aktiva) – Varenummer.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="6dcbc-116">Hvis du har valgt et aktivum i trevisningen, kan du velge **Aktive forespørsler** eller **Aktive arbeidsordrer** for å vise vedlikeholdsanmodningene eller arbeidsordrene som er relatert til aktivumet.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="6dcbc-117">Du kan også velge **Åpne** \> **Arbeidssted**, **Aktiva** eller **Stykkliste for aktiva** for å åpne den tilknyttede visningen.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="6dcbc-118">Alternativet **Arbeidssteder for aktiva** som du kan velge i **Visning**-feltet, er også tilgjengelig i alle aktivaoppslag der du kan velge et aktivum.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="6dcbc-119">Trevisningen vises i kategorien **Aktivavisning**, der du for eksempel [oppretter et aktivum](../objects/create-an-object.md), oppretter en vedlikeholdsanmodning eller oppretter en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
