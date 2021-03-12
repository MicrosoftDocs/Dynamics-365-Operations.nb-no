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
ms.openlocfilehash: d3df563b62b40970509340802a09bb36dda14777
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001006"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="a948d-103">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="a948d-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a948d-104">Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a948d-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="a948d-105">Legge til domener under initialisering av e-handel</span><span class="sxs-lookup"><span data-stu-id="a948d-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="a948d-106">Hvis du vil knytte domener til Dynamics 365 Commerce-e-handelsmiljøet, kan du initialisere e-handel som beskrevet i [Distribuere en ny e-handelsleier](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="a948d-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="a948d-107">Under initialiseringen blir du bedt om å oppgi informasjon som skal brukes til å klargjøre ditt e-handelsmiljø.</span><span class="sxs-lookup"><span data-stu-id="a948d-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="a948d-108">Legg til alle domenene du planlegger å bruke med dette miljøet, i feltet **Støttede vertsnavn**.</span><span class="sxs-lookup"><span data-stu-id="a948d-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="a948d-109">Flere domener må skilles med semikolon.</span><span class="sxs-lookup"><span data-stu-id="a948d-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="a948d-110">På denne måten konfigureres domenene i alle de nødvendige Commerce-komponentene, og de er klare til bruk når du bytter trafikk fra innholdsleveringsnettverket (CDN) eller nettserveren og peker den til e-handel-frontene.</span><span class="sxs-lookup"><span data-stu-id="a948d-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="a948d-111">Legge til domener etter initialisering av e-handel</span><span class="sxs-lookup"><span data-stu-id="a948d-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="a948d-112">Hvis du vil knytte nye domener til e-handelsmiljøet etter at e-handel initialiseres, må du sende en serviceforespørsel.</span><span class="sxs-lookup"><span data-stu-id="a948d-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a948d-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a948d-113">Additional resources</span></span>

[<span data-ttu-id="a948d-114">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="a948d-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a948d-115">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="a948d-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a948d-116">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="a948d-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a948d-117">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="a948d-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a948d-118">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="a948d-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a948d-119">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="a948d-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a948d-120">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="a948d-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a948d-121">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="a948d-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a948d-122">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="a948d-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a948d-123">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="a948d-123">Enable location-based store detection</span></span>](enable-store-detection.md)
