---
title: Oppdatere standard kostpris i et produksjonsmiljø
description: Denne artikkelen gir veiledning for hvordan du kan oppdatere standardkostnader i et produksjonsmiljø.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea810daab0ecdee59aba703f38d0001e2965f936
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214165"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="fd4a5-103">Oppdatere standard kostpris i et produksjonsmiljø</span><span class="sxs-lookup"><span data-stu-id="fd4a5-103">Update standard costs in a manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd4a5-104">Denne artikkelen gir veiledning for hvordan du kan oppdatere standardkostnader i et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="fd4a5-105">Oppdateringer kan gjenspeile nye varer, kostnadskategorier eller formler for beregning av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="fd4a5-106">De kan også gjenspeile korrigeringer og kostnadsendringer.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="fd4a5-107">Typen oppdatering påvirker trinnene som må fullføres for å oppdatere standard kostpris, som vist i følgende tilfeller:</span><span class="sxs-lookup"><span data-stu-id="fd4a5-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="fd4a5-108">Angi forventede endringer i standard kostpris for innkjøpte varer, og endre deretter status for varekostnadspostene til **Aktive** på den aktuelle datoen.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="fd4a5-109">Du må imidlertid ikke omberegne kostnadene for produserte varer som bruker de innkjøpte varene.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="fd4a5-110">Angi standard kostpris for en nyinnkjøpt vare, men ikke omberegn kostnadene for produserte varer som har en stykklisteversjon som har den nyinnkjøpte varen som komponent.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="fd4a5-111">Rett opp eller endre kostprisen for en innkjøpt vare, eller endre kostgruppen som er tilordnet en innkjøpt vare, og beregn kostnadene for alle produserte varer som har en stykklisteversjon som har den innkjøpte varen som komponent.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="fd4a5-112">Endre kostprisen for en kostnadskategori, og beregn kostnadene for alle produserte varer som har en ruteversjon som inneholder rutingoperasjoner som bruker kostnadskategorien.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="fd4a5-113">Endre kostnadskategoriene som er tilordnet til ruteoperasjoner eller kostgruppen som er tilordnet kostnadskategorier.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="fd4a5-114">Beregn deretter kostnadene for alle produserte varer som har en ruteversjon som inneholder rutingoperasjoner som bruker kostnadskategorien.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="fd4a5-115">Endre en beregningsformel for indirekte kostnader, og beregn kostnadene for alle produserte varer som påvirkes av endringen.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="fd4a5-116">Endre eller legg til et produksjonsanlegg for en produsert vare, og beregn varens produserte kostpris for anlegget.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="fd4a5-117">Beregn, eller omberegn, kostnadene for en produsert vare, og omberegn kostnadene for alle produserte varer som har en stykklisteversjon som har den produserte varen som komponent.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="fd4a5-118">Beregn kostnadene for en nyprodusert vare på grunnlag av den definerte, godkjente og aktive stykklisten og ruteinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="fd4a5-119">Hvert tilfelle krever nøye overveielse om hvordan standard kostpris skal oppdateres.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-119">Each case requires careful consideration about how to update standard costs.</span></span>



