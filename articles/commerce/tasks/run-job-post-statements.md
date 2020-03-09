---
title: Konfigurere og kjøre jobben for å postere utdrag
description: Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å postere utdrag for en valgt butikk eller en gruppe med butikker.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09a47e268e271cf86e63ceff913435842f017bb5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023522"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="ff65f-103">Konfigurere og kjøre jobben for å postere utdrag</span><span class="sxs-lookup"><span data-stu-id="ff65f-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ff65f-104">Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å postere utdrag for en valgt butikk eller en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="ff65f-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="ff65f-105">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="ff65f-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ff65f-106">Gå til Alle arbeidsområder > ..</span><span class="sxs-lookup"><span data-stu-id="ff65f-106">Go to All workspaces > ..</span></span> <span data-ttu-id="ff65f-107">> Finans for butikk.</span><span class="sxs-lookup"><span data-stu-id="ff65f-107">> Store financials.</span></span>
2. <span data-ttu-id="ff65f-108">Klikk på Poster utdrag satsvis.</span><span class="sxs-lookup"><span data-stu-id="ff65f-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="ff65f-109">Velg et organisasjonshierarki, og velg deretter en enkelt butikk eller node i organisasjonsnodetreet.</span><span class="sxs-lookup"><span data-stu-id="ff65f-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="ff65f-110">Velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="ff65f-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ff65f-111">Klikk pilen for å legge til valget.</span><span class="sxs-lookup"><span data-stu-id="ff65f-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="ff65f-112">Klikk på kategorien Kjør i bakgrunnen. ![Kjør i bakgrunnen](../dev-itpro/media/runbackground.png "Kjør i bakgrunnen")</span><span class="sxs-lookup"><span data-stu-id="ff65f-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="ff65f-113">Merk av eller fjern merket for Satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="ff65f-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="ff65f-114">![Satsvis behandling](../dev-itpro/media/batchprocessing.png "Satsvis behandling og gjentakelse")</span><span class="sxs-lookup"><span data-stu-id="ff65f-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="ff65f-115">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="ff65f-115">Click Recurrence.</span></span>
6. <span data-ttu-id="ff65f-116">Angi en dato i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff65f-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="ff65f-117">Angi et tidspunkt i Starttidspunkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff65f-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="ff65f-118">Velg om du vil avslutte gjentakelsen etter et bestemt antall kjøringer, på en bestemt dato eller aldri.</span><span class="sxs-lookup"><span data-stu-id="ff65f-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="ff65f-119">Velg deretter de ulike alternativene for å definere hvor ofte du vil at jobben skal kjøres.</span><span class="sxs-lookup"><span data-stu-id="ff65f-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="ff65f-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ff65f-120">Click OK.</span></span>
9. <span data-ttu-id="ff65f-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ff65f-121">Click OK.</span></span>
