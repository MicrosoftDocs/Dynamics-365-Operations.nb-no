---
title: Godkjenning
description: Denne artikkelen inneholder en oversikt over hvordan du kan godkjenne ved hjelp av API-et (Application Programming Interface) for Microsoft Dynamics 365 Human Resources-data.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dffe1db98ba39fde2229e69bc70bdbf113ff6ad
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793687"
---
# <a name="authentication"></a><span data-ttu-id="35f8c-103">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="35f8c-103">Authentication</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="35f8c-104">Denne artikkelen inneholder en oversikt over hvordan du kan godkjenne ved hjelp av API-et (Application Programming Interface) for Microsoft Dynamics 365 Human Resources-data.</span><span class="sxs-lookup"><span data-stu-id="35f8c-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="35f8c-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="35f8c-105">Overview</span></span>

<span data-ttu-id="35f8c-106">Data-API-et for Human Resources er en OData-implementering.</span><span class="sxs-lookup"><span data-stu-id="35f8c-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="35f8c-107">Hvis du vil ha mer informasjon, kan du se [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="35f8c-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="35f8c-108">Programmet må godkjennes som en autorisert kalle før API-et kan betjene forespørsler fra programmet.</span><span class="sxs-lookup"><span data-stu-id="35f8c-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="35f8c-109">Grunnleggende</span><span class="sxs-lookup"><span data-stu-id="35f8c-109">Fundamentals</span></span>

<span data-ttu-id="35f8c-110">For å kalle data-API-et må programmet hente et tilgangstoken fra Microsoft-identitetsplattformen.</span><span class="sxs-lookup"><span data-stu-id="35f8c-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="35f8c-111">Tilgangstokenet inneholder informasjon om programmet og tillatelsen det har til å kalle ressurser i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="35f8c-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="35f8c-112">Tilgangstoken</span><span class="sxs-lookup"><span data-stu-id="35f8c-112">Access token</span></span>

<span data-ttu-id="35f8c-113">Tilgangstokener som utstedes av Microsoft-identitetsplattformen, er base64-kodede webtokener for JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="35f8c-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="35f8c-114">De inneholder informasjon (krav) som data-API-et (og andre web-API-er som er sikret av Microsoft-identitetsplattformen) bruker til å validere kalleren og sørge for at kalleren har de riktige tillatelsene til å utføre operasjonen den er i ferd med å be om.</span><span class="sxs-lookup"><span data-stu-id="35f8c-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="35f8c-115">Under kall kan du behandle tilgangstokener som ugjennomsiktig.</span><span class="sxs-lookup"><span data-stu-id="35f8c-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="35f8c-116">Du bør alltid overføre tilgangstokener over en sikker kanal, for eksempel TLS (Transport Layer Security) og Secure Transfer Protocol (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="35f8c-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="35f8c-117">Her er et eksempel på et tilgangstoken som er utstedt av Microsoft-identitetsplattformen.</span><span class="sxs-lookup"><span data-stu-id="35f8c-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="35f8c-118">Hvis du vil kalle data-APIet, knytter du tilgangstokenet til autorisasjonshodet i HTTP-forespørselen.</span><span class="sxs-lookup"><span data-stu-id="35f8c-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="35f8c-119">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="35f8c-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="35f8c-120">Registrere et nytt program ved å bruke Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="35f8c-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="35f8c-121">Logg på [Microsoft Azure-portalen](https://portal.azure.com) med en jobb- eller skolekonto eller en personlig Microsoft-konto.</span><span class="sxs-lookup"><span data-stu-id="35f8c-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="35f8c-122">Hvis kontoen gir deg tilgang til mer enn én tenant, velger du kontoen i øvre høyre hjørne og angir portaløkten til Azure Active Directory (Azure AD)-tenanten du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="35f8c-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="35f8c-123">Velg **Azure Active Directory**-tjenesten i venstre rute, og velg deretter **Appregistreringer \> Ny registrering**.</span><span class="sxs-lookup"><span data-stu-id="35f8c-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="35f8c-124">Når siden **Legge til program** vises, angir du registreringsinformasjonen for programmet:</span><span class="sxs-lookup"><span data-stu-id="35f8c-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="35f8c-125">**Navn**: Skriv inn et meningsfylt programnavn som skal vises for brukere av appen.</span><span class="sxs-lookup"><span data-stu-id="35f8c-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="35f8c-126">**Støttede kontotyper**: Velg kontotypene som appen skal støtte.</span><span class="sxs-lookup"><span data-stu-id="35f8c-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="35f8c-127">Støttede kontotyper</span><span class="sxs-lookup"><span data-stu-id="35f8c-127">Supported account types</span></span> | <span data-ttu-id="35f8c-128">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="35f8c-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="35f8c-129">Bare kontoer i denne organisasjonskatalogen</span><span class="sxs-lookup"><span data-stu-id="35f8c-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="35f8c-130">Velg dette alternativet hvis du skal bygge en forretningsapp.</span><span class="sxs-lookup"><span data-stu-id="35f8c-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="35f8c-131">Dette alternativet er ikke tilgjengelig med mindre du registrerer appen i en katalog.</span><span class="sxs-lookup"><span data-stu-id="35f8c-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="35f8c-132">Dette alternativet er tilordnet til **Bare én Azure AD-tenant**.</span><span class="sxs-lookup"><span data-stu-id="35f8c-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="35f8c-133">Dette alternativet er standardalternativet med mindre du registrerer appen utenfor en katalog.</span><span class="sxs-lookup"><span data-stu-id="35f8c-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="35f8c-134">I så fall er standardalternativet **Flere Azure AD-tenanter og personlige Microsoft-kontoer**.</span><span class="sxs-lookup"><span data-stu-id="35f8c-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="35f8c-135">Kontoer i enhver organisasjonskatalog</span><span class="sxs-lookup"><span data-stu-id="35f8c-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="35f8c-136">Velg dette alternativet for å målrette alle forretnings- og utdanningskunder.</span><span class="sxs-lookup"><span data-stu-id="35f8c-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="35f8c-137">Dette alternativet er tilordnet til **Flere tenanter bare i Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="35f8c-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="35f8c-138">Hvis du registrerte appen som **Bare én Azure AD-tenant**, kan du bruke **Godkjenning**-bladet til å oppdatere den til **Flere tenanter bare i Azure AD** og tilbake til **Bare én Azure AD-tenant**.</span><span class="sxs-lookup"><span data-stu-id="35f8c-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="35f8c-139">Kontoer i enhver organisasjonskatalog og personlige Microsoft-kontoer</span><span class="sxs-lookup"><span data-stu-id="35f8c-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="35f8c-140">Velg dette alternativet for å målrette mot det bredeste settet med kunder.</span><span class="sxs-lookup"><span data-stu-id="35f8c-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="35f8c-141">Dette alternativet er tilordnet til **Flere Azure AD-tenanter og personlige Microsoft-kontoer**.</span><span class="sxs-lookup"><span data-stu-id="35f8c-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="35f8c-142">Hvis du registrerte appen som **Flere Azure AD-tenanter og personlige Microsoft-kontoer**, kan du ikke endre denne innstillingen i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="35f8c-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="35f8c-143">I stedet må du bruke redigeringsprogrammet for programmanifest for å endre de støttede kontotypene.</span><span class="sxs-lookup"><span data-stu-id="35f8c-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="35f8c-144">**URI for omadressering (valgfritt)** – Velg apptypen du bygger: **Web** eller **Offentlig klient (mobil og skrivebord)**.</span><span class="sxs-lookup"><span data-stu-id="35f8c-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="35f8c-145">Angi deretter URI-en for omadressering (eller URL-svaradressen) for appen.</span><span class="sxs-lookup"><span data-stu-id="35f8c-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="35f8c-146">For webapper oppgir du den primære URL-adressen til appen.</span><span class="sxs-lookup"><span data-stu-id="35f8c-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="35f8c-147">`http://localhost:31544` kan for eksempel være URL-adressen til en webapp som kjører på din lokale maskin.</span><span class="sxs-lookup"><span data-stu-id="35f8c-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="35f8c-148">Brukerne bruker deretter denne URL-adressen til å logge seg inn på en webklientapp.</span><span class="sxs-lookup"><span data-stu-id="35f8c-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="35f8c-149">For offentlige klientapper angir du URI-en som Azure AD bruker til å returnere tokensvar.</span><span class="sxs-lookup"><span data-stu-id="35f8c-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="35f8c-150">Angi en verdi som er spesifikk for appen, for eksempel `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="35f8c-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="35f8c-151">Hvis du vil se bestemte eksempler for webapper eller innebygde apper, kan du se hurtigstartene på [Microsoft-identitesplattformen (tidligere Azure Active Directory for utviklere)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="35f8c-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="35f8c-152">Under **API-tillatelser** velger du **Legg til en tillatelse**.</span><span class="sxs-lookup"><span data-stu-id="35f8c-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="35f8c-153">Deretter går du til fanen **API-er organisasjonen min bruker**, søker etter **Dynamics 365 Human Resources** og legger deretter til tillatelsen **user\_impersonation** for appen.</span><span class="sxs-lookup"><span data-stu-id="35f8c-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="35f8c-154">Program-ID-en for Human Resources er f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="35f8c-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="35f8c-155">Bruk denne ID-en til å sikre at du har valgt riktig program.</span><span class="sxs-lookup"><span data-stu-id="35f8c-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="35f8c-156">Velg **Registrer**.</span><span class="sxs-lookup"><span data-stu-id="35f8c-156">Select **Register**.</span></span>

   <span data-ttu-id="35f8c-157">[![Registrere en ny app i Azure-portalen](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="35f8c-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="35f8c-158">Azure AD tilordner en unik program-ID (klient-ID) til appen, og tar deg til **Oversikt**-siden for appen din.</span><span class="sxs-lookup"><span data-stu-id="35f8c-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="35f8c-159">Hvis du vil legge til flere funksjoner i appen, kan du velge andre konfigurasjonsalternativer, for eksempel alternativer for varemerking og for sertifikater og hemmeligheter.</span><span class="sxs-lookup"><span data-stu-id="35f8c-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="35f8c-160">Hente et tilgangstoken</span><span class="sxs-lookup"><span data-stu-id="35f8c-160">Retrieving an access token</span></span>

<span data-ttu-id="35f8c-161">Hvordan du henter et tilgangstoken for å kalle data-API-et for Human Resources, avhenger av hvilken teknologi du bruker til å utvikle klientprogrammet.</span><span class="sxs-lookup"><span data-stu-id="35f8c-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="35f8c-162">Du kan for eksempel [teste med et tredjeparts verktøy](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (for eksempel Postman), utvikle et program eller en webtjeneste på C#-konsollen eller bygge en javascript-/TypeScript-klient.</span><span class="sxs-lookup"><span data-stu-id="35f8c-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="35f8c-163">Eksempel på C#-klientprogram:</span><span class="sxs-lookup"><span data-stu-id="35f8c-163">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="35f8c-164">Når du har hentet et tilgangstoken, sender du tokenet i godkjenningshodet som et bærertoken med hver forespørsel som du sender til data-API-et, som beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="35f8c-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]