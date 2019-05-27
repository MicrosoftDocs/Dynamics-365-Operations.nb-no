---
title: Opprette avanserte regler for journaler
description: Denne fremgangsmåten viser hvordan du oppretter avanserte regler for journaler.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553113"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="87dea-103">Opprette avanserte regler for journaler</span><span class="sxs-lookup"><span data-stu-id="87dea-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87dea-104">Denne fremgangsmåten viser hvordan du oppretter avanserte regler for journaler.</span><span class="sxs-lookup"><span data-stu-id="87dea-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="87dea-105">Dette omfatter definering av journalkontroll og brukerposteringsrestriksjoner.</span><span class="sxs-lookup"><span data-stu-id="87dea-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="87dea-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="87dea-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="87dea-107">Definere journalkontroll</span><span class="sxs-lookup"><span data-stu-id="87dea-107">Set up journal control</span></span>
1. <span data-ttu-id="87dea-108">Gå til Økonomimodul > Journaloppsett > Journalnavn.</span><span class="sxs-lookup"><span data-stu-id="87dea-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="87dea-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="87dea-110">Klikk Journalkontroll.</span><span class="sxs-lookup"><span data-stu-id="87dea-110">Click Journal control.</span></span>
4. <span data-ttu-id="87dea-111">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="87dea-111">Click Add.</span></span>
5. <span data-ttu-id="87dea-112">Klikk rullegardinknappen i feltet Firmakontoer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="87dea-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="87dea-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="87dea-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="87dea-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="87dea-115">Click Add.</span></span>
9. <span data-ttu-id="87dea-116">Klikk rullegardinknappen i feltet Kontostruktur for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="87dea-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="87dea-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="87dea-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="87dea-119">Klikk rullegardinknappen i feltet Segment for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="87dea-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="87dea-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="87dea-121">Klikk rullegardinknappen i feltet Fra verdi for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="87dea-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="87dea-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="87dea-123">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="87dea-124">Klikk rullegardinknappen i feltet Til verdi for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="87dea-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="87dea-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="87dea-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="87dea-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="87dea-127">Definere posteringsrestriksjoner</span><span class="sxs-lookup"><span data-stu-id="87dea-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="87dea-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="87dea-128">Close the page.</span></span>
2. <span data-ttu-id="87dea-129">Klikk Posteringsrestriksjoner.</span><span class="sxs-lookup"><span data-stu-id="87dea-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="87dea-130">Velg Etter brukergruppe i Hvordan vil du konfigurere posteringsrestriksjoner.</span><span class="sxs-lookup"><span data-stu-id="87dea-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="87dea-131">Merk av for gruppen som du vil tillate postering for dette journalnavnet for, i treet.</span><span class="sxs-lookup"><span data-stu-id="87dea-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="87dea-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="87dea-132">Click OK.</span></span>

