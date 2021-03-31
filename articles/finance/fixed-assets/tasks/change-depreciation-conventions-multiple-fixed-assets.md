---
title: Endre avskrivningskonvensjoner for flere anleggsmidler
description: Dette skjemaet oppdaterer avskrivningskonvensjonen for en angitt gruppe anleggsmidler.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c64e4f7117c4ca70236a02b4d36a88e9f2a9906
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210029"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="cf884-103">Endre avskrivningskonvensjoner for flere anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="cf884-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf884-104">Dette skjemaet oppdaterer avskrivningskonvensjonen for en angitt gruppe anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="cf884-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="cf884-105">Denne oppgaveveiledningen bruker USMF demo firmaet.</span><span class="sxs-lookup"><span data-stu-id="cf884-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="cf884-106">Gå til Anleggsmidler > Periodiske oppgaver > Masseoppdatering</span><span class="sxs-lookup"><span data-stu-id="cf884-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="cf884-107">Klikk rullegardinknappen i feltet Avskrivningstablå for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="cf884-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cf884-108">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cf884-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cf884-109">Angi en dato i feltet Plassert nær tjenestens start.</span><span class="sxs-lookup"><span data-stu-id="cf884-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="cf884-110">Angi en dato i feltet Plassert nær tjenestens slutt.</span><span class="sxs-lookup"><span data-stu-id="cf884-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="cf884-111">Bare anleggsmidler som hører inn under avskrivningstablået du valgte, og som er tatt i bruk, vil bli oppdatert.</span><span class="sxs-lookup"><span data-stu-id="cf884-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="cf884-112">Velg et alternativ i feltet Gjeldende avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="cf884-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="cf884-113">Bare anleggsmidler som har den gjeldende avskrivningskonvensjonen, oppdateres.</span><span class="sxs-lookup"><span data-stu-id="cf884-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="cf884-114">Velg et alternativ i feltet Ny avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="cf884-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="cf884-115">Bekreft at rapporten skrives ut på det valgte målet.</span><span class="sxs-lookup"><span data-stu-id="cf884-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="cf884-116">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="cf884-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="cf884-117">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="cf884-117">Click Filter.</span></span>
10. <span data-ttu-id="cf884-118">Velg anleggsmiddelgruppen fra listen.</span><span class="sxs-lookup"><span data-stu-id="cf884-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="cf884-119">Klikk rullegardinknappen i Kriterier-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="cf884-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="cf884-120">Velg ønsket anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="cf884-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="cf884-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cf884-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="cf884-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="cf884-122">Click OK.</span></span>
15. <span data-ttu-id="cf884-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="cf884-123">Click OK.</span></span>
    *  <span data-ttu-id="cf884-124">Resultatene av prosessen vises i masseoppdateringsrapporten.</span><span class="sxs-lookup"><span data-stu-id="cf884-124">Results of the process are shown on the Mass update report.</span></span>     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]