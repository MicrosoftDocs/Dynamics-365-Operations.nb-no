--- 
title: " Konfigurere og kjøre en jobb for å postere utdrag"
description: "Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å postere utdrag for en valgt butikk eller en gruppe med butikker."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 564f628ff082887a0f6476ded76c13d2824abf08
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="9afb0-103"> Konfigurere og kjøre en jobb for å postere utdrag</span><span class="sxs-lookup"><span data-stu-id="9afb0-103">Configure and run a job to post statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9afb0-104">Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å postere utdrag for en valgt butikk eller en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="9afb0-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="9afb0-105">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="9afb0-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9afb0-106">Gå til Alle arbeidsområder > ..</span><span class="sxs-lookup"><span data-stu-id="9afb0-106">Go to All workspaces > ..</span></span> <span data-ttu-id="9afb0-107">> Finans for detaljhandelsbutikk.</span><span class="sxs-lookup"><span data-stu-id="9afb0-107">> Retail store financials.</span></span>
2. <span data-ttu-id="9afb0-108">Klikk Poster utdrag.</span><span class="sxs-lookup"><span data-stu-id="9afb0-108">Click Post statements.</span></span>
    * <span data-ttu-id="9afb0-109">Velg et organisasjonshierarki, og velg deretter en enkelt butikk eller node i organisasjonsnodetreet.</span><span class="sxs-lookup"><span data-stu-id="9afb0-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="9afb0-110">Velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="9afb0-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="9afb0-111">Klikk pilen for å legge til valget.</span><span class="sxs-lookup"><span data-stu-id="9afb0-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="9afb0-112">Klikk fanen Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="9afb0-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="9afb0-113">Merk av eller fjern merket for Satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="9afb0-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="9afb0-114">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="9afb0-114">Click Recurrence.</span></span>
6. <span data-ttu-id="9afb0-115">Angi en dato i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="9afb0-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="9afb0-116">Angi et tidspunkt i Starttidspunkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="9afb0-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="9afb0-117">Velg om du vil avslutte gjentakelsen etter et bestemt antall kjøringer, på en bestemt dato eller aldri.</span><span class="sxs-lookup"><span data-stu-id="9afb0-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="9afb0-118">Velg deretter de ulike alternativene for å definere hvor ofte du vil at jobben skal kjøres.</span><span class="sxs-lookup"><span data-stu-id="9afb0-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="9afb0-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9afb0-119">Click OK.</span></span>
9. <span data-ttu-id="9afb0-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9afb0-120">Click OK.</span></span>


