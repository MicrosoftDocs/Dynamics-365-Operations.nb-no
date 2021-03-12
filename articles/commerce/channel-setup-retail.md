---
title: Definere en detaljhandelskanal
description: Dette emnet beskriver hvordan du oppretter en ny detaljhandelskanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 100822ecea03d03267f98654c66e74f2f5924bd9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997731"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="aa087-103">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="aa087-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="aa087-104">Dette emnet beskriver hvordan du oppretter en ny detaljhandelskanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aa087-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aa087-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="aa087-105">Overview</span></span>

<span data-ttu-id="aa087-106">Dynamics 365 Commerce støtter flere kanaler for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="aa087-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="aa087-107">Disse detaljhandelskanalene omfatter nettbutikker, telefonsentre og detaljhandelsbutikker (også kalt fysiske butikker).</span><span class="sxs-lookup"><span data-stu-id="aa087-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="aa087-108">Hver detaljhandelsbutikkanal kan ha sine egne betalingsmåter, prisgrupper, salgsstedskasser, inntekts- og utgiftskontoer og ansatte.</span><span class="sxs-lookup"><span data-stu-id="aa087-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="aa087-109">Du må sette opp alle disse elementene før du kan opprette en detaljhandelsbutikkanal.</span><span class="sxs-lookup"><span data-stu-id="aa087-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="aa087-110">Før det opprettes en detaljhandelskanal, må du kontrollere at du følger [forutsetningene for kanal](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="aa087-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="aa087-111">Opprette og konfigurere en ny detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="aa087-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="aa087-112">I navigasjonsruten går du til **Moduler \> Kanaler \> Butikker \> Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="aa087-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="aa087-113">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aa087-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aa087-114">I **Navn**-feltet oppgir du et navn for den nye kanalen.</span><span class="sxs-lookup"><span data-stu-id="aa087-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="aa087-115">Oppgi et unikt butikknummer i **Butikknummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="aa087-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="aa087-116">Nummeret kan være alfanumerisk med opptil 10 tegn.</span><span class="sxs-lookup"><span data-stu-id="aa087-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="aa087-117">Angi den riktige juridiske enheten i rullegardinlisten **Juridisk enhet**.</span><span class="sxs-lookup"><span data-stu-id="aa087-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="aa087-118">Angi det riktige lageret i rullegardinlisten **Lager**.</span><span class="sxs-lookup"><span data-stu-id="aa087-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="aa087-119">Velg riktig tidssone i feltet **Tidssone for butikk**.</span><span class="sxs-lookup"><span data-stu-id="aa087-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="aa087-120">I rullegardinlisten **Merverdiavgiftsgruppe** velger du riktig merverdiavgiftsgruppe for butikken.</span><span class="sxs-lookup"><span data-stu-id="aa087-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="aa087-121">Velg riktig valuta i **Valuta**-feltet.</span><span class="sxs-lookup"><span data-stu-id="aa087-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="aa087-122">Angi en gyldig adressebok i feltet **Adressebok for kunde**.</span><span class="sxs-lookup"><span data-stu-id="aa087-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="aa087-123">Angi en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="aa087-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="aa087-124">I feltet **Funksjonalitetsprofil** velger du en funksjonalitetsprofil hvis det er aktuelt.</span><span class="sxs-lookup"><span data-stu-id="aa087-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="aa087-125">I feltet **Profil for e-postvarsling** oppgir du en gyldig profil for e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="aa087-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="aa087-126">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="aa087-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="aa087-127">Bildet nedenfor viser opprettelsen av en ny detaljhandelskanal.</span><span class="sxs-lookup"><span data-stu-id="aa087-127">The following image shows the creation of a new retail channel.</span></span>

![Ny detaljhandelskanal](media/channel-setup-retail-1.png)

<span data-ttu-id="aa087-129">Bildet nedenfor viser et eksempel på en detaljhandelskanal.</span><span class="sxs-lookup"><span data-stu-id="aa087-129">The following image shows an example retail channel.</span></span>

![Eksempel på detaljhandelskanal](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="aa087-131">Andre innstillinger</span><span class="sxs-lookup"><span data-stu-id="aa087-131">Other settings</span></span>

<span data-ttu-id="aa087-132">Det finnes mange andre valgfrie innstillinger som kan angis i delene **Utdrag/avslutning/** og **Diverse**, basert på behovene til detaljhandelsbutikken.</span><span class="sxs-lookup"><span data-stu-id="aa087-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="aa087-133">I tillegg kan du se [Skjermoppsett for salgssted](pos-screen-layouts.md) for informasjon om hvordan du konfigurerer standard skjermoppsett i delen **Skjermoppsett**, og [Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md) for konfigurasjonsinformasjon om delen **Maskinvarestasjoner**.</span><span class="sxs-lookup"><span data-stu-id="aa087-133">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="aa087-134">Bildet nedenfor viser et eksempel på en konfigurasjon av et detaljhandelskanaloppsett.</span><span class="sxs-lookup"><span data-stu-id="aa087-134">The following image shows an example retail channel setup configuration.</span></span>

![Eksempel på konfigurasjon av detaljhandelskanal](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="aa087-136">Ekstra kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="aa087-136">Additional channel set up</span></span>

<span data-ttu-id="aa087-137">Du finner flere elementer som må konfigureres for en kanal, i **handlingsruten** under **Oppsett**-delen.</span><span class="sxs-lookup"><span data-stu-id="aa087-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="aa087-138">Andre oppgaver som kreves for oppsett av Internett-kanal, omfatter definere betalingsmåter, kontantoppgjør, leveringsmåter, inntekts-/utgiftskonto, inndelinger, gruppetilordning for oppfyllelse og safer.</span><span class="sxs-lookup"><span data-stu-id="aa087-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="aa087-139">Følgende bilde viser diverse tilleggsalternativer for detaljhandelskanaloppsett i kategorien **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="aa087-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Definere kanal](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="aa087-141">Definere betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="aa087-141">Set up payment methods</span></span>

<span data-ttu-id="aa087-142">Hvis du vil definere betalingsmåter, følger du disse trinnene for hver betalingstype som støttes på denne kanalen.</span><span class="sxs-lookup"><span data-stu-id="aa087-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="aa087-143">I handlingsruten velger du kategorien **Oppsett** og deretter **Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="aa087-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="aa087-144">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aa087-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aa087-145">Velg en ønsket betalingsmåte i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="aa087-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="aa087-146">I delen **Generelt** angir du et **operasjonsnavn** og konfigurerer eventuelle andre ønskede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="aa087-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="aa087-147">Konfigurer eventuelle tilleggsinnstillinger som kreves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="aa087-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="aa087-148">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="aa087-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="aa087-149">Bildet nedenfor viser et eksempel på en kontantbetalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="aa087-149">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmåter](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="aa087-151">Definere kKontantoppgjør</span><span class="sxs-lookup"><span data-stu-id="aa087-151">Set up cash declaration</span></span>

1. <span data-ttu-id="aa087-152">I handlingsruten velger du kategorien **Oppsett** og deretter **Kontantoppgjør**.</span><span class="sxs-lookup"><span data-stu-id="aa087-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="aa087-153">Velg **Ny** i handlings ruten, og opprett deretter alle aktuelle **Mynt**- og **Seddel**-størrelser.</span><span class="sxs-lookup"><span data-stu-id="aa087-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="aa087-154">Bildet nedenfor viser et eksempel på et kontantoppgjør.</span><span class="sxs-lookup"><span data-stu-id="aa087-154">The following image shows an example of a cash declaration.</span></span>

![Definere kontantoppgjør](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="aa087-156">Definer leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="aa087-156">Set up modes of delivery</span></span>

<span data-ttu-id="aa087-157">Du kan se de konfigurerte leveringsmåtene ved å velge **Leveringsmåter** fra kategorien **Oppsett** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="aa087-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="aa087-158">Hvis du vil endre eller legge til en leveringsmåte, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="aa087-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="aa087-159">I navigasjonsruten går du til **Moduler \> Lagerstyring \> Leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="aa087-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="aa087-160">Velg **Ny** i handlingsruten for å opprette en ny leveringsmåte, eller velg en eksisterende måte.</span><span class="sxs-lookup"><span data-stu-id="aa087-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="aa087-161">I delen **Detaljhandelskanaler** velger du **Legg til linje** for å legge til kanalen.</span><span class="sxs-lookup"><span data-stu-id="aa087-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="aa087-162">Legge til kanaler ved hjelp av organisasjonsnoder i stedet for å legge til hver kanal for seg, kan effektivisere tillegg av kanaler</span><span class="sxs-lookup"><span data-stu-id="aa087-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="aa087-163">Bildet nedenfor viser et eksempel på en leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="aa087-163">The following image shows an example of a mode of delivery.</span></span>

![Definer leveringsmåter](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="aa087-165">Definere inntekts-/utgiftskonto</span><span class="sxs-lookup"><span data-stu-id="aa087-165">Set up income/expense account</span></span>

<span data-ttu-id="aa087-166">Gjør følgende for å konfigurere en inntekts-/utgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="aa087-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="aa087-167">I handlingsruten velger du kategorien **Oppsett** og deretter **Inntekts-/utgiftskonto**.</span><span class="sxs-lookup"><span data-stu-id="aa087-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="aa087-168">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aa087-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aa087-169">Under **Navn** skriver du inn et navn.</span><span class="sxs-lookup"><span data-stu-id="aa087-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="aa087-170">Under **Søkenavn** skriver du inn et søkenavn.</span><span class="sxs-lookup"><span data-stu-id="aa087-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="aa087-171">Under **Kontotype** angir du kontotypen.</span><span class="sxs-lookup"><span data-stu-id="aa087-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="aa087-172">Skriv inn tekst for **Meldingslinje 1**, **Meldingslinje 2**, **Bilagstekst 1** og **Bilagstekst 2** etter behov.</span><span class="sxs-lookup"><span data-stu-id="aa087-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="aa087-173">Angi posteringsinformasjon under **Postering**.</span><span class="sxs-lookup"><span data-stu-id="aa087-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="aa087-174">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="aa087-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="aa087-175">Bildet nedenfor viser et eksempel på en inntekts/utgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="aa087-175">The following image shows an example of an income/expense account.</span></span>

![Definere inntekts-/utgiftskontoer](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="aa087-177">Definere seksjoner</span><span class="sxs-lookup"><span data-stu-id="aa087-177">Set up sections</span></span>

<span data-ttu-id="aa087-178">Gjør følgende for å konfigurere seksjoner.</span><span class="sxs-lookup"><span data-stu-id="aa087-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="aa087-179">I handlingsruten velger du kategorien **Oppsett** og klikker deretter **Seksjoner**.</span><span class="sxs-lookup"><span data-stu-id="aa087-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="aa087-180">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aa087-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aa087-181">Under **Seksjonsnummer** angir du et seksjonsnummer.</span><span class="sxs-lookup"><span data-stu-id="aa087-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="aa087-182">Angi en beskrivelse under **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="aa087-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="aa087-183">Under **Seksjonsstørrelse** angir du en seksjonsstørrelse.</span><span class="sxs-lookup"><span data-stu-id="aa087-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="aa087-184">Konfigurer tilleggsinnstillinger for **Generelt** og **Salgsstatistikk** etter behov.</span><span class="sxs-lookup"><span data-stu-id="aa087-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="aa087-185">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="aa087-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="aa087-186">Definere en gruppetilordning for oppfyllelse</span><span class="sxs-lookup"><span data-stu-id="aa087-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="aa087-187">Hvis du vil konfigurere en gruppetilordning for oppfyllelse, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="aa087-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="aa087-188">I handlingsruten velger du kategorien **Oppsett** og deretter **Gruppetilordning for oppfyllelse**.</span><span class="sxs-lookup"><span data-stu-id="aa087-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="aa087-189">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aa087-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aa087-190">I rullegardinlisten **Oppfyllelsesgruppe** velger du en oppfyllelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="aa087-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="aa087-191">Angi en beskrivelse i rullegardinlisten **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="aa087-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="aa087-192">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="aa087-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="aa087-193">Det følgende bildet viser et eksempel på et oppsett for gruppetilordning for oppfyllelse.</span><span class="sxs-lookup"><span data-stu-id="aa087-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Definere gruppetilordninger for oppfyllelse](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="aa087-195">Definere safer</span><span class="sxs-lookup"><span data-stu-id="aa087-195">Set up safes</span></span>

<span data-ttu-id="aa087-196">Gjør følgende for å konfigurere safer.</span><span class="sxs-lookup"><span data-stu-id="aa087-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="aa087-197">I handlingsruten velger du kategorien **Oppsett** og klikker deretter **Safer**.</span><span class="sxs-lookup"><span data-stu-id="aa087-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="aa087-198">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aa087-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aa087-199">Angi et navn for safen.</span><span class="sxs-lookup"><span data-stu-id="aa087-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="aa087-200">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="aa087-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa087-201">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="aa087-201">Additional resources</span></span>

[<span data-ttu-id="aa087-202">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="aa087-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="aa087-203">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="aa087-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="aa087-204">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="aa087-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="aa087-205">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="aa087-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

