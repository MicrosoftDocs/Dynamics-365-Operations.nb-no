---
title: Påloggingskobling omdirigerer tilbake til et e-handelsområde
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en påloggingskobling omdirigerer tilbake til e-commerce-området i stedet for å gå til påloggingssiden.
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
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585457"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="1d636-103">Påloggingskobling omdirigerer tilbake til et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="1d636-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d636-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en påloggingskobling omdirigerer tilbake til e-commerce-området i stedet for å gå til påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="1d636-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="1d636-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1d636-105">Description</span></span>

<span data-ttu-id="1d636-106">Når du har konfigurert en ny Microsoft Azure Active Directory B2C-leietaker (Azure AD B2C) i Commerce-områdebyggeren, blir brukere som velger koblingen **Logg på**, sendt tilbake til hovedsiden for e-handel uten å gå til påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="1d636-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="1d636-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="1d636-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="1d636-108">Bekreft at svaradressen er riktig konfigurert i Azure AD B2C-programmet</span><span class="sxs-lookup"><span data-stu-id="1d636-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="1d636-109">Hvis du vil bekrefte at svaradressen er riktig konfigurert i Azure AD B2C-programmet, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="1d636-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="1d636-110">Gå til [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="1d636-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="1d636-111">Velg Azure AD B2C-programmet du opprettet for områdetilgang.</span><span class="sxs-lookup"><span data-stu-id="1d636-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="1d636-112">Velg programmet du opprettet i løpet av Azure AD B2C-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="1d636-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="1d636-113">Under **Svar-URL** må du kontrollere at listen inneholder oppføringer for både URL-adressen for områdedomenet og den e-handelsgenererte URL-adressen, som vist i eksemplet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="1d636-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![URL-oppføringer for Azure AD B2C-svar](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="1d636-115">Både områdets domene-URL og den e-handelsgenererte URL-adressen må være i et gyldig URL-format som ikke omfatter ledende eller etterfølgende skråstreker.</span><span class="sxs-lookup"><span data-stu-id="1d636-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d636-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1d636-116">Additional resources</span></span>

[<span data-ttu-id="1d636-117">Registrere et webprogram i Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="1d636-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="1d636-118">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="1d636-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
