---
title: Opprette avanserte regler for journaler
description: Denne fremgangsmåten viser hvordan du oppretter avanserte regler for journaler.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c06855c7a7648c5829b90bc548a7d2e400967698
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988608"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="e79c3-103">Opprette avanserte regler for journaler</span><span class="sxs-lookup"><span data-stu-id="e79c3-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e79c3-104">Denne fremgangsmåten viser hvordan du oppretter avanserte regler for journaler.</span><span class="sxs-lookup"><span data-stu-id="e79c3-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="e79c3-105">Dette omfatter definering av journalkontroll og brukerposteringsrestriksjoner.</span><span class="sxs-lookup"><span data-stu-id="e79c3-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="e79c3-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e79c3-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="e79c3-107">Definere journalkontroll</span><span class="sxs-lookup"><span data-stu-id="e79c3-107">Set up journal control</span></span>
1. <span data-ttu-id="e79c3-108">I **navigasjonsruten** går du til **Moduler > Økonomimodul > Journaloppsett > Journalnavn**.</span><span class="sxs-lookup"><span data-stu-id="e79c3-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="e79c3-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e79c3-110">Klikk **Journalkontroll** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="e79c3-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="e79c3-111">Klikk **Legg til** i hurtigfanen **Hvilke kontotyper kan posteres?**</span><span class="sxs-lookup"><span data-stu-id="e79c3-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="e79c3-112">Klikk rullegardinknappen i feltet **Firmakontoer** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e79c3-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e79c3-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e79c3-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e79c3-115">Klikk **Legg til** i hurtigfanen **Hvilke segmentverdier er gyldige for denne journalen?**</span><span class="sxs-lookup"><span data-stu-id="e79c3-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="e79c3-116">Klikk rullegardinknappen i feltet **Kontostruktur** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e79c3-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e79c3-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="e79c3-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e79c3-119">Klikk rullegardinknappen i feltet **Segment** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e79c3-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="e79c3-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="e79c3-121">Klikk rullegardinknappen i feltet **Fra verdi** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e79c3-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="e79c3-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="e79c3-123">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="e79c3-124">Klikk rullegardinknappen i feltet **Til verdi** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e79c3-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="e79c3-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="e79c3-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e79c3-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="e79c3-127">Definere posteringsrestriksjoner</span><span class="sxs-lookup"><span data-stu-id="e79c3-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="e79c3-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e79c3-128">Close the page.</span></span>
2. <span data-ttu-id="e79c3-129">Klikk **Posteringsrestriksjoner**.</span><span class="sxs-lookup"><span data-stu-id="e79c3-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="e79c3-130">Velg Etter brukergruppe i feltet **Hvordan vil du konfigurere posteringsrestriksjoner?**</span><span class="sxs-lookup"><span data-stu-id="e79c3-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="e79c3-131">Merk av for gruppen som du vil tillate postering for dette journalnavnet for, i treet.</span><span class="sxs-lookup"><span data-stu-id="e79c3-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="e79c3-132">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e79c3-132">Click **OK**.</span></span>

