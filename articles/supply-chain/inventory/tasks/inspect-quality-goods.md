---
title: Kontrollere varekvaliteten
description: Dette emnet forklarer hvordan du behandler en kvalitetsordre.
author: perlynne
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47e7156e5c57d5f983564cc966b4108f1180ff8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825921"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="90cba-103">Kontrollere varekvaliteten</span><span class="sxs-lookup"><span data-stu-id="90cba-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90cba-104">Dette emnet forklarer hvordan du behandler en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="90cba-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="90cba-105">Du kan bruke denne veiledningen i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="90cba-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="90cba-106">Før du starter denne eksempelprosedyren, må du bekrefte bestillingen "000016" og postere en produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="90cba-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="90cba-107">Dermed opprettes automatisk en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="90cba-107">This will automatically create a quality order.</span></span> <span data-ttu-id="90cba-108">Kvalitetsinspeksjoner utføres vanligvis av en kvalitetsassistent.</span><span class="sxs-lookup"><span data-stu-id="90cba-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="90cba-109">Velge en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="90cba-109">Select a quality order</span></span>
1. <span data-ttu-id="90cba-110">I navigasjonsruten går du til **Moduler > Lagerstyring > Periodiske oppgaver > Kvalitetsstyring > Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="90cba-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="90cba-111">Velg kvalitetsordren som ble opprettet før du startet denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="90cba-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="90cba-112">Registere testresultater</span><span class="sxs-lookup"><span data-stu-id="90cba-112">Record test results</span></span>
1. <span data-ttu-id="90cba-113">Velg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="90cba-113">Select **Results**.</span></span>
2. <span data-ttu-id="90cba-114">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="90cba-114">Select **Edit**.</span></span>
3. <span data-ttu-id="90cba-115">Angi et tall i **Resultatantall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="90cba-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="90cba-116">Velg det ønskede oppslaget på rullegardinmenyen i **Resultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="90cba-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="90cba-117">I dette eksemplet er resultatet basert på et forhåndsdefinert resultat.</span><span class="sxs-lookup"><span data-stu-id="90cba-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="90cba-118">Vanligvis vil du registrere et mer spesifikt testresultat, for eksempel en størrelse eller annen dimensjon.</span><span class="sxs-lookup"><span data-stu-id="90cba-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="90cba-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="90cba-119">Select **Save**.</span></span>
6. <span data-ttu-id="90cba-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="90cba-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="90cba-121">Valider kvalitetsordren</span><span class="sxs-lookup"><span data-stu-id="90cba-121">Validate the quality order</span></span>
1. <span data-ttu-id="90cba-122">Velg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="90cba-122">Select **Validate**.</span></span>
2. <span data-ttu-id="90cba-123">I feltet **Validert av** velger du brukeren som utfører inspeksjonen, fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="90cba-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="90cba-124">Klikk på **Velg**.</span><span class="sxs-lookup"><span data-stu-id="90cba-124">Click **Select**.</span></span>
4. <span data-ttu-id="90cba-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="90cba-125">Select **OK**.</span></span>
5. <span data-ttu-id="90cba-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="90cba-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]