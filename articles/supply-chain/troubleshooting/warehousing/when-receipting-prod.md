---
title: Det skrives bare ut én etikett for flere arbeidshoder i en enkelt kvittering
description: Det skrives bare ut én etikett for flere arbeidshoder i en enkelt kvittering.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026778"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="705cf-103">Det skrives bare ut én etikett for flere arbeidshoder i en enkelt kvittering</span><span class="sxs-lookup"><span data-stu-id="705cf-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="705cf-104">KB-nummer: 4614667</span><span class="sxs-lookup"><span data-stu-id="705cf-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="705cf-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="705cf-105">Symptoms</span></span>

<span data-ttu-id="705cf-106">Flere arbeidshoder opprettes for samme målnummerskilt som del av en enkelt lagerappmottakshendelse.</span><span class="sxs-lookup"><span data-stu-id="705cf-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="705cf-107">Det skrives imidlertid bare ut én lisensetikett når produktet mottas.</span><span class="sxs-lookup"><span data-stu-id="705cf-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="705cf-108">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="705cf-108">Resolution</span></span>

<span data-ttu-id="705cf-109">Systemet fungerer som tiltenkt.</span><span class="sxs-lookup"><span data-stu-id="705cf-109">The system is behaving as designed.</span></span>

<span data-ttu-id="705cf-110">I den gjeldende utformingen genereres det alltid én enkelt lisensetikett, uansett hvor mange arbeidshode- og arbeidslinjekombinasjoner som finnes.</span><span class="sxs-lookup"><span data-stu-id="705cf-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="705cf-111">Den genererte etiketten inneholder informasjon for bare én kombinasjon.</span><span class="sxs-lookup"><span data-stu-id="705cf-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="705cf-112">Du kan omgå dette problemet ved å sørge for at oppretting av arbeidshode alltid er tilordnet til bare én lisensavtale.</span><span class="sxs-lookup"><span data-stu-id="705cf-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
