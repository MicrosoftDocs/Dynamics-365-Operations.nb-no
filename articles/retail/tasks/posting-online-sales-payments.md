--- 
title: Postering av elektroniske salg og betalinger
description: "Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="ea11e-103">Postering av elektroniske salg og betalinger</span><span class="sxs-lookup"><span data-stu-id="ea11e-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ea11e-104">Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ea11e-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="ea11e-105">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="ea11e-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ea11e-106">Gå til Alle arbeidsområder > Finans for detaljhandelsbutikk.</span><span class="sxs-lookup"><span data-stu-id="ea11e-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="ea11e-107">Klikk Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="ea11e-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="ea11e-108">Velg Detaljhandelbutikker etter område i Organisasjonshierarki-feltet.</span><span class="sxs-lookup"><span data-stu-id="ea11e-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="ea11e-109">Velg en bestemt nettbutikk eller velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="ea11e-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ea11e-110">Klikk pilen for å legge til valget.</span><span class="sxs-lookup"><span data-stu-id="ea11e-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="ea11e-111">Klikk fanen Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="ea11e-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="ea11e-112">Merk av eller fjern merket for Satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="ea11e-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="ea11e-113">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="ea11e-113">Click Recurrence.</span></span>
7. <span data-ttu-id="ea11e-114">Velg Ingen sluttdato.</span><span class="sxs-lookup"><span data-stu-id="ea11e-114">Select the No end date option.</span></span>
8. <span data-ttu-id="ea11e-115">Angi et tall i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="ea11e-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="ea11e-116">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ea11e-116">Click OK.</span></span>
10. <span data-ttu-id="ea11e-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ea11e-117">Click OK.</span></span>


