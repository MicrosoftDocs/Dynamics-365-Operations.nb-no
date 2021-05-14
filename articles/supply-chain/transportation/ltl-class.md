---
title: Mindre enn vognlastklasser
description: Dette emnet beskriver hva mindre enn vognlastklasser (LTL) er, og beskriver hvordan du konfigurerer dem i Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941816"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="1d38c-103">Mindre enn vognlastklasser</span><span class="sxs-lookup"><span data-stu-id="1d38c-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d38c-104">En mindre enn vognlast-klasse (LTL) er en fraktforsendelsesklasse som brukes til å klassifisere varer som kan sendes.</span><span class="sxs-lookup"><span data-stu-id="1d38c-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="1d38c-105">Hver type produkt eller vare har vanligvis en NMFC-kode (National Motor Freight Classification) som tilsvarer et bestemt fraktklassenummer for LTL-forsendelser.</span><span class="sxs-lookup"><span data-stu-id="1d38c-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="1d38c-106">LTL-fraktklasser representerer varekategorier, mens NMFC-koder er relatert til bestemte varer i hver av de 18 fraktklassene.</span><span class="sxs-lookup"><span data-stu-id="1d38c-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="1d38c-107">Denne funksjonen lar deg bruke systemet til å utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="1d38c-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="1d38c-108">Definer LTL-fraktklassene som brukes i firmaet.</span><span class="sxs-lookup"><span data-stu-id="1d38c-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="1d38c-109">Tilordne hver LTL-klasse til en NMFC-kode på **NMFC-koder**-siden.</span><span class="sxs-lookup"><span data-stu-id="1d38c-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="1d38c-110">Hvis du vil ha mer informasjon, kan du se [NMFC-koder (National Motor Freight)](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1d38c-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="1d38c-111">Tilordne en NMFC-kode (og dermed den tilknyttet LTL-koden) til hvert produkt på **Produkt**-siden.</span><span class="sxs-lookup"><span data-stu-id="1d38c-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="1d38c-112">En nøyaktig evaluering av LTL-klassen for hvert produkt som en NMFC-kode er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="1d38c-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="1d38c-113">Fastgjør emballasjekrav for hver LTL-klasse ved å kontrollere de internasjonale LTL-standardene.</span><span class="sxs-lookup"><span data-stu-id="1d38c-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="1d38c-114">På denne måten sikrer du at produktene er godt beskyttet og trygt sendt.</span><span class="sxs-lookup"><span data-stu-id="1d38c-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="1d38c-115">Få nøyaktige forsendelsesestimater, basert på LTL-fraktklassen for hvert produkt.</span><span class="sxs-lookup"><span data-stu-id="1d38c-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="1d38c-116">Dette emnet beskriver hvordan du oppretter LTL-klassene i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1d38c-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="1d38c-117">Opprette en LTL-klasse</span><span class="sxs-lookup"><span data-stu-id="1d38c-117">Create an LTL class</span></span>

<span data-ttu-id="1d38c-118">Hvis du vil opprette en LTL-klasse, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="1d38c-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="1d38c-119">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="1d38c-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="1d38c-120">Gå til **Lagerstyring \> Oppsett \> Lager \> LTL-klasser**.</span><span class="sxs-lookup"><span data-stu-id="1d38c-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="1d38c-121">Gå til **Transportstyring \> Oppsett \> Transportstandarder \> LTL-klasser**.</span><span class="sxs-lookup"><span data-stu-id="1d38c-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="1d38c-122">I handlingsruten velger du **Ny** for å opprette en LTL-klasse.</span><span class="sxs-lookup"><span data-stu-id="1d38c-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="1d38c-123">Deretter angir du følgende felt:</span><span class="sxs-lookup"><span data-stu-id="1d38c-123">Then set the following fields:</span></span>

    - <span data-ttu-id="1d38c-124">**LTL-klasse** – Angi firmaets interne LTL-klasse-ID for varetypen.</span><span class="sxs-lookup"><span data-stu-id="1d38c-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="1d38c-125">De fleste firmaer bruker den internasjonale standarden.</span><span class="sxs-lookup"><span data-stu-id="1d38c-125">Most companies use the international standard.</span></span> <span data-ttu-id="1d38c-126">I så fall vil verdien i dette feltet samsvare med verdien i **Klasse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1d38c-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="1d38c-127">Hvis firmaet imidlertid bruker sin egen standard, angir du en kode som oppfyller denne standarden.</span><span class="sxs-lookup"><span data-stu-id="1d38c-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="1d38c-128">**Navn** – Angi et beskrivende navn som vil hjelpe deg og andre brukere med å velge riktig LTL-klasse for hver NMFC-kode.</span><span class="sxs-lookup"><span data-stu-id="1d38c-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="1d38c-129">**Klasse** – Angi den internasjonale standard LTL-klasse-IDen for varetypen.</span><span class="sxs-lookup"><span data-stu-id="1d38c-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="1d38c-130">Koden du angir her, må oppfylle den offisielle standarden.</span><span class="sxs-lookup"><span data-stu-id="1d38c-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="1d38c-131">Eksempel: Konfigurere LTL-klasser</span><span class="sxs-lookup"><span data-stu-id="1d38c-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="1d38c-132">Følgende eksempel viser hvordan du konfigurerer to ulike LTL-klasser som du kan bruke med forskjellige typer produkter.</span><span class="sxs-lookup"><span data-stu-id="1d38c-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="1d38c-133">Gå til **Lagerstyring \> Oppsett \> Lager \> LTL-klasser**.</span><span class="sxs-lookup"><span data-stu-id="1d38c-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="1d38c-134">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1d38c-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1d38c-135">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="1d38c-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1d38c-136">**LTL-klasse:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="1d38c-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="1d38c-137">**Navn:** *Datamaskiner, skjermer, kjøleskap*</span><span class="sxs-lookup"><span data-stu-id="1d38c-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="1d38c-138">**Klasse:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="1d38c-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="1d38c-139">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1d38c-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1d38c-140">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1d38c-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1d38c-141">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="1d38c-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1d38c-142">**LTL-klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="1d38c-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="1d38c-143">**Navn:** *Små hvitevarer*</span><span class="sxs-lookup"><span data-stu-id="1d38c-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="1d38c-144">**Klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="1d38c-144">**Class:** *125*</span></span>

1. <span data-ttu-id="1d38c-145">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1d38c-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d38c-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1d38c-146">Additional resources</span></span>

- [<span data-ttu-id="1d38c-147">NMFC-koder (National Motor Freight Classification)</span><span class="sxs-lookup"><span data-stu-id="1d38c-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="1d38c-148">Opprette et fraktbrev</span><span class="sxs-lookup"><span data-stu-id="1d38c-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
