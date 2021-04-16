---
title: Beregne en stykkliste ved hjelp av en struktur med ett nivå (februar 2016)
description: Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på ett enkelt nivå som er basert på kostarket.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013eddf1ba8e8cab3c87cb1f063d9bf886b0f833
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821399"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="da0ff-103">Beregne en stykkliste ved hjelp av en struktur med ett nivå (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="da0ff-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da0ff-104">Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på ett enkelt nivå som er basert på kostarket.</span><span class="sxs-lookup"><span data-stu-id="da0ff-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="da0ff-105">Dette er den sjette oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="da0ff-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="da0ff-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="da0ff-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="da0ff-107">Gå til Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="da0ff-107">Go to Released products.</span></span>
2. <span data-ttu-id="da0ff-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="da0ff-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da0ff-109">Velg produkt BOM_1.</span><span class="sxs-lookup"><span data-stu-id="da0ff-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="da0ff-110">Klikk på Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da0ff-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="da0ff-111">Klikk på Varepris.</span><span class="sxs-lookup"><span data-stu-id="da0ff-111">Click Item price.</span></span>
5. <span data-ttu-id="da0ff-112">Klikk på Beregn varekostnad.</span><span class="sxs-lookup"><span data-stu-id="da0ff-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="da0ff-113">Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="da0ff-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="da0ff-114">Klikk på rullegardinknappen i feltet Etterkalkuleringsversjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="da0ff-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="da0ff-115">Velg 10 for denne demonstrasjonen.</span><span class="sxs-lookup"><span data-stu-id="da0ff-115">For this demo, select 10.</span></span> <span data-ttu-id="da0ff-116">Dette er den samme etterkalkuleringsversjonen som brukes til å legge til kostprisen til komponentene.</span><span class="sxs-lookup"><span data-stu-id="da0ff-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="da0ff-117">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="da0ff-117">Click OK.</span></span>
8. <span data-ttu-id="da0ff-118">Klikk på Vis beregningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="da0ff-118">Click View calculation details.</span></span>
    * <span data-ttu-id="da0ff-119">Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="da0ff-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="da0ff-120">Her er sammensetningen av kostnaden:  \*    10 er avledet fra ITEM_A, 10 fra ITEM_B, 10 fra BOM_2.</span><span class="sxs-lookup"><span data-stu-id="da0ff-120">Here's the composition of the cost:  \*    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="da0ff-121">I dette tilfellet finnes det ingen detaljer for BOM_2 fordi det ble angitt som en standard kostnad på 10, men ikke utført gjennom beregning.</span><span class="sxs-lookup"><span data-stu-id="da0ff-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="da0ff-122">\*    7 er avledet fra oppstillingstiden, som er en konstant kostnad, og ytterligere 7 er avledet fra kjøretidsoperasjonen (prosess).</span><span class="sxs-lookup"><span data-stu-id="da0ff-122">\*    7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="da0ff-123">\*    Det finnes også andre beløp som samsvarer med indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="da0ff-123">\*    There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="da0ff-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="da0ff-124">@SysTaskRecorder:_RequestClose</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]