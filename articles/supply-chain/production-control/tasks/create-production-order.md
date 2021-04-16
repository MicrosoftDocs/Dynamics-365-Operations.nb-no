---
title: Opprette en produksjonsordre
description: Denne fremgangsmåten viser hvordan du oppretter en produksjonsordre.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e9358811f35e0417099ae65b0206e32a1455f84
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828976"
---
# <a name="create-a-production-order"></a><span data-ttu-id="171d0-103">Opprette en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="171d0-103">Create a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="171d0-104">Denne fremgangsmåten viser hvordan du oppretter en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="171d0-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="171d0-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="171d0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="171d0-106">Dette er den første fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="171d0-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="171d0-107">Opprette en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="171d0-107">Create a production order</span></span>
1. <span data-ttu-id="171d0-108">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="171d0-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="171d0-109">Klikk på Ny produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="171d0-109">Click New production order.</span></span>
3. <span data-ttu-id="171d0-110">Skriv inn D0001 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="171d0-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="171d0-111">Angi en leveringsdato i Levering-feltet.</span><span class="sxs-lookup"><span data-stu-id="171d0-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="171d0-112">Leveringsdatoen angir når produksjonsordren skal avsluttes for å levere i tide.</span><span class="sxs-lookup"><span data-stu-id="171d0-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="171d0-113">Denne datoen kan brukes i planleggingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="171d0-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="171d0-114">Du kan for eksempel planlegge ordren baklengs fra leveringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="171d0-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="171d0-115">Sett verdien for Antall til 20.</span><span class="sxs-lookup"><span data-stu-id="171d0-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="171d0-116">Merk: Feltet for stykklistenummer viser automatisk nummeret til eventuelle aktive stykklister for den gjeldende varen, men du kan endre stykklisten for produksjonsordren ved å velge en aktiv stykkliste fra listen over godkjente stykklisteversjoner.</span><span class="sxs-lookup"><span data-stu-id="171d0-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="171d0-117">Feltet for rutenummer viser automatisk nummeret til eventuelle aktive ruter for den gjeldende varen, men du kan endre ruten for produksjonsordren ved å velge en aktiv rute fra listen over godkjente ruteversjoner.</span><span class="sxs-lookup"><span data-stu-id="171d0-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="171d0-118">Klikk på Opprett.</span><span class="sxs-lookup"><span data-stu-id="171d0-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="171d0-119">Validere produksjonsordren</span><span class="sxs-lookup"><span data-stu-id="171d0-119">Validate the production order</span></span>
1. <span data-ttu-id="171d0-120">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="171d0-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="171d0-121">Klikk på koblingen for produksjonsordrenummeret du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="171d0-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="171d0-122">Dette åpner siden med detaljer for ordren.</span><span class="sxs-lookup"><span data-stu-id="171d0-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="171d0-123">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="171d0-123">Click Edit.</span></span>
3. <span data-ttu-id="171d0-124">Angi en leveringsdato i Levering-feltet.</span><span class="sxs-lookup"><span data-stu-id="171d0-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="171d0-125">Du kan for eksempel endre leveringsdatoen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="171d0-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="171d0-126">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="171d0-126">Click Save.</span></span>
5. <span data-ttu-id="171d0-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="171d0-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="171d0-128">Oppdatere stykklisten</span><span class="sxs-lookup"><span data-stu-id="171d0-128">Update the BOM</span></span>
1. <span data-ttu-id="171d0-129">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="171d0-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="171d0-130">Klikk på Stykkliste.</span><span class="sxs-lookup"><span data-stu-id="171d0-130">Click BOM.</span></span>
    * <span data-ttu-id="171d0-131">Åpne stykklistesiden for å validere stykklistedataene som ble kopiert fra standarddataene da produksjonsordren ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="171d0-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="171d0-132">I denne prosedyren må du oppdatere antallet for en stykkliste.</span><span class="sxs-lookup"><span data-stu-id="171d0-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="171d0-133">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="171d0-133">Click Edit.</span></span>
4. <span data-ttu-id="171d0-134">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="171d0-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="171d0-135">Endring av antallet på stykklistelinjen påvirker kostnadsestimatet av materialforbruk for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="171d0-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="171d0-136">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="171d0-136">Click Save.</span></span>
6. <span data-ttu-id="171d0-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="171d0-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="171d0-138">Oppdatere produksjonsruten</span><span class="sxs-lookup"><span data-stu-id="171d0-138">Update the production route</span></span>
1. <span data-ttu-id="171d0-139">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="171d0-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="171d0-140">Klikk på Rute.</span><span class="sxs-lookup"><span data-stu-id="171d0-140">Click Route.</span></span>
    * <span data-ttu-id="171d0-141">Åpne rutesiden for å validere dataene i produksjonsruten som ble kopiert fra standarddataene da produksjonsordren ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="171d0-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="171d0-142">I denne prosedyren må du oppdatere antallet for en av operasjonene i produksjonsruten.</span><span class="sxs-lookup"><span data-stu-id="171d0-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="171d0-143">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="171d0-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="171d0-144">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="171d0-144">Click Edit.</span></span>
5. <span data-ttu-id="171d0-145">I feltet Prosessantall angir du et nummer.</span><span class="sxs-lookup"><span data-stu-id="171d0-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="171d0-146">Endring av behandlingstiden påvirker det estimerte ruteforbruket og kostnadene for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="171d0-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="171d0-147">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="171d0-147">Click Save.</span></span>
7. <span data-ttu-id="171d0-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="171d0-148">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]