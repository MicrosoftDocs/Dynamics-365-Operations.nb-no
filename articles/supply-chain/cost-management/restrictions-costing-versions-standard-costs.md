---
title: Begrensninger på etterkalkuleringsversjoner for standard kostpris
description: Dette emnet beskriver begrensninger som gjelder for etterkalkuleringsversjoner for standard kostpriser.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5339c3c4a62b94a06cbffc200ed1e9b227d6b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963794"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="67fa9-103">Begrensninger på etterkalkuleringsversjoner for standard kostpris</span><span class="sxs-lookup"><span data-stu-id="67fa9-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67fa9-104">Dette emnet beskriver begrensninger som gjelder for etterkalkuleringsversjoner for standard kostpriser.</span><span class="sxs-lookup"><span data-stu-id="67fa9-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="67fa9-105">Begrensningene nedenfor sikrer at prinsippene for etterkalkulering av standard kostpriser overholdes:</span><span class="sxs-lookup"><span data-stu-id="67fa9-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="67fa9-106">Tillegg må inkluderes i en vares kostnad.</span><span class="sxs-lookup"><span data-stu-id="67fa9-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="67fa9-107">Tilleggene for en produsert vare representerer de amortiserte konstante kostnadene i stykkliste- og ruteinformasjon.</span><span class="sxs-lookup"><span data-stu-id="67fa9-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="67fa9-108">Derfor må tilleggene inkluderes i enhetskostnaden.</span><span class="sxs-lookup"><span data-stu-id="67fa9-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="67fa9-109">Tilleggene for en innkjøpt vare er også inkludert i varens enhetskostnad.</span><span class="sxs-lookup"><span data-stu-id="67fa9-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="67fa9-110">Beregning av standard kostpriser for produserte varer må bygge på kostnadspostene i en etterkalkuleringsversjon for standard kostpriser.</span><span class="sxs-lookup"><span data-stu-id="67fa9-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="67fa9-111">Alternative kilder til kostnadsdata kan bare brukes sammen med en etterkalkuleringsversjon for planlagte kostnader, for eksempel forretningsavtaler om innkjøpspris for innkjøpte varer.</span><span class="sxs-lookup"><span data-stu-id="67fa9-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="67fa9-112">Alternative kilder til kostnadsdata defineres av stykklisteberegningsgruppen.</span><span class="sxs-lookup"><span data-stu-id="67fa9-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="67fa9-113">Stykklisteberegninger må utføres med nedbryting på ett enkelt nivå.</span><span class="sxs-lookup"><span data-stu-id="67fa9-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="67fa9-114">Varekostnadsdata for standard kostpriser kan kopieres til en annen etterkalkuleringsversjon som inneholder standard kostpriser eller planlagte kostnader.</span><span class="sxs-lookup"><span data-stu-id="67fa9-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="67fa9-115">Imidlertid kan varekostnadsdataene for planlagte kostnader ikke kopieres til en etterkalkuleringsversjon som inneholder standard kostpriser, fordi begrensningene det vises til tidligere i dette emnet, ikke gjelder planlagte kostnader.</span><span class="sxs-lookup"><span data-stu-id="67fa9-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="67fa9-116">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="67fa9-116">Related topics</span></span>
--------

[<span data-ttu-id="67fa9-117">Oversikt over etterkalkuleringsversjoner</span><span class="sxs-lookup"><span data-stu-id="67fa9-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="67fa9-118">Oppdatere standardkostnader i et ikke-produksjonsmiljø</span><span class="sxs-lookup"><span data-stu-id="67fa9-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="67fa9-119">Forberede vedlikehold av standard kostpris for produserte varer</span><span class="sxs-lookup"><span data-stu-id="67fa9-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

