---
title: Kan ikke opprette et miljø i PowerApps-administrasjonssenteret
description: Dette emnet forklarer hva du gjør hvis administratoren ikke kan opprette et miljø i Microsoft PowerApps-administrasjonssenteret.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305687"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="63f14-103">Kan ikke opprette et miljø i PowerApps-administrasjonssenteret</span><span class="sxs-lookup"><span data-stu-id="63f14-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="63f14-104">**Utstede**</span><span class="sxs-lookup"><span data-stu-id="63f14-104">**Issue**</span></span>

- <span data-ttu-id="63f14-105">Leier-/miljøadministratoren kan ikke opprette et miljø i Microsoft PowerApps-administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="63f14-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="63f14-106">En lisens som gir brukerne rett til å utføre miljøopprettingstrinnet, er ikke tilordnet direkte til brukeren som utfører dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="63f14-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="63f14-107">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="63f14-107">**Solution**</span></span>

<span data-ttu-id="63f14-108">Kontroller at leieradministratoren har tilordnet en gyldig lisens for PowerApps P2 direkte til brukeren som utfører miljøopprettingstrinnet.</span><span class="sxs-lookup"><span data-stu-id="63f14-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="63f14-109">Her er Microsoft Dynamics-serviceplanene som gir denne rettigheten.</span><span class="sxs-lookup"><span data-stu-id="63f14-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="63f14-110">Generell produktlagerenhet (SKU)</span><span class="sxs-lookup"><span data-stu-id="63f14-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="63f14-111">PowerApps P2-serviceplan</span><span class="sxs-lookup"><span data-stu-id="63f14-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="63f14-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="63f14-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="63f14-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="63f14-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="63f14-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="63f14-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="63f14-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="63f14-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="63f14-116">Legg merke til at ulike Microsoft Office-SKUer også gir rettighet, sammen med frittstående PowerApps Plan 2-SKUer.</span><span class="sxs-lookup"><span data-stu-id="63f14-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="63f14-117">Det viktige er at én av disse SKU-ene er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="63f14-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="63f14-118">Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="63f14-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="63f14-119">Opprett miljøene ved å følge instruksjonene i [Klargjøre Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="63f14-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
