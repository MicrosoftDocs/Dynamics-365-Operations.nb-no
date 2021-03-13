---
title: Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder
description: Dette emnet beskriver hvordan du konfigurerer betalingsmåten for kundekonto for e-handelsområder (B2B, business-to-business).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 754e2f83d6c8ff5d3698d98062e54bba7ccd9836
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035946"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="5fff6-103">Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder</span><span class="sxs-lookup"><span data-stu-id="5fff6-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5fff6-104">Dette emnet beskriver hvordan du konfigurerer betalingsmåten for kundekonto for e-handelsområder (B2B, business-to-business).</span><span class="sxs-lookup"><span data-stu-id="5fff6-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="5fff6-105">Forhandlere kan ta imot ulike typer betaling i bytte mot produktene og tjenestene de selger i en e-handelskanal.</span><span class="sxs-lookup"><span data-stu-id="5fff6-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="5fff6-106">Hver betalingstype en forhandler godtar, må konfigureres i Microsoft Dynamics 365 Commerce når systemet defineres.</span><span class="sxs-lookup"><span data-stu-id="5fff6-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="5fff6-107">Kundekontoen-betalingsmåten (eller "a konto") må støttes på B2B-e-handelsområder.</span><span class="sxs-lookup"><span data-stu-id="5fff6-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="5fff6-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="5fff6-108">Prerequisites</span></span>

1. <span data-ttu-id="5fff6-109">Legg til betalingsmåten for kundekonto i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5fff6-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="5fff6-110">Knytt kundekontobetalingsmåten til e-handelskanalen.</span><span class="sxs-lookup"><span data-stu-id="5fff6-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="5fff6-111">Kontroller at **Tillat a konto** er aktivert for kunden i **Detaljhandel og handel \> Kunder \> Alle kunder \> Betalingsstandarder** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5fff6-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="5fff6-112">Kontroller også at **Kredittgrense**-parameterne er angitt på riktig måte for kunden i **Detaljhandel og handel \> Kunder \> Alle kunder \> Kreditt og innkreving** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5fff6-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="5fff6-113">Aktivere kundekontobetalingsmetode i Commerce-områdebygger</span><span class="sxs-lookup"><span data-stu-id="5fff6-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="5fff6-114">For å aktivere kundekontobetalingsmetode i Commerce-områdebygger, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="5fff6-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5fff6-115">Gå til **Områdeinnstillinger \> Tillegg**.</span><span class="sxs-lookup"><span data-stu-id="5fff6-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="5fff6-116">Sett egenskapen **Aktiver kundekontobetalinger** til **Aktivert for B2B-kunder**.</span><span class="sxs-lookup"><span data-stu-id="5fff6-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="5fff6-117">Velg **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="5fff6-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="5fff6-118">De nye innstillingene trer i kraft bare etter at filen app.settings.json er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="5fff6-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="5fff6-119">Hvis du vil ha mer informasjon, kan du se [Oppdateringer for SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="5fff6-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="5fff6-120">Aktivere betalingsmåten for kundekonto på betalingssiden for B2B-e-handelsområdet</span><span class="sxs-lookup"><span data-stu-id="5fff6-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="5fff6-121">Følg disse trinnene for å aktivere betalingsmåten for kundekonto på betalingssiden for B2B-e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="5fff6-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="5fff6-122">I Commerce-områdebygger finner og redigerer du utsjekkingsside eller fragmentet som inneholder utsjekkingsmodulen for B2B-e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="5fff6-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="5fff6-123">I sporet **Container for betalingsdel** velger du **Legg til modul**, og deretter legger du til en **Kundekontobetaling**-modul.</span><span class="sxs-lookup"><span data-stu-id="5fff6-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="5fff6-124">Plasser modulen **Kundekontobetaling** ved å velge ellipsen (**...**) og deretter velge **Flytt ned** eller **Flytt opp** etter behov.</span><span class="sxs-lookup"><span data-stu-id="5fff6-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="5fff6-125">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="5fff6-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="5fff6-126">Bekrefte at betalingsmåten for kundekonto er aktivert og publisert</span><span class="sxs-lookup"><span data-stu-id="5fff6-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="5fff6-127">For å bekrefte at betalingsmåten for kundekonto er aktivert, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="5fff6-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="5fff6-128">Logg på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="5fff6-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="5fff6-129">Legg til et produkt i handlevognen.</span><span class="sxs-lookup"><span data-stu-id="5fff6-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="5fff6-130">Gå til utsjekkingssiden.</span><span class="sxs-lookup"><span data-stu-id="5fff6-130">Go to the checkout page.</span></span> <span data-ttu-id="5fff6-131">Du skal nå¨se den nye betalingsmåten **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="5fff6-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fff6-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5fff6-132">Additional resources</span></span>

[<span data-ttu-id="5fff6-133">Definere et B2B-e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="5fff6-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="5fff6-134">Opprette organisasonsmodellhierarkier for B2B-organisasjoner</span><span class="sxs-lookup"><span data-stu-id="5fff6-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="5fff6-135">Administrere forretningspartnerbrukere på B2B-e-handelsområder</span><span class="sxs-lookup"><span data-stu-id="5fff6-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="5fff6-136">Angi produktantallsgrenser for B2B-e-handelsområder</span><span class="sxs-lookup"><span data-stu-id="5fff6-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="5fff6-137">Oppdateringer for SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="5fff6-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)
