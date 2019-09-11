---
title: Opprette en lokasjonsprofil
description: Dette emnet forklarer hvordan du oppretter en lokasjonsprofil i Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46aa1001c21ae39c158062444303ca02c0f41a45
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866985"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="db365-103">Opprette en lokasjonsprofil</span><span class="sxs-lookup"><span data-stu-id="db365-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db365-104">Dette emnet forklarer hvordan du oppretter en lokasjonsprofil i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="db365-104">This topic explains how to create a location profile in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="db365-105">Hver lokasjon på lageret må ha en tilknyttet lokasjonsprofil som beskriver egenskapene til lokasjonen, for eksempel om den tillater kombinerte varer.</span><span class="sxs-lookup"><span data-stu-id="db365-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="db365-106">I denne fremgangsmåten skal vi opprette en profil for en lokasjon som ikke krever nummerskiltkontroll.</span><span class="sxs-lookup"><span data-stu-id="db365-106">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="db365-107">Vi skal aktivere kombinerte varer og kombinerte lagerstatuser, og tillate syklustelling.</span><span class="sxs-lookup"><span data-stu-id="db365-107">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="db365-108">Du kan bruke prosedyren i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="db365-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="db365-109">I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Lager > Lokasjonsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="db365-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="db365-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="db365-110">Select **New**.</span></span>
3. <span data-ttu-id="db365-111">Skriv inn en verdi i feltet **Profil-ID for lokasjon**.</span><span class="sxs-lookup"><span data-stu-id="db365-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="db365-112">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="db365-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="db365-113">Angi eller velg en verdi i feltet **Lokasjonsformat**.</span><span class="sxs-lookup"><span data-stu-id="db365-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="db365-114">Angi eller velg en verdi i feltet **Lokasjonstype**.</span><span class="sxs-lookup"><span data-stu-id="db365-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="db365-115">Angi eller velg en verdi i feltet **ID for sonebehandlingsprofil**.</span><span class="sxs-lookup"><span data-stu-id="db365-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="db365-116">Velg **Ja** i feltet **Tillat kombinerte varer**.</span><span class="sxs-lookup"><span data-stu-id="db365-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="db365-117">Velg **Ja** i feltet **Tillat kombinerte lagerstatuser**.</span><span class="sxs-lookup"><span data-stu-id="db365-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="db365-118">Velg **Ja** i feltet **Tillat syklustelling**.</span><span class="sxs-lookup"><span data-stu-id="db365-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="db365-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="db365-119">Select **Save**.</span></span>

