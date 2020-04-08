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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6eee5c6dd7daf2b0c79dd34d15a7dde919bdd60
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143679"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="eee04-103">Opprette en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="eee04-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eee04-104">En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.</span><span class="sxs-lookup"><span data-stu-id="eee04-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="eee04-105">Satsvise jobber kjøres med samme sikkerhetslegitimasjon som brukeren som opprettet jobben.</span><span class="sxs-lookup"><span data-stu-id="eee04-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="eee04-106">Bruk fremgangsmåten nedenfor til å opprette en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="eee04-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="eee04-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="eee04-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="eee04-108">Opprette den satsvise jobben</span><span class="sxs-lookup"><span data-stu-id="eee04-108">Create the batch job</span></span>
1. <span data-ttu-id="eee04-109">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Forespørsler > Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="eee04-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="eee04-110">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="eee04-110">Click **New**.</span></span>
3. <span data-ttu-id="eee04-111">Skriv inn en verdi i **Jobbeskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="eee04-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="eee04-112">Angi en dato og et klokkeslett i feltet **Planlagt startdato/-klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="eee04-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="eee04-113">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="eee04-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="eee04-114">Opprette en gjentakelse</span><span class="sxs-lookup"><span data-stu-id="eee04-114">Create a recurrence</span></span>
1. <span data-ttu-id="eee04-115">Klikk på **Satsvis jobb** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eee04-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="eee04-116">Klikk på **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="eee04-116">Click **Recurrence**.</span></span> <span data-ttu-id="eee04-117">Bruk disse alternativene for å angi et område og mønster for regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="eee04-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="eee04-118">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="eee04-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="eee04-119">Legge til varsler</span><span class="sxs-lookup"><span data-stu-id="eee04-119">Add alerts</span></span>
1. <span data-ttu-id="eee04-120">Klikk på **Satsvis jobb** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eee04-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="eee04-121">Klikk på **Varsler**.</span><span class="sxs-lookup"><span data-stu-id="eee04-121">Click **Alerts**.</span></span> <span data-ttu-id="eee04-122">Angi om du vil at det skal sendes varslingsmeldinger når den satsvise jobben avsluttes, har en feil eller avbrytes.</span><span class="sxs-lookup"><span data-stu-id="eee04-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="eee04-123">Angi deretter om du vil at varslene skal vises som popup-meldinger.</span><span class="sxs-lookup"><span data-stu-id="eee04-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="eee04-124">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="eee04-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="eee04-125">Justere status for satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="eee04-125">Adjust batch job status</span></span>
1. <span data-ttu-id="eee04-126">Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="eee04-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="eee04-127">Velg den riktige satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="eee04-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="eee04-128">Klikk på **Satsvis jobb > Funksjoner > Endre status** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eee04-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="eee04-129">Velg den aktuelle statusen:</span><span class="sxs-lookup"><span data-stu-id="eee04-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="eee04-130">**Trekk tilbake**: Angi **tilbakeholdt** for den satsvise jobben, slik at den holdes tilbake fra planleggeren for satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="eee04-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="eee04-131">Tilsvarer *stopp*.</span><span class="sxs-lookup"><span data-stu-id="eee04-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="eee04-132">**Venter**: Angi **venter** for den satsvise jobben, slik at den venter på å bli hentet av planleggeren for satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="eee04-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="eee04-133">Tilsvarer *start*.</span><span class="sxs-lookup"><span data-stu-id="eee04-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="eee04-134">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="eee04-134">Click **OK**.</span></span>
