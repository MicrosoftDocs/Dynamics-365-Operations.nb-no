---
title: Påloggingskobling omdirigerer tilbake til et e-handelsområde
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en påloggingskobling omdirigerer tilbake til e-commerce-området i stedet for å gå til påloggingssiden.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: a1d0ae4e487c391020947c607d5d7cb5d1ba6af4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020609"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="c377a-103">Påloggingskobling omdirigerer tilbake til et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="c377a-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c377a-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en påloggingskobling omdirigerer tilbake til e-commerce-området i stedet for å gå til påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="c377a-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="c377a-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c377a-105">Description</span></span>

<span data-ttu-id="c377a-106">Når du har konfigurert en ny Microsoft Azure Active Directory B2C-leietaker (Azure AD B2C) i Commerce-områdebyggeren, blir brukere som velger koblingen **Logg på**, sendt tilbake til hovedsiden for e-handel uten å gå til påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="c377a-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="c377a-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="c377a-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="c377a-108">Bekreft at svaradressen er riktig konfigurert i Azure AD B2C-programmet</span><span class="sxs-lookup"><span data-stu-id="c377a-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="c377a-109">Hvis du vil bekrefte at svaradressen er riktig konfigurert i Azure AD B2C-programmet, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="c377a-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="c377a-110">Gå til [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="c377a-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="c377a-111">Velg Azure AD B2C-programmet du opprettet for områdetilgang.</span><span class="sxs-lookup"><span data-stu-id="c377a-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="c377a-112">Velg programmet du opprettet i løpet av Azure AD B2C-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="c377a-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="c377a-113">Under **Svar-URL** må du kontrollere at listen inneholder oppføringer for både URL-adressen for områdedomenet og den e-handelsgenererte URL-adressen, som vist i eksemplet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c377a-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![URL-oppføringer for Azure AD B2C-svar](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="c377a-115">Både områdets domene-URL og den e-handelsgenererte URL-adressen må være i et gyldig URL-format som ikke omfatter ledende eller etterfølgende skråstreker.</span><span class="sxs-lookup"><span data-stu-id="c377a-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c377a-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c377a-116">Additional resources</span></span>

[<span data-ttu-id="c377a-117">Registrere et webprogram i Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="c377a-117">Register a web application in Azure Active Directory B2C</span></span>](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="c377a-118">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="c377a-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)