---
title: Avbryte en hovedplanleggingsjobb
description: Dette emnet beskriver hvordan du avbryter en aktiv planleggingsjobb som bruker innebygd planleggingfunksjonalitet.
author: ChristianRytt
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 513aee3b9475506e28db4bffe90df58567b6b281
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816610"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="59944-103">Avbryte en hovedplanleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="59944-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59944-104">I Microsoft Dynamics 365 Supply Chain Management finnes det flere alternativer for å avbryte en hovedplanleggingjobb.</span><span class="sxs-lookup"><span data-stu-id="59944-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="59944-105">Det kan for eksempel hende at du vil avbryte en hovedplanleggingsjobb hvis den ble startet ved en feiltakelse eller kjører lenger tid enn forventet, og du vil avslutte den.</span><span class="sxs-lookup"><span data-stu-id="59944-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="59944-106">Den beste måten å avbryte en planleggingsjobb på, er fra siden **Uferdige planleggingsprosesser**.</span><span class="sxs-lookup"><span data-stu-id="59944-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="59944-107">Alternative valg fra sidene **satsvise jobber** og **satsvise jobber utvidet** bør bare brukes hvis avbrytelse av hovedplanleggingsjobben fra siden **Uferdige planleggingsprosesser** ikke ble fullført i løpet av få minutter.</span><span class="sxs-lookup"><span data-stu-id="59944-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="59944-108">Foretrukket avbruddsalternativ</span><span class="sxs-lookup"><span data-stu-id="59944-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="59944-109">Avbryte hovedplanleggingsjobb fra siden **Uferdige planleggingsprosesser**</span><span class="sxs-lookup"><span data-stu-id="59944-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="59944-110">Gå til **Hovedplanlegging > Forespørsler og rapporter > Hovedplanlegging > Uferdige planleggingsprosesser**.</span><span class="sxs-lookup"><span data-stu-id="59944-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="59944-111">Velg linjen med reparasjonen planleggingsprosessen du ønsker å avbryte.</span><span class="sxs-lookup"><span data-stu-id="59944-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="59944-112">Klikk på **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="59944-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="59944-113">Flere avbruddsalternativer</span><span class="sxs-lookup"><span data-stu-id="59944-113">Additional cancel options</span></span>
<span data-ttu-id="59944-114">Disse bør bare brukes hvis avbrytelse av hovedplanleggingsjobben fra siden **Uferdige planleggingsprosesser** ikke ble fullført i løpet av få minutter.</span><span class="sxs-lookup"><span data-stu-id="59944-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="59944-115">Slette hovedplanleggingsjobb fra siden **satsvise jobber**</span><span class="sxs-lookup"><span data-stu-id="59944-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="59944-116">Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="59944-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="59944-117">Velg linjen med planleggingsjobben du ønsker å slette.</span><span class="sxs-lookup"><span data-stu-id="59944-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="59944-118">Klikk på **Slett**.</span><span class="sxs-lookup"><span data-stu-id="59944-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="59944-119">Avbryte oppgave for hovedplanleggingsjobb fra siden **satsvise jobber utvidet**</span><span class="sxs-lookup"><span data-stu-id="59944-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="59944-120">Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="59944-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="59944-121">Hvis jobb-IDen ikke vises i listen, klikker du **Bytt til utvidet skjema**, ellers fortsetter du med neste trinn.</span><span class="sxs-lookup"><span data-stu-id="59944-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="59944-122">Åpne den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="59944-122">Open the batch job.</span></span> <span data-ttu-id="59944-123">Klikk på **Jobb-IDen** for den satsvise jobben med aktiviteter som du vil avslutte.</span><span class="sxs-lookup"><span data-stu-id="59944-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="59944-124">I **satsvise oppgaver** velger du aktivitetene som skal avsluttes.</span><span class="sxs-lookup"><span data-stu-id="59944-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="59944-125">Klikk på **Endre status**, velg **Avbryt**, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="59944-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="59944-126">Klikk på **Avbryt** i hurtigfanen **Satsvise oppgaver**.</span><span class="sxs-lookup"><span data-stu-id="59944-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]