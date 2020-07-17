---
title: Opprette et e-handelsområde
description: Dette emnet beskriver trinnene og informasjonen som kreves for å opprette et nytt e-handelsområde i Dynamics 365 Commerce-områdebyggeren.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ea3517a4f2b84db8a87a97d2f644bb4436f8693f
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533442"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="59a51-103">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="59a51-103">Create an e-Commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="59a51-104">Dette emnet beskriver trinnene og informasjonen som kreves for å opprette et nytt e-handelsområde i Dynamics 365 Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="59a51-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="59a51-105">Når du lisensierer mulighetene for e-handel, blir områdebygger klargjort med et startområde som du kan bruke som grunnlag for ditt eget område.</span><span class="sxs-lookup"><span data-stu-id="59a51-105">When you license the e-Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="59a51-106">Hvis du imidlertid vil starte fra grunnen av, eller hvis du vil opprette et annet område, må du opprette et nytt område i områdets redigeringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="59a51-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="59a51-107">Konfigurere området</span><span class="sxs-lookup"><span data-stu-id="59a51-107">Set up your site</span></span>

<span data-ttu-id="59a51-108">Gjør følgende for å opprette området.</span><span class="sxs-lookup"><span data-stu-id="59a51-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="59a51-109">Åpne områdebyggermiljøet.</span><span class="sxs-lookup"><span data-stu-id="59a51-109">Open the site builder environment.</span></span> <span data-ttu-id="59a51-110">Du kan finne en kobling til områdebyggertjenesten i Microsoft Lifecycle Services (LCS) på siden for miljøfunksjoner for Commerce.</span><span class="sxs-lookup"><span data-stu-id="59a51-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="59a51-111">Velg **Nytt område**på startsiden for områderedigeringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="59a51-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="59a51-112">Angi følgende informasjon i dialogboksen **Nytt område**.</span><span class="sxs-lookup"><span data-stu-id="59a51-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="59a51-113">Felt</span><span class="sxs-lookup"><span data-stu-id="59a51-113">Field</span></span>                               | <span data-ttu-id="59a51-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="59a51-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="59a51-115">Områdenavn</span><span class="sxs-lookup"><span data-stu-id="59a51-115">Site name</span></span>                           | <span data-ttu-id="59a51-116">Angi visningsnavnet som skal brukes for området, i redigeringsmiljøet for området.</span><span class="sxs-lookup"><span data-stu-id="59a51-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="59a51-117">Dette navnet vises bare i redigeringsmiljøet og blir ikke vist for kunder.</span><span class="sxs-lookup"><span data-stu-id="59a51-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="59a51-118">Sikkerhetsgruppe for områdeadministrator</span><span class="sxs-lookup"><span data-stu-id="59a51-118">Site administrator's security group</span></span> | <span data-ttu-id="59a51-119">Angi sikkerhetsgruppen for Microsoft Azure Active Directory (Azure AD) som administrerer brukere som har områdeadministratorrollen på dette området.</span><span class="sxs-lookup"><span data-stu-id="59a51-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="59a51-120">Standardkanal (driftsenhetsnummer)</span><span class="sxs-lookup"><span data-stu-id="59a51-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="59a51-121">Velg nettbutikken som dette området skal fungere som webbutikkfasade for.</span><span class="sxs-lookup"><span data-stu-id="59a51-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="59a51-122">Hvis du vil at ditt e-handelsområde skal støtte flere nettbutikker, må du knytte butikkene til området i **Områdeinnstillinger** etter at området er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="59a51-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="59a51-123">Standardspråk</span><span class="sxs-lookup"><span data-stu-id="59a51-123">Default language</span></span>                            | <span data-ttu-id="59a51-124">Angi standardspråket for denne nettbutikken og dette markedet.</span><span class="sxs-lookup"><span data-stu-id="59a51-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="59a51-125">En nettbutikk kan støtte flere språk.</span><span class="sxs-lookup"><span data-stu-id="59a51-125">An online store can support multiple languages.</span></span> <span data-ttu-id="59a51-126">Hvis du vil støtte flere språk for denne nettbutikken eller en annen nettbutikk, kan du konfigurere støtten i **Områdeinnstillinger** etter at området er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="59a51-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="59a51-127">Domene</span><span class="sxs-lookup"><span data-stu-id="59a51-127">Domain</span></span>                              | <span data-ttu-id="59a51-128">Velg et domenenavn som skal være domene for denne nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="59a51-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="59a51-129">Hvis du ikke har konfigurert noen domener i LCS, kan du la dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="59a51-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="59a51-130">Når domenet er konfigurert i LCS, må du legge det til i nettbutikken under **Områdeinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="59a51-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="59a51-131">Bane</span><span class="sxs-lookup"><span data-stu-id="59a51-131">Path</span></span>                              | <span data-ttu-id="59a51-132">Når området støtter mer enn ett språk for et gitt domenenavn, kan du bruke banefeltet til å opprette en unik område-URL-adresse for dette domenet og denne språkkombinasjonen.</span><span class="sxs-lookup"><span data-stu-id="59a51-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="59a51-133">Hvis språket du angav i **Standardspråk**-feltet, er det eneste språket du vil støtte for dette domenet eller vil fortsette å være standardspråket etter at du har lokalisert området til flere språk, anbefaler vi at du lar dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="59a51-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="59a51-134">Når området er opprettet, kan du kontrollere at det er tilknyttet nettbutikken din, ved å velge kategorien **Produker**. Du skal se sortimentet av produkter som er tilordnet nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="59a51-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="59a51-135">Du kan også bruke rullegardinmenyen øverst til venstre på siden for å få tilgang til de tildelte produktene etter kategori.</span><span class="sxs-lookup"><span data-stu-id="59a51-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59a51-136">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="59a51-136">Additional resources</span></span>

[<span data-ttu-id="59a51-137">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="59a51-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="59a51-138">Distribuere et nytt e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="59a51-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="59a51-139">Knytte et nettområde til en kanal</span><span class="sxs-lookup"><span data-stu-id="59a51-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="59a51-140">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="59a51-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="59a51-141">Laste opp URL-adresser for omadressering samtidig</span><span class="sxs-lookup"><span data-stu-id="59a51-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="59a51-142">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="59a51-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="59a51-143">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="59a51-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="59a51-144">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="59a51-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="59a51-145">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="59a51-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="59a51-146">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="59a51-146">Enable location-based store detection</span></span>](enable-store-detection.md)
