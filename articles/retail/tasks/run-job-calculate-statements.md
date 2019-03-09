---
title: Konfigurere og kjøre jobb for å beregne utdrag
description: Denne prosedyren hjelper med å konfigurere og kjøre gjentakende satsvise jobber for å opprette og beregne utdrag for en valgt butikk eller en gruppe med butikker.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "365184"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="e8469-103">Konfigurere og kjøre jobb for å beregne utdrag</span><span class="sxs-lookup"><span data-stu-id="e8469-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e8469-104">Denne prosedyren hjelper med å konfigurere og kjøre gjentakende satsvise jobber for å opprette og beregne utdrag for en valgt butikk eller en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="e8469-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="e8469-105">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="e8469-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e8469-106">Gå til Alle arbeidsområder > Finans for detaljhandelsbutikk.</span><span class="sxs-lookup"><span data-stu-id="e8469-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="e8469-107">Klikk Beregn utdrag.</span><span class="sxs-lookup"><span data-stu-id="e8469-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="e8469-108">Velg en bestemt butikk eller en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="e8469-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="e8469-109">Klikk pilen for å legge til valget.</span><span class="sxs-lookup"><span data-stu-id="e8469-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="e8469-110">Klikk fanen Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="e8469-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="e8469-111">Velg Ja under Satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="e8469-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="e8469-112">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="e8469-112">Click Recurrence.</span></span>
6. <span data-ttu-id="e8469-113">Angi en dato i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="e8469-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="e8469-114">Angi et tidspunkt i Starttidspunkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="e8469-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="e8469-115">Velg Ingen sluttdato.</span><span class="sxs-lookup"><span data-stu-id="e8469-115">Select the No end date option.</span></span>
9. <span data-ttu-id="e8469-116">Angi Dager i PatternUnit-feltet.</span><span class="sxs-lookup"><span data-stu-id="e8469-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="e8469-117">Angi et tall i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="e8469-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="e8469-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e8469-118">Click OK.</span></span>
12. <span data-ttu-id="e8469-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e8469-119">Click OK.</span></span>

