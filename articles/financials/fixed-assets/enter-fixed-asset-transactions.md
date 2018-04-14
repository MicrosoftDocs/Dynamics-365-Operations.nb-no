---
title: Alternativer for anleggsmiddeltransaksjon
description: Denne artikkelen beskriver de ulike metodene som er tilgjengelige for oppretting av anleggsmiddeltransaksjoner.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2a7fa7a28437e29f390efdf566e946c6a1082370
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="5882f-103">Alternativer for anleggsmiddeltransaksjon</span><span class="sxs-lookup"><span data-stu-id="5882f-103">Fixed asset transaction options</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="5882f-104">Denne artikkelen beskriver de ulike metodene som er tilgjengelige for oppretting av anleggsmiddeltransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5882f-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="5882f-105">Du kan definere anleggsmidler for integrasjon med Leverandører, Kunder, Innkjøp og leverandører og Økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="5882f-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="5882f-106">Du kan også overføre varer i Lagerstyring til Anleggsmidler hvis du vil bruke disse elementene internt.</span><span class="sxs-lookup"><span data-stu-id="5882f-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="5882f-107">Leverandører</span><span class="sxs-lookup"><span data-stu-id="5882f-107">Accounts payable</span></span>
<span data-ttu-id="5882f-108">Du kan registrere anleggsmiddeltransaksjoner på Journalbilag-siden.</span><span class="sxs-lookup"><span data-stu-id="5882f-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="5882f-109">Denne siden kan åpnes fra Fakturajournal-siden.</span><span class="sxs-lookup"><span data-stu-id="5882f-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="5882f-110">Du kan også åpne siden Journalbilag fra Fakturagodkjenningsjournal-siden.</span><span class="sxs-lookup"><span data-stu-id="5882f-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="5882f-111">I feltet Motkontotype velger du Anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="5882f-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="5882f-112">Deretter velger du et anleggmiddelnummer i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="5882f-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="5882f-113">I kategorien Anleggsmidler angir du verdier i feltene Transaksjonstype og Tablå.</span><span class="sxs-lookup"><span data-stu-id="5882f-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="5882f-114">Kundereskontro</span><span class="sxs-lookup"><span data-stu-id="5882f-114">Accounts receivable</span></span>
<span data-ttu-id="5882f-115">Du kan registrere anleggsmiddeltransaksjoner på Fritekstfaktura-siden.</span><span class="sxs-lookup"><span data-stu-id="5882f-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="5882f-116">På siden Fritekstfakturaer, i rutenettet Fakturalinjer, velger du en linjevare.</span><span class="sxs-lookup"><span data-stu-id="5882f-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="5882f-117">Klikk hurtigfanen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="5882f-117">Click the Line details FastTab.</span></span> <span data-ttu-id="5882f-118">Angi nummeret og tablået for anleggsmiddelet i avhendingstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="5882f-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="5882f-119">Når det gjelder fritekstfakturaer, er anleggsmiddeltransaksjoner alltid av typen Avhendingssalg.</span><span class="sxs-lookup"><span data-stu-id="5882f-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="5882f-120">Innkjøp og leverandører</span><span class="sxs-lookup"><span data-stu-id="5882f-120">Procurement and sourcing</span></span>
<span data-ttu-id="5882f-121">Du kan registrere anleggsmiddeltransaksjoner på Bestilling-siden.</span><span class="sxs-lookup"><span data-stu-id="5882f-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="5882f-122">Angi nødvendig informasjon for å opprette en salgsordre, og klikk deretter OK.</span><span class="sxs-lookup"><span data-stu-id="5882f-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="5882f-123">Klikk hurtigfanen Linjedetaljer på siden Bestilling.</span><span class="sxs-lookup"><span data-stu-id="5882f-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="5882f-124">Deretter angir du informasjon om anleggsmiddelet i kategorien Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="5882f-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="5882f-125">Hvis du vil postere en anskaffelsestransaksjon for et eksisterende anleggsmiddel, må du angi anleggsmiddelets nummer, tablå og transaksjonstype.</span><span class="sxs-lookup"><span data-stu-id="5882f-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="5882f-126">Anlegsmidlet kan ikke posteres hvis noe av denne informasjonen mangler.</span><span class="sxs-lookup"><span data-stu-id="5882f-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="5882f-127">Hvis du vil postere en anskaffelsestransaksjon for et nytt anleggsmiddel, merker du av for Nytt anleggsmiddel og velger anleggsmiddelgruppen som det nye anleggsmiddelet skal tilordnes.</span><span class="sxs-lookup"><span data-stu-id="5882f-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="5882f-128">Ingen anleggsmiddelfelt er imidlertid tilgjengelige for en linje hvis varen er en lagermodellgruppe som bruker en lagermodell med standard kostpris.</span><span class="sxs-lookup"><span data-stu-id="5882f-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="5882f-129">I tillegg avgjør alternativene som er definert på siden Parametere for anleggsmidler, om du kan postere anskaffelsestransaksjoner fra innkjøpsmodulene.</span><span class="sxs-lookup"><span data-stu-id="5882f-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="5882f-130">Når en bestilling eller Lager til anleggsmidler-journalen brukes til anskaffelse av anleggsmidler, påvirkes lagerverdien.</span><span class="sxs-lookup"><span data-stu-id="5882f-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="5882f-131">Økonomimodul</span><span class="sxs-lookup"><span data-stu-id="5882f-131">General ledger</span></span>
<span data-ttu-id="5882f-132">Alle typer anleggsmiddeltransaksjoner kan posteres på siden Økonomijournal.</span><span class="sxs-lookup"><span data-stu-id="5882f-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="5882f-133">Du kan også bruke journaler i Anleggsmidler til å postere anleggsmiddeltransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5882f-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="5882f-134">Alternativer for å angi anleggsmiddeltransaksjonstyper</span><span class="sxs-lookup"><span data-stu-id="5882f-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="5882f-135">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="5882f-135">Transaction type</span></span>                    | <span data-ttu-id="5882f-136">Modul</span><span class="sxs-lookup"><span data-stu-id="5882f-136">Module</span></span>                   | <span data-ttu-id="5882f-137">Opsjoner</span><span class="sxs-lookup"><span data-stu-id="5882f-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="5882f-138">Anskaffelse, Anskaffelsesjustering</span><span class="sxs-lookup"><span data-stu-id="5882f-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="5882f-139">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="5882f-139">Fixed assets</span></span>             | <span data-ttu-id="5882f-140">Anleggsmidler, Beholdning til anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="5882f-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="5882f-141">Økonomimodul</span><span class="sxs-lookup"><span data-stu-id="5882f-141">General ledger</span></span>           | <span data-ttu-id="5882f-142">Økonomijournal</span><span class="sxs-lookup"><span data-stu-id="5882f-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="5882f-143">Leverandører</span><span class="sxs-lookup"><span data-stu-id="5882f-143">Accounts payable</span></span>         | <span data-ttu-id="5882f-144">Fakturajournal, Fakturagodkjenningsjournal</span><span class="sxs-lookup"><span data-stu-id="5882f-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="5882f-145">Innkjøp og leverandører</span><span class="sxs-lookup"><span data-stu-id="5882f-145">Procurement and sourcing</span></span> | <span data-ttu-id="5882f-146">Bestilling</span><span class="sxs-lookup"><span data-stu-id="5882f-146">Purchase order</span></span>                            |
| <span data-ttu-id="5882f-147">Avskrivning</span><span class="sxs-lookup"><span data-stu-id="5882f-147">Depreciation</span></span>                        | <span data-ttu-id="5882f-148">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="5882f-148">Fixed assets</span></span>             | <span data-ttu-id="5882f-149">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="5882f-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="5882f-150">Økonomimodul</span><span class="sxs-lookup"><span data-stu-id="5882f-150">General ledger</span></span>           | <span data-ttu-id="5882f-151">Økonomijournal</span><span class="sxs-lookup"><span data-stu-id="5882f-151">General journal</span></span>                           |
| <span data-ttu-id="5882f-152">Avhending</span><span class="sxs-lookup"><span data-stu-id="5882f-152">Disposal</span></span>                            | <span data-ttu-id="5882f-153">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="5882f-153">Fixed assets</span></span>             | <span data-ttu-id="5882f-154">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="5882f-154">Fixed assets</span></span>                              |
| <span data-ttu-id="5882f-155">** **</span><span class="sxs-lookup"><span data-stu-id="5882f-155">** **</span></span>                               | <span data-ttu-id="5882f-156">Økonomimodul</span><span class="sxs-lookup"><span data-stu-id="5882f-156">General ledger</span></span>           | <span data-ttu-id="5882f-157">Økonomijournal</span><span class="sxs-lookup"><span data-stu-id="5882f-157">General journal</span></span>                           |
| <span data-ttu-id="5882f-158">** **</span><span class="sxs-lookup"><span data-stu-id="5882f-158">** **</span></span>                               | <span data-ttu-id="5882f-159">Kundereskontro</span><span class="sxs-lookup"><span data-stu-id="5882f-159">Accounts receivable</span></span>      | <span data-ttu-id="5882f-160">Fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="5882f-160">Free text invoice</span></span>                         |



<span data-ttu-id="5882f-161">Hvis du vil ha mer informasjon, se [Integrering av anleggsmidler](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="5882f-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




