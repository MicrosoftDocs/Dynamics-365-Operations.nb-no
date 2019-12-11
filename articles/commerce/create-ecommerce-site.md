---
title: Opprette et e-handelsområde
description: Dette emnet beskriver oppgavene som er knyttet til oppretting av et nytt e-handelsområde i Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697135"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="ad262-103">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="ad262-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ad262-104">Dette emnet beskriver oppgavene som er knyttet til oppretting av et nytt e-handelsområde i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad262-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ad262-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="ad262-105">Overview</span></span>

<span data-ttu-id="ad262-106">Hvis du vil begynne å utvikle ditt e-handelsområde, må du først opprette et nytt område i områdetsredigeringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="ad262-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="ad262-107">Før du kan opprette et nytt område må du opprette minst én nettbutikk i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="ad262-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="ad262-108">Konfigurere området</span><span class="sxs-lookup"><span data-stu-id="ad262-108">Set up your site</span></span>

<span data-ttu-id="ad262-109">Gjør følgende for å opprette området.</span><span class="sxs-lookup"><span data-stu-id="ad262-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="ad262-110">I Microsoft Lifecycle Services (LCS) klikker du koblingen for områderedigeringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="ad262-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="ad262-111">Velg **Nytt område**på startsiden for områderedigeringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="ad262-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="ad262-112">Angi følgende informasjon i dialogboksen **Nytt område**.</span><span class="sxs-lookup"><span data-stu-id="ad262-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="ad262-113">Felt</span><span class="sxs-lookup"><span data-stu-id="ad262-113">Field</span></span>                               | <span data-ttu-id="ad262-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ad262-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="ad262-115">Områdenavn</span><span class="sxs-lookup"><span data-stu-id="ad262-115">Site name</span></span>                           | <span data-ttu-id="ad262-116">Angi visningsnavnet som skal brukes for området, i redigeringsmiljøet for området.</span><span class="sxs-lookup"><span data-stu-id="ad262-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="ad262-117">Dette navnet vises bare i redigeringsmiljøet og blir ikke vist for kunder.</span><span class="sxs-lookup"><span data-stu-id="ad262-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="ad262-118">Sikkerhetsgruppe for områdeadministrator</span><span class="sxs-lookup"><span data-stu-id="ad262-118">Site administrator's security group</span></span> | <span data-ttu-id="ad262-119">Angi sikkerhetsgruppen for Microsoft Azure Active Directory (Azure AD) som administrerer brukere som har områdeadministratorrollen på dette området.</span><span class="sxs-lookup"><span data-stu-id="ad262-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="ad262-120">Standardkanal (driftsenhetsnummer)</span><span class="sxs-lookup"><span data-stu-id="ad262-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="ad262-121">Velg nettbutikken som dette området skal fungere som webbutikkfasade for.</span><span class="sxs-lookup"><span data-stu-id="ad262-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="ad262-122">Hvis du vil at ditt e-handelsområde skal støtte flere nettbutikker, må du knytte butikkene til området i **Områdeinnstillinger** etter at området er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="ad262-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="ad262-123">Standardspråk</span><span class="sxs-lookup"><span data-stu-id="ad262-123">Default language</span></span>                            | <span data-ttu-id="ad262-124">Angi standardspråket for denne nettbutikken og dette markedet.</span><span class="sxs-lookup"><span data-stu-id="ad262-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="ad262-125">En nettbutikk kan støtte flere språk.</span><span class="sxs-lookup"><span data-stu-id="ad262-125">An online store can support multiple languages.</span></span> <span data-ttu-id="ad262-126">Hvis du vil støtte flere språk for denne nettbutikken eller en annen nettbutikk, kan du konfigurere støtten i **Områdeinnstillinger** etter at området er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="ad262-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="ad262-127">Domene</span><span class="sxs-lookup"><span data-stu-id="ad262-127">Domain</span></span>                              | <span data-ttu-id="ad262-128">Velg et domenenavn som skal være domene for denne nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="ad262-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="ad262-129">Hvis du ikke har konfigurert noen domener i LCS, kan du la dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="ad262-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="ad262-130">Når domenet er konfigurert i LCS, må du legge det til i nettbutikken under **Områdeinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="ad262-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="ad262-131">Bane</span><span class="sxs-lookup"><span data-stu-id="ad262-131">Path</span></span>                              | <span data-ttu-id="ad262-132">Når området støtter mer enn ett språk for et gitt domenenavn, kan du bruke banefeltet til å opprette en unik område-URL-adresse for dette domenet og denne språkkombinasjonen.</span><span class="sxs-lookup"><span data-stu-id="ad262-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="ad262-133">Hvis språket du angav i **Standardspråk**-feltet, er det eneste språket du vil støtte for dette domenet eller vil fortsette å være standardspråket etter at du har lokalisert området til flere språk, anbefaler vi at du lar dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="ad262-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="ad262-134">Når området er opprettet, kan du kontrollere at det er tilknyttet nettbutikken din, ved å velge kategorien **Produker**. Du skal se sortimentet av produkter som er tilordnet nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="ad262-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="ad262-135">Du kan også bruke rullegardinmenyen øverst til venstre på siden for å få tilgang til de tildelte produktene etter kategori.</span><span class="sxs-lookup"><span data-stu-id="ad262-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad262-136">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ad262-136">Additional resources</span></span>

[<span data-ttu-id="ad262-137">Oversikt over nettbutikk</span><span class="sxs-lookup"><span data-stu-id="ad262-137">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="ad262-138">Distribuere et nytt e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="ad262-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ad262-139">Knytte et nettområde til en kanal</span><span class="sxs-lookup"><span data-stu-id="ad262-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ad262-140">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="ad262-140">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ad262-141">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="ad262-141">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ad262-142">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="ad262-142">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="ad262-143">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="ad262-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="ad262-144">Oversikt over redigering av startside</span><span class="sxs-lookup"><span data-stu-id="ad262-144">Authoring home page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="ad262-145">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="ad262-145">Add a new site page</span></span>](add-new-page.md)
