---
title: Begrense tilgang til en butikkfasade under testing eller utvikling
description: Dette emnet beskriver hvordan du begrenser tilgang til en Microsoft Dynamics 365 Commerce-butikkfasade når det skjer intern testing eller utvikling.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585469"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="a45d2-103">Begrense tilgang til en butikkfasade under testing eller utvikling</span><span class="sxs-lookup"><span data-stu-id="a45d2-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a45d2-104">Dette emnet beskriver hvordan du begrenser tilgang til en Microsoft Dynamics 365 Commerce-butikkfasade når det skjer intern testing eller utvikling.</span><span class="sxs-lookup"><span data-stu-id="a45d2-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="a45d2-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a45d2-105">Description</span></span>

<span data-ttu-id="a45d2-106">Under intern testing eller aktiv utvikling kan det hende at du vil begrense tilgangen til området for å hindre at eksterne brukere får tilgang til de publiserte butikkområdesidene.</span><span class="sxs-lookup"><span data-stu-id="a45d2-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="a45d2-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="a45d2-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="a45d2-108">Konfigurere Azure AD B2C ved hjelp av standard brukerflyter</span><span class="sxs-lookup"><span data-stu-id="a45d2-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="a45d2-109">Hvis du vil ha mer informasjon om hvordan du konfigurerer Azure Active Directory B2C (Azure AD B2C) for e-handelsområdet, kan du se [Definere en B2C-leier i Commerce](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="a45d2-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="a45d2-110">Begrense brukertilgang til butikksider og blokkere oppretting av nye brukere</span><span class="sxs-lookup"><span data-stu-id="a45d2-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="a45d2-111">Følg denne fremgangsmåten for å begrense brukertilgang til butikksider i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="a45d2-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a45d2-112">Gå til området ditt.</span><span class="sxs-lookup"><span data-stu-id="a45d2-112">Go to your site.</span></span>
1. <span data-ttu-id="a45d2-113">Velg **Sider**, og velg deretter siden du vil begrense brukertilgang for.</span><span class="sxs-lookup"><span data-stu-id="a45d2-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="a45d2-114">Velg modul- eller fragmentsporet, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a45d2-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="a45d2-115">Velg **Krever pålogging?** i egenskapsruten, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="a45d2-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="a45d2-116">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="a45d2-116">Select **Publish**.</span></span>

<span data-ttu-id="a45d2-117">Følg denne fremgangsmåten for å blokkere opprettingen av nye Azure AD-brukere.</span><span class="sxs-lookup"><span data-stu-id="a45d2-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="a45d2-118">Gå til [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="a45d2-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="a45d2-119">Velg Azure AD B2C-programmet du opprettet for områdetilgang.</span><span class="sxs-lookup"><span data-stu-id="a45d2-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="a45d2-120">Velg **Brukerflyter** til venstre.</span><span class="sxs-lookup"><span data-stu-id="a45d2-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="a45d2-121">Øverst på siden **Brukerflyter** velger du **Ny brukerflyt**.</span><span class="sxs-lookup"><span data-stu-id="a45d2-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="a45d2-122">Velg **Forhåndsvisning** på siden **Velg en brukerflyttype**.</span><span class="sxs-lookup"><span data-stu-id="a45d2-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="a45d2-123">På midten av siden velger du **Logg på v2**.</span><span class="sxs-lookup"><span data-stu-id="a45d2-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="a45d2-124">Følg deretter trinnene i [Konfigurere en B2C-leier i Commerce](../set-up-b2c-tenant.md) for å konfigurere flyten som områdets standard brukerflyt for Azure AD B2C under testing eller utvikling.</span><span class="sxs-lookup"><span data-stu-id="a45d2-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a45d2-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a45d2-125">Additional resources</span></span>

[<span data-ttu-id="a45d2-126">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="a45d2-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="a45d2-127">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="a45d2-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
