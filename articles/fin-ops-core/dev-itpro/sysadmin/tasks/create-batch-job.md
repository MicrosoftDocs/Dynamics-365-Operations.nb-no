---
title: Opprette en satsvis jobb
description: En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4360cd7068658a170f5b44c2ce7c71c39c44fa8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679894"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="e6b7c-103">Opprette en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="e6b7c-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6b7c-104">En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="e6b7c-105">Satsvise jobber kjøres med samme sikkerhetslegitimasjon som brukeren som opprettet jobben.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="e6b7c-106">Bruk fremgangsmåten nedenfor til å opprette en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="e6b7c-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="e6b7c-108">Opprette den satsvise jobben</span><span class="sxs-lookup"><span data-stu-id="e6b7c-108">Create the batch job</span></span>
1. <span data-ttu-id="e6b7c-109">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Forespørsler > Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="e6b7c-110">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-110">Click **New**.</span></span>
3. <span data-ttu-id="e6b7c-111">Skriv inn en verdi i **Jobbeskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="e6b7c-112">Angi en dato og et klokkeslett i feltet **Planlagt startdato/-klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="e6b7c-113">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="e6b7c-114">Opprette en gjentakelse</span><span class="sxs-lookup"><span data-stu-id="e6b7c-114">Create a recurrence</span></span>
1. <span data-ttu-id="e6b7c-115">Klikk på **Satsvis jobb** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="e6b7c-116">Klikk på **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-116">Click **Recurrence**.</span></span> <span data-ttu-id="e6b7c-117">Bruk disse alternativene for å angi et område og mønster for regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="e6b7c-118">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="e6b7c-119">Legge til varsler</span><span class="sxs-lookup"><span data-stu-id="e6b7c-119">Add alerts</span></span>
1. <span data-ttu-id="e6b7c-120">Klikk på **Satsvis jobb** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="e6b7c-121">Klikk på **Varsler**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-121">Click **Alerts**.</span></span> <span data-ttu-id="e6b7c-122">Angi om du vil at det skal sendes varslingsmeldinger når den satsvise jobben avsluttes, har en feil eller avbrytes.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="e6b7c-123">Angi deretter om du vil at varslene skal vises som popup-meldinger.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="e6b7c-124">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="e6b7c-125">Justere status for satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="e6b7c-125">Adjust batch job status</span></span>
1. <span data-ttu-id="e6b7c-126">Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="e6b7c-127">Velg den riktige satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="e6b7c-128">Klikk på **Satsvis jobb > Funksjoner > Endre status** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="e6b7c-129">Velg den aktuelle statusen:</span><span class="sxs-lookup"><span data-stu-id="e6b7c-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="e6b7c-130">**Trekk tilbake**: Angi **tilbakeholdt** for den satsvise jobben, slik at den holdes tilbake fra planleggeren for satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="e6b7c-131">Tilsvarer *stopp*.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="e6b7c-132">**Venter**: Angi **venter** for den satsvise jobben, slik at den venter på å bli hentet av planleggeren for satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="e6b7c-133">Tilsvarer *start*.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="e6b7c-134">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6b7c-134">Click **OK**.</span></span>
