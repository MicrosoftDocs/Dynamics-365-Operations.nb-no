---
title: Tilbakestille satsvise jobber som står fast
description: Dette emnet beskriver hvordan du løser problemer med satsvise jobber som står fast.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 906a391b3c28d15445f6ddf0fc547ebcf842ba19
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881766"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="1d21f-103">Tilbakestille satsvise jobber som står fast</span><span class="sxs-lookup"><span data-stu-id="1d21f-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="1d21f-104">Problem</span><span class="sxs-lookup"><span data-stu-id="1d21f-104">Issue</span></span>

<span data-ttu-id="1d21f-105">Microsoft Dynamics 365 Human Resources kan oppleve problemer med satsvise jobber som står fast i enten en **Kjører** eller **Avbryter**-tilstand, og som ikke fullføres.</span><span class="sxs-lookup"><span data-stu-id="1d21f-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="1d21f-106">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="1d21f-106">Resolution</span></span>

<span data-ttu-id="1d21f-107">Når en satsvis jobb blir stående fast i en **Kjører**- eller **Avbryter**-tilstand, kan du tilbakestille statusen ved å fremtvingen at jobben avbrytes.</span><span class="sxs-lookup"><span data-stu-id="1d21f-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="1d21f-108">Når du har avbrutt den, kan du tilbakestille den satsvise jobben ved å angi den til **Venter**-status.</span><span class="sxs-lookup"><span data-stu-id="1d21f-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="1d21f-109">Deretter blir den plukket opp på nytt for utføring i neste planlagte satsvise kjøring.</span><span class="sxs-lookup"><span data-stu-id="1d21f-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="1d21f-110">I arbeidsområdet **Systemadministrasjon** velger du **Koblinger**-siden og velger deretter **Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="1d21f-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="1d21f-111">På listesiden **Satsvis jobb** velger du jobben som må tilbakestilles.</span><span class="sxs-lookup"><span data-stu-id="1d21f-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="1d21f-112">På handlingsbåndet velger du **Tving avbrudd**, og bekreft deretter handlingen.</span><span class="sxs-lookup"><span data-stu-id="1d21f-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="1d21f-113">Handlingen **Tving avbrudd** er bare tilgjengelig når den valgte satsvise jobben har statusen **Kjører** eller **Avbryter**, og ingen prosesser for satsvise kjøring eller avbrudd kjører for jobben.</span><span class="sxs-lookup"><span data-stu-id="1d21f-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="1d21f-114">På handlingsbåndet velger du **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="1d21f-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="1d21f-115">På siden **Velg ny status** velger du **Venter** og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="1d21f-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Velge en ny status for den satsvise jobben](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="1d21f-117">Se også</span><span class="sxs-lookup"><span data-stu-id="1d21f-117">See also</span></span>

[<span data-ttu-id="1d21f-118">Optimalisere ytelsen ved å planlegge satsvise jobber etter timer</span><span class="sxs-lookup"><span data-stu-id="1d21f-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="1d21f-119">Optimalisere ytelsen med oppgaver for automatisk opprydding</span><span class="sxs-lookup"><span data-stu-id="1d21f-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
