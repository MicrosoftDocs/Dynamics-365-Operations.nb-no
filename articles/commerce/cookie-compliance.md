---
title: Samsvar for informasjonskapsel
description: Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446919"
---
# <a name="cookie-compliance"></a><span data-ttu-id="6c56c-103">Samsvar for informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="6c56c-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c56c-104">Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c56c-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6c56c-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="6c56c-105">Overview</span></span>

<span data-ttu-id="6c56c-106">Personvern er en viktig faktor når det brukes sporingsteknologier som påvirker e-handelskunder.</span><span class="sxs-lookup"><span data-stu-id="6c56c-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="6c56c-107">På grunn av standarder for overholdelse av personvern, for eksempel EUs personvernforordning (GDPR) i den europeiske union (EU), må det tas hensyn til elektroniske personvernsretningslinjer for alle nettsteder som er aktive i dag.</span><span class="sxs-lookup"><span data-stu-id="6c56c-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="6c56c-108">Fordi mange e-handelsområder er globalt tilgjengelige som standard, er det viktig at du går gjennom samsvarsstandardene for e-handelsområdet ditt.</span><span class="sxs-lookup"><span data-stu-id="6c56c-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="6c56c-109">Hvis du vil vite mer om de grunnleggende prinsippene som Microsoft bruker for samsvar for informasjonskapsler, kan du gå til [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="6c56c-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="6c56c-110">På dette området kan du også få mer informasjon om samsvarsområder og personvern.</span><span class="sxs-lookup"><span data-stu-id="6c56c-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="6c56c-111">Tabellen nedenfor viser gjeldende referanseliste over informasjonskapsler for Dynamics 365 Commerce-områder.</span><span class="sxs-lookup"><span data-stu-id="6c56c-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="6c56c-112">Navn på informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="6c56c-112">Cookie name</span></span>                               | <span data-ttu-id="6c56c-113">Bruk</span><span class="sxs-lookup"><span data-stu-id="6c56c-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="6c56c-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="6c56c-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="6c56c-115">Lagre Microsoft Azure Active Directory (Azure AD)-godkjenningsinformasjonskapsler for enkel pålogging (single sign-on – SSO).</span><span class="sxs-lookup"><span data-stu-id="6c56c-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="6c56c-116">Lagrer krypter hovedinformasjon for brukeren (namn, etternavn, e-post).</span><span class="sxs-lookup"><span data-stu-id="6c56c-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="6c56c-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="6c56c-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="6c56c-118">Handlekurv-ID som brukes til å hente liste over produkter som er lagt til i handlekurvforekomst.</span><span class="sxs-lookup"><span data-stu-id="6c56c-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="6c56c-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="6c56c-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="6c56c-120">Sporing av informasjonskapselsamsvar.</span><span class="sxs-lookup"><span data-stu-id="6c56c-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="6c56c-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="6c56c-121">ai_session</span></span>                                  | <span data-ttu-id="6c56c-122">Registrerer hvor mange økter med brukeraktivitet som har tatt med bestemte sider og funksjoner i appen.</span><span class="sxs-lookup"><span data-stu-id="6c56c-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="6c56c-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="6c56c-123">ai_user</span></span>                                     | <span data-ttu-id="6c56c-124">Oppdager hvor mange personer som brukte appen og funksjonene i den.</span><span class="sxs-lookup"><span data-stu-id="6c56c-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="6c56c-125">Brukere telles ved hjelp av anonyme IDer.</span><span class="sxs-lookup"><span data-stu-id="6c56c-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="6c56c-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="6c56c-126">b2cru</span></span>                                       | <span data-ttu-id="6c56c-127">Butikker omadresserer URL dynamisk.</span><span class="sxs-lookup"><span data-stu-id="6c56c-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="6c56c-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="6c56c-128">JSESSIONID</span></span>                                  | <span data-ttu-id="6c56c-129">Brukes av betalingskoblingen Adyen til å lagre brukerøkt.</span><span class="sxs-lookup"><span data-stu-id="6c56c-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="6c56c-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="6c56c-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="6c56c-131">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="6c56c-131">Authentication</span></span>                                               |
| <span data-ttu-id="6c56c-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="6c56c-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="6c56c-133">Brukes til å vedlikeholde forespørselstilstanden.</span><span class="sxs-lookup"><span data-stu-id="6c56c-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="6c56c-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="6c56c-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="6c56c-135">CRSF-token (forfalskning av forespørsler på tvers av nettsteder) som brukes til beskyttelse fra CRSF.</span><span class="sxs-lookup"><span data-stu-id="6c56c-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="6c56c-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="6c56c-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="6c56c-137">Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="6c56c-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="6c56c-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="6c56c-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="6c56c-139">Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="6c56c-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="6c56c-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="6c56c-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="6c56c-141">Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="6c56c-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="6c56c-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="6c56c-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="6c56c-143">Brukes til vedlikehold av SSO-økten.</span><span class="sxs-lookup"><span data-stu-id="6c56c-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="6c56c-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="6c56c-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="6c56c-145">Brukes til å spore transaksjoner (antallet åpne faner som godkjennes mot et forretning-til-forbruker-område) (B2C), inkludert den gjeldende transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="6c56c-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="6c56c-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6c56c-146">Additional resources</span></span>

[<span data-ttu-id="6c56c-147">Funksjoner og egenskaper for tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="6c56c-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="6c56c-148">Samsvarsoversikt</span><span class="sxs-lookup"><span data-stu-id="6c56c-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="6c56c-149">Legge til en side for personvernpolicy</span><span class="sxs-lookup"><span data-stu-id="6c56c-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="6c56c-150">Erstatte bruker-IDer knyttet til sporede innholdsendringer</span><span class="sxs-lookup"><span data-stu-id="6c56c-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
