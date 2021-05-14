---
title: Arbeid blokkeres ikke
description: Arbeid blokkeres ikke
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924210"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="06d26-103">Arbeid er ikke sperret</span><span class="sxs-lookup"><span data-stu-id="06d26-103">Work isn't blocked</span></span>

<span data-ttu-id="06d26-104">Feilkode: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="06d26-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="06d26-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="06d26-105">Symptoms</span></span>

<span data-ttu-id="06d26-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="06d26-106">The system shows the following error message:</span></span>

> <span data-ttu-id="06d26-107">Arbeid med ID-en %1 er ikke blokkert.</span><span class="sxs-lookup"><span data-stu-id="06d26-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="06d26-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="06d26-108">Cause</span></span>

<span data-ttu-id="06d26-109">Alternativet **Blokkert bølge** i bølgen er satt til *Nei*.</span><span class="sxs-lookup"><span data-stu-id="06d26-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="06d26-110">Blokkering av arbeidet kan ikke oppheves, fordi det i øyeblikket ikke er blokkert.</span><span class="sxs-lookup"><span data-stu-id="06d26-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="06d26-111">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="06d26-111">Resolution</span></span>

 <span data-ttu-id="06d26-112">Bare arbeid der alternativet **Blokkert bølge** er satt til *Ja*, kan oppheve blokkering.</span><span class="sxs-lookup"><span data-stu-id="06d26-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
