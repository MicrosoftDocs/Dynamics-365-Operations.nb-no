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
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000299"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="452bb-103">Dele et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="452bb-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="452bb-104">Dette emnet forklarer hvordan du deler en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå.</span><span class="sxs-lookup"><span data-stu-id="452bb-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="452bb-105">Den bruker regnskapsførerrollen og USMF-demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="452bb-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="452bb-106">Opprett et nytt anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="452bb-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="452bb-107">I navigasjonsruten går du til **Moduler \> Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="452bb-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="452bb-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="452bb-108">Select **New**.</span></span>
3. <span data-ttu-id="452bb-109">Angi eller velg en verdi i feltet **Anleggsmiddelgruppe**.</span><span class="sxs-lookup"><span data-stu-id="452bb-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="452bb-110">Noter anleggsmiddelnummeret for senere bruk i prosessen for deling.</span><span class="sxs-lookup"><span data-stu-id="452bb-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="452bb-111">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="452bb-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="452bb-112">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="452bb-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="452bb-113">Dele et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="452bb-113">Split a fixed asset</span></span>

<span data-ttu-id="452bb-114">Før et ferdig avskrevet anleggsmiddel deles, skal anleggsmiddelstatusen endres manuelt fra **Lukket** til **Åpen**.</span><span class="sxs-lookup"><span data-stu-id="452bb-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="452bb-115">Dette trinnet er nødvendig fordi den bokførte statusen må være **Åpen** hvis du må postere transaksjoner for anleggsmiddelet (for eksempel for et salg).</span><span class="sxs-lookup"><span data-stu-id="452bb-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="452bb-116">Etter at anleggsmiddelstatusen er endret, følger du disse trinnene for å dele opp anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="452bb-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="452bb-117">I listen finner og velger du koblingen for anleggsmidlet som skal deles.</span><span class="sxs-lookup"><span data-stu-id="452bb-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="452bb-118">Velg **Bøker**.</span><span class="sxs-lookup"><span data-stu-id="452bb-118">Select **Books**.</span></span> <span data-ttu-id="452bb-119">Velg tablået som skal deles til det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="452bb-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="452bb-120">Velg **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="452bb-120">Select **Functions**.</span></span>
4. <span data-ttu-id="452bb-121">Velg **Del anleggsmiddel**.</span><span class="sxs-lookup"><span data-stu-id="452bb-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="452bb-122">Angi eller velg en verdi i feltet **Til anleggsmiddel**.</span><span class="sxs-lookup"><span data-stu-id="452bb-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="452bb-123">Velg rullegardinknappen i feltet **Til tablå** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="452bb-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="452bb-124">Angi en dato i feltet **Transaksjonsdato**.</span><span class="sxs-lookup"><span data-stu-id="452bb-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="452bb-125">Angi et tall i **Prosent** -feltet.</span><span class="sxs-lookup"><span data-stu-id="452bb-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="452bb-126">Angi eller velg en verdi i feltet **Journalnavn**.</span><span class="sxs-lookup"><span data-stu-id="452bb-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="452bb-127">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="452bb-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="452bb-128">Postere journaltransaksjonen</span><span class="sxs-lookup"><span data-stu-id="452bb-128">Post the journal transaction</span></span>

1. <span data-ttu-id="452bb-129">I navigasjonsruten går du til **Moduler \> Anleggsmidler \> Journaloppføringer \> Anleggsmiddeljournal**.</span><span class="sxs-lookup"><span data-stu-id="452bb-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="452bb-130">Velg journalen som ble opprettet med prosessen for deling, fra listen.</span><span class="sxs-lookup"><span data-stu-id="452bb-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="452bb-131">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="452bb-131">Select **Lines**.</span></span>

    - <span data-ttu-id="452bb-132">Kontroller journallinjene som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="452bb-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="452bb-133">En anskaffelsesjusteringstransaksjon opprettes for det originale anleggsmiddelet for å redusere verdien av prosenten som er angitt under prosessen med deling.</span><span class="sxs-lookup"><span data-stu-id="452bb-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="452bb-134">En anskaffelsestransaksjon er opprettet for det nye anleggsmiddelet for det samme beløpet.</span><span class="sxs-lookup"><span data-stu-id="452bb-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="452bb-135">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="452bb-135">Select **Post**.</span></span>
