---
title: Aktivere stedsbasert butikkregistrering
description: Dette emnet beskriver hvordan du aktiverer stedsbasert butikkregistrering for Dynamics 365 Commerce-området.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71e523cab20281d5db7efff40b5ef4f7293a4765
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799137"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="71cab-103">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="71cab-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71cab-104">Dette emnet beskriver hvordan du aktiverer stedsbasert butikkregistrering for Dynamics 365 Commerce-området.</span><span class="sxs-lookup"><span data-stu-id="71cab-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="71cab-105">Med stedsbasert butikkregistrering i Commerce kan du gi relevant områdeinnhold til kunder basert på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="71cab-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="71cab-106">Når stedsbasert butikkregistrering er aktivert, bruker Commerce-gjengivelsestjenesten lands-/områdeinformasjonen fra IP-adressen til kundens webleser til å dirigere kunden til den beste geografiske områdekonfigurasjonen som er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="71cab-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="71cab-107">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="71cab-107">Privacy notice</span></span>

<span data-ttu-id="71cab-108">Hvis du aktiverer den stedsbaserte butikkregistreringsfunksjonen, sendes informasjon fra kundens webleser til en Microsoft-stedstjeneste.</span><span class="sxs-lookup"><span data-stu-id="71cab-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="71cab-109">Denne informasjonen brukes deretter til å angi kundeinnholdet som er relevant for hans eller hennes lokasjon.</span><span class="sxs-lookup"><span data-stu-id="71cab-109">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="71cab-110">Både informasjon som sendes fra kundens webleser, og den stedsbaserte informasjonen som returneres til kunden, er underlagt retningslinjer for personvern og informasjonskapsler.</span><span class="sxs-lookup"><span data-stu-id="71cab-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="71cab-111">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="71cab-111">Turn on location-based store detection</span></span>

<span data-ttu-id="71cab-112">Følg denne fremgangsmåten for å aktivere stedsbasert butikkregistrering i Commerce.</span><span class="sxs-lookup"><span data-stu-id="71cab-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="71cab-113">Gå til området ditt i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="71cab-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="71cab-114">Velg **Områdebehandling** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="71cab-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="71cab-115">Velg **Områdeinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="71cab-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="71cab-116">Sett **Aktiver registrering av plasseringsbasert butikk** til **På**.</span><span class="sxs-lookup"><span data-stu-id="71cab-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71cab-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="71cab-117">Additional resources</span></span>

[<span data-ttu-id="71cab-118">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="71cab-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="71cab-119">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="71cab-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="71cab-120">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="71cab-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="71cab-121">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="71cab-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="71cab-122">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="71cab-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="71cab-123">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="71cab-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="71cab-124">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="71cab-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="71cab-125">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="71cab-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="71cab-126">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="71cab-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="71cab-127">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="71cab-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
