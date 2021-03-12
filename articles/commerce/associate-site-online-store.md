---
title: Knytte et Dynamics 365 Commerce-nettsted til en nettkanal
description: Dette emnet forklarer hvordan du knytter Microsoft Dynamics 365 Commerce-området til én eller flere nettbutikker.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc93441bd09deccdb8c7ecf955c0ec5177c0b31e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980029"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="c1f32-103">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="c1f32-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c1f32-104">Dette emnet forklarer hvordan du knytter Microsoft Dynamics 365 Commerce-området til én eller flere nettbutikker.</span><span class="sxs-lookup"><span data-stu-id="c1f32-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="c1f32-105">Når du har klargjort Dynamics 365 Commerce-e-handelsmiljøet ved hjelp av portalen for Microsoft Dynamics Lifecycle Services (LCS), er du klar til å opprette ditt første nettsted for e-handel.</span><span class="sxs-lookup"><span data-stu-id="c1f32-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="c1f32-106">Som en del av opprettelsen av første område, kan du knytte området til en nettbutikk som er opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="c1f32-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="c1f32-107">Dette trinnet binder området til en Internett-kanal og lar området vise navigasjonshierarkiet, produkter, kategorier, priser, leveringsalternativer og alt annet som du definerte i nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="c1f32-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="c1f32-108">Hvis du vil opprette et nytt område og knytte til en nettbutikk, kan du i LCS velge koblingen for områdets redigeringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="c1f32-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="c1f32-109">Velg deretter **Nytt område** på startsiden for områderedigeringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="c1f32-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="c1f32-110">I dialogboksen **Nytt område** må du gi grunnleggende informasjon om området.</span><span class="sxs-lookup"><span data-stu-id="c1f32-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="c1f32-111">Hvis du vil ha en fullstendig forklaring på informasjonen du må oppgi, kan du se [Opprette et nytt e-handelsområde](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="c1f32-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="c1f32-112">Når området er opprettet, kan du kontrollere at det er tilknyttet nettbutikken din, ved å velge kategorien **Produker**. Du skal se sortimentet av produkter som er tilordnet nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="c1f32-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="c1f32-113">Du kan også bruke rullegardinfeltet øverst til venstre på siden for å få tilgang til produktene etter kategori.</span><span class="sxs-lookup"><span data-stu-id="c1f32-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1f32-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c1f32-114">Additional resources</span></span>

[<span data-ttu-id="c1f32-115">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="c1f32-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="c1f32-116">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="c1f32-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="c1f32-117">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="c1f32-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="c1f32-118">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="c1f32-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="c1f32-119">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="c1f32-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="c1f32-120">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="c1f32-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="c1f32-121">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="c1f32-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="c1f32-122">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="c1f32-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="c1f32-123">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="c1f32-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="c1f32-124">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="c1f32-124">Enable location-based store detection</span></span>](enable-store-detection.md)
