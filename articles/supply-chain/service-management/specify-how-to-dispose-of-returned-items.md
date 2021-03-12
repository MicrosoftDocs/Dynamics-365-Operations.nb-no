---
title: Angi hvordan du kvitter deg med returnerte varer
description: Angi hvordan du kvitter deg med returnerte varer.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0049e47d5e0e5f8a2a6d7cc5feb29593c764d323
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991546"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="cc3a6-103">Angi hvordan du kvitter deg med returnerte varer</span><span class="sxs-lookup"><span data-stu-id="cc3a6-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cc3a6-104">Når du håndterer en returordre, må du angi en returårsakskode for å identifisere produktet som returneres.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="cc3a6-105">Du må også angi en disposisjonskode og en disposisjonshandling for å avgjøre hva som skal gjøres med det returnerte produktet.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="cc3a6-106">En disposisjonskode kan brukes når du oppretter returordren, registrerer vareankomst eller følgeseddeloppdaterer en vareankomst og avslutter karanteneordrer.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="cc3a6-107">Du kan angi hvilken som helst disposisjonskode for å støtte forretningsprosessene.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="cc3a6-108">Tabellen nedenfor inneholder et sett med vanlige koder som kan tildeles returvaredisposisjon.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc3a6-109">Disposisjonstype</span><span class="sxs-lookup"><span data-stu-id="cc3a6-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="cc3a6-110">Felleskode</span><span class="sxs-lookup"><span data-stu-id="cc3a6-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="cc3a6-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc3a6-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-112">Avhending</span><span class="sxs-lookup"><span data-stu-id="cc3a6-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-113">SC</span><span class="sxs-lookup"><span data-stu-id="cc3a6-113">SC</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-114">Kasting/avhending</span><span class="sxs-lookup"><span data-stu-id="cc3a6-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-115">Avhending</span><span class="sxs-lookup"><span data-stu-id="cc3a6-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-116">DC</span><span class="sxs-lookup"><span data-stu-id="cc3a6-116">DC</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-117">Gave til veldedig organisasjon</span><span class="sxs-lookup"><span data-stu-id="cc3a6-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-118">Avhending</span><span class="sxs-lookup"><span data-stu-id="cc3a6-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-119">TD</span><span class="sxs-lookup"><span data-stu-id="cc3a6-119">TD</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-120">Avhending av tredjepart</span><span class="sxs-lookup"><span data-stu-id="cc3a6-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-121">Avhending</span><span class="sxs-lookup"><span data-stu-id="cc3a6-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-122">SL</span><span class="sxs-lookup"><span data-stu-id="cc3a6-122">SL</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-123">Gjenbruk</span><span class="sxs-lookup"><span data-stu-id="cc3a6-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-124">Avhending</span><span class="sxs-lookup"><span data-stu-id="cc3a6-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-125">TS</span><span class="sxs-lookup"><span data-stu-id="cc3a6-125">TS</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-126">Salg av tredjepart (annenhåndsmarkeder)</span><span class="sxs-lookup"><span data-stu-id="cc3a6-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-127">Reparasjon/modifisering</span><span class="sxs-lookup"><span data-stu-id="cc3a6-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-128">RW</span><span class="sxs-lookup"><span data-stu-id="cc3a6-128">RW</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-129">Omarbeiding</span><span class="sxs-lookup"><span data-stu-id="cc3a6-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-130">Reparasjon/modifisering</span><span class="sxs-lookup"><span data-stu-id="cc3a6-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-131">RF</span><span class="sxs-lookup"><span data-stu-id="cc3a6-131">RF</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-132">Refabrikkering/renovering</span><span class="sxs-lookup"><span data-stu-id="cc3a6-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-133">Reparasjon/modifisering</span><span class="sxs-lookup"><span data-stu-id="cc3a6-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-134">MD</span><span class="sxs-lookup"><span data-stu-id="cc3a6-134">MD</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-135">Modifisering</span><span class="sxs-lookup"><span data-stu-id="cc3a6-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-136">Reparasjon/modifisering</span><span class="sxs-lookup"><span data-stu-id="cc3a6-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-137">RP</span><span class="sxs-lookup"><span data-stu-id="cc3a6-137">RP</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-138">Reparering</span><span class="sxs-lookup"><span data-stu-id="cc3a6-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-139">Reparasjon/modifisering</span><span class="sxs-lookup"><span data-stu-id="cc3a6-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-140">RV</span><span class="sxs-lookup"><span data-stu-id="cc3a6-140">RV</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-141">Retur til leverandør</span><span class="sxs-lookup"><span data-stu-id="cc3a6-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-142">Annet</span><span class="sxs-lookup"><span data-stu-id="cc3a6-142">Other</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-143">AI</span><span class="sxs-lookup"><span data-stu-id="cc3a6-143">AI</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-144">Bruk varen som den er</span><span class="sxs-lookup"><span data-stu-id="cc3a6-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-145">Annet</span><span class="sxs-lookup"><span data-stu-id="cc3a6-145">Other</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-146">RS</span><span class="sxs-lookup"><span data-stu-id="cc3a6-146">RS</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-147">Videresalg</span><span class="sxs-lookup"><span data-stu-id="cc3a6-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-148">Annet</span><span class="sxs-lookup"><span data-stu-id="cc3a6-148">Other</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-149">EX</span><span class="sxs-lookup"><span data-stu-id="cc3a6-149">EX</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-150">Veksle</span><span class="sxs-lookup"><span data-stu-id="cc3a6-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-151">Annet</span><span class="sxs-lookup"><span data-stu-id="cc3a6-151">Other</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-152">MS</span><span class="sxs-lookup"><span data-stu-id="cc3a6-152">MS</span></span></p></td>
<td><p><span data-ttu-id="cc3a6-153">Diverse</span><span class="sxs-lookup"><span data-stu-id="cc3a6-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc3a6-154">Du må velge en disposisjonshandling for hver ny disposisjonskode du angir.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="cc3a6-155">Disposisjonshandlingen avgjør de fysiske og økonomiske implikasjonene for disposisjonskodene.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="cc3a6-156">Disposisjonshandlingen avgjør for eksempel den fysiske handlingen for den returnerte varen, den økonomiske effekten av den returnerte varen, og om det må sendes en erstatningsvare til kunden.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="cc3a6-157">Du kan konfigurere et ubegrenset antall disposisjonskoder i henhold til dine forretningsbehov, men du kan bare velge blant seks forhåndsdefinerte disposisjonshandlinger.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="cc3a6-158">Tabellen nedenfor inneholder disposisjonshandlingene og definisjonene.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc3a6-159">Disposisjonshandling</span><span class="sxs-lookup"><span data-stu-id="cc3a6-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="cc3a6-160">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc3a6-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-161"><strong>Kreditt</strong></span><span class="sxs-lookup"><span data-stu-id="cc3a6-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="cc3a6-162">Returner varen til lageret, og krediter kunden.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-163"><strong>Bare kreditering</strong></span><span class="sxs-lookup"><span data-stu-id="cc3a6-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="cc3a6-164">Krediter kunder uten å kreve eller forvente at varen returneres.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-165"><strong>Svinn</strong></span><span class="sxs-lookup"><span data-stu-id="cc3a6-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="cc3a6-166">Kasser varen, og krediter kunden.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-167"><strong>Erstatt og krediter</strong></span><span class="sxs-lookup"><span data-stu-id="cc3a6-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="cc3a6-168">Returner varen til lageret, opprett en erstatningsordre og krediter kunden.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc3a6-169"><strong>Erstatt og kasser</strong></span><span class="sxs-lookup"><span data-stu-id="cc3a6-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="cc3a6-170">Kasser varen, opprett en erstatningsordre og krediter kunden.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc3a6-171"><strong>Returner til kunde</strong></span><span class="sxs-lookup"><span data-stu-id="cc3a6-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="cc3a6-172">Avvis den returnerte varen, og returner den til kunden.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="cc3a6-173">Velg en disposisjonskode for en karanteneordre</span><span class="sxs-lookup"><span data-stu-id="cc3a6-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="cc3a6-174">Klikk på **Lagerstyring** \> **Periodisk** \> **Kvalitetsstyring** \> **Karanteneordrer**.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="cc3a6-175">Velg en handling fra feltet **Disposisjonskode** i fanen **Oversikt** hvis det gjelder en eksisterende karanteneordre.</span><span class="sxs-lookup"><span data-stu-id="cc3a6-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="cc3a6-176">Se også</span><span class="sxs-lookup"><span data-stu-id="cc3a6-176">See also</span></span>

<span data-ttu-id="cc3a6-177">[Karanteneordre (skjema)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="cc3a6-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="cc3a6-178">[Disposisjonskoder (skjema)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="cc3a6-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  


