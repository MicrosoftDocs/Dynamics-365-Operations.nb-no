---
title: Optimalisere ytelsen ved å planlegge satsvise jobber utenom arbeidstid
description: Dette emnet beskriver hvordan du løser ytelsesproblemer med Microsoft Dynamics 365 Human Resources ved å planlegge tidkrevende satsvise jobber utenom arbeidstid.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500511"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="6ace0-103">Optimalisere ytelsen ved å planlegge satsvise jobber utenom arbeidstid</span><span class="sxs-lookup"><span data-stu-id="6ace0-103">Optimize performance by scheduling batch jobs after hours</span></span>

## <a name="issue"></a><span data-ttu-id="6ace0-104">Avgang</span><span class="sxs-lookup"><span data-stu-id="6ace0-104">Issue</span></span>

<span data-ttu-id="6ace0-105">Microsoft Dynamics 365 Human Resources kan oppleve ytelsesproblemer hvis tidkrevende satsvise jobber kjøres i arbeidstiden.</span><span class="sxs-lookup"><span data-stu-id="6ace0-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="6ace0-106">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="6ace0-106">Resolution</span></span>

<span data-ttu-id="6ace0-107">Planlegg følgende satsvise jobber utenom arbeidstid.</span><span class="sxs-lookup"><span data-stu-id="6ace0-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="6ace0-108">Vi anbefaler også å se gjennom frekvensen for satsvise jobber som kjører ofte.</span><span class="sxs-lookup"><span data-stu-id="6ace0-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="6ace0-109">Reduser gjentakelsen av den satsvise jobben hvis mulig.</span><span class="sxs-lookup"><span data-stu-id="6ace0-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="6ace0-110">I mange tilfeller er standardfrekvensen tilstrekkelig.</span><span class="sxs-lookup"><span data-stu-id="6ace0-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="6ace0-111">Følgende satsvise jobber bør kjøres om kvelden eller utenom arbeidstid.</span><span class="sxs-lookup"><span data-stu-id="6ace0-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="6ace0-112">Pass på at du kontrollerer tidssonen for disse gjentakende satsvise jobbene.</span><span class="sxs-lookup"><span data-stu-id="6ace0-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="6ace0-113">Noen satsvise jobber kan bruke Stillehavskysten (normaltid).</span><span class="sxs-lookup"><span data-stu-id="6ace0-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="6ace0-114">Satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="6ace0-114">Batch job</span></span> | <span data-ttu-id="6ace0-115">Standardfrekvens</span><span class="sxs-lookup"><span data-stu-id="6ace0-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="6ace0-116">Opprydding i logg for satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="6ace0-116">Batch job history cleanup</span></span> | <span data-ttu-id="6ace0-117">1 gang per måned</span><span class="sxs-lookup"><span data-stu-id="6ace0-117">1 time per month</span></span> |
| <span data-ttu-id="6ace0-118">Eksporter opprydding i oppsamling</span><span class="sxs-lookup"><span data-stu-id="6ace0-118">Export staging cleanup</span></span> | <span data-ttu-id="6ace0-119">1 gang per dag</span><span class="sxs-lookup"><span data-stu-id="6ace0-119">1 time per day</span></span> |
| <span data-ttu-id="6ace0-120">Manglende forespørselssynkronisering for Common Data Service-integrering</span><span class="sxs-lookup"><span data-stu-id="6ace0-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="6ace0-121">1 gang per dag</span><span class="sxs-lookup"><span data-stu-id="6ace0-121">1 time per day</span></span> |
| <span data-ttu-id="6ace0-122">Systemjobb for databasekomprimering som må kjøres regelmessig utenom arbeidstid</span><span class="sxs-lookup"><span data-stu-id="6ace0-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="6ace0-123">1 gang per dag</span><span class="sxs-lookup"><span data-stu-id="6ace0-123">1 time per day</span></span> |
| <span data-ttu-id="6ace0-124">Systemjobb for databaseindeksgjenoppbygging som må kjøres regelmessig utenom arbeidstid</span><span class="sxs-lookup"><span data-stu-id="6ace0-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="6ace0-125">1 gang per dag</span><span class="sxs-lookup"><span data-stu-id="6ace0-125">1 time per day</span></span> |

1. <span data-ttu-id="6ace0-126">Velg **Systemadministrasjon**i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6ace0-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="6ace0-127">I **Søk**-feltet søker du etter en av de satsvise jobbene ovenfor.</span><span class="sxs-lookup"><span data-stu-id="6ace0-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="6ace0-128">Velg **Kjør i bakgrunnen**, og velg deretter **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="6ace0-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Angi regelmessighet](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="6ace0-130">Under **Definer regelmessighet** angir du **Startdato** og **Starttidspunkt** som skal utføres utenom arbeidstiden eller i helgen.</span><span class="sxs-lookup"><span data-stu-id="6ace0-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="6ace0-131">Velg **Ingen sluttdato**.</span><span class="sxs-lookup"><span data-stu-id="6ace0-131">Select **No end date**.</span></span> 

   ![Definere startdato og -klokkeslettet for regelmessighet](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="6ace0-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ace0-133">Select **OK**.</span></span>

6. <span data-ttu-id="6ace0-134">Endre eventuelle andre parametere under **Kjør i bakgrunnen** etter behov, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ace0-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ace0-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6ace0-135">Additional resources</span></span>

[<span data-ttu-id="6ace0-136">Optimalisere ytelsen med oppgaver for automatisk opprydding</span><span class="sxs-lookup"><span data-stu-id="6ace0-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
