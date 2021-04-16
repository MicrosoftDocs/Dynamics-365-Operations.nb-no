---
title: Samsvar for informasjonskapsel
description: Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 08/31/2020
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
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796033"
---
# <a name="cookie-compliance"></a><span data-ttu-id="8a78c-103">Informasjonskapselsamsvar</span><span class="sxs-lookup"><span data-stu-id="8a78c-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a78c-104">Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a78c-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8a78c-105">Personvern er en viktig faktor når det brukes sporingsteknologier som påvirker e-handelskunder.</span><span class="sxs-lookup"><span data-stu-id="8a78c-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="8a78c-106">På grunn av standarder for overholdelse av personvern, for eksempel EUs personvernforordning (GDPR) i den europeiske union (EU), må det tas hensyn til elektroniske personvernsretningslinjer for alle nettsteder som er aktive i dag.</span><span class="sxs-lookup"><span data-stu-id="8a78c-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="8a78c-107">Fordi mange e-handelsområder er globalt tilgjengelige som standard, er det viktig at du går gjennom samsvarsstandardene for e-handelsområdet ditt.</span><span class="sxs-lookup"><span data-stu-id="8a78c-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="8a78c-108">Hvis du vil vite mer om de grunnleggende prinsippene som Microsoft bruker for samsvar for informasjonskapsler, kan du gå til [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="8a78c-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="8a78c-109">På dette området kan du også få mer informasjon om samsvarsområder og personvern.</span><span class="sxs-lookup"><span data-stu-id="8a78c-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="8a78c-110">Tabellen nedenfor viser gjeldende referanseliste over informasjonskapsler for Dynamics 365 Commerce-områder.</span><span class="sxs-lookup"><span data-stu-id="8a78c-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="8a78c-111">Navn på informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="8a78c-111">Cookie name</span></span>                               | <span data-ttu-id="8a78c-112">Bruk</span><span class="sxs-lookup"><span data-stu-id="8a78c-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="8a78c-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="8a78c-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="8a78c-114">Lagre Microsoft Azure Active Directory (Azure AD)-godkjenningsinformasjonskapsler for enkel pålogging (single sign-on – SSO).</span><span class="sxs-lookup"><span data-stu-id="8a78c-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="8a78c-115">Lagrer krypter hovedinformasjon for brukeren (namn, etternavn, e-post).</span><span class="sxs-lookup"><span data-stu-id="8a78c-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="8a78c-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="8a78c-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="8a78c-117">Handlekurv-ID som brukes til å hente liste over produkter som er lagt til i handlekurvforekomst.</span><span class="sxs-lookup"><span data-stu-id="8a78c-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="8a78c-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="8a78c-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="8a78c-119">Sporing av informasjonskapselsamsvar.</span><span class="sxs-lookup"><span data-stu-id="8a78c-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="8a78c-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="8a78c-120">ai_session</span></span>                                  | <span data-ttu-id="8a78c-121">Registrerer hvor mange økter med brukeraktivitet som har tatt med bestemte sider og funksjoner i appen.</span><span class="sxs-lookup"><span data-stu-id="8a78c-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="8a78c-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="8a78c-122">ai_user</span></span>                                     | <span data-ttu-id="8a78c-123">Oppdager hvor mange personer som brukte appen og funksjonene i den.</span><span class="sxs-lookup"><span data-stu-id="8a78c-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="8a78c-124">Brukere telles ved hjelp av anonyme IDer.</span><span class="sxs-lookup"><span data-stu-id="8a78c-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="8a78c-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="8a78c-125">b2cru</span></span>                                       | <span data-ttu-id="8a78c-126">Butikker omadresserer URL dynamisk.</span><span class="sxs-lookup"><span data-stu-id="8a78c-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="8a78c-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="8a78c-127">JSESSIONID</span></span>                                  | <span data-ttu-id="8a78c-128">Brukes av betalingskoblingen Adyen til å lagre brukerøkt.</span><span class="sxs-lookup"><span data-stu-id="8a78c-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="8a78c-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="8a78c-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="8a78c-130">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="8a78c-130">Authentication</span></span>                                               |
| <span data-ttu-id="8a78c-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="8a78c-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="8a78c-132">Brukes til å vedlikeholde forespørselstilstanden.</span><span class="sxs-lookup"><span data-stu-id="8a78c-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="8a78c-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="8a78c-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="8a78c-134">CRSF-token (forfalskning av forespørsler på tvers av nettsteder) som brukes til beskyttelse fra CRSF.</span><span class="sxs-lookup"><span data-stu-id="8a78c-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="8a78c-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="8a78c-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="8a78c-136">Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="8a78c-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="8a78c-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="8a78c-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="8a78c-138">Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="8a78c-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="8a78c-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="8a78c-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="8a78c-140">Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="8a78c-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="8a78c-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="8a78c-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="8a78c-142">Brukes til vedlikehold av SSO-økten.</span><span class="sxs-lookup"><span data-stu-id="8a78c-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="8a78c-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="8a78c-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="8a78c-144">Brukes til å spore transaksjoner (antallet åpne faner som godkjennes mot et forretning-til-forbruker-område) (B2C), inkludert den gjeldende transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="8a78c-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="8a78c-145">Godkjenning av områdebrukerens informasjonskapsel på et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="8a78c-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="8a78c-146">Hvis en funksjon i et e-handelsområde eller en modul bruker en ikke-vesentlig informasjonskapsel, må du oppnå en brukers tillatelse før informasjonskapselen spores.</span><span class="sxs-lookup"><span data-stu-id="8a78c-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="8a78c-147">Hvis du vil tillate at brukere skal kunne tilby informasjonskapseltillatelse på e-handelsområdet, må en områdeforfatter legge til og konfigurere en samtykkemodul for informasjonskapsler i topptekstmodulen for siden for å sikre at samtykke blir bedt om og mottatt.</span><span class="sxs-lookup"><span data-stu-id="8a78c-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="8a78c-148">Brukersamtykke for område må gis før en funksjon eller modul som bruker en ikke-vesentlig informasjonskapsel, kan gjengis på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="8a78c-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a78c-149">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8a78c-149">Additional resources</span></span>

[<span data-ttu-id="8a78c-150">Funksjoner og egenskaper for tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="8a78c-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="8a78c-151">Samsvarsoversikt</span><span class="sxs-lookup"><span data-stu-id="8a78c-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="8a78c-152">Legge til en side for personvernpolicy</span><span class="sxs-lookup"><span data-stu-id="8a78c-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="8a78c-153">Erstatte bruker-ID-er som er knyttet til sporede innholdsendringer</span><span class="sxs-lookup"><span data-stu-id="8a78c-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="8a78c-154">Samtykkemodul for informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="8a78c-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="8a78c-155">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="8a78c-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
