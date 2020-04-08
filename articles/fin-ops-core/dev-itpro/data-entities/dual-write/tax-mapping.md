---
title: Integrert avgift
description: Dette emnet beskriver integreringen av avgiftsdata mellom Finance and Operations og Common Data Service .
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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173091"
---
# <a name="integrated-tax"></a><span data-ttu-id="3c375-103">Integrert avgift</span><span class="sxs-lookup"><span data-stu-id="3c375-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3c375-104">Avgiftsoppsettsdata definerer oppsettet for både indirekte avgifter (mva, merverdiavgift, salgsskatt) og kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="3c375-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="3c375-105">Den beskriver avgiftsberegningsregelen, mva-satsen, avgiftsregnskapet, utligningen og andre begreper.</span><span class="sxs-lookup"><span data-stu-id="3c375-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="3c375-106">Maler</span><span class="sxs-lookup"><span data-stu-id="3c375-106">Templates</span></span>

<span data-ttu-id="3c375-107">Avgiftsdata inkluderer en samling enhetstilordninger som fungerer sammen under datasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="3c375-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="3c375-108">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="3c375-108">Finance and Operations apps</span></span> | <span data-ttu-id="3c375-109">Modelldrevne apper i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3c375-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="3c375-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3c375-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="3c375-111">Mva-koder</span><span class="sxs-lookup"><span data-stu-id="3c375-111">Tax codes</span></span>                   | <span data-ttu-id="3c375-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="3c375-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="3c375-113">Mva-grupper</span><span class="sxs-lookup"><span data-stu-id="3c375-113">Tax groups</span></span>                 | <span data-ttu-id="3c375-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="3c375-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="3c375-115">Mva-varegrupper</span><span class="sxs-lookup"><span data-stu-id="3c375-115">Tax item groups</span></span>             | <span data-ttu-id="3c375-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="3c375-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="3c375-117">Avgiftsfritak</span><span class="sxs-lookup"><span data-stu-id="3c375-117">Tax Exemptions</span></span>             | <span data-ttu-id="3c375-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="3c375-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="3c375-119">Skattemyndigheter</span><span class="sxs-lookup"><span data-stu-id="3c375-119">Tax Authorities</span></span>             | <span data-ttu-id="3c375-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="3c375-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="3c375-121">Kildeskattkoder</span><span class="sxs-lookup"><span data-stu-id="3c375-121">Withholding tax codes</span></span>       | <span data-ttu-id="3c375-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="3c375-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="3c375-123">Kildeskattgrupper</span><span class="sxs-lookup"><span data-stu-id="3c375-123">Withholding tax groups</span></span>     | <span data-ttu-id="3c375-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="3c375-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="3c375-125">Finanskontogruppe for avgift</span><span class="sxs-lookup"><span data-stu-id="3c375-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="3c375-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="3c375-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

