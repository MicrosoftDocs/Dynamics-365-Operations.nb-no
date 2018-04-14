--- 
title: " Postere elektroniske salg og betalinger"
description: "Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner."
author: jashanno
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
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b1ec55edb0799ff141c77575ce53ab0313d9cca9
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="811f0-103"> Postere elektroniske salg og betalinger</span><span class="sxs-lookup"><span data-stu-id="811f0-103">Post online sales and payments</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="811f0-104">Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="811f0-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="811f0-105">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="811f0-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="811f0-106">Gå til Alle arbeidsområder > Finans for detaljhandelsbutikk.</span><span class="sxs-lookup"><span data-stu-id="811f0-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="811f0-107">Klikk Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="811f0-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="811f0-108">Velg Detaljhandelbutikker etter område i Organisasjonshierarki-feltet.</span><span class="sxs-lookup"><span data-stu-id="811f0-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="811f0-109">Velg en bestemt nettbutikk eller velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="811f0-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="811f0-110">Klikk pilen for å legge til valget.</span><span class="sxs-lookup"><span data-stu-id="811f0-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="811f0-111">Klikk fanen Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="811f0-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="811f0-112">Merk av eller fjern merket for Satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="811f0-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="811f0-113">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="811f0-113">Click Recurrence.</span></span>
7. <span data-ttu-id="811f0-114">Velg Ingen sluttdato.</span><span class="sxs-lookup"><span data-stu-id="811f0-114">Select the No end date option.</span></span>
8. <span data-ttu-id="811f0-115">Angi et tall i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="811f0-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="811f0-116">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="811f0-116">Click OK.</span></span>
10. <span data-ttu-id="811f0-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="811f0-117">Click OK.</span></span>


