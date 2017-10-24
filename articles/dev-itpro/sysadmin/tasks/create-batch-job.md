--- 
title: Opprette en satsvis jobb
description: En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-batch-job"></a><span data-ttu-id="9a194-103">Opprette en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="9a194-103">Create a batch job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a194-104">En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.</span><span class="sxs-lookup"><span data-stu-id="9a194-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="9a194-105">Satsvise jobber kjøres med samme sikkerhetslegitimasjon som brukeren som opprettet jobben.</span><span class="sxs-lookup"><span data-stu-id="9a194-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="9a194-106">Bruk fremgangsmåten nedenfor til å opprette en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="9a194-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="9a194-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="9a194-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="9a194-108">Opprette den satsvise jobben</span><span class="sxs-lookup"><span data-stu-id="9a194-108">Create the batch job</span></span>
1. <span data-ttu-id="9a194-109">Gå til Systemadministrasjon > Forespørsler > Satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="9a194-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="9a194-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9a194-110">Click New.</span></span>
3. <span data-ttu-id="9a194-111">Skriv inn en verdi i Jobbeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="9a194-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="9a194-112">Angi en dato og et klokkeslett i feltet Planlagt startdato/-klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="9a194-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="9a194-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9a194-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="9a194-114">Opprette en gjentakelse</span><span class="sxs-lookup"><span data-stu-id="9a194-114">Create a recurrence</span></span>
1. <span data-ttu-id="9a194-115">Klikk Satsvis jobb i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9a194-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="9a194-116">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="9a194-116">Click Recurrence.</span></span>
    * <span data-ttu-id="9a194-117">Bruk disse alternativene for å angi et område og mønster for regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="9a194-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="9a194-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9a194-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="9a194-119">Legge til varsler</span><span class="sxs-lookup"><span data-stu-id="9a194-119">Add alerts</span></span>
1. <span data-ttu-id="9a194-120">Klikk Satsvis jobb i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9a194-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="9a194-121">Klikk Varsler.</span><span class="sxs-lookup"><span data-stu-id="9a194-121">Click Alerts.</span></span>
    * <span data-ttu-id="9a194-122">Angi om du vil at det skal sendes varslingsmeldinger når den satsvise jobben avsluttes, har en feil eller avbrytes.</span><span class="sxs-lookup"><span data-stu-id="9a194-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="9a194-123">Angi deretter om du vil at varslene skal vises som popup-meldinger.</span><span class="sxs-lookup"><span data-stu-id="9a194-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="9a194-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9a194-124">Click OK.</span></span>


