---
title: Definere en telefonsenterkanal
description: Dette emnet beskriver hvordan du oppretter en ny telefonsenterkanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.openlocfilehash: 3f8c47c00b920dae01213d1d241ac8ee6a18d4e3
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/24/2020
ms.locfileid: "4414796"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="569c0-103">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="569c0-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="569c0-104">Dette emnet beskriver hvordan du oppretter en ny telefonsenterkanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="569c0-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="569c0-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="569c0-105">Overview</span></span>


<span data-ttu-id="569c0-106">I Dynamics 365 Commerce er et telefonsenter en type Commerce-kanal som kan defineres i programmet.</span><span class="sxs-lookup"><span data-stu-id="569c0-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="569c0-107">Ved å definere en kanal for telefonsenterenheter kan systemet knytte bestemte data og ordrebehandlingsstandarder til salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="569c0-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="569c0-108">Selv om et firma kan definere flere telefonsenterkanaler i Commerce, er det viktig å være oppmerksom på at en enkelt bruker bare kan kobles til én telefonsenterkanal.</span><span class="sxs-lookup"><span data-stu-id="569c0-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="569c0-109">Før du oppretter en ny telefonsenterkanal, må du kontrollere at du har oppfylt [Forutsetninger for kanaloppsett](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="569c0-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="569c0-110">Opprette og konfigurere en ny telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="569c0-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="569c0-111">Hvis du vil opprette og konfigurere en ny telefonsenterkanal, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="569c0-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="569c0-112">I navigasjonsruten går du til **Detaljhandel og handel \> Kanaler \> Telefonsentre \> Alle telefonsentre**.</span><span class="sxs-lookup"><span data-stu-id="569c0-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="569c0-113">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="569c0-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="569c0-114">I **Navn**-feltet oppgir du et navn for den nye kanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="569c0-115">Velg den aktuelle **juridiske enheten** fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="569c0-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="569c0-116">Velg det aktuelle **lagerstedet** fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="569c0-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="569c0-117">Denne lokasjonen brukes som standard på salgsordrer som er opprettet for denne telefonsenterkanalen, med mindre andre standarder er definert på kunde- eller varenivået.</span><span class="sxs-lookup"><span data-stu-id="569c0-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="569c0-118">Angi en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="569c0-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="569c0-119">Disse dataene brukes til å hjelpe med automatisk utfylling av standarder når nye kundeoppføringer opprettes.</span><span class="sxs-lookup"><span data-stu-id="569c0-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="569c0-120">Når du oppretter telefonsenterordrer, er det ikke lurt å opprette ordrer for standardkunden.</span><span class="sxs-lookup"><span data-stu-id="569c0-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="569c0-121">I feltet **Profil for e-postvarsling** oppgir du en gyldig profil for e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="569c0-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="569c0-122">Når telefonsenterordrer opprettes og behandles, brukes e-postvarslingsprofilen til å utløse automatiske e-postvarsler til kunder med informasjon om deres ordrestatus.</span><span class="sxs-lookup"><span data-stu-id="569c0-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="569c0-123">Angi en infokode for **Prisoverstyring**.</span><span class="sxs-lookup"><span data-stu-id="569c0-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="569c0-124">Du må kanskje opprette en informasjonskode for dette først.</span><span class="sxs-lookup"><span data-stu-id="569c0-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="569c0-125">Denne informasjonskoden gir et sett med årsakskoder som brukeren blir bedt om å velge blant når han/hun bruker funksjonen for prisoverstyring på en telefonsenterordre.</span><span class="sxs-lookup"><span data-stu-id="569c0-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="569c0-126">Oppgi en infokode for **Sperrekode**.</span><span class="sxs-lookup"><span data-stu-id="569c0-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="569c0-127">Du må kanskje opprette en informasjonskode for dette først.</span><span class="sxs-lookup"><span data-stu-id="569c0-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="569c0-128">Denne informasjonskoden gir et sett med valgfrie årsakskoder som brukeren blir bedt om å velge blant når han/hun setter en ordre på vent.</span><span class="sxs-lookup"><span data-stu-id="569c0-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="569c0-129">Angi en infokode for **Kreditt**.</span><span class="sxs-lookup"><span data-stu-id="569c0-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="569c0-130">Du må kanskje opprette en informasjonskode for dette først.</span><span class="sxs-lookup"><span data-stu-id="569c0-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="569c0-131">Denne informasjonskoden inneholder årsakskoder som brukeren kan velge blant ved bruk av funksjonen for ordrekreditt i telefonsenteret for å gi diverse refunderinger til kunden av hensyn til kundeservice.</span><span class="sxs-lookup"><span data-stu-id="569c0-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="569c0-132">Valgfritt: definer finansdimensjoner i hurtigfanen **Finansdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="569c0-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="569c0-133">Dimensjonene som angis her, brukes som standard på alle salgsordrer som er opprettet i denne telefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="569c0-134">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="569c0-134">Click **Save**.</span></span>

<span data-ttu-id="569c0-135">Bildet nedenfor viser opprettelsen av en ny telefonsenterkanal.</span><span class="sxs-lookup"><span data-stu-id="569c0-135">The following image shows the creation of a new call center channel.</span></span>

![Ny telefonsenterkanal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="569c0-137">Bildet nedenfor viser et eksempel på en telefonsenterkanal.</span><span class="sxs-lookup"><span data-stu-id="569c0-137">The following image shows an example call center channel.</span></span>

![Eksempel på telefonsenterkanal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="569c0-139">Ekstra kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="569c0-139">Additional channel setup</span></span>

<span data-ttu-id="569c0-140">Andre oppgaver som kreves for oppsett av telefonsenterkanal, omfatter definere betalingsmåter og leveringsmåter.</span><span class="sxs-lookup"><span data-stu-id="569c0-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="569c0-141">Bildet nedenfor viser oppsettsalternativene **Leveringsmåter** og **Betalingsmåter** i kategorien **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="569c0-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Ekstra konfigurasjonshandlinger for telefonsenterkanal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="569c0-143">Definere betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="569c0-143">Set up payment methods</span></span>

<span data-ttu-id="569c0-144">Hvis du vil definere betalingsmåter, følger du disse trinnene for hver betalingstype som støttes på denne kanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="569c0-145">Brukere må velge fra forhåndsdefinerte betalingsmetoder for å koble dem til telefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="569c0-146">Før du definerer betalingsmetodene for telefonsenteret, må du først definere hovedmetodene for betaling i **Detaljhandel og handel \> Kanaloppsett \> Betalingsmåter \> Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="569c0-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="569c0-147">I handlingsruten velger du kategorien **Oppsett** og deretter **Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="569c0-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="569c0-148">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="569c0-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="569c0-149">I navigasjonsruten velger du en betalingsmetode fra de tilgjengelige forhåndsdefinerte betalingene.</span><span class="sxs-lookup"><span data-stu-id="569c0-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="569c0-150">Konfigurer eventuelle tilleggsinnstillinger som kreves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="569c0-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="569c0-151">Når det gjelder kredittkort, gavekort eller fordelskort, kreves det ytterligere oppsett ved å velge **Kortoppsett**-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="569c0-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="569c0-152">Konfigurer riktige posteringskontoer for betalingstypen i **Postering**-delen.</span><span class="sxs-lookup"><span data-stu-id="569c0-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="569c0-153">Klikk på **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="569c0-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="569c0-154">Bildet nedenfor viser et eksempel på en kontantbetalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="569c0-154">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmåter](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="569c0-156">Definer leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="569c0-156">Set up modes of delivery</span></span>

<span data-ttu-id="569c0-157">Du kan se de konfigurerte leveringsmåtene ved å velge **Leveringsmåter** fra kategorien **Oppsett** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="569c0-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="569c0-158">Følg denne fremgangsmåten for å endre eller legge til en leveringsmåte som skal knyttes til telefonsenterkanalen:</span><span class="sxs-lookup"><span data-stu-id="569c0-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="569c0-159">Velg **Behandle leveringsmåter** fra skjemaet for leveringsmåter for samtalesenteret.</span><span class="sxs-lookup"><span data-stu-id="569c0-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="569c0-160">Velg **Ny** i handlingsruten for å opprette en ny leveringsmåte, eller velg en eksisterende måte.</span><span class="sxs-lookup"><span data-stu-id="569c0-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="569c0-161">I delen **Detaljhandelskanaler** velger du **Legg til linje** for å legge til telefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="569c0-162">Legge til kanaler ved hjelp av organisasjonsnoder i stedet for å legge til hver kanal for seg, kan effektivisere tillegg av kanaler</span><span class="sxs-lookup"><span data-stu-id="569c0-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="569c0-163">Kontroller at leveringsmåten er konfigurert med data i hurtigfanen **Produkter** og hurtigfanen **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="569c0-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="569c0-164">Hvis ingen produkter eller leveringsadresser er gyldige for leveringsmåten, vil det føre til feil å velge den under ordreregistrering.</span><span class="sxs-lookup"><span data-stu-id="569c0-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="569c0-165">Når det er gjort endringer i leveringskonfigurasjoner for telefonsenteret, må jobben **Behandle leveringsmåter** kjøres for å bryte ned endringsmatrisen.</span><span class="sxs-lookup"><span data-stu-id="569c0-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="569c0-166">Du finner denne jobben ved å navigere til **Detaljhandel og handel \> IT for detaljhandel og handel \> Behandle leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="569c0-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="569c0-167">Bildet nedenfor viser et eksempel på en leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="569c0-167">The following image shows an example of a mode of delivery.</span></span>

![Definer leveringsmåter](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="569c0-169">Definere kanalbrukere</span><span class="sxs-lookup"><span data-stu-id="569c0-169">Set up channel users</span></span>

<span data-ttu-id="569c0-170">Hvis du vil opprette en salgsordre som er koblet til telefonsenterkanalen fra Commerce Headquarters, må brukeren som oppretter salgsordren, være koblet til telefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="569c0-171">Brukeren kan ikke koble en salgsordre som er opprettet i Commerce Headquarters manuelt til telefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="569c0-172">Koblingen er systematisk, og er basert på brukeren og brukerens forhold til telefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="569c0-173">En bruker kan bare være koblet til én telefonsenterkanal.</span><span class="sxs-lookup"><span data-stu-id="569c0-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="569c0-174">I handlingsruten velger du kategorien **Kanal** og deretter **Kanalbrukere**.</span><span class="sxs-lookup"><span data-stu-id="569c0-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="569c0-175">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="569c0-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="569c0-176">Velg en eksisterende **Bruker-ID** fra rullegardinlisten for å koble denne brukeren til telefonsenterkanalen</span><span class="sxs-lookup"><span data-stu-id="569c0-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="569c0-177">Når brukeroppsettet for kanalen er fullført og brukeren oppretter en ny salgsordre i Commerce Headquarters, blir salgsordren koblet til den tilknyttede telefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="569c0-178">Konfigurasjoner for denne kanalen vil bli brukt systematisk på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="569c0-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="569c0-179">En bruker kan bekrefte hvilken telefonsenterkanal salgsordren er koblet til ved å vise kanalnavnreferansen i salgsordrehodet.</span><span class="sxs-lookup"><span data-stu-id="569c0-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="569c0-180">Definere prisgrupper</span><span class="sxs-lookup"><span data-stu-id="569c0-180">Set up price groups</span></span>

<span data-ttu-id="569c0-181">Prisgrupper er valgfrie, men hvis de brukes, kan de styre hvilke salgspriser som skal tilbys kunder som legger inn ordrer i telefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="569c0-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="569c0-182">Hvis en prisgruppe ikke er konfigurert for kunden, eller hvis katalogprisgrupper ikke er brukt på salgsordren (ved hjelp av feltet **Kildekode-ID** i ordrehodet i samtalesenteret), brukes kanalprisgruppen til å finne varepriser.</span><span class="sxs-lookup"><span data-stu-id="569c0-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="569c0-183">Hvis det ikke blir funnet en prisgruppe i telefonsenterkanalen, brukes standard hovedpriser.</span><span class="sxs-lookup"><span data-stu-id="569c0-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="569c0-184">Hvis du vil definere en prisgruppe, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="569c0-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="569c0-185">I handlingsruten velger du kategorien **Kanal** og deretter **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="569c0-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="569c0-186">I handlingsruten klikker du på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="569c0-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="569c0-187">Velg en **detaljhandelsprisgruppe** fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="569c0-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="569c0-188">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="569c0-188">Additional resources</span></span>

[<span data-ttu-id="569c0-189">Kanaloppsettsforutsetninger</span><span class="sxs-lookup"><span data-stu-id="569c0-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="569c0-190">Salgsfunksjonalitet for telefonsenter</span><span class="sxs-lookup"><span data-stu-id="569c0-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="569c0-191">Definere ordrebehandlingsalternativer for telefonsenter</span><span class="sxs-lookup"><span data-stu-id="569c0-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="569c0-192">Telefonsenterkataloger</span><span class="sxs-lookup"><span data-stu-id="569c0-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="569c0-193">Definere og arbeide med svindelvarsler</span><span class="sxs-lookup"><span data-stu-id="569c0-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="569c0-194">Definere kontinuitetsprogrammer for telefonsentre</span><span class="sxs-lookup"><span data-stu-id="569c0-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
