---
title: Kan ikke opprette et miljø i administrasjonssenteret for Power Apps
description: Denne artikkelen forklarer hva du gjør hvis administratoren ikke kan opprette et miljø i Microsoft Power Apps-administrasjonssenteret.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1a086f1b710de9bad898abc740286c174ae3be7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797991"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="73275-103">Kan ikke opprette et miljø i administrasjonssenteret for Power Apps</span><span class="sxs-lookup"><span data-stu-id="73275-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="73275-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="73275-104">**Issue**</span></span>

- <span data-ttu-id="73275-105">Leier-/miljøadministratoren kan ikke opprette et miljø i Microsoft Power Apps-administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="73275-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="73275-106">Brukeren har ikke en lisens som gir rett til å opprette miljøer.</span><span class="sxs-lookup"><span data-stu-id="73275-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="73275-107">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="73275-107">**Solution**</span></span>

<span data-ttu-id="73275-108">Kontroller at leietakeradministratoren har tilordnet en gyldig Power Apps P2-lisens til brukeren som oppretter miljøet.</span><span class="sxs-lookup"><span data-stu-id="73275-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="73275-109">Følgende Microsoft Dynamics-serviceplaner gir tillatelser til å opprette miljøer:</span><span class="sxs-lookup"><span data-stu-id="73275-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="73275-110">Generell produktlagerenhet (SKU)</span><span class="sxs-lookup"><span data-stu-id="73275-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="73275-111">Power Apps P2-serviceplan</span><span class="sxs-lookup"><span data-stu-id="73275-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="73275-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="73275-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="73275-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="73275-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="73275-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="73275-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="73275-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="73275-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="73275-116">Legg merke til at ulike Microsoft Office-SKUer også gir rettighet, sammen med frittstående Power Apps Plan 2-SKUer.</span><span class="sxs-lookup"><span data-stu-id="73275-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="73275-117">Det viktige er at én av disse SKU-ene er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="73275-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="73275-118">Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="73275-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="73275-119">Opprett miljøene ved å følge instruksjonene i [Klargjøre Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="73275-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]