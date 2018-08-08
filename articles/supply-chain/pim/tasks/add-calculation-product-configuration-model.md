--- 
title: Legge til beregning i en produktkonfigurasjonsmodell
description: "Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell."
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5ca3f1a104fc85d6e33c2abcc27e4e6860406412
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="03e46-103">Legge til beregning i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="03e46-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03e46-104">Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="03e46-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="03e46-105">Den viser hvordan du kan opprette et logisk uttrykk ved hjelp av operatoren "If" for å angi en høyttalerhøyde på 10 for hvite høyttalere og 15 for alle andre kabinettyper.</span><span class="sxs-lookup"><span data-stu-id="03e46-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="03e46-106">Fremgangsmåten bruker komponenten for High-end-høyttaler i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="03e46-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="03e46-107">Legge til en beregning</span><span class="sxs-lookup"><span data-stu-id="03e46-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="03e46-108">Opprette beregningsuttrykk</span><span class="sxs-lookup"><span data-stu-id="03e46-108">Create calculation expression</span></span>
1. <span data-ttu-id="03e46-109">Klikk Rediger uttrykk.</span><span class="sxs-lookup"><span data-stu-id="03e46-109">Click Edit expression.</span></span>
2. <span data-ttu-id="03e46-110">I ConstraintBody-feltet skriver du inn If[CabinetFinish=="White", 10, 15].</span><span class="sxs-lookup"><span data-stu-id="03e46-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="03e46-111">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="03e46-111">Click Validate.</span></span>
4. <span data-ttu-id="03e46-112">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="03e46-112">Click Close.</span></span>
5. <span data-ttu-id="03e46-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="03e46-113">Click OK.</span></span>


