---
title: Velge å bruke vurderinger og anmeldelser
description: Dette emnet forklarer hvordan du velger å bruke vurderinger og omtaler på Microsoft Dynamics 365 Commerce-området.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697986"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="545d7-103">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="545d7-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="545d7-104">Dette emnet forklarer hvordan du velger å bruke vurderinger og omtaler på Microsoft Dynamics 365 Commerce-området.</span><span class="sxs-lookup"><span data-stu-id="545d7-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="545d7-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="545d7-105">Overview</span></span>

<span data-ttu-id="545d7-106">Løsningen for vurderinger og omtaler er en omnikanalløsning som du kan gjøre tilgjengelig i Dynamics 365 Commerce ved å bruke Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="545d7-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="545d7-107">LCS er en administrasjonsportal som forhandlere bruker for å administrere sine miljøer fra klargjøring til avvikling.</span><span class="sxs-lookup"><span data-stu-id="545d7-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="545d7-108">Hvis du vil bruke løsningen for vurderinger og omtaler på webområdet for Commerce, må du først velge å bruke løsningen.</span><span class="sxs-lookup"><span data-stu-id="545d7-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="545d7-109">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="545d7-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="545d7-110">Følg denne fremgangsmåten for å velge å bruke vurderinger og omtaler på området ditt.</span><span class="sxs-lookup"><span data-stu-id="545d7-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="545d7-111">Følg fremgangsmåten i [Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="545d7-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="545d7-112">Mens du fortsatt er i LCS, kan du gå til **Konfigurasjon av distribusjon av Retail \> Andre innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="545d7-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="545d7-113">Sett alternativet **Aktiver tjenesten for vurderinger og omtale** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="545d7-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="545d7-114">I **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler (sikkerhetsgruppeobjekt-ID)** angir du IDen til Microsoft Azure Active Directory (Azure AD)-sikkerhetsgruppen som inkluderer moderatorene for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="545d7-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Velge å bruke vurderinger og anmeldelser](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="545d7-116">Fullfør initialiseringsprosessen for e-handel.</span><span class="sxs-lookup"><span data-stu-id="545d7-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="545d7-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="545d7-117">Additional resources</span></span>

[<span data-ttu-id="545d7-118">Oversikt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="545d7-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="545d7-119">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="545d7-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="545d7-120">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="545d7-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="545d7-121">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="545d7-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
