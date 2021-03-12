---
title: Legge til beregning i en produktkonfigurasjonsmodell
description: Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987060"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="fc004-103">Legge til beregning i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="fc004-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc004-104">Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="fc004-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="fc004-105">Den viser hvordan du kan opprette et logisk uttrykk ved hjelp av operatoren "If" for å angi en høyttalerhøyde på 10 for hvite høyttalere og 15 for alle andre kabinettyper.</span><span class="sxs-lookup"><span data-stu-id="fc004-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="fc004-106">Fremgangsmåten bruker komponenten for High-end-høyttaler i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="fc004-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="fc004-107">Legge til en beregning</span><span class="sxs-lookup"><span data-stu-id="fc004-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="fc004-108">Opprette beregningsuttrykk</span><span class="sxs-lookup"><span data-stu-id="fc004-108">Create calculation expression</span></span>
1. <span data-ttu-id="fc004-109">Klikk på Rediger uttrykk.</span><span class="sxs-lookup"><span data-stu-id="fc004-109">Click Edit expression.</span></span>
2. <span data-ttu-id="fc004-110">I ConstraintBody-feltet skriver du inn If[CabinetFinish=="White", 10, 15].</span><span class="sxs-lookup"><span data-stu-id="fc004-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="fc004-111">Klikk på Valider.</span><span class="sxs-lookup"><span data-stu-id="fc004-111">Click Validate.</span></span>
4. <span data-ttu-id="fc004-112">Klikk på Lukk.</span><span class="sxs-lookup"><span data-stu-id="fc004-112">Click Close.</span></span>
5. <span data-ttu-id="fc004-113">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="fc004-113">Click OK.</span></span>

