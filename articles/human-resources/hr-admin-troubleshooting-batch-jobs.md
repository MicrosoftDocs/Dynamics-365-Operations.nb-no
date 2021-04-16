---
title: Optimalisere ytelsen ved å planlegge satsvise jobber utenom arbeidstid
description: Dette emnet beskriver hvordan du løser ytelsesproblemer med Microsoft Dynamics 365 Human Resources ved å planlegge tidkrevende satsvise jobber utenom arbeidstid.
author: andreabichsel
ms.date: 06/23/2020
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
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 92dd281ed718be5c7ebd843d015c108ee121f30a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794931"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="788be-103">Optimalisere ytelsen ved å planlegge satsvise jobber utenom arbeidstid</span><span class="sxs-lookup"><span data-stu-id="788be-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="788be-104">Avgang</span><span class="sxs-lookup"><span data-stu-id="788be-104">Issue</span></span>

<span data-ttu-id="788be-105">Microsoft Dynamics 365 Human Resources kan oppleve ytelsesproblemer hvis tidkrevende satsvise jobber kjøres i arbeidstiden.</span><span class="sxs-lookup"><span data-stu-id="788be-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="788be-106">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="788be-106">Resolution</span></span>

<span data-ttu-id="788be-107">Planlegg følgende satsvise jobber utenom arbeidstid.</span><span class="sxs-lookup"><span data-stu-id="788be-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="788be-108">Det anbefales også å se gjennom frekvensen for satsvise jobber som kjører ofte.</span><span class="sxs-lookup"><span data-stu-id="788be-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="788be-109">Reduser gjentakelsen av den satsvise jobben hvis mulig.</span><span class="sxs-lookup"><span data-stu-id="788be-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="788be-110">I mange tilfeller er standardfrekvensen tilstrekkelig.</span><span class="sxs-lookup"><span data-stu-id="788be-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="788be-111">Følgende satsvise jobber bør kjøres om kvelden eller utenom arbeidstid.</span><span class="sxs-lookup"><span data-stu-id="788be-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="788be-112">Pass på at du kontrollerer tidssonen for disse gjentakende satsvise jobbene.</span><span class="sxs-lookup"><span data-stu-id="788be-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="788be-113">Noen satsvise jobber kan bruke Stillehavskysten (normaltid).</span><span class="sxs-lookup"><span data-stu-id="788be-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="788be-114">Satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="788be-114">Batch job</span></span> | <span data-ttu-id="788be-115">Standardfrekvens</span><span class="sxs-lookup"><span data-stu-id="788be-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="788be-116">Opprydding i logg for satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="788be-116">Batch job history cleanup</span></span> | <span data-ttu-id="788be-117">1 gang per måned</span><span class="sxs-lookup"><span data-stu-id="788be-117">1 time per month</span></span> |
| <span data-ttu-id="788be-118">Eksporter opprydding i oppsamling</span><span class="sxs-lookup"><span data-stu-id="788be-118">Export staging cleanup</span></span> | <span data-ttu-id="788be-119">1 gang per dag</span><span class="sxs-lookup"><span data-stu-id="788be-119">1 time per day</span></span> |
| <span data-ttu-id="788be-120">Manglende forespørselssynkronisering for Common Data Service-integrering</span><span class="sxs-lookup"><span data-stu-id="788be-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="788be-121">1 gang per dag</span><span class="sxs-lookup"><span data-stu-id="788be-121">1 time per day</span></span> |
| <span data-ttu-id="788be-122">Systemjobb for databasekomprimering som må kjøres regelmessig utenom arbeidstid</span><span class="sxs-lookup"><span data-stu-id="788be-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="788be-123">1 gang per dag</span><span class="sxs-lookup"><span data-stu-id="788be-123">1 time per day</span></span> |
| <span data-ttu-id="788be-124">Systemjobb for databaseindeksgjenoppbygging som må kjøres regelmessig utenom arbeidstid</span><span class="sxs-lookup"><span data-stu-id="788be-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="788be-125">1 gang per dag</span><span class="sxs-lookup"><span data-stu-id="788be-125">1 time per day</span></span> |

1. <span data-ttu-id="788be-126">Velg **Systemadministrasjon** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="788be-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="788be-127">I **Søk**-feltet søker du etter en av de satsvise jobbene ovenfor.</span><span class="sxs-lookup"><span data-stu-id="788be-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="788be-128">Velg **Kjør i bakgrunnen**, og velg deretter **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="788be-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Angi regelmessighet](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="788be-130">Under **Definer regelmessighet** angir du **Startdato** og **Starttidspunkt** som skal utføres utenom arbeidstiden eller i helgen.</span><span class="sxs-lookup"><span data-stu-id="788be-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="788be-131">Velg **Ingen sluttdato**.</span><span class="sxs-lookup"><span data-stu-id="788be-131">Select **No end date**.</span></span> 

   ![Definere startdato og -klokkeslettet for regelmessighet](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="788be-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="788be-133">Select **OK**.</span></span>

6. <span data-ttu-id="788be-134">Endre eventuelle andre parametere under **Kjør i bakgrunnen** etter behov, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="788be-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="788be-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="788be-135">Additional resources</span></span>

[<span data-ttu-id="788be-136">Optimalisere ytelsen med oppgaver for automatisk opprydding</span><span class="sxs-lookup"><span data-stu-id="788be-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]