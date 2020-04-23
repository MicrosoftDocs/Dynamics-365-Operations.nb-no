---
title: Opprette og vedlikeholde en lagerblokkering
description: Denne fremgangsmåten viser hvordan du forhindrer at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter ved å bruke lagerblokkeringen.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e76c3d1f46e31dcd2171682a629dabe5bf5db418
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204154"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="98f8d-103">Opprette og vedlikeholde en lagerblokkering</span><span class="sxs-lookup"><span data-stu-id="98f8d-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98f8d-104">Denne fremgangsmåten viser hvordan du forhindrer at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter ved å bruke lagerblokkeringen.</span><span class="sxs-lookup"><span data-stu-id="98f8d-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="98f8d-105">Du kan kjøre prosedyren i demonstrasjonsdatafirmaet USMF med eksempelverdiene som vises.</span><span class="sxs-lookup"><span data-stu-id="98f8d-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="98f8d-106">Du må ha en vare med fysisk lagerbeholdning tilgjengelig før du starter denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="98f8d-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="98f8d-107">Opprette en lagerblokkering</span><span class="sxs-lookup"><span data-stu-id="98f8d-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="98f8d-108">I **navigasjonsruten** går du til **Moduler > Lagerstyring > Periodiske oppgaver > Lagerblokkering**.</span><span class="sxs-lookup"><span data-stu-id="98f8d-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="98f8d-109">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="98f8d-109">Click **New**.</span></span>
3. <span data-ttu-id="98f8d-110">Klikk rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="98f8d-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="98f8d-111">Velg varen du vil bruke, i listen.</span><span class="sxs-lookup"><span data-stu-id="98f8d-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="98f8d-112">Velg et varenummer med fysisk lagerbeholdning som du vil blokkere.</span><span class="sxs-lookup"><span data-stu-id="98f8d-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="98f8d-113">Hvis du bruker USMF, kan du velge vare M9201.</span><span class="sxs-lookup"><span data-stu-id="98f8d-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="98f8d-114">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="98f8d-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="98f8d-115">Hvis du bruker varen M9201, må du velge mindre enn 200.</span><span class="sxs-lookup"><span data-stu-id="98f8d-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="98f8d-116">Vis hurtigfanen **Lagerdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="98f8d-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="98f8d-117">Klikk rullegardinknappen i **Lager**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="98f8d-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="98f8d-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="98f8d-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="98f8d-119">Hvis du bruker vare M9201, kan du velge lager 51.</span><span class="sxs-lookup"><span data-stu-id="98f8d-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="98f8d-120">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="98f8d-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="98f8d-121">Oppdatere betingelsene for lagerblokkeringen</span><span class="sxs-lookup"><span data-stu-id="98f8d-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="98f8d-122">Angi et tall i hurtigfanen **Generelt** i feltet **Antall**.</span><span class="sxs-lookup"><span data-stu-id="98f8d-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="98f8d-123">Oppdater lagerantall-feltet for å gjenspeile antallet som skal blokkeres.</span><span class="sxs-lookup"><span data-stu-id="98f8d-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="98f8d-124">Angi en dato i feltet **Forventet dato**.</span><span class="sxs-lookup"><span data-stu-id="98f8d-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="98f8d-125">Du kan angi når den blokkerte lagertransaksjonen forventes å bli tilgjengelig for reservasjon, ved å tilordne en forventet dato.</span><span class="sxs-lookup"><span data-stu-id="98f8d-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="98f8d-126">Hvis alternativet Forventede mottak er valgt for lagerblokkeringen, som den er som standard når du manuelt oppretter en blokkering, vises denne datoen på den forventede transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="98f8d-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="98f8d-127">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="98f8d-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="98f8d-128">Fjerne lagerblokkeringen</span><span class="sxs-lookup"><span data-stu-id="98f8d-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="98f8d-129">Klikk **Slett** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="98f8d-129">On the **Action pane**, click **Delete**.</span></span>
2. <span data-ttu-id="98f8d-130">Klikk **Ja**.</span><span class="sxs-lookup"><span data-stu-id="98f8d-130">Click **Yes**.</span></span>
3. <span data-ttu-id="98f8d-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98f8d-131">Close the page.</span></span>

