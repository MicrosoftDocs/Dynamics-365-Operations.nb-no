---
title: Telefonsenterfunksjonalitet
description: Dette emnet gir en oversikt over telefonsenterspesifikke salgsfunksjoner i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 55bad891f9295eca6b0bf39847ede890b7294370
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---

# <a name="call-center-functionality"></a><span data-ttu-id="029dc-103">Telefonsenterfunksjonalitet</span><span class="sxs-lookup"><span data-stu-id="029dc-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="029dc-104">Denne artikkelen gir en oversikt over telefonsenterspesifikke salgsfunksjoner i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="029dc-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="029dc-105">Dynamics 365 for Retail støtter også telefonsentre som en type detaljhandelskanal.</span><span class="sxs-lookup"><span data-stu-id="029dc-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="029dc-106">I et telefonsenter tar arbeidere imot ordrer fra kunder over telefon og oppretter salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="029dc-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="029dc-107">Telefonsenterfunksjonaliteten omfatter funksjoner som er utviklet for å gjøre det enklere å ta imot telefonordrer og håndtere kundeservice under oppfyllelsen av ordren.</span><span class="sxs-lookup"><span data-stu-id="029dc-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="029dc-108">Telefonsenterarbeidere kan for eksempel angi betalingsinformasjon direkte i salgsordren, og kan vise en detaljert oversikt over gebyrer og betalinger før de sender ordren.</span><span class="sxs-lookup"><span data-stu-id="029dc-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="029dc-109">Arbeidere har også alternativer for styring av priser, og de har tilgang til forskjellige data om kunder, produkter og priser fra siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="029dc-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="029dc-110">Telefonsentre har også forbedret funksjonalitet for sporing av kundehistorikk og ordrestatus.</span><span class="sxs-lookup"><span data-stu-id="029dc-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="029dc-111">Hvert telefonsenter kan ha sine egne brukere, betalingsmåter, prisgrupper, finansdimensjoner og leveringsmåter.</span><span class="sxs-lookup"><span data-stu-id="029dc-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="029dc-112">Du kan konfigurere disse alternativene når du oppretter telefonsenteret.</span><span class="sxs-lookup"><span data-stu-id="029dc-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="029dc-113">Du kan også bruke siden **Telefonsenter** til å aktivere eller deaktivere følgende funksjonsgrupper som er unike for telefonsentre:</span><span class="sxs-lookup"><span data-stu-id="029dc-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="029dc-114">**Ordrefullføring** – Denne gruppen inneholder funksjoner som er relatert til betalinger og ordrefullføring på siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="029dc-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="029dc-115">**Styrt salg** – Denne gruppen inneholder funksjoner som er knyttet til kildekoder, skript og katalogforespørsler.</span><span class="sxs-lookup"><span data-stu-id="029dc-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="029dc-116">Når du aktiverer disse funksjonene i innstillingene for telefonsenter, blir de tilgjengelige på siden **Salgsordre** for brukere som er knyttet til telefonsenteret.</span><span class="sxs-lookup"><span data-stu-id="029dc-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="029dc-117">De fleste av disse funksjonene krever ekstra oppsett før de kan brukes.</span><span class="sxs-lookup"><span data-stu-id="029dc-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="029dc-118">Før brukere kan opprette telefonsenterordrer, må du legge til disse brukerne i telefonsenteret som telefonsenterbrukere.</span><span class="sxs-lookup"><span data-stu-id="029dc-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="029dc-119">Dette trinnet aktiverer kanalspesifikke konfigurasjon og funksjonalitet for telefonsenteret.</span><span class="sxs-lookup"><span data-stu-id="029dc-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="029dc-120">Her er noen eksempler på hvilke funksjoner som er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="029dc-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="029dc-121">Veiledet salg omfatter konfigurasjonsalternativer for telefonsalgskript og produktbilder for å hjelpe og veilede salgsassistenter mens de tar imot ordrer.</span><span class="sxs-lookup"><span data-stu-id="029dc-121">Guided selling provides configuration options for tele-sales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="029dc-122">Ordrer kan ikke fullføres før salgsassistenten har registrert minimum én betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="029dc-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="029dc-123">Regler for mersalg og kryssalg kan konfigureres til å be salgsassistenter om å fremme bestemte produkter til kunden.</span><span class="sxs-lookup"><span data-stu-id="029dc-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="029dc-124">Salgsassistenter kan registrere kildekoden for katalogen som en kunde bestiller fra.</span><span class="sxs-lookup"><span data-stu-id="029dc-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="029dc-125">Salgsassistenter kan legge til en forhandlers kuponger i ordren.</span><span class="sxs-lookup"><span data-stu-id="029dc-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="029dc-126">Salgassistenter kan selge kontinuitetsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="029dc-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="029dc-127">Ordrer kan settes på vent manuelt eller automatisk, for å angi at andre undersøkelser kreves før ordren kan behandles.</span><span class="sxs-lookup"><span data-stu-id="029dc-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





