---
title: Opprette en satsvis jobb
description: En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562887"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="30d32-103">Opprette en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="30d32-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30d32-104">En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.</span><span class="sxs-lookup"><span data-stu-id="30d32-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="30d32-105">Satsvise jobber kjøres med samme sikkerhetslegitimasjon som brukeren som opprettet jobben.</span><span class="sxs-lookup"><span data-stu-id="30d32-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="30d32-106">Bruk fremgangsmåten nedenfor til å opprette en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="30d32-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="30d32-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="30d32-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="30d32-108">Opprette den satsvise jobben</span><span class="sxs-lookup"><span data-stu-id="30d32-108">Create the batch job</span></span>
1. <span data-ttu-id="30d32-109">Gå til Systemadministrasjon > Forespørsler > Satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="30d32-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="30d32-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="30d32-110">Click New.</span></span>
3. <span data-ttu-id="30d32-111">Skriv inn en verdi i Jobbeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="30d32-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="30d32-112">Angi en dato og et klokkeslett i feltet Planlagt startdato/-klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="30d32-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="30d32-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="30d32-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="30d32-114">Opprette en gjentakelse</span><span class="sxs-lookup"><span data-stu-id="30d32-114">Create a recurrence</span></span>
1. <span data-ttu-id="30d32-115">Klikk Satsvis jobb i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="30d32-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="30d32-116">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="30d32-116">Click Recurrence.</span></span>
    * <span data-ttu-id="30d32-117">Bruk disse alternativene for å angi et område og mønster for regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="30d32-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="30d32-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="30d32-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="30d32-119">Legge til varsler</span><span class="sxs-lookup"><span data-stu-id="30d32-119">Add alerts</span></span>
1. <span data-ttu-id="30d32-120">Klikk Satsvis jobb i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="30d32-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="30d32-121">Klikk Varsler.</span><span class="sxs-lookup"><span data-stu-id="30d32-121">Click Alerts.</span></span>
    * <span data-ttu-id="30d32-122">Angi om du vil at det skal sendes varslingsmeldinger når den satsvise jobben avsluttes, har en feil eller avbrytes.</span><span class="sxs-lookup"><span data-stu-id="30d32-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="30d32-123">Angi deretter om du vil at varslene skal vises som popup-meldinger.</span><span class="sxs-lookup"><span data-stu-id="30d32-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="30d32-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="30d32-124">Click OK.</span></span>

