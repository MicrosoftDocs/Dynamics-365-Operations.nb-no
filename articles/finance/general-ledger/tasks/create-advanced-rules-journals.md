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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea6ca24d27bb5b00bbe31060ce2f7e40bf2fb335
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145222"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="078fc-103">Opprette avanserte regler for journaler</span><span class="sxs-lookup"><span data-stu-id="078fc-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="078fc-104">Denne fremgangsmåten viser hvordan du oppretter avanserte regler for journaler.</span><span class="sxs-lookup"><span data-stu-id="078fc-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="078fc-105">Dette omfatter definering av journalkontroll og brukerposteringsrestriksjoner.</span><span class="sxs-lookup"><span data-stu-id="078fc-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="078fc-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="078fc-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="078fc-107">Definere journalkontroll</span><span class="sxs-lookup"><span data-stu-id="078fc-107">Set up journal control</span></span>
1. <span data-ttu-id="078fc-108">I **navigasjonsruten** går du til **Moduler > Økonomimodul > Journaloppsett > Journalnavn**.</span><span class="sxs-lookup"><span data-stu-id="078fc-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="078fc-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="078fc-110">Klikk **Journalkontroll** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="078fc-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="078fc-111">Klikk **Legg til** i hurtigfanen**Hvilke kontotyper kan posteres?**</span><span class="sxs-lookup"><span data-stu-id="078fc-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="078fc-112">Klikk rullegardinknappen i feltet **Firmakontoer** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="078fc-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="078fc-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="078fc-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="078fc-115">Klikk **Legg til** i hurtigfanen **Hvilke segmentverdier er gyldige for denne journalen?**</span><span class="sxs-lookup"><span data-stu-id="078fc-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="078fc-116">Klikk rullegardinknappen i feltet **Kontostruktur** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="078fc-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="078fc-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="078fc-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="078fc-119">Klikk rullegardinknappen i feltet **Segment** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="078fc-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="078fc-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="078fc-121">Klikk rullegardinknappen i feltet **Fra verdi** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="078fc-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="078fc-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="078fc-123">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="078fc-124">Klikk rullegardinknappen i feltet **Til verdi** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="078fc-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="078fc-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="078fc-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="078fc-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="078fc-127">Definere posteringsrestriksjoner</span><span class="sxs-lookup"><span data-stu-id="078fc-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="078fc-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="078fc-128">Close the page.</span></span>
2. <span data-ttu-id="078fc-129">Klikk **Posteringsrestriksjoner**.</span><span class="sxs-lookup"><span data-stu-id="078fc-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="078fc-130">Velg Etter brukergruppe i feltet **Hvordan vil du konfigurere posteringsrestriksjoner?**</span><span class="sxs-lookup"><span data-stu-id="078fc-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="078fc-131">Merk av for gruppen som du vil tillate postering for dette journalnavnet for, i treet.</span><span class="sxs-lookup"><span data-stu-id="078fc-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="078fc-132">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="078fc-132">Click **OK**.</span></span>

