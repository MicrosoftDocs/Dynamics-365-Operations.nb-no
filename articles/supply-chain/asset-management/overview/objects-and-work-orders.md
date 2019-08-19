---
title: Aktiva og arbeidsordrer
description: Dette emnet beskriver aktiva og arbeidsordrer i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783484"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="80d56-103">Aktiva og arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="80d56-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="80d56-104">Dette emnet beskriver aktiva og arbeidsordrer i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="80d56-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="80d56-105">Aktiva og arbeidsordrer er de sentrale delene av Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="80d56-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="80d56-106">Et *aktivum* er en maskin eller maskindel som krever kontinuerlig vedlikehold og service.</span><span class="sxs-lookup"><span data-stu-id="80d56-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="80d56-107">Aktiva kan opprettes i en hierarkisk struktur, og de kan være relatert til arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="80d56-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="80d56-108">Vedlikeholdsjobber kan planlegges på alle nivåer i aktivastrukturen.</span><span class="sxs-lookup"><span data-stu-id="80d56-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="80d56-109">Forskjellige data, for eksempel produktinformasjon og spesifikasjon av aktiva, og nødvendige vedlikeholdsplaner er definert for hvert aktivum.</span><span class="sxs-lookup"><span data-stu-id="80d56-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="80d56-110">Illustrasjonen nedenfor viser en oversikt over aktivadata og tilknytningen av aktiva til jobbtyper.</span><span class="sxs-lookup"><span data-stu-id="80d56-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="80d56-111">Rød tekst brukes til eksempler som viser arv og avhengigheter.</span><span class="sxs-lookup"><span data-stu-id="80d56-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Figur 1](media/05-overview-image.png)

<span data-ttu-id="80d56-113">Hver arbeidsordre har en arbeidsordretype, for eksempel forebyggende vedlikehold, korrigerende vedlikehold eller inspeksjon.</span><span class="sxs-lookup"><span data-stu-id="80d56-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="80d56-114">Arbeidsordren inneholder én eller flere arbeidsordrejobber.</span><span class="sxs-lookup"><span data-stu-id="80d56-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="80d56-115">Hver arbeidsordrejobb definerer en jobb som må utføres på et aktivum og en relatert jobbtype.</span><span class="sxs-lookup"><span data-stu-id="80d56-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="80d56-116">Eksempler på relaterte jobbtyper omfatter 10 000 km, 50 000 km, 1-års service og sikkerhetsinspeksjon.</span><span class="sxs-lookup"><span data-stu-id="80d56-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="80d56-117">Én arbeidsordre kan knyttes til flere aktiva.</span><span class="sxs-lookup"><span data-stu-id="80d56-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="80d56-118">Følgende illustrasjon viser en oversikt over nøkkeldataene i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="80d56-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Figur 2](media/06-overview-image.png)

<span data-ttu-id="80d56-120">En arbeidsordre kan knyttes til en annen arbeidsordre, og jobbtyper kan inneholde etterfølgende jobber som oppretter en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="80d56-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="80d56-121">Generelt er det ingen avhengigheter mellom arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="80d56-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="80d56-122">De kan derfor endre livsløpstilstanden for arbeidsordrer og kan planlegges uavhengig av hverandre.</span><span class="sxs-lookup"><span data-stu-id="80d56-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="80d56-123">Arbeidsordrer kan opprettes på forskjellige måter som er relatert til korrigerende, forebyggende eller reaktivt vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="80d56-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="80d56-124">Du kan også opprette arbeidsordrer manuelt.</span><span class="sxs-lookup"><span data-stu-id="80d56-124">You can also create work orders manually.</span></span> <span data-ttu-id="80d56-125">Illustrasjonen nedenfor viser en oversikt over prosessen for automatisk eller manuell oppretting av arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="80d56-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Figur 3](media/07-overview-image.png)

<span data-ttu-id="80d56-127">Du må fylle ut flere trinn når du vil planlegge og kjøre en vedlikeholdsjobb på en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="80d56-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="80d56-128">Følgende illustrasjon viser en oversikt over behandlingen for en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="80d56-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Figur 4](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="80d56-130">Generelt, når du arbeider i Microsoft Dynamics 365 for Finance and Operations og **Aktivastyring**-modulen, velger du **Ny** for å opprette en ny post, du velger **Rediger** for å oppdatere en eksisterende post, og du velger **Lagre** for å lagre nye eller redigerte data.</span><span class="sxs-lookup"><span data-stu-id="80d56-130">In general, when you work in Microsoft Dynamics 365 for Finance and Operations and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
