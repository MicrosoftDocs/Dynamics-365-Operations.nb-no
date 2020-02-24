---
title: Aktivere stedsbasert butikkregistrering
description: Dette emnet beskriver hvordan du aktiverer stedsbasert butikkregistrering for Dynamics 365 Commerce-området.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 304d8d2f05916295b9c6320561d6a25ff40df955
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003102"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="bfa79-103">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="bfa79-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bfa79-104">Dette emnet beskriver hvordan du aktiverer stedsbasert butikkregistrering for Dynamics 365 Commerce-området.</span><span class="sxs-lookup"><span data-stu-id="bfa79-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="bfa79-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="bfa79-105">Overview</span></span>

<span data-ttu-id="bfa79-106">Med stedsbasert butikkregistrering i Commerce kan du gi relevant områdeinnhold til kunder basert på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="bfa79-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="bfa79-107">Når stedsbasert butikkregistrering er aktivert, bruker Commerce-gjengivelsestjenesten lands-/områdeinformasjonen fra IP-adressen til kundens webleser til å dirigere kunden til den beste geografiske områdekonfigurasjonen som er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="bfa79-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="bfa79-108">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="bfa79-108">Privacy notice</span></span>

<span data-ttu-id="bfa79-109">Hvis du aktiverer den stedsbaserte butikkregistreringsfunksjonen, sendes informasjon fra kundens webleser til en Microsoft-stedstjeneste.</span><span class="sxs-lookup"><span data-stu-id="bfa79-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="bfa79-110">Denne informasjonen brukes deretter til å angi kundeinnholdet som er relevant for hans eller hennes lokasjon.</span><span class="sxs-lookup"><span data-stu-id="bfa79-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="bfa79-111">Både informasjon som sendes fra kundens webleser, og den stedsbaserte informasjonen som returneres til kunden, er underlagt retningslinjer for personvern og informasjonskapsler.</span><span class="sxs-lookup"><span data-stu-id="bfa79-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="bfa79-112">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="bfa79-112">Turn on location-based store detection</span></span>

<span data-ttu-id="bfa79-113">Følg denne fremgangsmåten for å aktivere stedsbasert butikkregistrering i Commerce.</span><span class="sxs-lookup"><span data-stu-id="bfa79-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bfa79-114">Gå til området ditt i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="bfa79-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="bfa79-115">Velg **Områdebehandling** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="bfa79-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="bfa79-116">Velg **Områdeinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="bfa79-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="bfa79-117">Sett **Aktiver registrering av plasseringsbasert butikk** til **På**.</span><span class="sxs-lookup"><span data-stu-id="bfa79-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bfa79-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bfa79-118">Additional resources</span></span>

[<span data-ttu-id="bfa79-119">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="bfa79-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="bfa79-120">Distribuere et nytt e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="bfa79-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="bfa79-121">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="bfa79-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="bfa79-122">Knytte et nettområde til en kanal</span><span class="sxs-lookup"><span data-stu-id="bfa79-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="bfa79-123">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="bfa79-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="bfa79-124">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="bfa79-124">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="bfa79-125">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="bfa79-125">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
