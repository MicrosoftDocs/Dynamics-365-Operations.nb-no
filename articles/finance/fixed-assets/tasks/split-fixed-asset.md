---
title: Dele et anleggsmiddel
description: Dette emnet forklarer hvordan du deler en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ccf187e77faf338ac29452d823c3652b806a21
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138121"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="8a3e4-103">Dele et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="8a3e4-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a3e4-104">Dette emnet forklarer hvordan du deler en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="8a3e4-105">Den bruker regnskapsførerrollen og USMF-demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="8a3e4-106">Opprett et nytt anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="8a3e4-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="8a3e4-107">I navigasjonsruten går du til **Moduler > Anleggsmidler > Anleggsmidler > Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="8a3e4-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-108">Select **New**.</span></span>
3. <span data-ttu-id="8a3e4-109">Angi eller velg en verdi i feltet **Anleggsmiddelgruppe**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="8a3e4-110">Noter anleggsmiddelnummeret for senere bruk i prosessen for deling.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="8a3e4-111">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8a3e4-112">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="8a3e4-113">Dele et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="8a3e4-113">Split a fixed asset</span></span>
1. <span data-ttu-id="8a3e4-114">I listen finner og velger du koblingen for anleggsmidlet som skal deles.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="8a3e4-115">Velg **Bøker**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-115">Select **Books**.</span></span> <span data-ttu-id="8a3e4-116">Velg tablået som skal deles til det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="8a3e4-117">Velg **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-117">Select **Functions**.</span></span>
4. <span data-ttu-id="8a3e4-118">Velg **Del anleggsmiddel**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="8a3e4-119">Angi eller velg en verdi i feltet **Til anleggsmiddel**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="8a3e4-120">Velg rullegardinknappen i feltet **Til tablå** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8a3e4-121">Angi en dato i feltet **Transaksjonsdato**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="8a3e4-122">Angi et tall i **Prosent**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="8a3e4-123">Angi eller velg en verdi i feltet **Journalnavn**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="8a3e4-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="8a3e4-125">Postere journaltransaksjonen</span><span class="sxs-lookup"><span data-stu-id="8a3e4-125">Post the journal transaction</span></span>
1. <span data-ttu-id="8a3e4-126">I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="8a3e4-127">Velg journalen som ble opprettet med prosessen for deling, fra listen.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="8a3e4-128">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-128">Select **Lines**.</span></span>

    - <span data-ttu-id="8a3e4-129">Kontroller journallinjene som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="8a3e4-130">En anskaffelsesjusteringstransaksjon opprettes for det originale anleggsmiddelet for å redusere verdien av prosenten som er angitt under prosessen med deling.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="8a3e4-131">En anskaffelsestransaksjon er opprettet for det nye anleggsmiddelet for det samme beløpet.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="8a3e4-132">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-132">Select **Post**.</span></span>

