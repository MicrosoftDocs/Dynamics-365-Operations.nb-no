---
title: Gavekortmodul
description: Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b7d28e041b8adc828a2447ab09a0c1d28cc2aec0
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022011"
---
# <a name="gift-card-module"></a><span data-ttu-id="5cd02-103">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="5cd02-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5cd02-104">Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5cd02-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5cd02-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="5cd02-105">Overview</span></span>

<span data-ttu-id="5cd02-106">Gavekortmoduler kan brukes i betalingsmoduler til å godta gavekort, som er en vanlig betalingsform som brukes i e-handelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5cd02-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="5cd02-107">Gavekortmodulen støtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="5cd02-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="5cd02-108">SVS- og Givex-gavekort løses inn via betalingsleverandøren Adyen.</span><span class="sxs-lookup"><span data-stu-id="5cd02-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="5cd02-109">Hvis du vil ha mer informasjon om støtte for eksterne gavekort som SVS og Givex, kan du se [Støtte for eksterne gavekort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="5cd02-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5cd02-110">Støtte for innløsning av SVS- og Givex-gavekort under utsjekkingsflyten er tilgjengelig i Dynamics 365 Commerce 10.0.11-versjonen.</span><span class="sxs-lookup"><span data-stu-id="5cd02-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="5cd02-111">Det finnes to tilgjengelige gavekortmoduler:</span><span class="sxs-lookup"><span data-stu-id="5cd02-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="5cd02-112">**Gavekort** – Denne modulen kan brukes på en betalingsside til å løse ut et gavekort som et betalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="5cd02-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="5cd02-113">**Kontroll av gavekortsaldo** – Denne modulen kan brukes på alle sider til å kontrollere saldoen på et gavekort.</span><span class="sxs-lookup"><span data-stu-id="5cd02-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="5cd02-114">Denne modulen er tilgjengelig i Commerce versjon 10.0.14 og nyere.</span><span class="sxs-lookup"><span data-stu-id="5cd02-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="5cd02-115">Støtte for kontroll av gavekortsaldo er tilgjengelig i Dynamics 365 Commerce 10.0.14-versjonen.</span><span class="sxs-lookup"><span data-stu-id="5cd02-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="5cd02-116">Bildet nedenfor viser et eksempel på en gavekortmodul på en kasseside.</span><span class="sxs-lookup"><span data-stu-id="5cd02-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på en gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="5cd02-118">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="5cd02-118">Module properties</span></span>

- <span data-ttu-id="5cd02-119">**Vis flere felt** – Denne egenskapen definerer hvilke felt som skal vises for gavekort i tillegg til gavekortnummeret, som alltid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="5cd02-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="5cd02-120">Noen gavekort støtter for eksempel visning av et personlig identifikasjonsnummer (PIN), og andre støtter visning av en PIN-kode og en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="5cd02-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="5cd02-121">Alternativt kan denne egenskapen settes til "Ingen", som bare vil vise gavekortnummeret og ingen flere felt.</span><span class="sxs-lookup"><span data-stu-id="5cd02-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="5cd02-122">Verdier som støttes:</span><span class="sxs-lookup"><span data-stu-id="5cd02-122">Supported values:</span></span>
-   <span data-ttu-id="5cd02-123">PIN-kode</span><span class="sxs-lookup"><span data-stu-id="5cd02-123">PIN</span></span>
-   <span data-ttu-id="5cd02-124">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="5cd02-124">Expiration date</span></span>
-   <span data-ttu-id="5cd02-125">PIN-kode og utløpsdato</span><span class="sxs-lookup"><span data-stu-id="5cd02-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="5cd02-126">None</span><span class="sxs-lookup"><span data-stu-id="5cd02-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="5cd02-127">Områdeinnstillinger for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="5cd02-127">Site settings for gift card modules</span></span>

<span data-ttu-id="5cd02-128">I Commerce-områdebygger under **Områdeinnstillinger \> Tillegg** er det en innstilling for gavekortmodulen kalt **Støttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="5cd02-128">In Commerce site builder under **Site Settings \> Extensions** , there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="5cd02-129">Denne innstillingen støtter tre verdier:</span><span class="sxs-lookup"><span data-stu-id="5cd02-129">This setting supports three values:</span></span>
- <span data-ttu-id="5cd02-130">**Dynamics 365-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="5cd02-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="5cd02-131">Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="5cd02-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="5cd02-132">**SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="5cd02-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="5cd02-133">Denne innstillingen støttes for påloggede og anonyme brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="5cd02-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="5cd02-134">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen innløsning av Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="5cd02-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="5cd02-135">Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="5cd02-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5cd02-136">Disse innstillingene er tilgjengelige i Dynamics 365 Commerce 10.0.11-versjonen og er bare nødvendige hvis du trenger støtte for SVS- eller Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="5cd02-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="5cd02-137">Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen.</span><span class="sxs-lookup"><span data-stu-id="5cd02-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="5cd02-138">Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="5cd02-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="5cd02-139">Legge til en gavekortmodul på en side</span><span class="sxs-lookup"><span data-stu-id="5cd02-139">Add a gift card module to a page</span></span>

<span data-ttu-id="5cd02-140">Hvis du vil ha informasjon om hvordan du legger til en gavekortmodul på en kasseside og angir de nødvendige egenskapene, kan du se [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="5cd02-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5cd02-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5cd02-141">Additional resources</span></span>

[<span data-ttu-id="5cd02-142">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="5cd02-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5cd02-143">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="5cd02-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="5cd02-144">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="5cd02-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5cd02-145">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="5cd02-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="5cd02-146">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="5cd02-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="5cd02-147">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="5cd02-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="5cd02-148">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="5cd02-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5cd02-149">Støtte for eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="5cd02-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="5cd02-150">Oppdateringer for SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="5cd02-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
