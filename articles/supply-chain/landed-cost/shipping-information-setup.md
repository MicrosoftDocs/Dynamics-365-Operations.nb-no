---
title: Konfigurasjon av forsendelsesinformasjon
description: Dette emnet beskriver hvordan du definerer forsendelsesinformasjon for modulen Netto innkjøpspris.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5093e42b0b5247c24c271ad50c80889516586d58
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020893"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="196bc-103">Konfigurasjon av forsendelsesinformasjon</span><span class="sxs-lookup"><span data-stu-id="196bc-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="196bc-104">Dette emnet beskriver hvordan du definerer forsendelsesinformasjon for modulen **Netto innkjøpspris**.</span><span class="sxs-lookup"><span data-stu-id="196bc-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="196bc-105">Beskrivelse av varer</span><span class="sxs-lookup"><span data-stu-id="196bc-105">Description of goods</span></span>

<span data-ttu-id="196bc-106">Beskrivelser av varer hjelper til med å identifisere en sjøreise, forsendelsescontainer eller last og varene i den.</span><span class="sxs-lookup"><span data-stu-id="196bc-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="196bc-107">Du kan velge en beskrivelse av varer i forsendelsescontainerens topptekst eller i foliotoppteksten.</span><span class="sxs-lookup"><span data-stu-id="196bc-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="196bc-108">Hvis du vil jobbe med varebeskrivelser, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Beskrivelse av varer**.</span><span class="sxs-lookup"><span data-stu-id="196bc-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="196bc-109">Der kan du vise, åpne, opprette og slette poster for beskrivelser av varer.</span><span class="sxs-lookup"><span data-stu-id="196bc-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="196bc-110">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="196bc-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="196bc-111">Felt</span><span class="sxs-lookup"><span data-stu-id="196bc-111">Field</span></span> | <span data-ttu-id="196bc-112">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-112">Description</span></span> |
|---|---|
| <span data-ttu-id="196bc-113">Beskrivelse av varer</span><span class="sxs-lookup"><span data-stu-id="196bc-113">Description of goods</span></span> | <span data-ttu-id="196bc-114">Angi et unikt identifikasjonsnavn/-nummer for varetypen som skal bruke denne beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="196bc-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="196bc-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-115">Description</span></span> | <span data-ttu-id="196bc-116">Angi en beskrivelse av varetypen i denne kategorien.</span><span class="sxs-lookup"><span data-stu-id="196bc-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="196bc-117">Fartøy</span><span class="sxs-lookup"><span data-stu-id="196bc-117">Vessels</span></span>

<span data-ttu-id="196bc-118">Et fartøy er det unike navn på et skip eller transportmiddel som brukes av et forsendelsesfirma eller byrå.</span><span class="sxs-lookup"><span data-stu-id="196bc-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="196bc-119">Når du oppretter en sjøreise, må du alltid velge eller legge inn et transportmiddel for sjøreisen.</span><span class="sxs-lookup"><span data-stu-id="196bc-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="196bc-120">Hvis du ofte bruker de samme transportmidlene, kan du gjøre det raskere og enklere å opprette en ny sjøreise ved å opprette en transportmiddelpost for hver av dem. Dermed gir du brukerne muligheten til å velge transportmidlet fra en liste i stedet for å oppgi navnet eller nummeret manuelt hver gang.</span><span class="sxs-lookup"><span data-stu-id="196bc-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="196bc-121">Hvis du vil arbeide med transportmidler, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Transportmidler**.</span><span class="sxs-lookup"><span data-stu-id="196bc-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="196bc-122">Der kan du vise, åpne, opprette og slette poster for transportmidler.</span><span class="sxs-lookup"><span data-stu-id="196bc-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="196bc-123">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="196bc-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="196bc-124">Felt</span><span class="sxs-lookup"><span data-stu-id="196bc-124">Field</span></span> | <span data-ttu-id="196bc-125">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-125">Description</span></span> |
|---|---|
| <span data-ttu-id="196bc-126">Fartøy</span><span class="sxs-lookup"><span data-stu-id="196bc-126">Vessel</span></span> | <span data-ttu-id="196bc-127">Angi et unikt identifikasjonsnavn/-nummer for skipet som skal brukes til å transportere varer på en sjøreise.</span><span class="sxs-lookup"><span data-stu-id="196bc-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="196bc-128">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-128">Description</span></span> | <span data-ttu-id="196bc-129">Angi en beskrivelse av transportmidlet.</span><span class="sxs-lookup"><span data-stu-id="196bc-129">Enter a description of the vessel.</span></span> <span data-ttu-id="196bc-130">Denne beskrivelsen identifiserer vanligvis navnet på skipet og forsendelsesfirmaet/-agenten.</span><span class="sxs-lookup"><span data-stu-id="196bc-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="196bc-131">Leveringsmiddel</span><span class="sxs-lookup"><span data-stu-id="196bc-131">Mode of delivery</span></span> | <span data-ttu-id="196bc-132">Velg leveringsmåten som for eksempel transportmidlet bruker (for eksempel _Lufttransport_, _Sjøtransport_ eller _Togtransport_).</span><span class="sxs-lookup"><span data-stu-id="196bc-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="196bc-133">Eksportører</span><span class="sxs-lookup"><span data-stu-id="196bc-133">Exporters</span></span>

<span data-ttu-id="196bc-134">Hver eksportørpost identifiserer en leverandør eller eksportør som kan defineres som leverandøren for en sjøreise.</span><span class="sxs-lookup"><span data-stu-id="196bc-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="196bc-135">Eksportøren kan knyttes til en sjøreise og brukes til rapportering.</span><span class="sxs-lookup"><span data-stu-id="196bc-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="196bc-136">Hvis du vil arbeide med eksportører, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Eksportører**.</span><span class="sxs-lookup"><span data-stu-id="196bc-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="196bc-137">Der kan du vise, åpne, opprette og slette poster for eksportører.</span><span class="sxs-lookup"><span data-stu-id="196bc-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="196bc-138">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="196bc-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="196bc-139">Felt</span><span class="sxs-lookup"><span data-stu-id="196bc-139">Field</span></span> | <span data-ttu-id="196bc-140">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-140">Description</span></span> |
|---|---|
| <span data-ttu-id="196bc-141">Eksportør</span><span class="sxs-lookup"><span data-stu-id="196bc-141">Exporter</span></span> | <span data-ttu-id="196bc-142">Angi et unikt identifikasjonsnavn/-nummer for eksportøren av varer som blir transportert på en sjøreise.</span><span class="sxs-lookup"><span data-stu-id="196bc-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="196bc-143">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-143">Description</span></span> | <span data-ttu-id="196bc-144">Angi en beskrivelse av eksportøren.</span><span class="sxs-lookup"><span data-stu-id="196bc-144">Enter a description of the exporter.</span></span> <span data-ttu-id="196bc-145">Denne beskrivelsen identifiserer det fulle navnet på forsendelsesfirmaet/-agenten.</span><span class="sxs-lookup"><span data-stu-id="196bc-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="196bc-146">Artikkelkoder</span><span class="sxs-lookup"><span data-stu-id="196bc-146">Commodity codes</span></span>

<span data-ttu-id="196bc-147">Du bruker varekoder til å bidra med tollidentifikasjon og beregning av tollsatser for varer på en sjøreise.</span><span class="sxs-lookup"><span data-stu-id="196bc-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="196bc-148">Du kan velge varekoder på siden **Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="196bc-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="196bc-149">Hvis du vil arbeide med varekoder, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Varekoder**.</span><span class="sxs-lookup"><span data-stu-id="196bc-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="196bc-150">Der kan du vise, åpne, opprette og slette poster for varekoder.</span><span class="sxs-lookup"><span data-stu-id="196bc-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="196bc-151">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="196bc-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="196bc-152">Felt</span><span class="sxs-lookup"><span data-stu-id="196bc-152">Field</span></span> | <span data-ttu-id="196bc-153">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-153">Description</span></span> |
|---|---|
| <span data-ttu-id="196bc-154">Artikkelkode</span><span class="sxs-lookup"><span data-stu-id="196bc-154">Commodity code</span></span> | <span data-ttu-id="196bc-155">Angi en unik kode for denne typen vare.</span><span class="sxs-lookup"><span data-stu-id="196bc-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="196bc-156">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-156">Description</span></span> | <span data-ttu-id="196bc-157">Angi en beskrivelse av varetypen.</span><span class="sxs-lookup"><span data-stu-id="196bc-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="196bc-158">Tollbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-158">Customs description</span></span>

<span data-ttu-id="196bc-159">Tollbeskrivelser hjelper med å identifisere varer for tollformål.</span><span class="sxs-lookup"><span data-stu-id="196bc-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="196bc-160">Du kan velge en tollbeskrivelse på siden **Frigitte produkter** eller på bestillingslinjer.</span><span class="sxs-lookup"><span data-stu-id="196bc-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="196bc-161">Hvis du vil arbeide med tollbeskrivelser, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Tollbeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="196bc-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="196bc-162">Der kan du vise, åpne, opprette og slette poster for tollbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="196bc-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="196bc-163">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="196bc-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="196bc-164">Felt</span><span class="sxs-lookup"><span data-stu-id="196bc-164">Field</span></span> | <span data-ttu-id="196bc-165">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-165">Description</span></span> |
|---|---|
| <span data-ttu-id="196bc-166">Tollbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-166">Customs description</span></span> | <span data-ttu-id="196bc-167">Angi en unik kode for denne typen tollklassifikasjon.</span><span class="sxs-lookup"><span data-stu-id="196bc-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="196bc-168">Ofte vil denne koden være den offisielle beskrivelsen som formidles av en tollmyndighet for beskrivelsen og den kvalitative verdien av varene.</span><span class="sxs-lookup"><span data-stu-id="196bc-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="196bc-169">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="196bc-169">Description</span></span> | <span data-ttu-id="196bc-170">Angi en beskrivelse av tollklassifikasjonen.</span><span class="sxs-lookup"><span data-stu-id="196bc-170">Enter a description of the customs classification.</span></span> |
