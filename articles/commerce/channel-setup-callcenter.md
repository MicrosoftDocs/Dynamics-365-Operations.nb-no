---
title: Definere en telefonsenterkanal
description: Dette emnet beskriver hvordan du oppretter en ny telefonsenterkanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002456"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="e2e47-103">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="e2e47-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e2e47-104">Dette emnet beskriver hvordan du oppretter en ny telefonsenterkanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e2e47-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e2e47-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e2e47-105">Overview</span></span>

<span data-ttu-id="e2e47-106">I Dynamics 365 Commerce er et telefonsenter en type detaljhandelskanal som kan defineres i programmet.</span><span class="sxs-lookup"><span data-stu-id="e2e47-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="e2e47-107">Ved å definere en kanal for telefonsenterenheter kan systemet knytte bestemte data og ordrebehandlingsstandarder til salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="e2e47-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="e2e47-108">Et firma kan definere flere telefonsenterkanaler i Commerce.</span><span class="sxs-lookup"><span data-stu-id="e2e47-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="e2e47-109">Før du oppretter en ny telefonsenterkanal, må du kontrollere at du har oppfylt [Forutsetninger for kanaloppsett](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="e2e47-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="e2e47-110">Opprette og konfigurere en ny telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="e2e47-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="e2e47-111">Hvis du vil opprette og konfigurere en ny telefonsenterkanal, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="e2e47-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="e2e47-112">I navigasjonsruten går du til **Moduler \> Kanaler \> Telefonsentre \> Alle telefonsentre**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="e2e47-113">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e2e47-114">I **Navn**-feltet oppgir du et navn for den nye kanalen.</span><span class="sxs-lookup"><span data-stu-id="e2e47-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="e2e47-115">Velg den aktuelle **juridiske enheten** fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="e2e47-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="e2e47-116">Velg det aktuelle **lagerstedet** fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="e2e47-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="e2e47-117">Angi en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="e2e47-118">I feltet **Profil for e-postvarsling** oppgir du en gyldig profil for e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="e2e47-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="e2e47-119">Angi en infokode for **Prisoverstyring**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="e2e47-120">Merk at du kanskje må opprette en informasjonskode for dette først.</span><span class="sxs-lookup"><span data-stu-id="e2e47-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="e2e47-121">Oppgi en infokode for **Sperrekode**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="e2e47-122">Merk at du kanskje må opprette en informasjonskode for dette først.</span><span class="sxs-lookup"><span data-stu-id="e2e47-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="e2e47-123">Angi en infokode for **Kreditt**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="e2e47-124">Merk at du kanskje må opprette en informasjonskode for dette først.</span><span class="sxs-lookup"><span data-stu-id="e2e47-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="e2e47-125">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-125">Select **Save**.</span></span>

<span data-ttu-id="e2e47-126">Bildet nedenfor viser opprettelsen av en ny telefonsenterkanal.</span><span class="sxs-lookup"><span data-stu-id="e2e47-126">The following image shows the creation of a new call center channel.</span></span>

![Ny telefonsenterkanal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="e2e47-128">Bildet nedenfor viser et eksempel på en telefonsenterkanal.</span><span class="sxs-lookup"><span data-stu-id="e2e47-128">The following image shows an example call center channel.</span></span>

![Eksempel på telefonsenterkanal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="e2e47-130">Ekstra kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="e2e47-130">Additional channel setup</span></span>

<span data-ttu-id="e2e47-131">Andre oppgaver som kreves for oppsett av telefonsenterkanal, omfatter definere betalingsmåter og leveringsmåter.</span><span class="sxs-lookup"><span data-stu-id="e2e47-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="e2e47-132">Bildet nedenfor viser oppsettsalternativene **Leveringsmåter** og **Betalingsmåter** i kategorien **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Ekstra konfigurasjonshandlinger for telefonsenterkanal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="e2e47-134">Definere betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="e2e47-134">Set up payment methods</span></span>

<span data-ttu-id="e2e47-135">Hvis du vil definere betalingsmåter, følger du disse trinnene for hver betalingstype som støttes på denne kanalen.</span><span class="sxs-lookup"><span data-stu-id="e2e47-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="e2e47-136">I handlingsruten velger du kategorien **Oppsett** og deretter **Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="e2e47-137">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e2e47-138">Velg en ønsket betalingsmåte i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="e2e47-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="e2e47-139">I delen **Generelt** angir du et **operasjonsnavn** og konfigurerer eventuelle andre ønskede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="e2e47-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="e2e47-140">Konfigurer eventuelle tilleggsinnstillinger som kreves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="e2e47-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="e2e47-141">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e2e47-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="e2e47-142">Bildet nedenfor viser et eksempel på en kontantbetalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="e2e47-142">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmåter](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="e2e47-144">Definer leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="e2e47-144">Set up modes of delivery</span></span>

<span data-ttu-id="e2e47-145">Du kan se de konfigurerte leveringsmåtene ved å velge **Leveringsmåter** fra kategorien **Oppsett** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="e2e47-146">Hvis du vil endre eller legge til en leveringsmåte, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="e2e47-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="e2e47-147">I navigasjonsruten går du til **Moduler \> Lagerstyring \> Leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="e2e47-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="e2e47-148">Velg **Ny** i handlingsruten for å opprette en ny leveringsmåte, eller velg en eksisterende måte.</span><span class="sxs-lookup"><span data-stu-id="e2e47-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="e2e47-149">I delen **Detaljhandelskanaler** velger du **Legg til linje** for å legge til kanalen.</span><span class="sxs-lookup"><span data-stu-id="e2e47-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="e2e47-150">Legge til kanaler ved hjelp av organisasjonsnoder i stedet for å legge til hver kanal for seg, kan effektivisere tillegg av kanaler</span><span class="sxs-lookup"><span data-stu-id="e2e47-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="e2e47-151">Bildet nedenfor viser et eksempel på en leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="e2e47-151">The following image shows an example of a mode of delivery.</span></span>

![Definer leveringsmåter](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="e2e47-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e2e47-153">Additional resources</span></span>

[<span data-ttu-id="e2e47-154">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="e2e47-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="e2e47-155">Salgsfunksjonalitet for telefonsenter</span><span class="sxs-lookup"><span data-stu-id="e2e47-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="e2e47-156">Definere ordrebehandlingsalternativer for telefonsenter</span><span class="sxs-lookup"><span data-stu-id="e2e47-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="e2e47-157">Telefonsenterkataloger</span><span class="sxs-lookup"><span data-stu-id="e2e47-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="e2e47-158">Definere og arbeide med svindelvarsler</span><span class="sxs-lookup"><span data-stu-id="e2e47-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="e2e47-159">Definere kontinuitetsprogrammer for telefonsentre</span><span class="sxs-lookup"><span data-stu-id="e2e47-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
