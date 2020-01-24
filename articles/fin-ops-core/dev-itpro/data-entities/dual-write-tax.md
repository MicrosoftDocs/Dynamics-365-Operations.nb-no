---
title: Integrert avgift
description: Dette emnet beskriver integreringen av avgiftsdata mellom Finance and Operations og Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853865"
---
# <a name="integrated-tax"></a><span data-ttu-id="3dbb7-103">Integrert avgift</span><span class="sxs-lookup"><span data-stu-id="3dbb7-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3dbb7-104">Avgiftsoppsettsdata definerer oppsettet for både indirekte avgifter (mva, merverdiavgift, salgsskatt) og kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="3dbb7-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="3dbb7-105">Den beskriver avgiftsberegningsregelen, mva-satsen, avgiftsregnskapet, utligningen og andre begreper.</span><span class="sxs-lookup"><span data-stu-id="3dbb7-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="3dbb7-106">Maler</span><span class="sxs-lookup"><span data-stu-id="3dbb7-106">Templates</span></span>

<span data-ttu-id="3dbb7-107">Avgiftsdata inkluderer en samling enhetstilordninger som fungerer sammen under datasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="3dbb7-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="3dbb7-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dbb7-108">Finance and Operations</span></span>   | <span data-ttu-id="3dbb7-109">Andre Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="3dbb7-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="3dbb7-110">Mva-koder</span><span class="sxs-lookup"><span data-stu-id="3dbb7-110">Tax codes</span></span>                  | <span data-ttu-id="3dbb7-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="3dbb7-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="3dbb7-112">Mva-grupper</span><span class="sxs-lookup"><span data-stu-id="3dbb7-112">Tax groups</span></span>               | <span data-ttu-id="3dbb7-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="3dbb7-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="3dbb7-114">Mva-varegrupper</span><span class="sxs-lookup"><span data-stu-id="3dbb7-114">Tax item groups</span></span>          | <span data-ttu-id="3dbb7-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="3dbb7-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="3dbb7-116">Avgiftsfritak</span><span class="sxs-lookup"><span data-stu-id="3dbb7-116">Tax Exemptions</span></span>           | <span data-ttu-id="3dbb7-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="3dbb7-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="3dbb7-118">Skattemyndigheter</span><span class="sxs-lookup"><span data-stu-id="3dbb7-118">Tax Authorities</span></span>          | <span data-ttu-id="3dbb7-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="3dbb7-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="3dbb7-120">Kildeskattkoder</span><span class="sxs-lookup"><span data-stu-id="3dbb7-120">Withholding tax codes</span></span>      | <span data-ttu-id="3dbb7-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="3dbb7-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="3dbb7-122">Kildeskattgrupper</span><span class="sxs-lookup"><span data-stu-id="3dbb7-122">Withholding tax groups</span></span>   | <span data-ttu-id="3dbb7-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="3dbb7-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="3dbb7-124">Finanskontogruppe for avgift</span><span class="sxs-lookup"><span data-stu-id="3dbb7-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="3dbb7-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="3dbb7-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

