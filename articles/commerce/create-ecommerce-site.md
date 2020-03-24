---
title: Opprette et e-handelsområde
description: Dette emnet beskriver trinnene og informasjonen som kreves for å opprette et nytt e-handelsområde i Dynamics 365 Commerce-områdebyggeren.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
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
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096780"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="6f276-103">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="6f276-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6f276-104">Dette emnet beskriver trinnene og informasjonen som kreves for å opprette et nytt e-handelsområde i Dynamics 365 Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="6f276-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="6f276-105">Før du kan begynne å utvikle e-handelsområdet, må du først etablere et nytt område i områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="6f276-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="6f276-106">Hvis du vil begynne å utvikle ditt e-handelsområde, må du først opprette et nytt område i områdetsredigeringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="6f276-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="6f276-107">Før du kan opprette et nytt område må du opprette minst én nettbutikk i Commerce.</span><span class="sxs-lookup"><span data-stu-id="6f276-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="6f276-108">Konfigurere området</span><span class="sxs-lookup"><span data-stu-id="6f276-108">Set up your site</span></span>

<span data-ttu-id="6f276-109">Gjør følgende for å opprette området.</span><span class="sxs-lookup"><span data-stu-id="6f276-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="6f276-110">Åpne områdebyggermiljøet.</span><span class="sxs-lookup"><span data-stu-id="6f276-110">Open the site builder environment.</span></span> <span data-ttu-id="6f276-111">Du kan finne en kobling til områdebyggertjenesten i Microsoft Lifecycle Services (LCS) på siden for miljøfunksjoner for Commerce.</span><span class="sxs-lookup"><span data-stu-id="6f276-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="6f276-112">Velg **Nytt område**på startsiden for områderedigeringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="6f276-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="6f276-113">Angi følgende informasjon i dialogboksen **Nytt område**.</span><span class="sxs-lookup"><span data-stu-id="6f276-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="6f276-114">Felt</span><span class="sxs-lookup"><span data-stu-id="6f276-114">Field</span></span>                               | <span data-ttu-id="6f276-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6f276-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="6f276-116">Områdenavn</span><span class="sxs-lookup"><span data-stu-id="6f276-116">Site name</span></span>                           | <span data-ttu-id="6f276-117">Angi visningsnavnet som skal brukes for området, i redigeringsmiljøet for området.</span><span class="sxs-lookup"><span data-stu-id="6f276-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="6f276-118">Dette navnet vises bare i redigeringsmiljøet og blir ikke vist for kunder.</span><span class="sxs-lookup"><span data-stu-id="6f276-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="6f276-119">Sikkerhetsgruppe for områdeadministrator</span><span class="sxs-lookup"><span data-stu-id="6f276-119">Site administrator's security group</span></span> | <span data-ttu-id="6f276-120">Angi sikkerhetsgruppen for Microsoft Azure Active Directory (Azure AD) som administrerer brukere som har områdeadministratorrollen på dette området.</span><span class="sxs-lookup"><span data-stu-id="6f276-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="6f276-121">Standardkanal (driftsenhetsnummer)</span><span class="sxs-lookup"><span data-stu-id="6f276-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="6f276-122">Velg nettbutikken som dette området skal fungere som webbutikkfasade for.</span><span class="sxs-lookup"><span data-stu-id="6f276-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="6f276-123">Hvis du vil at ditt e-handelsområde skal støtte flere nettbutikker, må du knytte butikkene til området i **Områdeinnstillinger** etter at området er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="6f276-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="6f276-124">Standardspråk</span><span class="sxs-lookup"><span data-stu-id="6f276-124">Default language</span></span>                            | <span data-ttu-id="6f276-125">Angi standardspråket for denne nettbutikken og dette markedet.</span><span class="sxs-lookup"><span data-stu-id="6f276-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="6f276-126">En nettbutikk kan støtte flere språk.</span><span class="sxs-lookup"><span data-stu-id="6f276-126">An online store can support multiple languages.</span></span> <span data-ttu-id="6f276-127">Hvis du vil støtte flere språk for denne nettbutikken eller en annen nettbutikk, kan du konfigurere støtten i **Områdeinnstillinger** etter at området er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="6f276-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="6f276-128">Domene</span><span class="sxs-lookup"><span data-stu-id="6f276-128">Domain</span></span>                              | <span data-ttu-id="6f276-129">Velg et domenenavn som skal være domene for denne nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="6f276-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="6f276-130">Hvis du ikke har konfigurert noen domener i LCS, kan du la dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="6f276-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="6f276-131">Når domenet er konfigurert i LCS, må du legge det til i nettbutikken under **Områdeinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="6f276-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="6f276-132">Bane</span><span class="sxs-lookup"><span data-stu-id="6f276-132">Path</span></span>                              | <span data-ttu-id="6f276-133">Når området støtter mer enn ett språk for et gitt domenenavn, kan du bruke banefeltet til å opprette en unik område-URL-adresse for dette domenet og denne språkkombinasjonen.</span><span class="sxs-lookup"><span data-stu-id="6f276-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="6f276-134">Hvis språket du angav i **Standardspråk**-feltet, er det eneste språket du vil støtte for dette domenet eller vil fortsette å være standardspråket etter at du har lokalisert området til flere språk, anbefaler vi at du lar dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="6f276-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="6f276-135">Når området er opprettet, kan du kontrollere at det er tilknyttet nettbutikken din, ved å velge kategorien **Produker**. Du skal se sortimentet av produkter som er tilordnet nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="6f276-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="6f276-136">Du kan også bruke rullegardinmenyen øverst til venstre på siden for å få tilgang til de tildelte produktene etter kategori.</span><span class="sxs-lookup"><span data-stu-id="6f276-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f276-137">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6f276-137">Additional resources</span></span>

[<span data-ttu-id="6f276-138">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="6f276-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6f276-139">Distribuere et nytt e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="6f276-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6f276-140">Definere en kanal for nettbutikk</span><span class="sxs-lookup"><span data-stu-id="6f276-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="6f276-141">Knytte et nettområde til en kanal</span><span class="sxs-lookup"><span data-stu-id="6f276-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6f276-142">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="6f276-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6f276-143">Laste opp URL-adresser for omadressering samtidig</span><span class="sxs-lookup"><span data-stu-id="6f276-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="6f276-144">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="6f276-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="6f276-145">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="6f276-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6f276-146">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="6f276-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6f276-147">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="6f276-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6f276-148">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="6f276-148">Enable location-based store detection</span></span>](enable-store-detection.md)
