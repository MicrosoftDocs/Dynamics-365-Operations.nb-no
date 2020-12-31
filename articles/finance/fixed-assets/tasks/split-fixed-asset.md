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
ms.openlocfilehash: da2dd4889a5f4722ff60a76a4a023c63fb59ad55
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514332"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="4c9f7-103">Dele et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="4c9f7-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c9f7-104">Dette emnet forklarer hvordan du deler en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="4c9f7-105">Den bruker regnskapsførerrollen og USMF-demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="4c9f7-106">Opprett et nytt anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="4c9f7-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="4c9f7-107">I navigasjonsruten går du til **Moduler \> Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="4c9f7-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-108">Select **New**.</span></span>
3. <span data-ttu-id="4c9f7-109">Angi eller velg en verdi i feltet **Anleggsmiddelgruppe**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="4c9f7-110">Noter anleggsmiddelnummeret for senere bruk i prosessen for deling.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="4c9f7-111">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="4c9f7-112">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="4c9f7-113">Dele et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="4c9f7-113">Split a fixed asset</span></span>

<span data-ttu-id="4c9f7-114">Før et ferdig avskrevet anleggsmiddel deles, skal anleggsmiddelstatusen endres manuelt fra **Lukket** til **Åpen**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="4c9f7-115">Dette trinnet er nødvendig fordi den bokførte statusen må være **Åpen** hvis du må postere transaksjoner for anleggsmiddelet (for eksempel for et salg).</span><span class="sxs-lookup"><span data-stu-id="4c9f7-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="4c9f7-116">Du må også aktivere parameteren **Tillat flere transaksjoner i ett bilag** i kategorien **Generelt** på siden **Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="4c9f7-117">Når statusen for anleggstablået er endret, og flere transaksjoner innenfor ett bilag er tillatt, fullfører du trinnene nedenfor for å dele opp aktivaet.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="4c9f7-118">I listen finner og velger du koblingen for anleggsmidlet som skal deles.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="4c9f7-119">Velg **Bøker**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-119">Select **Books**.</span></span> <span data-ttu-id="4c9f7-120">Velg tablået som skal deles til det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="4c9f7-121">Velg **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-121">Select **Functions**.</span></span>
4. <span data-ttu-id="4c9f7-122">Velg **Del anleggsmiddel**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="4c9f7-123">Angi eller velg en verdi i feltet **Til anleggsmiddel**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="4c9f7-124">Velg rullegardinknappen i feltet **Til tablå** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4c9f7-125">Angi en dato i feltet **Transaksjonsdato**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="4c9f7-126">Angi et tall i **Prosent**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="4c9f7-127">Angi eller velg en verdi i feltet **Journalnavn**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="4c9f7-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="4c9f7-129">Postere journaltransaksjonen</span><span class="sxs-lookup"><span data-stu-id="4c9f7-129">Post the journal transaction</span></span>

1. <span data-ttu-id="4c9f7-130">I navigasjonsruten går du til **Moduler \> Anleggsmidler \> Journaloppføringer \> Anleggsmiddeljournal**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="4c9f7-131">Velg journalen som ble opprettet med prosessen for deling, fra listen.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="4c9f7-132">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-132">Select **Lines**.</span></span>

    - <span data-ttu-id="4c9f7-133">Kontroller journallinjene som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="4c9f7-134">En anskaffelsesjusteringstransaksjon opprettes for det originale anleggsmiddelet for å redusere verdien av prosenten som er angitt under prosessen med deling.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="4c9f7-135">En anskaffelsestransaksjon er opprettet for det nye anleggsmiddelet for det samme beløpet.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="4c9f7-136">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-136">Select **Post**.</span></span>
