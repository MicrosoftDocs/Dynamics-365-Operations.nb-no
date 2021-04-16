---
title: Parti- og nummerskiltbekreftelse
description: Dette emnet beskriver hvordan du definerer og bruker parti- og nummerskiltbekreftelse fra en mobilenhet.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c588e6ed11d275b75133e2824f3d385048050426
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837543"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="20566-103">Parti- og nummerskiltbekreftelse</span><span class="sxs-lookup"><span data-stu-id="20566-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20566-104">Partibekreftelse lar deg bekrefte at det riktige partiet velges fra mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="20566-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="20566-105">Første gang du plukker arbeid bare for *Parti-over\[sted\]*, der parti over angir at partiet er plassert høyere enn plasseringen i søkehierarkiet, må du bekrefte at partiet som plukkes, samsvarer med partiet på arbeidslinjen.</span><span class="sxs-lookup"><span data-stu-id="20566-105">On the initial pick of work for *Batch-above\[location\]* items only, where batch-above indicates that batch is placed higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="20566-106">Nummerskiltbekreftelse lar deg bekrefte at det nummerskiltet velges fra mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="20566-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="20566-107">Når du plukker arbeid fra en stadielokasjon, må du bekrefte at nummerskilt som plukkes, svarer til nummerskiltet som er knyttet til arbeidet.</span><span class="sxs-lookup"><span data-stu-id="20566-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="20566-108">Hvis arbeidet startes ved å skanne et nummerskilt, utelates dette bekreftelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="20566-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="20566-109">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="20566-109">Where it applies</span></span>

<span data-ttu-id="20566-110">Bekreftelse gjelder i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="20566-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="20566-111">Partibekreftelse gjelder for de første plukkingene av arbeid for parti over-varer.</span><span class="sxs-lookup"><span data-stu-id="20566-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="20566-112">Nummerskiltbekreftelse gjelder for plukking fra stadielokasjoner.</span><span class="sxs-lookup"><span data-stu-id="20566-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20566-113">Etterfylling støttes ikke for nummerskiltbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="20566-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="20566-114">Når du utfører etterfyllingsarbeid, opprettes det ikke noe trinn for nummerskiltbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="20566-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="20566-115">Konfigurere parti- og nummerskiltbekreftelse</span><span class="sxs-lookup"><span data-stu-id="20566-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="20566-116">Du kan konfigurere parti- og nummerskiltbekreftelse fra menyelementene på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="20566-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="20566-117">Gå til arbeidsbekreftelsesoppsettet fra menyelementene på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="20566-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="20566-118">Velg alternativet for partibekreftelse eller nummerskiltbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="20566-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="20566-119">Begge alternativene er tilgjengelige for arbeidstypeplukk der automatisk bekreftelse ikke er aktivert.</span><span class="sxs-lookup"><span data-stu-id="20566-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
