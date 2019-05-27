---
title: Dele et anleggsmiddel
description: Denne oppgaveveiledningen vil dele en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566898"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="d0ae0-103">Dele et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="d0ae0-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0ae0-104">Denne oppgaveveiledningen vil dele en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="d0ae0-105">Den bruker regnskapsførerrollen og USMF-demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="d0ae0-106">Opprett et nytt anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="d0ae0-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="d0ae0-107">Gå til Anleggsmidler > Anleggsmidler > Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="d0ae0-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-108">Click New.</span></span>
3. <span data-ttu-id="d0ae0-109">Angi eller velg en verdi i feltet Anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="d0ae0-110">Noter anleggsmiddelnummeret for senere bruk i prosessen for deling.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="d0ae0-111">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d0ae0-112">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="d0ae0-113">Dele et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="d0ae0-113">Split a fixed asset</span></span>
1. <span data-ttu-id="d0ae0-114">I listen finner og merker du anleggsmidlet som skal deles.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="d0ae0-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="d0ae0-116">Klikk Tablåer.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-116">Click Books.</span></span>
    * <span data-ttu-id="d0ae0-117">Velg tablået som skal deles til det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="d0ae0-118">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-118">Click Functions.</span></span>
5. <span data-ttu-id="d0ae0-119">Klikk Del anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="d0ae0-120">Angi eller velg en verdi i feltet Til anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="d0ae0-121">Klikk rullegardinknappen i feltet Til tablå for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d0ae0-122">Angi en dato i feltet Transaksjonsdato.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="d0ae0-123">Angi et tall i Prosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="d0ae0-124">Angi eller velg en verdi i feltet Journalnavn.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="d0ae0-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="d0ae0-126">Postere journaltransaksjonen</span><span class="sxs-lookup"><span data-stu-id="d0ae0-126">Post the journal transaction</span></span>
1. <span data-ttu-id="d0ae0-127">Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="d0ae0-128">Velg journalen som ble opprettet med prosessen for deling, fra listen.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="d0ae0-129">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-129">Click Lines.</span></span>
    * <span data-ttu-id="d0ae0-130">Kontroller journallinjene som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-130">Verify the journal lines created.</span></span>  <span data-ttu-id="d0ae0-131">En anskaffelsesjusteringstransaksjon opprettes for det originale anleggsmiddelet for å redusere verdien av prosenten som er angitt under prosessen med deling.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="d0ae0-132">En anskaffelsestransaksjon er opprettet for det nye anleggsmiddelet for det samme beløpet.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="d0ae0-133">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-133">Click Post.</span></span>

