---
title: Gavekortmodul
description: Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962769"
---
# <a name="gift-card-module"></a><span data-ttu-id="8e4f1-103">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="8e4f1-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e4f1-104">Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8e4f1-105">Gavekortmoduler kan brukes i betalingsmoduler til å godta gavekort, som er en vanlig betalingsform som brukes i e-handelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="8e4f1-106">Gavekortmodulen støtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="8e4f1-107">SVS- og Givex-gavekort løses inn via betalingsleverandøren Adyen.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="8e4f1-108">Hvis du vil ha mer informasjon om støtte for eksterne gavekort som SVS og Givex, kan du se [Støtte for eksterne gavekort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="8e4f1-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8e4f1-109">Støtte for innløsning av SVS- og Givex-gavekort under utsjekkingsflyten er tilgjengelig i Dynamics 365 Commerce 10.0.11-versjonen.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="8e4f1-110">Det finnes to tilgjengelige gavekortmoduler:</span><span class="sxs-lookup"><span data-stu-id="8e4f1-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="8e4f1-111">**Gavekort** – Denne modulen kan brukes på en betalingsside til å løse ut et gavekort som et betalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="8e4f1-112">**Kontroll av gavekortsaldo** – Denne modulen kan brukes på alle sider til å kontrollere saldoen på et gavekort.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="8e4f1-113">Denne modulen er tilgjengelig i Commerce versjon 10.0.14 og nyere.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="8e4f1-114">Støtte for kontroll av gavekortsaldo er tilgjengelig i Dynamics 365 Commerce 10.0.14-versjonen.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="8e4f1-115">Bildet nedenfor viser et eksempel på en gavekortmodul på en kasseside.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på en gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="8e4f1-117">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="8e4f1-117">Module properties</span></span>

- <span data-ttu-id="8e4f1-118">**Vis flere felt** – Denne egenskapen definerer hvilke felt som skal vises for gavekort i tillegg til gavekortnummeret, som alltid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="8e4f1-119">Noen gavekort støtter for eksempel visning av et personlig identifikasjonsnummer (PIN), og andre støtter visning av en PIN-kode og en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="8e4f1-120">Alternativt kan denne egenskapen settes til "Ingen", som bare vil vise gavekortnummeret og ingen flere felt.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="8e4f1-121">Verdier som støttes:</span><span class="sxs-lookup"><span data-stu-id="8e4f1-121">Supported values:</span></span>
-   <span data-ttu-id="8e4f1-122">PIN-kode</span><span class="sxs-lookup"><span data-stu-id="8e4f1-122">PIN</span></span>
-   <span data-ttu-id="8e4f1-123">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="8e4f1-123">Expiration date</span></span>
-   <span data-ttu-id="8e4f1-124">PIN-kode og utløpsdato</span><span class="sxs-lookup"><span data-stu-id="8e4f1-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="8e4f1-125">None</span><span class="sxs-lookup"><span data-stu-id="8e4f1-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="8e4f1-126">Områdeinnstillinger for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="8e4f1-126">Site settings for gift card modules</span></span>

<span data-ttu-id="8e4f1-127">I Commerce-områdebygger under **Områdeinnstillinger \> Tillegg** er det en innstilling for gavekortmodulen kalt **Støttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="8e4f1-128">Denne innstillingen støtter tre verdier:</span><span class="sxs-lookup"><span data-stu-id="8e4f1-128">This setting supports three values:</span></span>
- <span data-ttu-id="8e4f1-129">**Dynamics 365-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="8e4f1-130">Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="8e4f1-131">**SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="8e4f1-132">Denne innstillingen støttes for påloggede og anonyme brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="8e4f1-133">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen innløsning av Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="8e4f1-134">Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e4f1-135">Disse innstillingene er tilgjengelige i Dynamics 365 Commerce 10.0.11-versjonen og er bare nødvendige hvis du trenger støtte for SVS- eller Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="8e4f1-136">Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="8e4f1-137">Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="8e4f1-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="8e4f1-138">Utvide interne gavekort til bruk i butikkfasader for e-handel på nettet</span><span class="sxs-lookup"><span data-stu-id="8e4f1-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="8e4f1-139">Interne gavekort er som standard ikke optimalisert for bruk i butikkfasader for e-handel på nettet.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="8e4f1-140">Før du tillater bruk av interne gavekort til betaling, bør du derfor konfigurere dem med utvidelser som gjør det sikrere å bruke dem.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="8e4f1-141">Her er gavekortområdene du bør utvide før du tillater bruk av interne gavekort i produksjon:</span><span class="sxs-lookup"><span data-stu-id="8e4f1-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="8e4f1-142">**Gavekortnummer** – Nummerserier brukes til å generere gavekortnumre for interne gavekort.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="8e4f1-143">Siden nummerserier lett kan forutses, bør du utvide genereringen av gavekortnumre slik at tilfeldige, kryptografisk sikre strenger brukes for gavekortnumrene som utstedes.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="8e4f1-144">**GetBalance** – **GetBalance**-API-en brukes til å slå opp gavekortsaldoer.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="8e4f1-145">Som standard er denne API-en offentlig.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-145">By default, this API public.</span></span> <span data-ttu-id="8e4f1-146">Hvis en PIN-kode ikke kreves for å slå opp gavekortsaldoer, er det en risiko for at angrep med rå kraft kan bruke **GetBalance**-APIen til å prøve å slå opp gavekortnumre som har saldoer.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="8e4f1-147">Ved å implementere både PIN-krav til interne gavekort og API-begrensning, kan du redusere risikoen.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="8e4f1-148">**PIN-kode** – Som standard støtter ikke interne gavekort PIN-koder.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="8e4f1-149">Du bør utvide interne gavekort, slik at en PIN-kode kreves for å slå opp saldoer.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="8e4f1-150">Denne funksjonaliteten kan også brukes til å låse gavekort etter fortløpende feil forsøk på å angi PIN-kode.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="8e4f1-151">Aktivere gavekortbetalinger for gjesteutsjekking</span><span class="sxs-lookup"><span data-stu-id="8e4f1-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="8e4f1-152">Som standard er ikke gavekortbetalinger aktivert for gjestutsjekking (anonym).</span><span class="sxs-lookup"><span data-stu-id="8e4f1-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="8e4f1-153">Følg denne fremgangsmåten for å aktivere dem.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="8e4f1-154">I Commerce Headquarters går du til **Retail og Commerce \> Kanaloppsett \> POS-oppsett \> POS \> POS-operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="8e4f1-155">Merk og hold (eller høyreklikk) hodet i rutenettet, og velg deretter **Sett inn kolonner**.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="8e4f1-156">Merk av for **AllowAnonymousAccess** i dialogboksen **Sett inn kolonner**.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="8e4f1-157">Velg **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-157">Select **Update**.</span></span>
1. <span data-ttu-id="8e4f1-158">For operasjonene **520** (gavekortsaldo) og **214** setter du verdien **AllowAnonymousAccess** til **1**.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="8e4f1-159">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-159">Select **Save**.</span></span>
1. <span data-ttu-id="8e4f1-160">Kjør planleggerjobben **1090** for å synkronisere endringer i kanaldatabasen.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="8e4f1-161">Legge til en gavekortmodul på en side</span><span class="sxs-lookup"><span data-stu-id="8e4f1-161">Add a gift card module to a page</span></span>

<span data-ttu-id="8e4f1-162">Hvis du vil ha informasjon om hvordan du legger til en gavekortmodul på en kasseside og angir de nødvendige egenskapene, kan du se [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="8e4f1-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e4f1-163">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8e4f1-163">Additional resources</span></span>

[<span data-ttu-id="8e4f1-164">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="8e4f1-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8e4f1-165">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="8e4f1-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="8e4f1-166">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="8e4f1-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8e4f1-167">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="8e4f1-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="8e4f1-168">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="8e4f1-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="8e4f1-169">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="8e4f1-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="8e4f1-170">Henteinformasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="8e4f1-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="8e4f1-171">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="8e4f1-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8e4f1-172">Støtte for eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="8e4f1-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="8e4f1-173">Oppdateringer for SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="8e4f1-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
