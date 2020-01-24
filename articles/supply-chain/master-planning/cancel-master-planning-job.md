---
title: Avbryte en hovedplanleggingsjobb
description: Dette emnet beskriver hvordan du avbryter en aktiv planleggingsjobb som bruker innebygd planleggingfunksjonalitet.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 66d5b10e1471b98274d4049df18a2e53873f789a
ms.sourcegitcommit: 92cd55028be556a0bd41b6972c9c6d14b695dfa0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947486"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="9cf8f-103">Avbryte en hovedplanleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="9cf8f-103">Cancel a master planning job</span></span>

<span data-ttu-id="9cf8f-104">I Microsoft Dynamics 365 Supply Chain Management finnes det flere alternativer for å avbryte en hovedplanleggingjobb.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="9cf8f-105">Det kan for eksempel hende at du vil avbryte en hovedplanleggingsjobb hvis den ble startet ved en feiltakelse eller kjører lenger tid enn forventet, og du vil avslutte den.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="9cf8f-106">Den beste måten å avbryte en planleggingsjobb på, er fra siden **Uferdige planleggingsprosesser**.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="9cf8f-107">Alternative valg fra sidene **satsvise jobber** og **satsvise jobber utvidet** bør bare brukes hvis avbrytelse av hovedplanleggingsjobben fra siden **Uferdige planleggingsprosesser** ikke ble fullført i løpet av få minutter.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="9cf8f-108">Foretrukket avbruddsalternativ</span><span class="sxs-lookup"><span data-stu-id="9cf8f-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="9cf8f-109">Avbryte hovedplanleggingsjobb fra siden **Uferdige planleggingsprosesser**</span><span class="sxs-lookup"><span data-stu-id="9cf8f-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="9cf8f-110">Gå til **Hovedplanlegging > Forespørsler og rapporter > Hovedplanlegging > Uferdige planleggingsprosesser**.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="9cf8f-111">Velg linjen med reparasjonen planleggingsprosessen du ønsker å avbryte.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="9cf8f-112">Klikk på **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="9cf8f-113">Flere avbruddsalternativer</span><span class="sxs-lookup"><span data-stu-id="9cf8f-113">Additional cancel options</span></span>
<span data-ttu-id="9cf8f-114">Disse bør bare brukes hvis avbrytelse av hovedplanleggingsjobben fra siden **Uferdige planleggingsprosesser** ikke ble fullført i løpet av få minutter.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-114">These should only be used iif cancelin the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="9cf8f-115">Slette hovedplanleggingsjobb fra siden **satsvise jobber**</span><span class="sxs-lookup"><span data-stu-id="9cf8f-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="9cf8f-116">Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="9cf8f-117">Velg linjen med planleggingsjobben du ønsker å slette.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="9cf8f-118">Klikk **Slett**.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="9cf8f-119">Avbryte oppgave for hovedplanleggingsjobb fra siden **satsvise jobber utvidet**</span><span class="sxs-lookup"><span data-stu-id="9cf8f-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="9cf8f-120">Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="9cf8f-121">Hvis jobb-IDen ikke vises i listen, klikker du **Bytt til utvidet skjema**, ellers fortsetter du med neste trinn.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="9cf8f-122">Åpne den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-122">Open the batch job.</span></span> <span data-ttu-id="9cf8f-123">Klikk **Jobb-IDen** for den satsvise jobben med aktiviteter som du vil avslutte.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="9cf8f-124">I **satsvise oppgaver** velger du aktivitetene som skal avsluttes.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="9cf8f-125">Klikk **Avbryt** i hurtigfanen **Satsvise oppgaver**.</span><span class="sxs-lookup"><span data-stu-id="9cf8f-125">On the **Batch tasks** FastTab, click **Abort**.</span></span>
