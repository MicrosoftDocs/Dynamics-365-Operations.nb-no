---
title: Konfigurere domenenavnet
description: Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365.
author: psimolin
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096826"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="b531c-103">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="b531c-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b531c-104">Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b531c-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="b531c-105">Legge til domener under initialisering av e-handel</span><span class="sxs-lookup"><span data-stu-id="b531c-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="b531c-106">Hvis du vil knytte domener til ditt e-handelsmiljø, kan du initialisere e-handel som beskrevet i [Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="b531c-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="b531c-107">Under initialiseringen blir du bedt om å oppgi informasjon som skal brukes til å klargjøre ditt e-handelsmiljø.</span><span class="sxs-lookup"><span data-stu-id="b531c-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="b531c-108">Legg til alle domenene du planlegger å bruke med dette miljøet, i feltet **Støttede vertsnavn**.</span><span class="sxs-lookup"><span data-stu-id="b531c-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="b531c-109">Flere domener må skilles med semikolon.</span><span class="sxs-lookup"><span data-stu-id="b531c-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="b531c-110">På denne måten konfigureres domenene i alle de nødvendige komponentene for e-handel, og de er klare til bruk når du bytter trafikk fra innholdsleveringsnettverket (CDN) eller webserveren og peker den til e-handel-frontene.</span><span class="sxs-lookup"><span data-stu-id="b531c-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="b531c-111">Legge til domener etter initialisering av e-handel</span><span class="sxs-lookup"><span data-stu-id="b531c-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="b531c-112">Hvis du vil knytte nye domener til e-handelsmiljøet etter at e-handel initialiseres, må du sende en serviceforespørsel.</span><span class="sxs-lookup"><span data-stu-id="b531c-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b531c-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b531c-113">Additional resources</span></span>

[<span data-ttu-id="b531c-114">Distribuere et nytt e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="b531c-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b531c-115">Definere en kanal for nettbutikk</span><span class="sxs-lookup"><span data-stu-id="b531c-115">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="b531c-116">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="b531c-116">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b531c-117">Knytte et nettområde til en kanal</span><span class="sxs-lookup"><span data-stu-id="b531c-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b531c-118">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="b531c-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b531c-119">Laste opp URL-adresser for omadressering samtidig</span><span class="sxs-lookup"><span data-stu-id="b531c-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="b531c-120">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="b531c-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="b531c-121">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="b531c-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b531c-122">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="b531c-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="b531c-123">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="b531c-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b531c-124">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="b531c-124">Enable location-based store detection</span></span>](enable-store-detection.md)
