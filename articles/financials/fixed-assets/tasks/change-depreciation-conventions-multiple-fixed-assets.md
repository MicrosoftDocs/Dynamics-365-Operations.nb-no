--- 
title: Endre avskrivningskonvensjoner for flere anleggsmidler
description: Dette skjemaet oppdaterer avskrivningskonvensjonen for en angitt gruppe anleggsmidler.
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0f711d2e18a13ab972e548d3304652dee3f2e406
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="c3ae7-103">Endre avskrivningskonvensjoner for flere anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="c3ae7-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3ae7-104">Dette skjemaet oppdaterer avskrivningskonvensjonen for en angitt gruppe anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="c3ae7-105">Denne oppgaveveiledningen bruker USMF demo firmaet.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="c3ae7-106">Gå til Anleggsmidler > Periodiske oppgaver > Masseoppdatering</span><span class="sxs-lookup"><span data-stu-id="c3ae7-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="c3ae7-107">Klikk rullegardinknappen i feltet Avskrivningstablå for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c3ae7-108">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c3ae7-109">Angi en dato i feltet Plassert nær tjenestens start.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="c3ae7-110">Angi en dato i feltet Plassert nær tjenestens slutt.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="c3ae7-111">Bare anleggsmidler som hører inn under avskrivningstablået du valgte, og som er tatt i bruk, vil bli oppdatert.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="c3ae7-112">Velg et alternativ i feltet Gjeldende avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="c3ae7-113">Bare anleggsmidler som har den gjeldende avskrivningskonvensjonen, oppdateres.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="c3ae7-114">Velg et alternativ i feltet Ny avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="c3ae7-115">Bekreft at rapporten skrives ut på det valgte målet.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="c3ae7-116">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="c3ae7-117">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-117">Click Filter.</span></span>
10. <span data-ttu-id="c3ae7-118">Velg anleggsmiddelgruppen fra listen.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="c3ae7-119">Klikk rullegardinknappen i Kriterier-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="c3ae7-120">Velg ønsket anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="c3ae7-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c3ae7-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-122">Click OK.</span></span>
15. <span data-ttu-id="c3ae7-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-123">Click OK.</span></span>
    *  <span data-ttu-id="c3ae7-124">Resultatene av prosessen vises i masseoppdateringsrapporten.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-124">Results of the process are shown on the Mass update report.</span></span>     


