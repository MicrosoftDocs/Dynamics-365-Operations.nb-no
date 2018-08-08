--- 
title: Tilordne en produktlivssyklustilstand til en frigitt produktstandard
description: "Denne fremgangsmåten viser hvordan du tilordner en produktlivssyklustilstand til en frigitt produktstandard og tilhørende varianter."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: dd9d40bb331b9e024617c8be55330dfce8ba1cc6
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="85c85-103">Tilordne en produktlivssyklustilstand til en frigitt produktstandard</span><span class="sxs-lookup"><span data-stu-id="85c85-103">Assign a product lifecycle state to a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85c85-104">Denne fremgangsmåten viser hvordan du tilordner en produktlivssyklustilstand til en frigitt produktstandard og tilhørende varianter.</span><span class="sxs-lookup"><span data-stu-id="85c85-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="85c85-105">Forutsetning: Du må spille av oppgaveveiledningen Opprette en ny produktlivssyklustilstand først for å være sikker på at du har minst én produktlivssyklustilstand opprettet før du kan spille av denne oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="85c85-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="85c85-106">Finne en frigitt produktstandard</span><span class="sxs-lookup"><span data-stu-id="85c85-106">Find a released product master</span></span>
1. <span data-ttu-id="85c85-107">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="85c85-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="85c85-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="85c85-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="85c85-109">En produktstandard har produktets undertype Produktstandard.</span><span class="sxs-lookup"><span data-stu-id="85c85-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="85c85-110">Oppdatere livssyklustilstanden</span><span class="sxs-lookup"><span data-stu-id="85c85-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="85c85-111">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="85c85-111">Click Edit.</span></span>
2. <span data-ttu-id="85c85-112">Angi eller velg en verdi i feltet Livssyklustilstand for produkt.</span><span class="sxs-lookup"><span data-stu-id="85c85-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="85c85-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="85c85-113">Click Save.</span></span>
4. <span data-ttu-id="85c85-114">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="85c85-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="85c85-115">Hvis Ja er valgt, oppdateres også alle de tilknyttede frigitte produktvariantene som har samme opprinnelige status som den frigitte produktstandarden, til den nye produktlivssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="85c85-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="85c85-116">Hvis Nei er valgt, beholder alle varianter den faktiske tilstanden.</span><span class="sxs-lookup"><span data-stu-id="85c85-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="85c85-117">Varianter som har en annen produktlivssyklustilstand fra den frigitte produktstandarden, blir ikke oppdatert.</span><span class="sxs-lookup"><span data-stu-id="85c85-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="85c85-118">Kontrollere livssyklustilstanden for variantene</span><span class="sxs-lookup"><span data-stu-id="85c85-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="85c85-119">Klikk Frigitte produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="85c85-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="85c85-120">Vær oppmerksom på at alle varianter har arvet den valgte livssyklustilstanden fra den frigitte produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="85c85-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="85c85-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="85c85-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="85c85-122">Angi eller velg en verdi i feltet Livssyklustilstand for produkt.</span><span class="sxs-lookup"><span data-stu-id="85c85-122">In the Product lifecycle state field, enter or select a value.</span></span>


