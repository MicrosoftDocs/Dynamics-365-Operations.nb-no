---
title: Parti- og nummerskiltbekreftelse
description: Dette emnet beskriver hvordan du definerer og bruker parti- og nummerskiltbekreftelse fra en mobilenhet.
author: Mirzaab
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97790b91d4de536b89b580c26ef1e37145f7d7c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977444"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="6fa69-103">Parti- og nummerskiltbekreftelse</span><span class="sxs-lookup"><span data-stu-id="6fa69-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fa69-104">Partibekreftelse lar deg bekrefte at det riktige partiet velges fra mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="6fa69-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="6fa69-105">Første gang du plukker arbeid bare for parti over-varer, der parti over angir at partiet går høyere enn plasseringen i søkehierarkiet, må du bekrefte at partiet som plukkes, samsvarer med partiet på arbeidslinjen.</span><span class="sxs-lookup"><span data-stu-id="6fa69-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="6fa69-106">Nummerskiltbekreftelse lar deg bekrefte at det nummerskiltet velges fra mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="6fa69-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="6fa69-107">Når du plukker arbeid fra en stadielokasjon, må du bekrefte at nummerskilt som plukkes, svarer til nummerskiltet som er knyttet til arbeidet.</span><span class="sxs-lookup"><span data-stu-id="6fa69-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="6fa69-108">Hvis arbeidet startes ved å skanne et nummerskilt, utelates dette bekreftelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="6fa69-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="6fa69-109">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="6fa69-109">Where it applies</span></span>

<span data-ttu-id="6fa69-110">Bekreftelse gjelder i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="6fa69-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="6fa69-111">Partibekreftelse gjelder for de første plukkingene av arbeid for parti over-varer.</span><span class="sxs-lookup"><span data-stu-id="6fa69-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="6fa69-112">Nummerskiltbekreftelse gjelder for plukking fra stadielokasjoner.</span><span class="sxs-lookup"><span data-stu-id="6fa69-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6fa69-113">Etterfylling støttes ikke for nummerskiltbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="6fa69-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="6fa69-114">Når du utfører etterfyllingsarbeid, opprettes det ikke noe trinn for nummerskiltbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="6fa69-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="6fa69-115">Konfigurere parti- og nummerskiltbekreftelse</span><span class="sxs-lookup"><span data-stu-id="6fa69-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="6fa69-116">Du kan konfigurere parti- og nummerskiltbekreftelse fra menyelementene på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="6fa69-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="6fa69-117">Gå til arbeidsbekreftelsesoppsettet fra menyelementene på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="6fa69-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="6fa69-118">Velg alternativet for partibekreftelse eller nummerskiltbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="6fa69-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="6fa69-119">Begge alternativene er tilgjengelige for arbeidstypeplukk der automatisk bekreftelse ikke er aktivert.</span><span class="sxs-lookup"><span data-stu-id="6fa69-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  
