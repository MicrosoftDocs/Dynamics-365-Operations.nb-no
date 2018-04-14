--- 
title: "Definere avskrivningstablåer "
description: "Denne oppgaveveiledningen oppretter et nytt avskrivningstablå og knytter den til en anleggsmiddelgruppe."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 264e671774a1be03f4529339990d4727d20f6d38
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-depreciation-books"></a><span data-ttu-id="8967c-103">Definere avskrivningstablåer </span><span class="sxs-lookup"><span data-stu-id="8967c-103">Set up depreciation books</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8967c-104">Denne oppgaveveiledningen oppretter et nytt avskrivningstablå og knytter den til en anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="8967c-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="8967c-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="8967c-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="8967c-106">Opprette et avskrivningstablå</span><span class="sxs-lookup"><span data-stu-id="8967c-106">Create a depreciation book</span></span>
1. <span data-ttu-id="8967c-107">Gå til Anleggsmidler > Oppsett > Avskrivningstablåer.</span><span class="sxs-lookup"><span data-stu-id="8967c-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="8967c-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8967c-108">Click New.</span></span>
3. <span data-ttu-id="8967c-109">Skriv inn en verdi i feltet Avskrivningstablå.</span><span class="sxs-lookup"><span data-stu-id="8967c-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="8967c-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8967c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8967c-111">Merk av eller fjern merket i boksen Beregn avskrivning.</span><span class="sxs-lookup"><span data-stu-id="8967c-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="8967c-112">Klikk rullegardinknappen i feltet Avskrivningsprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8967c-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8967c-113">Finn og velg ønsket avskrivningsprofil i listen.</span><span class="sxs-lookup"><span data-stu-id="8967c-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="8967c-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8967c-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8967c-115">Klikk rullegardinknappen i feltet Alternativ avskrivningsprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8967c-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="8967c-116">Velg ønsket avskrivningsprofil i listen.</span><span class="sxs-lookup"><span data-stu-id="8967c-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="8967c-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8967c-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8967c-118">Den ekstraordinære avskrivningsprofilen brukes til ytterligere avskrivning av et aktiva i uvanlige omstendigheter.</span><span class="sxs-lookup"><span data-stu-id="8967c-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="8967c-119">Du kan for eksempel bruke denne til å registrere avskrivning som skyldes en naturkatastrofe.</span><span class="sxs-lookup"><span data-stu-id="8967c-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="8967c-120">Merk av eller fjern merket i boksen Opprett avskrivningsjusteringer med basisjusteringer.</span><span class="sxs-lookup"><span data-stu-id="8967c-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="8967c-121">Klikk rullegardinknappen i Kalender-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8967c-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="8967c-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8967c-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="8967c-123">Knytte avskrivningstablået til en anleggsmiddelgruppe</span><span class="sxs-lookup"><span data-stu-id="8967c-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="8967c-124">Klikk Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="8967c-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="8967c-125">Klikk rullegardinknappen i feltet Anleggsmiddelgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8967c-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="8967c-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8967c-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="8967c-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8967c-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8967c-128">Velg et alternativ i feltet Avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="8967c-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="8967c-129">Angi et tall i Levetid-feltet.</span><span class="sxs-lookup"><span data-stu-id="8967c-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="8967c-130">Legg merke til at verdien i feltet Avskrivningsperioder beregnes etter at levetiden er angitt.</span><span class="sxs-lookup"><span data-stu-id="8967c-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


