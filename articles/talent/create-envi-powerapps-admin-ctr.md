---
title: Kan ikke opprette et miljø i administrasjonssenteret for Power Apps
description: Dette emnet forklarer hva du gjør hvis administratoren ikke kan opprette et miljø i Microsoft Power Apps-administrasjonssenteret.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7a66b7624655aaf976aaa63b2626f65c54d0ea38
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898826"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="67eb5-103">Kan ikke opprette et miljø i administrasjonssenteret for Power Apps</span><span class="sxs-lookup"><span data-stu-id="67eb5-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="67eb5-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="67eb5-104">**Issue**</span></span>

- <span data-ttu-id="67eb5-105">Leier-/miljøadministratoren kan ikke opprette et miljø i Microsoft Power Apps-administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="67eb5-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="67eb5-106">En lisens som gir brukerne rett til å utføre miljøopprettingstrinnet, er ikke tilordnet direkte til brukeren som utfører dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="67eb5-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="67eb5-107">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="67eb5-107">**Solution**</span></span>

<span data-ttu-id="67eb5-108">Kontroller at leieradministratoren har tilordnet en gyldig lisens for Power Apps P2 direkte til brukeren som utfører miljøopprettingstrinnet.</span><span class="sxs-lookup"><span data-stu-id="67eb5-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="67eb5-109">Her er Microsoft Dynamics-serviceplanene som gir denne rettigheten.</span><span class="sxs-lookup"><span data-stu-id="67eb5-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="67eb5-110">Generell produktlagerenhet (SKU)</span><span class="sxs-lookup"><span data-stu-id="67eb5-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="67eb5-111">Power Apps P2-serviceplan</span><span class="sxs-lookup"><span data-stu-id="67eb5-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="67eb5-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="67eb5-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="67eb5-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="67eb5-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="67eb5-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="67eb5-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="67eb5-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="67eb5-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="67eb5-116">Legg merke til at ulike Microsoft Office-SKUer også gir rettighet, sammen med frittstående Power Apps Plan 2-SKUer.</span><span class="sxs-lookup"><span data-stu-id="67eb5-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="67eb5-117">Det viktige er at én av disse SKU-ene er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="67eb5-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="67eb5-118">Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="67eb5-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="67eb5-119">Opprett miljøene ved å følge instruksjonene i [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="67eb5-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
