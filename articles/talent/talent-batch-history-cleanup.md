---
title: Optimalisere ytelsen med automatiske ryddeoppgaver
description: Dette emnet beskriver hvordan du løser visse ytelsesproblemer med Microsoft Dynamics 365 Talent ved å rydde opp i loggen for satsvise jobber.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a053c9094151f4e12e4aadc533dd272258779540
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832588"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="b5729-103">Optimalisere ytelsen med automatiske ryddeoppgaver</span><span class="sxs-lookup"><span data-stu-id="b5729-103">Optimize performance with auto cleanup tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b5729-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="b5729-104">**Issue**</span></span>

<span data-ttu-id="b5729-105">Det kan oppstå ytelsesproblemer for Microsoft Dynamics 365 Talent hvis den loggen for satsvise jobber blir for stor.</span><span class="sxs-lookup"><span data-stu-id="b5729-105">Microsoft Dynamics 365 Talent can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="b5729-106">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="b5729-106">**Cause**</span></span>

<span data-ttu-id="b5729-107">Satsvise jobber som kjører ofte, kan føre til uholdbar vekst i loggen for satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="b5729-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="b5729-108">Dette kan føre til ytelsesproblemer.</span><span class="sxs-lookup"><span data-stu-id="b5729-108">This can cause performance issues.</span></span> 

<span data-ttu-id="b5729-109">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="b5729-109">**Resolution**</span></span>

<span data-ttu-id="b5729-110">Planlegg en automatisk oppgave som skal rydde opp i loggen for satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="b5729-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="b5729-111">Vi anbefaler at du konfigurerer at oppgaven skal kjøre ukentlig, men du må kanskje kjøre oppryddingen oftere eller sjeldnere, avhengig av miljøet.</span><span class="sxs-lookup"><span data-stu-id="b5729-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="b5729-112">Fremgangsmåten nedenfor inneholder anbefalte innstillinger, men du kan endre disse i henhold til dine behov.</span><span class="sxs-lookup"><span data-stu-id="b5729-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="b5729-113">Velg **Systemadministrasjon** i Talent.</span><span class="sxs-lookup"><span data-stu-id="b5729-113">In Talent, select **System administration**.</span></span>

2. <span data-ttu-id="b5729-114">I **Søk**-feltet angir **Opprydding av historikk for satsvis jobb**.</span><span class="sxs-lookup"><span data-stu-id="b5729-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Søk etter opprydding i logg for satsvis jobb](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="b5729-116">Angi **30** i **Historikkgrense (dager)**.</span><span class="sxs-lookup"><span data-stu-id="b5729-116">In **History limit (days)**, enter **30**.</span></span>

   ![Sett historikkgrense til 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="b5729-118">Velg **Kjør i bakgrunnen**, og velg deretter **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="b5729-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Angi regelmessighet](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="b5729-120">Under **Definer regelmessighet** angir du **Startdato** og **Starttidspunkt** som skal utføres utenom arbeidstiden eller i helgen, og deretter velger du **INGEN SLUTTDATO**.</span><span class="sxs-lookup"><span data-stu-id="b5729-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Definere startdato og -klokkeslettet for regelmessighet](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="b5729-122">Under **MØNSTER FOR REGELMESSIGHET** velger du **Dager** og setter **GJENTA ETTER ANGITT INTERVALL** til **7**.</span><span class="sxs-lookup"><span data-stu-id="b5729-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Sette opprydding til å gjentas ukentlig](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="b5729-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5729-124">Select **OK**.</span></span>

8. <span data-ttu-id="b5729-125">Endre eventuelle andre parametere under **Kjør i bakgrunnen** etter behov, og velg deretter **OK.**</span><span class="sxs-lookup"><span data-stu-id="b5729-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

