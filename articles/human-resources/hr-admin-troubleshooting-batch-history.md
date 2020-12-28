---
title: Optimalisere ytelsen med oppgaver for automatisk opprydding
description: Denne artikkelen beskriver hvordan du løser visse ytelsesproblemer med Microsoft Dynamics 365 Human Resources ved å rydde opp i loggen for satsvise jobber.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a983fde8ba393ab25f2b330014e04a1379f0e4d0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419840"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="94ebc-103">Optimalisere ytelsen med automatiske ryddeoppgaver</span><span class="sxs-lookup"><span data-stu-id="94ebc-103">Optimize performance with auto cleanup tasks</span></span>

<span data-ttu-id="94ebc-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="94ebc-104">**Issue**</span></span>

<span data-ttu-id="94ebc-105">Det kan oppstå ytelsesproblemer for Microsoft Dynamics 365 Human Resources hvis den loggen for satsvise jobber blir for stor.</span><span class="sxs-lookup"><span data-stu-id="94ebc-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="94ebc-106">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="94ebc-106">**Cause**</span></span>

<span data-ttu-id="94ebc-107">Satsvise jobber som kjører ofte, kan føre til uholdbar vekst i loggen for satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="94ebc-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="94ebc-108">Dette kan føre til ytelsesproblemer.</span><span class="sxs-lookup"><span data-stu-id="94ebc-108">This can cause performance issues.</span></span> 

<span data-ttu-id="94ebc-109">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="94ebc-109">**Resolution**</span></span>

<span data-ttu-id="94ebc-110">Planlegg en automatisk oppgave som skal rydde opp i loggen for satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="94ebc-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="94ebc-111">Vi anbefaler at du konfigurerer at oppgaven skal kjøre ukentlig, men du må kanskje kjøre oppryddingen oftere eller sjeldnere, avhengig av miljøet.</span><span class="sxs-lookup"><span data-stu-id="94ebc-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="94ebc-112">Fremgangsmåten nedenfor inneholder anbefalte innstillinger, men du kan endre disse i henhold til dine behov.</span><span class="sxs-lookup"><span data-stu-id="94ebc-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="94ebc-113">Velg **Systemadministrasjon** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="94ebc-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="94ebc-114">I **Søk**-feltet angir **Opprydding av historikk for satsvis jobb**.</span><span class="sxs-lookup"><span data-stu-id="94ebc-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Søk etter opprydding i logg for satsvis jobb](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="94ebc-116">Angi **30** i **Historikkgrense (dager)**.</span><span class="sxs-lookup"><span data-stu-id="94ebc-116">In **History limit (days)**, enter **30**.</span></span>

   ![Sett historikkgrense til 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="94ebc-118">Velg **Kjør i bakgrunnen**, og velg deretter **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="94ebc-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Angi regelmessighet](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="94ebc-120">Under **Definer regelmessighet** angir du **Startdato** og **Starttidspunkt** som skal utføres utenom arbeidstiden eller i helgen, og deretter velger du **INGEN SLUTTDATO**.</span><span class="sxs-lookup"><span data-stu-id="94ebc-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Definere startdato og -klokkeslettet for regelmessighet](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="94ebc-122">Under **MØNSTER FOR REGELMESSIGHET** velger du **Dager** og setter **GJENTA ETTER ANGITT INTERVALL** til **7**.</span><span class="sxs-lookup"><span data-stu-id="94ebc-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Sette opprydding til å gjentas ukentlig](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="94ebc-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="94ebc-124">Select **OK**.</span></span>

8. <span data-ttu-id="94ebc-125">Endre eventuelle andre parametere under **Kjør i bakgrunnen** etter behov, og velg deretter **OK.**</span><span class="sxs-lookup"><span data-stu-id="94ebc-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

