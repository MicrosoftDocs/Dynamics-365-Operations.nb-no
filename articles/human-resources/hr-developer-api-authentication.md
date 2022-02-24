---
title: Godkjenning
description: Denne artikkelen inneholder en oversikt over hvordan du kan godkjenne ved hjelp av API-et (Application Programming Interface) for Microsoft Dynamics 365 Human Resources-data.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: a0509ce99205d49d516e180203ffb65a1dc09a7c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419826"
---
# <a name="authentication"></a>Godkjenning

Denne artikkelen inneholder en oversikt over hvordan du kan godkjenne ved hjelp av API-et (Application Programming Interface) for Microsoft Dynamics 365 Human Resources-data.

## <a name="overview"></a>Oversikt

Data-API-et for Human Resources er en OData-implementering. Hvis du vil ha mer informasjon, kan du se [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Programmet må godkjennes som en autorisert kalle før API-et kan betjene forespørsler fra programmet.

## <a name="fundamentals"></a>Grunnleggende

For å kalle data-API-et må programmet hente et tilgangstoken fra Microsoft-identitetsplattformen. Tilgangstokenet inneholder informasjon om programmet og tillatelsen det har til å kalle ressurser i Human Resources.

### <a name="access-token"></a>Tilgangstoken

Tilgangstokener som utstedes av Microsoft-identitetsplattformen, er base64-kodede webtokener for JSON (JavaScript Object Notation). De inneholder informasjon (krav) som data-API-et (og andre web-API-er som er sikret av Microsoft-identitetsplattformen) bruker til å validere kalleren og sørge for at kalleren har de riktige tillatelsene til å utføre operasjonen den er i ferd med å be om. Under kall kan du behandle tilgangstokener som ugjennomsiktig. Du bør alltid overføre tilgangstokener over en sikker kanal, for eksempel TLS (Transport Layer Security) og Secure Transfer Protocol (HTTPS).

Her er et eksempel på et tilgangstoken som er utstedt av Microsoft-identitetsplattformen.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Hvis du vil kalle data-APIet, knytter du tilgangstokenet til autorisasjonshodet i HTTP-forespørselen. Her er et eksempel:

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Registrere et nytt program ved å bruke Azure-portalen

1. Logg på [Microsoft Azure-portalen](https://portal.azure.com) med en jobb- eller skolekonto eller en personlig Microsoft-konto.

2. Hvis kontoen gir deg tilgang til mer enn én tenant, velger du kontoen i øvre høyre hjørne og angir portaløkten til Azure Active Directory (Azure AD)-tenanten du vil bruke.

3. Velg **Azure Active Directory**-tjenesten i venstre rute, og velg deretter **Appregistreringer \> Ny registrering**.

4. Når siden **Legge til program** vises, angir du registreringsinformasjonen for programmet:

    - **Navn**: Skriv inn et meningsfylt programnavn som skal vises for brukere av appen.
    - **Støttede kontotyper**: Velg kontotypene som appen skal støtte.

        | Støttede kontotyper | Beskrivelse |
        |-------------------------|-------------|
        | Bare kontoer i denne organisasjonskatalogen | Velg dette alternativet hvis du skal bygge en forretningsapp. Dette alternativet er ikke tilgjengelig med mindre du registrerer appen i en katalog.<p>Dette alternativet er tilordnet til **Bare én Azure AD-tenant**.</p><p>Dette alternativet er standardalternativet med mindre du registrerer appen utenfor en katalog. I så fall er standardalternativet **Flere Azure AD-tenanter og personlige Microsoft-kontoer**.</p> |
        | Kontoer i enhver organisasjonskatalog | Velg dette alternativet for å målrette alle forretnings- og utdanningskunder.<p>Dette alternativet er tilordnet til **Flere tenanter bare i Azure AD**.</p><p>Hvis du registrerte appen som **Bare én Azure AD-tenant**, kan du bruke **Godkjenning**-bladet til å oppdatere den til **Flere tenanter bare i Azure AD** og tilbake til **Bare én Azure AD-tenant**.</p> |
        | Kontoer i enhver organisasjonskatalog og personlige Microsoft-kontoer | Velg dette alternativet for å målrette mot det bredeste settet med kunder.<p>Dette alternativet er tilordnet til **Flere Azure AD-tenanter og personlige Microsoft-kontoer**.</p><p>Hvis du registrerte appen som **Flere Azure AD-tenanter og personlige Microsoft-kontoer**, kan du ikke endre denne innstillingen i brukergrensesnittet. I stedet må du bruke redigeringsprogrammet for programmanifest for å endre de støttede kontotypene.</p> |

    - **URI for omadressering (valgfritt)** – Velg apptypen du bygger: **Web** eller **Offentlig klient (mobil og skrivebord)**. Angi deretter URI-en for omadressering (eller URL-svaradressen) for appen.

        - For webapper oppgir du den primære URL-adressen til appen. `http://localhost:31544` kan for eksempel være URL-adressen til en webapp som kjører på din lokale maskin. Brukerne bruker deretter denne URL-adressen til å logge seg inn på en webklientapp.
        - For offentlige klientapper angir du URI-en som Azure AD bruker til å returnere tokensvar. Angi en verdi som er spesifikk for appen, for eksempel `myapp://auth`.

        Hvis du vil se bestemte eksempler for webapper eller innebygde apper, kan du se hurtigstartene på [Microsoft-identitesplattformen (tidligere Azure Active Directory for utviklere)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).

5. Under **API-tillatelser** velger du **Legg til en tillatelse**. Deretter går du til fanen **API-er organisasjonen min bruker**, søker etter **Dynamics 365 Human Resources** og legger deretter til tillatelsen **user\_impersonation** for appen. Program-ID-en for Human Resources er f9be0c49-aa22-4ec6-911a-c5da515226ff. Bruk denne ID-en til å sikre at du har valgt riktig program.

6. Velg **Registrer**.

   [![Registrere en ny app i Azure-portalen](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD tilordner en unik program-ID (klient-ID) til appen, og tar deg til **Oversikt**-siden for appen din. Hvis du vil legge til flere funksjoner i appen, kan du velge andre konfigurasjonsalternativer, for eksempel alternativer for varemerking og for sertifikater og hemmeligheter.

## <a name="retrieving-an-access-token"></a>Hente et tilgangstoken

Hvordan du henter et tilgangstoken for å kalle data-API-et for Human Resources, avhenger av hvilken teknologi du bruker til å utvikle klientprogrammet. Du kan for eksempel [teste med et tredjeparts verktøy](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (for eksempel Postman), utvikle et program eller en webtjeneste på C#-konsollen eller bygge en javascript-/TypeScript-klient.

Eksempel på C#-klientprogram:
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

Når du har hentet et tilgangstoken, sender du tokenet i godkjenningshodet som et bærertoken med hver forespørsel som du sender til data-API-et, som beskrevet ovenfor.
