---
title: Konfigurere domenenavnet
description: Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8b7bc322b1a42190d5eec99f89a34025c34ba09f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220492"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="aa1bd-103">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="aa1bd-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="aa1bd-104">Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="aa1bd-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="aa1bd-105">Legge til domener under initialisering av e-handel</span><span class="sxs-lookup"><span data-stu-id="aa1bd-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="aa1bd-106">Hvis du vil knytte domener til Dynamics 365 Commerce-e-handelsmiljøet, kan du initialisere e-handel som beskrevet i [Distribuere en ny e-handelsleier](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="aa1bd-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="aa1bd-107">Under initialiseringen blir du bedt om å oppgi informasjon som skal brukes til å klargjøre ditt e-handelsmiljø.</span><span class="sxs-lookup"><span data-stu-id="aa1bd-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="aa1bd-108">Legg til alle domenene du planlegger å bruke med dette miljøet, i feltet **Støttede vertsnavn**.</span><span class="sxs-lookup"><span data-stu-id="aa1bd-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="aa1bd-109">Flere domener må skilles med semikolon.</span><span class="sxs-lookup"><span data-stu-id="aa1bd-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="aa1bd-110">På denne måten konfigureres domenene i alle de nødvendige Commerce-komponentene, og de er klare til bruk når du bytter trafikk fra innholdsleveringsnettverket (CDN) eller nettserveren og peker den til e-handel-frontene.</span><span class="sxs-lookup"><span data-stu-id="aa1bd-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="aa1bd-111">Legge til domener etter initialisering av e-handel</span><span class="sxs-lookup"><span data-stu-id="aa1bd-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="aa1bd-112">Hvis du vil knytte nye domener til e-handelsmiljøet etter at e-handel initialiseres, må du sende en serviceforespørsel.</span><span class="sxs-lookup"><span data-stu-id="aa1bd-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa1bd-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="aa1bd-113">Additional resources</span></span>

[<span data-ttu-id="aa1bd-114">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="aa1bd-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="aa1bd-115">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="aa1bd-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="aa1bd-116">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="aa1bd-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="aa1bd-117">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="aa1bd-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="aa1bd-118">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="aa1bd-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="aa1bd-119">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="aa1bd-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="aa1bd-120">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="aa1bd-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="aa1bd-121">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="aa1bd-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="aa1bd-122">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="aa1bd-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="aa1bd-123">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="aa1bd-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]