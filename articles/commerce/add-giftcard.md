---
title: Gavekortmodul
description: Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761087"
---
# <a name="gift-card-module"></a><span data-ttu-id="88571-103">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="88571-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="88571-104">Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="88571-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="88571-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="88571-105">Overview</span></span>

<span data-ttu-id="88571-106">Gavekortmoduler kan brukes i betalingsmoduler til å godta gavekort, som er en vanlig betalingsform som brukes i e-handelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="88571-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="88571-107">Gavekortmodulen støtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="88571-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="88571-108">SVS- og Givex-gavekort løses inn via betalingsleverandøren Adyen.</span><span class="sxs-lookup"><span data-stu-id="88571-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="88571-109">Hvis du vil ha mer informasjon om støtte for eksterne gavekort som SVS og Givex, kan du se [Støtte for eksterne gavekort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="88571-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="88571-110">Det finnes to tilgjengelige gavekortmoduler:</span><span class="sxs-lookup"><span data-stu-id="88571-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="88571-111">**Gavekort** – Denne modulen kan brukes på en betalingsside til å løse ut et gavekort som et betalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="88571-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="88571-112">**Kontroll av gavekortsaldo** – Denne modulen kan brukes på alle sider til å kontrollere saldoen på et gavekort.</span><span class="sxs-lookup"><span data-stu-id="88571-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="88571-113">Denne modulen er tilgjengelig i Commerce versjon 10.0.14 og nyere.</span><span class="sxs-lookup"><span data-stu-id="88571-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="88571-114">Bildet nedenfor viser et eksempel på en gavekortmodul på en kasseside.</span><span class="sxs-lookup"><span data-stu-id="88571-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på en gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="88571-116">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="88571-116">Module properties</span></span>

- <span data-ttu-id="88571-117">**Vis flere felt** – Denne egenskapen definerer hvilke felt som skal vises for gavekort i tillegg til gavekortnummeret, som alltid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="88571-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="88571-118">Noen gavekort støtter for eksempel visning av et personlig identifikasjonsnummer (PIN), og andre støtter visning av en PIN-kode og en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="88571-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="88571-119">Alternativt kan denne egenskapen settes til "Ingen", som bare vil vise gavekortnummeret og ingen flere felt.</span><span class="sxs-lookup"><span data-stu-id="88571-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="88571-120">Verdier som støttes:</span><span class="sxs-lookup"><span data-stu-id="88571-120">Supported values:</span></span>
-   <span data-ttu-id="88571-121">PIN-kode</span><span class="sxs-lookup"><span data-stu-id="88571-121">PIN</span></span>
-   <span data-ttu-id="88571-122">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="88571-122">Expiration date</span></span>
-   <span data-ttu-id="88571-123">PIN-kode og utløpsdato</span><span class="sxs-lookup"><span data-stu-id="88571-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="88571-124">None</span><span class="sxs-lookup"><span data-stu-id="88571-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="88571-125">Områdeinnstillinger for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="88571-125">Site settings for gift card modules</span></span>

<span data-ttu-id="88571-126">I Commerce-områdebygger under **Områdeinnstillinger \> Tillegg** er det en innstilling for gavekortmodulen kalt **Støttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="88571-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="88571-127">Denne innstillingen støtter tre verdier:</span><span class="sxs-lookup"><span data-stu-id="88571-127">This setting supports three values:</span></span>
- <span data-ttu-id="88571-128">**Dynamics 365-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="88571-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="88571-129">Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="88571-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="88571-130">**SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="88571-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="88571-131">Denne innstillingen støttes for påloggede og anonyme brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="88571-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="88571-132">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen innløsning av Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="88571-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="88571-133">Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="88571-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="88571-134">Legge til en gavekortmodul på en side</span><span class="sxs-lookup"><span data-stu-id="88571-134">Add a gift card module to a page</span></span>

<span data-ttu-id="88571-135">Hvis du vil ha informasjon om hvordan du legger til en gavekortmodul på en kasseside og angir de nødvendige egenskapene, kan du se [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="88571-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88571-136">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="88571-136">Additional resources</span></span>

[<span data-ttu-id="88571-137">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="88571-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="88571-138">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="88571-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="88571-139">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="88571-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="88571-140">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="88571-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="88571-141">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="88571-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="88571-142">Modul for leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="88571-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="88571-143">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="88571-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="88571-144">Støtte for eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="88571-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
