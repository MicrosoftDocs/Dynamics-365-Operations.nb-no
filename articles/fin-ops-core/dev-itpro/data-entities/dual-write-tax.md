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
ms.openlocfilehash: b6be53e9a2065373ca37c2791568a8161823803f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772416"
---
## <a name="integrated-tax"></a><span data-ttu-id="a044a-103">Integrert avgift</span><span class="sxs-lookup"><span data-stu-id="a044a-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a044a-104">Avgiftsoppsettsdata definerer oppsettet for både indirekte avgifter (mva, merverdiavgift, salgsskatt) og kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="a044a-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="a044a-105">Den beskriver avgiftsberegningsregelen, mva-satsen, avgiftsregnskapet, utligningen og andre begreper.</span><span class="sxs-lookup"><span data-stu-id="a044a-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="a044a-106">Maler</span><span class="sxs-lookup"><span data-stu-id="a044a-106">Templates</span></span>

<span data-ttu-id="a044a-107">Avgiftsdata inkluderer en samling enhetstilordninger som fungerer sammen under datasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="a044a-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="a044a-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a044a-108">Finance and Operations</span></span>   | <span data-ttu-id="a044a-109">Customer Engagement-programmet</span><span class="sxs-lookup"><span data-stu-id="a044a-109">Customer Engagement application</span></span>
-------------------------|---------------------------------
<span data-ttu-id="a044a-110">Mva-koder</span><span class="sxs-lookup"><span data-stu-id="a044a-110">Tax codes</span></span>                  | <span data-ttu-id="a044a-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="a044a-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="a044a-112">Mva-grupper</span><span class="sxs-lookup"><span data-stu-id="a044a-112">Tax groups</span></span>               | <span data-ttu-id="a044a-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="a044a-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="a044a-114">Mva-varegrupper</span><span class="sxs-lookup"><span data-stu-id="a044a-114">Tax item groups</span></span>          | <span data-ttu-id="a044a-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="a044a-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="a044a-116">Avgiftsfritak</span><span class="sxs-lookup"><span data-stu-id="a044a-116">Tax Exemptions</span></span>           | <span data-ttu-id="a044a-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="a044a-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="a044a-118">Skattemyndigheter</span><span class="sxs-lookup"><span data-stu-id="a044a-118">Tax Authorities</span></span>          | <span data-ttu-id="a044a-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="a044a-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="a044a-120">Kildeskattkoder</span><span class="sxs-lookup"><span data-stu-id="a044a-120">Withholding tax codes</span></span>      | <span data-ttu-id="a044a-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="a044a-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="a044a-122">Kildeskattgrupper</span><span class="sxs-lookup"><span data-stu-id="a044a-122">Withholding tax groups</span></span>   | <span data-ttu-id="a044a-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="a044a-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="a044a-124">Finanskontogruppe for avgift</span><span class="sxs-lookup"><span data-stu-id="a044a-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="a044a-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="a044a-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

