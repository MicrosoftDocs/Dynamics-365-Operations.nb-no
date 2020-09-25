---
title: Samsvar for informasjonskapsel
description: Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761327"
---
# <a name="cookie-compliance"></a><span data-ttu-id="ddbd7-103">Samsvar for informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="ddbd7-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ddbd7-104">Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ddbd7-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="ddbd7-105">Overview</span></span>

<span data-ttu-id="ddbd7-106">Personvern er en viktig faktor når det brukes sporingsteknologier som påvirker e-handelskunder.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="ddbd7-107">På grunn av standarder for overholdelse av personvern, for eksempel EUs personvernforordning (GDPR) i den europeiske union (EU), må det tas hensyn til elektroniske personvernsretningslinjer for alle nettsteder som er aktive i dag.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="ddbd7-108">Fordi mange e-handelsområder er globalt tilgjengelige som standard, er det viktig at du går gjennom samsvarsstandardene for e-handelsområdet ditt.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="ddbd7-109">Hvis du vil vite mer om de grunnleggende prinsippene som Microsoft bruker for samsvar for informasjonskapsler, kan du gå til [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="ddbd7-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="ddbd7-110">På dette området kan du også få mer informasjon om samsvarsområder og personvern.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="ddbd7-111">Tabellen nedenfor viser gjeldende referanseliste over informasjonskapsler for Dynamics 365 Commerce-områder.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="ddbd7-112">Navn på informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="ddbd7-112">Cookie name</span></span>                               | <span data-ttu-id="ddbd7-113">Bruk</span><span class="sxs-lookup"><span data-stu-id="ddbd7-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="ddbd7-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="ddbd7-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="ddbd7-115">Lagre Microsoft Azure Active Directory (Azure AD)-godkjenningsinformasjonskapsler for enkel pålogging (single sign-on – SSO).</span><span class="sxs-lookup"><span data-stu-id="ddbd7-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="ddbd7-116">Lagrer krypter hovedinformasjon for brukeren (namn, etternavn, e-post).</span><span class="sxs-lookup"><span data-stu-id="ddbd7-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="ddbd7-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="ddbd7-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="ddbd7-118">Handlekurv-ID som brukes til å hente liste over produkter som er lagt til i handlekurvforekomst.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="ddbd7-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="ddbd7-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="ddbd7-120">Sporing av informasjonskapselsamsvar.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="ddbd7-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="ddbd7-121">ai_session</span></span>                                  | <span data-ttu-id="ddbd7-122">Registrerer hvor mange økter med brukeraktivitet som har tatt med bestemte sider og funksjoner i appen.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="ddbd7-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="ddbd7-123">ai_user</span></span>                                     | <span data-ttu-id="ddbd7-124">Oppdager hvor mange personer som brukte appen og funksjonene i den.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="ddbd7-125">Brukere telles ved hjelp av anonyme IDer.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="ddbd7-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="ddbd7-126">b2cru</span></span>                                       | <span data-ttu-id="ddbd7-127">Butikker omadresserer URL dynamisk.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="ddbd7-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="ddbd7-128">JSESSIONID</span></span>                                  | <span data-ttu-id="ddbd7-129">Brukes av betalingskoblingen Adyen til å lagre brukerøkt.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="ddbd7-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="ddbd7-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="ddbd7-131">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="ddbd7-131">Authentication</span></span>                                               |
| <span data-ttu-id="ddbd7-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="ddbd7-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="ddbd7-133">Brukes til å vedlikeholde forespørselstilstanden.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="ddbd7-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="ddbd7-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="ddbd7-135">CRSF-token (forfalskning av forespørsler på tvers av nettsteder) som brukes til beskyttelse fra CRSF.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="ddbd7-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="ddbd7-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="ddbd7-137">Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="ddbd7-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="ddbd7-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="ddbd7-139">Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="ddbd7-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="ddbd7-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="ddbd7-141">Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="ddbd7-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="ddbd7-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="ddbd7-143">Brukes til vedlikehold av SSO-økten.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="ddbd7-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="ddbd7-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="ddbd7-145">Brukes til å spore transaksjoner (antallet åpne faner som godkjennes mot et forretning-til-forbruker-område) (B2C), inkludert den gjeldende transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="ddbd7-146">Godkjenning av områdebrukerens informasjonskapsel på et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="ddbd7-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="ddbd7-147">Hvis en funksjon i et e-handelsområde eller en modul bruker en ikke-vesentlig informasjonskapsel, må du oppnå en brukers tillatelse før informasjonskapselen spores.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="ddbd7-148">Hvis du vil tillate at brukere skal kunne tilby informasjonskapseltillatelse på e-handelsområdet, må en områdeforfatter legge til og konfigurere en samtykkemodul for informasjonskapsler i topptekstmodulen for siden for å sikre at samtykke blir bedt om og mottatt.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="ddbd7-149">Brukersamtykke for område må gis før en funksjon eller modul som bruker en ikke-vesentlig informasjonskapsel, kan gjengis på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ddbd7-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ddbd7-150">Additional resources</span></span>

[<span data-ttu-id="ddbd7-151">Funksjoner og egenskaper for tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="ddbd7-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="ddbd7-152">Samsvarsoversikt</span><span class="sxs-lookup"><span data-stu-id="ddbd7-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="ddbd7-153">Legge til en side for personvernpolicy</span><span class="sxs-lookup"><span data-stu-id="ddbd7-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="ddbd7-154">Erstatte bruker-ID-er som er knyttet til sporede innholdsendringer</span><span class="sxs-lookup"><span data-stu-id="ddbd7-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="ddbd7-155">Samtykkemodul for informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="ddbd7-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="ddbd7-156">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="ddbd7-156">Header module</span></span>](author-header-module.md)
