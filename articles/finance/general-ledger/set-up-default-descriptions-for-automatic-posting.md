---
title: Definere standardbeskrivelser for automatisk postering
description: Dette emnet forklarer hvordan du definerer standardtekst som brukes til å beskrive regnskapsoppføringer som posteres automatisk til økonomimodulen. Du kan definere standard beskrivelsestekst ved å bruke frihåndstekst eller velge faste variabler.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5fc73f636a5cac25c259ce2cbae5c5407dca9b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446227"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="d7831-104">Definere standardbeskrivelser for automatisk postering</span><span class="sxs-lookup"><span data-stu-id="d7831-104">Set up default descriptions for automatic posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7831-105">Dette emnet forklarer hvordan du definerer standardtekst som brukes til å beskrive regnskapsoppføringer som posteres automatisk til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="d7831-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="d7831-106">Du kan definere standard beskrivelsestekst ved å bruke frihåndstekst eller velge faste variabler.</span><span class="sxs-lookup"><span data-stu-id="d7831-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="d7831-107">For enkelte transaksjonstyper i noen land eller områder kan du også inkludere tekst fra felter i Microsoft Dynamics AX-databasen som er relatert til disse transaksjonstypene.</span><span class="sxs-lookup"><span data-stu-id="d7831-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="d7831-108">Hvis du vil ha en liste over transaksjonstypene og landene og regionene, se [Valgfritt: Legge til annen tekst i standardbeskrivelser](#optional-add-other-text-to-default-descriptions) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="d7831-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="d7831-109">Definere standardbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="d7831-109">Set up default descriptions</span></span>

1. <span data-ttu-id="d7831-110">Gå til **Organisasjonsstyring** \> **Oppsett** \> **Standardbeskrivelser**.</span><span class="sxs-lookup"><span data-stu-id="d7831-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="d7831-111">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d7831-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="d7831-112">Velg transaksjonstypen du vil opprette en standardbeskrivelse for i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="d7831-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="d7831-113">I **Språk**-feltet velger du språket denne beskrivelsen gjelder for.</span><span class="sxs-lookup"><span data-stu-id="d7831-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="d7831-114">I **Tekst**-feltet angir du standardbeskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="d7831-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="d7831-115">Du kan skrive inn tekst i feltet, eller du kan bruke én eller flere av de følgende fritekstvariablene:</span><span class="sxs-lookup"><span data-stu-id="d7831-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="d7831-116">**%1** – Legg til transaksjonsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d7831-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="d7831-117">**%2** – Legg til en identifikator som tilsvarer dokumenttypen som posteres til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="d7831-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="d7831-118">Fo transaksjonstyper som er relatert til fakturaer for eksempel, legger variabelen **%2** til fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="d7831-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="d7831-119">**%3** – Legg til en identifikator som er relatert til dokumenttypen som posteres til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="d7831-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="d7831-120">For transaksjonstyper som er relatert til fakturaer for eksempel, legger variabelen **%3** til kundens kontonummer.</span><span class="sxs-lookup"><span data-stu-id="d7831-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="d7831-121">Valgfritt: Legge til annen tekst i standardbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="d7831-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="d7831-122">For enkelte transaksjonstyper i noen land eller områder, kan tekst inkluderes i standardbeskrivelsene som kommer fra felt i dataene som er relatert til disse transaksjonstypene.</span><span class="sxs-lookup"><span data-stu-id="d7831-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="d7831-123">Følgende liste viser transaksjonstyper og land/områder som dette alternativet er tilgjengelig for.</span><span class="sxs-lookup"><span data-stu-id="d7831-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="d7831-124">**Transaksjonstyper**</span><span class="sxs-lookup"><span data-stu-id="d7831-124">**Transaction types**</span></span>

<span data-ttu-id="d7831-125">Du kan legge til annen tekst i standardbeskrivelser for transaksjonstyper som er knyttet til følgende dokumenttyper:</span><span class="sxs-lookup"><span data-stu-id="d7831-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="d7831-126">Kundefakturaer</span><span class="sxs-lookup"><span data-stu-id="d7831-126">Customer invoices</span></span>
- <span data-ttu-id="d7831-127">Kundekredittnotaer</span><span class="sxs-lookup"><span data-stu-id="d7831-127">Customer credit notes</span></span>
- <span data-ttu-id="d7831-128">Kundekontantbetalinger</span><span class="sxs-lookup"><span data-stu-id="d7831-128">Customer cash payments</span></span>
- <span data-ttu-id="d7831-129">Leverandørbetalinger</span><span class="sxs-lookup"><span data-stu-id="d7831-129">Vendor payments</span></span>
- <span data-ttu-id="d7831-130">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="d7831-130">Sales orders</span></span>
- <span data-ttu-id="d7831-131">Bestillinger</span><span class="sxs-lookup"><span data-stu-id="d7831-131">Purchase orders</span></span>
- <span data-ttu-id="d7831-132">Lagerjournaler</span><span class="sxs-lookup"><span data-stu-id="d7831-132">Inventory journals</span></span>
- <span data-ttu-id="d7831-133">Hovedplanlegging (MPS)</span><span class="sxs-lookup"><span data-stu-id="d7831-133">Master planning (MRP)</span></span>
- <span data-ttu-id="d7831-134">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="d7831-134">Fixed assets</span></span>

<span data-ttu-id="d7831-135">**Land og områder**</span><span class="sxs-lookup"><span data-stu-id="d7831-135">**Countries and regions**</span></span>

<span data-ttu-id="d7831-136">Dette alternativet er tilgjengelig for følgende land og regioner:</span><span class="sxs-lookup"><span data-stu-id="d7831-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="d7831-137">Brasil</span><span class="sxs-lookup"><span data-stu-id="d7831-137">Brazil</span></span>
- <span data-ttu-id="d7831-138">Kina</span><span class="sxs-lookup"><span data-stu-id="d7831-138">China</span></span>
- <span data-ttu-id="d7831-139">Tsjekkia</span><span class="sxs-lookup"><span data-stu-id="d7831-139">Czech Republic</span></span>
- <span data-ttu-id="d7831-140">Øst-Europa</span><span class="sxs-lookup"><span data-stu-id="d7831-140">Eastern Europe</span></span>
- <span data-ttu-id="d7831-141">Ungarn</span><span class="sxs-lookup"><span data-stu-id="d7831-141">Hungary</span></span>
- <span data-ttu-id="d7831-142">India</span><span class="sxs-lookup"><span data-stu-id="d7831-142">India</span></span>
- <span data-ttu-id="d7831-143">Japan</span><span class="sxs-lookup"><span data-stu-id="d7831-143">Japan</span></span>
- <span data-ttu-id="d7831-144">Litauen</span><span class="sxs-lookup"><span data-stu-id="d7831-144">Lithuania</span></span>
- <span data-ttu-id="d7831-145">Latvia</span><span class="sxs-lookup"><span data-stu-id="d7831-145">Latvia</span></span>
- <span data-ttu-id="d7831-146">Polen</span><span class="sxs-lookup"><span data-stu-id="d7831-146">Poland</span></span>
- <span data-ttu-id="d7831-147">Russland</span><span class="sxs-lookup"><span data-stu-id="d7831-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="d7831-148">Legge til tekst i standardbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="d7831-148">Add text to default descriptions</span></span>

<span data-ttu-id="d7831-149">Når du har fullført trinnene i [Definere standardbeskrivelser](#set-up-default-descriptions) tidligere i dette emnet, følger du denne fremgangsmåten for å legge til annen tekst i standardbeskrivelsene.</span><span class="sxs-lookup"><span data-stu-id="d7831-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="d7831-150">Velg **Legg til** på hurtigfanen **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="d7831-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="d7831-151">Velg databasetabellen du vil legge til parameterdata i beskrivelsen fra, i **Referansetabell**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d7831-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="d7831-152">Velg feltet du vil legge til parameterdata i beskrivelsen fra, i **Referansefelt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d7831-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="d7831-153">Gjenta trinn 1 til og med 3 hvis du vil legge til flere parametere.</span><span class="sxs-lookup"><span data-stu-id="d7831-153">Repeat steps 1 through 3 to add more parameters.</span></span>
