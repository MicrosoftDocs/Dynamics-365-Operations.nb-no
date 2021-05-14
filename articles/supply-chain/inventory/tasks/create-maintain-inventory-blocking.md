---
title: Opprette og vedlikeholde en lagerblokkering
description: Dette emnet beskriver hvordan du bruker lagerblokkering til å forhindre at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956164"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="5b371-103">Opprette og vedlikeholde en lagerblokkering</span><span class="sxs-lookup"><span data-stu-id="5b371-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b371-104">Dette emnet beskriver hvordan du bruker lagerblokkering til å forhindre at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="5b371-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="5b371-105">Du må ha en vare som fysisk lagerbeholdning er tilgjengelig for, før du starter denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5b371-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="5b371-106">Sperr beholdning</span><span class="sxs-lookup"><span data-stu-id="5b371-106">Block inventory</span></span>

<span data-ttu-id="5b371-107">Følg denne fremgangsmåten for å opprette en lagerblokkeringspost, slik at lageret er sperret.</span><span class="sxs-lookup"><span data-stu-id="5b371-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="5b371-108">Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerblokkering**.</span><span class="sxs-lookup"><span data-stu-id="5b371-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="5b371-109">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b371-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b371-110">Angi hodet i den nye blokkeringsposten, angi feltet **Varenummer** til varen du vil blokkere, og angi en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="5b371-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="5b371-111">Skriv inn et antall elementer som skal blokkeres, i hurtigfanen **Generelt** i feltet **Antall**.</span><span class="sxs-lookup"><span data-stu-id="5b371-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="5b371-112">Angi området og lageret der varene du vil blokkere, for øyeblikket finnes i hurtigkategorien **Lagerdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="5b371-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="5b371-113">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b371-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="5b371-114">Oppdatere betingelsene for lagerblokkeringen</span><span class="sxs-lookup"><span data-stu-id="5b371-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="5b371-115">Følg denne fremgangsmåten for å oppdatere en lagerblokkeringspost.</span><span class="sxs-lookup"><span data-stu-id="5b371-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="5b371-116">Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerblokkering**.</span><span class="sxs-lookup"><span data-stu-id="5b371-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="5b371-117">I listeruten velger du den relevante blokkeringsposten.</span><span class="sxs-lookup"><span data-stu-id="5b371-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="5b371-118">Rediger posten etter behov.</span><span class="sxs-lookup"><span data-stu-id="5b371-118">Edit the record as required.</span></span> <span data-ttu-id="5b371-119">Du kan for eksempel endre verdien i feltet **Forventet dato** for å angi når det blokkerte lageret forventes å bli tilgjengelig for reservasjon.</span><span class="sxs-lookup"><span data-stu-id="5b371-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="5b371-120">Hvis alternativet **Forventede mottak** er valgt, vises datoen på den forventede transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="5b371-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="5b371-121">(Alternativet **Forventede mottak** velges som standard når du oppretter en blokkeringspost manuelt.)</span><span class="sxs-lookup"><span data-stu-id="5b371-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="5b371-122">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b371-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="5b371-123">Oppheve blokkering av lager</span><span class="sxs-lookup"><span data-stu-id="5b371-123">Unblock inventory</span></span>

<span data-ttu-id="5b371-124">Følg denne fremgangsmåten for å fjerne en lagerblokkeringspost, slik at sperring av lageret oppheves.</span><span class="sxs-lookup"><span data-stu-id="5b371-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="5b371-125">Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerblokkering**.</span><span class="sxs-lookup"><span data-stu-id="5b371-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="5b371-126">I listeruten velger du den relevante blokkeringsposten.</span><span class="sxs-lookup"><span data-stu-id="5b371-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="5b371-127">Velg deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b371-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="5b371-128">Du blir bedt om å bekrefte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="5b371-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="5b371-129">Klikk på **Ja** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="5b371-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="5b371-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b371-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
