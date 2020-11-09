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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 26818ceace7d2b7e7c3ed4d0bb0bd9ab2e884aba
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997606"
---
# <a name="integrated-tax"></a><span data-ttu-id="55ca1-103">Integrert avgift</span><span class="sxs-lookup"><span data-stu-id="55ca1-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="55ca1-104">Avgiftsoppsettsdata definerer oppsettet for både indirekte avgifter (mva, merverdiavgift, salgsskatt) og kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="55ca1-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="55ca1-105">Den beskriver avgiftsberegningsregelen, mva-satsen, avgiftsregnskapet, utligningen og andre begreper.</span><span class="sxs-lookup"><span data-stu-id="55ca1-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="55ca1-106">Maler</span><span class="sxs-lookup"><span data-stu-id="55ca1-106">Templates</span></span>

<span data-ttu-id="55ca1-107">Avgiftsdata inkluderer en samling enhetstilordninger som fungerer sammen under datasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="55ca1-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="55ca1-108">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="55ca1-108">Finance and Operations apps</span></span> | <span data-ttu-id="55ca1-109">Modelldrevne apper i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="55ca1-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="55ca1-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="55ca1-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="55ca1-111">Merverdiavgiftsgruppe for vare</span><span class="sxs-lookup"><span data-stu-id="55ca1-111">Item sales tax group</span></span> | <span data-ttu-id="55ca1-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="55ca1-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="55ca1-113">Skattemyndigheter</span><span class="sxs-lookup"><span data-stu-id="55ca1-113">Sales tax authorities</span></span> | <span data-ttu-id="55ca1-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="55ca1-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="55ca1-115">Enhet for mva-fritakskoder for CDS</span><span class="sxs-lookup"><span data-stu-id="55ca1-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="55ca1-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="55ca1-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="55ca1-117">Mva-grupper</span><span class="sxs-lookup"><span data-stu-id="55ca1-117">Sales tax groups</span></span> | <span data-ttu-id="55ca1-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="55ca1-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="55ca1-119">Finansposteringsgrupper for mva V2</span><span class="sxs-lookup"><span data-stu-id="55ca1-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="55ca1-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="55ca1-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="55ca1-121">Kildeskattkoder</span><span class="sxs-lookup"><span data-stu-id="55ca1-121">Withholding tax codes</span></span> | <span data-ttu-id="55ca1-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="55ca1-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="55ca1-123">Kildeskattgrupper</span><span class="sxs-lookup"><span data-stu-id="55ca1-123">Withholding tax groups</span></span> | <span data-ttu-id="55ca1-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="55ca1-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

