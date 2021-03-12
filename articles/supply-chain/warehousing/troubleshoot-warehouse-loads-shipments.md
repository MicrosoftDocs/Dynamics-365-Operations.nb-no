---
title: Feilsøke lastplanlegging og forsendelser
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lastplanlegging og forsendelser i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994048"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="0b55b-103">Feilsøke lastplanlegging og forsendelser</span><span class="sxs-lookup"><span data-stu-id="0b55b-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b55b-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lastplanlegging og forsendelser i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b55b-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="0b55b-105">Jeg får følgende feilmelding: Du kan ikke opprette en lastlinje for denne ordrelinjen fordi den inneholder lagerdimensjoner som er ugyldige ...</span><span class="sxs-lookup"><span data-stu-id="0b55b-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0b55b-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="0b55b-106">Issue description</span></span>

<span data-ttu-id="0b55b-107">Du får følgende feilmelding når du prøver å frigi en retursalgsordre til lageret:</span><span class="sxs-lookup"><span data-stu-id="0b55b-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="0b55b-108">Du kan ikke opprette en lastlinje for denne ordrelinjen fordi den inneholder lagerdimensjoner som er ugyldige.</span><span class="sxs-lookup"><span data-stu-id="0b55b-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="0b55b-109">Du kan ikke referere til lagerdimensjoner som finnes under lokasjonsdimensjonen i reservasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="0b55b-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="0b55b-110">Fjern de ugyldige dimensjonene fra ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b55b-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0b55b-111">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="0b55b-111">Issue resolution</span></span>

<span data-ttu-id="0b55b-112">Dessverre støtter ikke produktet lastbehandling for en salgsreturprosess.</span><span class="sxs-lookup"><span data-stu-id="0b55b-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="0b55b-113">Derfor kan du ikke frigi retursalgsordren til lageret.</span><span class="sxs-lookup"><span data-stu-id="0b55b-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="0b55b-114">På salgsordretransaksjoner kan du ikke referere til lagerdimensjoner som finnes under **Lokasjon**-dimensjonen i reservasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="0b55b-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="0b55b-115">Løsningen er å fjerne de ugyldige dimensjonene fra ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b55b-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="0b55b-116">Jeg får følgende feilmelding: En av linjene er allerede på en last.</span><span class="sxs-lookup"><span data-stu-id="0b55b-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="0b55b-117">Kan ikke frigi til lager.</span><span class="sxs-lookup"><span data-stu-id="0b55b-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0b55b-118">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="0b55b-118">Issue description</span></span>

<span data-ttu-id="0b55b-119">Hvis du oppretter laster manuelt, eller hvis du definerer prosessen slik at laster allerede er opprettet før salgsordrelinjeposten inntreffer, antas det at den påfølgende frigivelsen utføres manuelt, og at ruten og vurderingen fra lasten skal brukes.</span><span class="sxs-lookup"><span data-stu-id="0b55b-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="0b55b-120">I et annet scenario vil du prøve å utføre en automatisk frigivelse av lageret, men bølgeprosessen kan ikke opprette arbeid.</span><span class="sxs-lookup"><span data-stu-id="0b55b-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="0b55b-121">Derfor blir det fremdeles opprettet en åpen forsendelse eller last.</span><span class="sxs-lookup"><span data-stu-id="0b55b-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="0b55b-122">Denne åpne forsendelsen eller lasten blokkerer deretter etterfølgende forsøk på å frigi ordren automatisk til du sletter den åpne forsendelsen eller lasten, eller manuelt behandler bølgen på nytt.</span><span class="sxs-lookup"><span data-stu-id="0b55b-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0b55b-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="0b55b-123">Issue resolution</span></span>

<span data-ttu-id="0b55b-124">Du kan frigi fra salgsordresiden eller automatisk frigivelse fra siden frigivelse av salgsordre, bare hvis det ikke finnes en last før frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="0b55b-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="0b55b-125">Lasten vil automatisk bli opprettet etter at bølgen er behandlet.</span><span class="sxs-lookup"><span data-stu-id="0b55b-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="0b55b-126">Jeg får følgende feilmelding: Korrigeringen av følgeseddelen kan ikke behandles.</span><span class="sxs-lookup"><span data-stu-id="0b55b-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="0b55b-127">Følgeseddelen inneholder bare varer som er underlagt lagerstyringsprosesser, siden disse ikke støttes av følgeseddelkorrigering.</span><span class="sxs-lookup"><span data-stu-id="0b55b-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0b55b-128">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="0b55b-128">Issue description</span></span>

<span data-ttu-id="0b55b-129">Når du har postert en følgeseddel, kan du ikke avbryte den fordi **Avbryt**-knappen ikke er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="0b55b-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="0b55b-130">Du kan heller ikke korrigere følgeseddelen.</span><span class="sxs-lookup"><span data-stu-id="0b55b-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="0b55b-131">Hvis du prøver, får du denne feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="0b55b-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0b55b-132">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="0b55b-132">Issue resolution</span></span>

<span data-ttu-id="0b55b-133">Hvis du vil korrigere posterte følgesedler for varer som er aktivert for avansert lagerstyring (WMS), må du utføre posteringen fra lasten, ikke direkte fra ordren.</span><span class="sxs-lookup"><span data-stu-id="0b55b-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="0b55b-134">Hvordan kan jeg opprette arbeid fra utgående laster i stedet for bølger?</span><span class="sxs-lookup"><span data-stu-id="0b55b-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="0b55b-135">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="0b55b-135">Issue description</span></span>

<span data-ttu-id="0b55b-136">Her er en måte å gjenskape dette problemet på.</span><span class="sxs-lookup"><span data-stu-id="0b55b-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="0b55b-137">Opprette en utgående last ved hjelp av en salgsordre eller overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="0b55b-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="0b55b-138">Frigi belastningen til lageret.</span><span class="sxs-lookup"><span data-stu-id="0b55b-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="0b55b-139">Legg merke til at det ennå ikke er generert noe plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="0b55b-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0b55b-140">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="0b55b-140">Issue resolution</span></span>

<span data-ttu-id="0b55b-141">Hvis arbeid må genereres umiddelbart når lasten frigis, må du konfigurere bølgemalen i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="0b55b-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="0b55b-142">I bølgemalen angir du følgende alternativer til *Ja*:</span><span class="sxs-lookup"><span data-stu-id="0b55b-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="0b55b-143">Automatisk oppretting av bølge</span><span class="sxs-lookup"><span data-stu-id="0b55b-143">Automate wave creation</span></span>
- <span data-ttu-id="0b55b-144">Behandle bølge ved frigivelse til lager</span><span class="sxs-lookup"><span data-stu-id="0b55b-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="0b55b-145">Frigi bølge automatisk</span><span class="sxs-lookup"><span data-stu-id="0b55b-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="0b55b-146">Jeg kan ikke frigi en delvis levert last på nytt.</span><span class="sxs-lookup"><span data-stu-id="0b55b-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0b55b-147">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="0b55b-147">Issue description</span></span>

<span data-ttu-id="0b55b-148">Du kan ikke frigi en delvis levert last til lageret.</span><span class="sxs-lookup"><span data-stu-id="0b55b-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="0b55b-149">Når du gjør frigivelsen til lageret, vises meldingen Operasjon fullført, men ingenting skjer ikke, og det opprettes ikke noe arbeid for restantallet.</span><span class="sxs-lookup"><span data-stu-id="0b55b-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="0b55b-150">Dette problemet oppstår når du bruker funksjonalitet for transportlast, og det er en ufullstendig reservasjon.</span><span class="sxs-lookup"><span data-stu-id="0b55b-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0b55b-151">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="0b55b-151">Issue resolution</span></span>

<span data-ttu-id="0b55b-152">[KB-problem 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) (Delvis leverte laster kan bølges og behandles på nytt) er løst i [frigivelses 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="0b55b-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>
