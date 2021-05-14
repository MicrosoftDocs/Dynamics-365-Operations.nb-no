---
title: Bølge er ikke kvalifisert for opprydding
description: Bølge er ikke kvalifisert for opprydding
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924333"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="73865-103">Bølge er ikke kvalifisert for opprydding</span><span class="sxs-lookup"><span data-stu-id="73865-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="73865-104">Feilkode: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="73865-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="73865-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="73865-105">Symptoms</span></span>

<span data-ttu-id="73865-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="73865-106">The system shows the following error message:</span></span>

> <span data-ttu-id="73865-107">Bølgen %1 er ikke berettiget til opprydding.</span><span class="sxs-lookup"><span data-stu-id="73865-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="73865-108">Bølgedataene kan ikke ryddes opp.</span><span class="sxs-lookup"><span data-stu-id="73865-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="73865-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="73865-109">Cause</span></span>

<span data-ttu-id="73865-110">Bølgen behandles i øyeblikket, som angitt ved en av følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="73865-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="73865-111">Feltet **Bølgestatus** er satt til *Utfører*.</span><span class="sxs-lookup"><span data-stu-id="73865-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="73865-112">Når du velger **Satsvis jobb** i **Bølge**-gruppen i kategorien **Bølge** i handlingsruten, er ikke **Status**-feltet angitt til *Avsluttet*, *Feil* eller *Avbrutt*.</span><span class="sxs-lookup"><span data-stu-id="73865-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="73865-113">Derfor er det for øyeblikket en satsvis jobb som kjører.</span><span class="sxs-lookup"><span data-stu-id="73865-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="73865-114">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="73865-114">Resolution</span></span>

<span data-ttu-id="73865-115">I handlingsruten i kategorien **Bølge** i **Bølge**-gruppen velger du **Satsvis jobb**, og følger deretter ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="73865-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="73865-116">Hvis **Status**-feltet er satt til *Utfører*: I handlingsruten i kategorien **Satsvis jobb**, i **Satvis jobb**-gruppen, velger du **Vis oppgaver**.</span><span class="sxs-lookup"><span data-stu-id="73865-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="73865-117">Du kan følge fremdriften ved å oppdatere siden **Satsvise oppgaver**.</span><span class="sxs-lookup"><span data-stu-id="73865-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="73865-118">Hvis **Status**-feltet ikke er satt til *Utfører*: I handlingsruten i kategorien **Satsvis jobb**, i **Funksjoner**-gruppen, velger du **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="73865-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="73865-119">I feltet **Velg ny status** velger du *Venter*.</span><span class="sxs-lookup"><span data-stu-id="73865-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="73865-120">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="73865-120">Then select **OK**.</span></span>
