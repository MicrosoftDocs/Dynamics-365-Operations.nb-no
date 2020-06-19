---
title: Gavekortmodul
description: Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a8428963e105e422dcd048863c17df0926a409ac
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411118"
---
# <a name="gift-card-module"></a><span data-ttu-id="6be18-103">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="6be18-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6be18-104">Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6be18-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6be18-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="6be18-105">Overview</span></span>

<span data-ttu-id="6be18-106">Gavekort er en vanlig betalingsmåte, og gavekortmodulen kan brukes i en kassemodul for å godta gavekort.</span><span class="sxs-lookup"><span data-stu-id="6be18-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="6be18-107">Gavekortmodulen støtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="6be18-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="6be18-108">SVS- og Givex-gavekort løses inn via betalingsleverandøren Adyen.</span><span class="sxs-lookup"><span data-stu-id="6be18-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="6be18-109">Hvis du vil ha mer informasjon om støtte for eksterne gavekort som SVS og Givex, kan du se [Støtte for eksterne gavekort](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="6be18-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="6be18-110">Bildet nedenfor viser et eksempel på en gavekortmodul på en kasseside.</span><span class="sxs-lookup"><span data-stu-id="6be18-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på en gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="6be18-112">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="6be18-112">Module properties</span></span>

- <span data-ttu-id="6be18-113">**Vis flere felt** – Denne egenskapen definerer hvilke felt som skal vises for gavekort i tillegg til gavekortnummeret, som alltid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="6be18-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="6be18-114">Noen gavekort støtter for eksempel visning av et personlig identifikasjonsnummer (PIN), og andre støtter visning av en PIN-kode og en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="6be18-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="6be18-115">Alternativt kan denne egenskapen settes til "Ingen", som bare vil vise gavekortnummeret og ingen flere felt.</span><span class="sxs-lookup"><span data-stu-id="6be18-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="6be18-116">Verdier som støttes:</span><span class="sxs-lookup"><span data-stu-id="6be18-116">Supported values:</span></span>
-   <span data-ttu-id="6be18-117">PIN-kode</span><span class="sxs-lookup"><span data-stu-id="6be18-117">PIN</span></span>
-   <span data-ttu-id="6be18-118">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="6be18-118">Expiration date</span></span>
-   <span data-ttu-id="6be18-119">PIN-kode og utløpsdato</span><span class="sxs-lookup"><span data-stu-id="6be18-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="6be18-120">None</span><span class="sxs-lookup"><span data-stu-id="6be18-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="6be18-121">Områdeinnstillinger for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="6be18-121">Site settings for gift card modules</span></span>

<span data-ttu-id="6be18-122">I Commerce-områdebygger under **Områdeinnstillinger \> Tillegg** er det en innstilling for gavekortmodulen kalt **Støttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="6be18-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="6be18-123">Denne innstillingen støtter tre verdier:</span><span class="sxs-lookup"><span data-stu-id="6be18-123">This setting supports three values:</span></span>
- <span data-ttu-id="6be18-124">**Dynamics 365-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="6be18-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="6be18-125">Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="6be18-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="6be18-126">**SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="6be18-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="6be18-127">Denne innstillingen støttes for påloggede og anonyme brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="6be18-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="6be18-128">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen innløsning av Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="6be18-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="6be18-129">Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="6be18-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="6be18-130">Legge til en gavekortmodul på en side</span><span class="sxs-lookup"><span data-stu-id="6be18-130">Add a gift card module to a page</span></span>

<span data-ttu-id="6be18-131">Hvis du vil ha informasjon om hvordan du legger til en gavekortmodul på en kasseside og angir de nødvendige egenskapene, kan du se [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="6be18-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6be18-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6be18-132">Additional resources</span></span>

[<span data-ttu-id="6be18-133">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="6be18-133">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6be18-134">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="6be18-134">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6be18-135">Støtte for eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="6be18-135">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
