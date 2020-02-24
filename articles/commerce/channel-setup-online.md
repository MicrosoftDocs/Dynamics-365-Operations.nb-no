---
title: Definere en Internett-kanal
description: Dette emnet beskriver hvordan du oppretter en ny Internett-kanal i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002433"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="49d14-103">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="49d14-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="49d14-104">Dette emnet beskriver hvordan du oppretter en ny Internett-kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="49d14-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="49d14-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="49d14-105">Overview</span></span>

<span data-ttu-id="49d14-106">Dynamics 365 Commerce støtter flere kanaler for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="49d14-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="49d14-107">Disse detaljhandelskanalene omfatter nettbutikker, telefonsentre og detaljhandelsbutikker (også kalt fysiske butikker).</span><span class="sxs-lookup"><span data-stu-id="49d14-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="49d14-108">Med en nettbutikk kan kundene kjøpe produkter i forhandlerens nettbutikk i tillegg til den vanlige butikken.</span><span class="sxs-lookup"><span data-stu-id="49d14-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="49d14-109">Hvis du vil opprette en nettbutikk i Commerce, må du først opprette en Internett-kanal.</span><span class="sxs-lookup"><span data-stu-id="49d14-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="49d14-110">Før du oppretter en ny Internett-kanal, må du kontrollere at du har oppfylt [Forutsetninger for kanaloppsett](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="49d14-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="49d14-111">Opprette og konfigurere en ny Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="49d14-111">Create and configure a new online channel</span></span>

<span data-ttu-id="49d14-112">Hvis du vil opprette og konfigurere en ny Internett-kanal, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="49d14-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="49d14-113">I navigasjonsruten går du til **Moduler \> Kanaler \> Nettbutikker**.</span><span class="sxs-lookup"><span data-stu-id="49d14-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="49d14-114">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="49d14-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="49d14-115">I **Navn**-feltet oppgir du et navn for den nye kanalen.</span><span class="sxs-lookup"><span data-stu-id="49d14-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="49d14-116">Angi den riktige juridiske enheten i rullegardinlisten **Juridisk enhet**.</span><span class="sxs-lookup"><span data-stu-id="49d14-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="49d14-117">Angi det riktige lageret i rullegardinlisten **Lager**.</span><span class="sxs-lookup"><span data-stu-id="49d14-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="49d14-118">Velg riktig tidssone i feltet **Tidssone for butikk**.</span><span class="sxs-lookup"><span data-stu-id="49d14-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="49d14-119">Velg riktig valuta i **Valuta**-feltet.</span><span class="sxs-lookup"><span data-stu-id="49d14-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="49d14-120">Angi en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="49d14-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="49d14-121">Angi en gyldig adressebok i feltet **Adressebok for kunde**.</span><span class="sxs-lookup"><span data-stu-id="49d14-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="49d14-122">I feltet **Funksjonalitetsprofil** velger du en funksjonalitetsprofil hvis det er aktuelt.</span><span class="sxs-lookup"><span data-stu-id="49d14-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="49d14-123">I feltet **Profil for e-postvarsling** oppgir du en gyldig profil for e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="49d14-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="49d14-124">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="49d14-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="49d14-125">Bildet nedenfor viser opprettelsen av en ny Internett-kanal.</span><span class="sxs-lookup"><span data-stu-id="49d14-125">The following image shows the creation of a new online channel.</span></span>

![Ny Internett-kanal](media/channel-setup-online-1.png)

<span data-ttu-id="49d14-127">Bildet nedenfor viser et eksempel på en Internett-kanal.</span><span class="sxs-lookup"><span data-stu-id="49d14-127">The following image shows an example online channel.</span></span>

![Eksempel på Internett-kanal](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="49d14-129">Definere språk</span><span class="sxs-lookup"><span data-stu-id="49d14-129">Set up languages</span></span>

<span data-ttu-id="49d14-130">Hvis området for e-handel støtter flere språk, kan du utvide delen **Språk** og legge til flere språk etter behov.</span><span class="sxs-lookup"><span data-stu-id="49d14-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="49d14-131">Definere betalingskonto</span><span class="sxs-lookup"><span data-stu-id="49d14-131">Set up payment account</span></span>

<span data-ttu-id="49d14-132">I delen **Betalingskonto** kan du legge til en tredjeparts betalingsleverandør.</span><span class="sxs-lookup"><span data-stu-id="49d14-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="49d14-133">Hvis du vil ha informasjon om hvordan du definerer en Adyen-betalingskobling, kan du se [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="49d14-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="49d14-134">Ekstra kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="49d14-134">Additional channel set up</span></span>

<span data-ttu-id="49d14-135">Andre oppgaver som kreves for oppsett av Internett-kanal, omfatter definere betalingsmåter, leveringsmåter og gruppetilordning for oppfyllelse.</span><span class="sxs-lookup"><span data-stu-id="49d14-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="49d14-136">Bildet nedenfor viser oppsettsalternativene **Leveringsmåter**, **Betalingsmåter** og **Gruppetilordning for oppfyllelse** i kategorien **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="49d14-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Ekstra konfigurasjonshandlinger for Internett-kanal](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="49d14-138">Definere betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="49d14-138">Set up payment methods</span></span>

<span data-ttu-id="49d14-139">Hvis du vil definere betalingsmåter, følger du disse trinnene for hver betalingstype som støttes på denne kanalen.</span><span class="sxs-lookup"><span data-stu-id="49d14-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="49d14-140">I handlingsruten velger du kategorien **Oppsett** og deretter **Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="49d14-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="49d14-141">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="49d14-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="49d14-142">Velg en ønsket betalingsmåte i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="49d14-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="49d14-143">I delen **Generelt** angir du et **operasjonsnavn** og konfigurerer eventuelle andre ønskede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="49d14-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="49d14-144">Konfigurer eventuelle tilleggsinnstillinger som kreves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="49d14-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="49d14-145">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="49d14-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="49d14-146">Bildet nedenfor viser et eksempel på en kontantbetalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="49d14-146">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmåter](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="49d14-148">Definer leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="49d14-148">Set up modes of delivery</span></span>

<span data-ttu-id="49d14-149">Du kan se de konfigurerte leveringsmåtene ved å velge **Leveringsmåter** fra kategorien **Oppsett** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="49d14-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="49d14-150">Hvis du vil endre eller legge til en leveringsmåte, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="49d14-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="49d14-151">I navigasjonsruten går du til **Moduler \> Lagerstyring \> Leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="49d14-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="49d14-152">Velg **Ny** i handlingsruten for å opprette en ny leveringsmåte, eller velg en eksisterende måte.</span><span class="sxs-lookup"><span data-stu-id="49d14-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="49d14-153">I delen **Detaljhandelskanaler** velger du **Legg til linje** for å legge til kanalen.</span><span class="sxs-lookup"><span data-stu-id="49d14-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="49d14-154">Legge til kanaler ved hjelp av organisasjonsnoder i stedet for å legge til hver kanal for seg, kan effektivisere tillegg av kanaler</span><span class="sxs-lookup"><span data-stu-id="49d14-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="49d14-155">Bildet nedenfor viser et eksempel på en leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="49d14-155">The following image shows an example of a mode of delivery.</span></span>

![Definer leveringsmåter](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="49d14-157">Definere en gruppetilordning for oppfyllelse</span><span class="sxs-lookup"><span data-stu-id="49d14-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="49d14-158">Hvis du vil konfigurere en gruppetilordning for oppfyllelse, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="49d14-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="49d14-159">I handlingsruten velger du kategorien **Oppsett** og deretter **Gruppetilordning for oppfyllelse**.</span><span class="sxs-lookup"><span data-stu-id="49d14-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="49d14-160">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="49d14-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="49d14-161">I rullegardinlisten **Oppfyllelsesgruppe** velger du en oppfyllelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="49d14-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="49d14-162">Angi en beskrivelse i rullegardinlisten **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="49d14-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="49d14-163">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="49d14-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="49d14-164">Det følgende bildet viser et eksempel på et oppsett for gruppetilordning for oppfyllelse.</span><span class="sxs-lookup"><span data-stu-id="49d14-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Definere gruppetilordning for oppfyllelse](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="49d14-166">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="49d14-166">Additional resources</span></span>

[<span data-ttu-id="49d14-167">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="49d14-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="49d14-168">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="49d14-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="49d14-169">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="49d14-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="49d14-170">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="49d14-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="49d14-171">Dynamics 365 Payment Connector for Adyen</span><span class="sxs-lookup"><span data-stu-id="49d14-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
