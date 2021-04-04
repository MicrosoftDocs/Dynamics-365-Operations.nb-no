---
title: Kontrollere varekvaliteten
description: Dette emnet forklarer hvordan du behandler en kvalitetsordre.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e37ac8c9320d427b9f9a3ca32b0e4667c7023339
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244429"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="18234-103">Kontrollere varekvaliteten</span><span class="sxs-lookup"><span data-stu-id="18234-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18234-104">Dette emnet forklarer hvordan du behandler en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="18234-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="18234-105">Du kan bruke denne veiledningen i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="18234-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="18234-106">Før du starter denne eksempelprosedyren, må du bekrefte bestillingen "000016" og postere en produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="18234-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="18234-107">Dermed opprettes automatisk en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="18234-107">This will automatically create a quality order.</span></span> <span data-ttu-id="18234-108">Kvalitetsinspeksjoner utføres vanligvis av en kvalitetsassistent.</span><span class="sxs-lookup"><span data-stu-id="18234-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="18234-109">Velge en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="18234-109">Select a quality order</span></span>
1. <span data-ttu-id="18234-110">I navigasjonsruten går du til **Moduler > Lagerstyring > Periodiske oppgaver > Kvalitetsstyring > Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="18234-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="18234-111">Velg kvalitetsordren som ble opprettet før du startet denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="18234-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="18234-112">Registere testresultater</span><span class="sxs-lookup"><span data-stu-id="18234-112">Record test results</span></span>
1. <span data-ttu-id="18234-113">Velg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="18234-113">Select **Results**.</span></span>
2. <span data-ttu-id="18234-114">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="18234-114">Select **Edit**.</span></span>
3. <span data-ttu-id="18234-115">Angi et tall i **Resultatantall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="18234-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="18234-116">Velg det ønskede oppslaget på rullegardinmenyen i **Resultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="18234-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="18234-117">I dette eksemplet er resultatet basert på et forhåndsdefinert resultat.</span><span class="sxs-lookup"><span data-stu-id="18234-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="18234-118">Vanligvis vil du registrere et mer spesifikt testresultat, for eksempel en størrelse eller annen dimensjon.</span><span class="sxs-lookup"><span data-stu-id="18234-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="18234-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="18234-119">Select **Save**.</span></span>
6. <span data-ttu-id="18234-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="18234-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="18234-121">Valider kvalitetsordren</span><span class="sxs-lookup"><span data-stu-id="18234-121">Validate the quality order</span></span>
1. <span data-ttu-id="18234-122">Velg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="18234-122">Select **Validate**.</span></span>
2. <span data-ttu-id="18234-123">I feltet **Validert av** velger du brukeren som utfører inspeksjonen, fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="18234-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="18234-124">Klikk på **Velg**.</span><span class="sxs-lookup"><span data-stu-id="18234-124">Click **Select**.</span></span>
4. <span data-ttu-id="18234-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="18234-125">Select **OK**.</span></span>
5. <span data-ttu-id="18234-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="18234-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]