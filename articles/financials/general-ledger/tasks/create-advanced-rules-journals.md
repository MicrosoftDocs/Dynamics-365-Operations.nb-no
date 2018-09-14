--- 
title: Opprette avanserte regler for journaler
description: "Denne fremgangsmåten viser hvordan du oppretter avanserte regler for journaler."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="68f5f-103">Opprette avanserte regler for journaler</span><span class="sxs-lookup"><span data-stu-id="68f5f-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68f5f-104">Denne fremgangsmåten viser hvordan du oppretter avanserte regler for journaler.</span><span class="sxs-lookup"><span data-stu-id="68f5f-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="68f5f-105">Dette omfatter definering av journalkontroll og brukerposteringsrestriksjoner.</span><span class="sxs-lookup"><span data-stu-id="68f5f-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="68f5f-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="68f5f-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="68f5f-107">Definere journalkontroll</span><span class="sxs-lookup"><span data-stu-id="68f5f-107">Set up journal control</span></span>
1. <span data-ttu-id="68f5f-108">Gå til Økonomimodul > Journaloppsett > Journalnavn.</span><span class="sxs-lookup"><span data-stu-id="68f5f-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="68f5f-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="68f5f-110">Klikk Journalkontroll.</span><span class="sxs-lookup"><span data-stu-id="68f5f-110">Click Journal control.</span></span>
4. <span data-ttu-id="68f5f-111">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="68f5f-111">Click Add.</span></span>
5. <span data-ttu-id="68f5f-112">Klikk rullegardinknappen i feltet Firmakontoer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="68f5f-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="68f5f-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="68f5f-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="68f5f-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="68f5f-115">Click Add.</span></span>
9. <span data-ttu-id="68f5f-116">Klikk rullegardinknappen i feltet Kontostruktur for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="68f5f-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="68f5f-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="68f5f-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="68f5f-119">Klikk rullegardinknappen i feltet Segment for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="68f5f-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="68f5f-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="68f5f-121">Klikk rullegardinknappen i feltet Fra verdi for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="68f5f-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="68f5f-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="68f5f-123">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="68f5f-124">Klikk rullegardinknappen i feltet Til verdi for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="68f5f-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="68f5f-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="68f5f-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="68f5f-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="68f5f-127">Definere posteringsrestriksjoner</span><span class="sxs-lookup"><span data-stu-id="68f5f-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="68f5f-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="68f5f-128">Close the page.</span></span>
2. <span data-ttu-id="68f5f-129">Klikk Posteringsrestriksjoner.</span><span class="sxs-lookup"><span data-stu-id="68f5f-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="68f5f-130">Velg Etter brukergruppe i Hvordan vil du konfigurere posteringsrestriksjoner.</span><span class="sxs-lookup"><span data-stu-id="68f5f-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="68f5f-131">Merk av for gruppen som du vil tillate postering for dette journalnavnet for, i treet.</span><span class="sxs-lookup"><span data-stu-id="68f5f-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="68f5f-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="68f5f-132">Click OK.</span></span>


