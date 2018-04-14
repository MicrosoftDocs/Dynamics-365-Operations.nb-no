---
title: Parti- og nummerskiltbekreftelse
description: Dette emnet beskriver hvordan du definerer og bruker parti- og nummerskiltbekreftelse fra en mobilenhet.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 90a45347cb5ed94259587024027eb8d1c4643fc6
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="db406-103">Parti- og nummerskiltbekreftelse</span><span class="sxs-lookup"><span data-stu-id="db406-103">Batch and license plate confirmation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="db406-104">Partibekreftelse lar deg bekrefte at det riktige partiet velges fra mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="db406-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="db406-105">Første gang du plukker arbeid bare for parti over-varer, der parti over angir at partiet går høyere enn plasseringen i søkehierarkiet, må du bekrefte at partiet som plukkes, samsvarer med partiet på arbeidslinjen.</span><span class="sxs-lookup"><span data-stu-id="db406-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="db406-106">Nummerskiltbekreftelse lar deg bekrefte at det nummerskiltet velges fra mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="db406-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="db406-107">Når du plukker arbeid fra en stadielokasjon, må du bekrefte at nummerskilt som plukkes, svarer til nummerskiltet som er knyttet til arbeidet.</span><span class="sxs-lookup"><span data-stu-id="db406-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="db406-108">Hvis arbeidet startes ved å skanne et nummerskilt, utelates dette bekreftelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="db406-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="db406-109">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="db406-109">Where it applies</span></span>
<span data-ttu-id="db406-110">Bekreftelse gjelder i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="db406-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="db406-111">Partibekreftelse gjelder for de første plukkingene av arbeid for parti over-varer.</span><span class="sxs-lookup"><span data-stu-id="db406-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="db406-112">Nummerskiltbekreftelse gjelder for plukking fra stadielokasjoner.</span><span class="sxs-lookup"><span data-stu-id="db406-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="db406-113">Konfigurere parti- og nummerskiltbekreftelse</span><span class="sxs-lookup"><span data-stu-id="db406-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="db406-114">Du kan konfigurere parti- og nummerskiltbekreftelse fra menyelementene på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="db406-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="db406-115">Gå til arbeidsbekreftelsesoppsettet fra menyelementene på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="db406-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="db406-116">Velg alternativet for partibekreftelse eller nummerskiltbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="db406-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="db406-117">Begge alternativene er tilgjengelige for arbeidstypeplukk der automatisk bekreftelse ikke er aktivert.</span><span class="sxs-lookup"><span data-stu-id="db406-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  

