---
title: Velge å bruke vurderinger og anmeldelser
description: Dette emnet forklarer hvordan du velger å bruke vurderinger og omtaler på Microsoft Dynamics 365 Commerce-området.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eda7fbaeea8d3c1a07f7b43cafe44886d149a211
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027271"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="a6968-103">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="a6968-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a6968-104">Dette emnet forklarer hvordan du velger å bruke vurderinger og omtaler på Microsoft Dynamics 365 Commerce-området.</span><span class="sxs-lookup"><span data-stu-id="a6968-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="a6968-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="a6968-105">Overview</span></span>

<span data-ttu-id="a6968-106">Løsningen for vurderinger og omtaler er en omnikanalløsning som du kan gjøre tilgjengelig i Dynamics 365 Commerce ved å bruke Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a6968-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a6968-107">LCS er en administrasjonsportal som forhandlere bruker for å administrere sine miljøer fra klargjøring til avvikling.</span><span class="sxs-lookup"><span data-stu-id="a6968-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="a6968-108">Hvis du vil bruke for vurderinger og omtaler på handelsområdet ditt, må du velge vurdering og omtaler under distribusjon av e-handelsområdet ditt på Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6968-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="a6968-109">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="a6968-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="a6968-110">Følg denne fremgangsmåten for å velge å bruke vurderinger og omtaler på området ditt.</span><span class="sxs-lookup"><span data-stu-id="a6968-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="a6968-111">Følg fremgangsmåten i [Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="a6968-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="a6968-112">Mens du fortsatt er i LCS, kan du gå til **Konfigurasjon av distribusjon av Retail \> Andre innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="a6968-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="a6968-113">Sett alternativet **Aktiver tjenesten for vurderinger og omtale** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a6968-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="a6968-114">I **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler (sikkerhetsgruppeobjekt-ID)** angir du IDen til Microsoft Azure Active Directory (Azure AD)-sikkerhetsgruppen som inkluderer moderatorene for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="a6968-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Velge å bruke vurderinger og anmeldelser](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="a6968-116">Fullfør initialiseringsprosessen for e-handel.</span><span class="sxs-lookup"><span data-stu-id="a6968-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="a6968-117">Hvis du er en eksisterende Dynamics 365 Commerce-kunde som allerede har distribuert et e-handelsområde uten å ha valgt vurderinger og omtaler, og som nå ønsker å bruke for vurderinger og omtaler fra Dynamics 365 Commerce-pakken, kan du sende en tjenesteforespørsel.</span><span class="sxs-lookup"><span data-stu-id="a6968-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="a6968-118">Hvis du vil ha informasjon om hvordan du sender en tjenesteforespørsel, kan du se [Prosess for å sende inn tjenesteforespørsler](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="a6968-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="a6968-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a6968-119">Additional resources</span></span>

[<span data-ttu-id="a6968-120">Oversikt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="a6968-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="a6968-121">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="a6968-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="a6968-122">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="a6968-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="a6968-123">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="a6968-123">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


