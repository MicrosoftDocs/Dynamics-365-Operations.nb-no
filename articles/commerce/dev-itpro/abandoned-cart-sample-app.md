---
title: Registrere forlatte handlekurver og sende varslinger til kunder
description: Dette emnet beskriver hvordan du tilpasser eksempelappen for kobling for forlatt handlekurv i Microsoft Dynamics 365 Commerce for å registrere forlatte handlekurver og sende e-postvarslinger med påminnelse til kunder.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 82848f1ff068cea0adfc6ec1b33fc4bb035f78dc
ms.sourcegitcommit: 374bbdde90fc9a68c0799158a50409bfbe8ca64e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/25/2022
ms.locfileid: "8353364"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Registrere forlatte handlekurver og sende varslinger til kunder

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du tilpasser eksempelappen for kobling for forlatt handlekurv i Microsoft Dynamics 365 Commerce for å registrere forlatte handlekurver og sende e-postvarslinger med påminnelse til kunder.

Det å kunne gjenvinne inntekt og beholde kunder via varslinger om forlatte handlekurver er en viktig funksjon som Dynamics 365 Commerce støtter. Detaljister kan få tilgang til handlekurver på Retail Server som ikke er endret innen et tidsvindu som detaljistene definerer, ved å tilpasse eksempelappen for kobling for forlatt handlekurv i Commerce. Disse handlekurvene kan deretter hentes, forsterkes med produkt- og kundedata og sendes videre til en tredjepartsleverandør av e-postmarkedsføring som kan generere e-postvarslinger og sende dem til kunder.

E-postvarslingen om forlatt handlekurv som kunder mottar, kan inneholde følgende informasjon:

- Fornavnet på kunden.
- Etternavnet på kunden.
- E-postadressen til kunden.
- En nettadresse som returnerer kunden til handlekurven.
- Transaksjonsvalutaen.
- En liste over produkter i handlekurven til kunden. Følgende informasjon tas med for hvert produkt:

    - visningsnavnet for produktet
    - produkt-ID-en (brukes til å sette sammen en nettadresse til siden for produktbeskrivelse)
    - et produktbilde som kan få størrelsen tilpasset automatisk til ulike visningsportstørrelser
    - alternativ tekst for produktbildet
    - enhetsprisen på produktet

## <a name="abandoned-cart-connector-sample"></a>eksempel på kobling for forlatt handlekurv

En koblingsmodell som Microsoft tilbyr via SDK-en (Software Development Kit) for Retail gjør at informasjon om forlatt handlekurv kan hentes og sendes til en tredjepartsleverandør av e-postmarkedsføring. Denne koblingen håndterer kommunikasjon med Retail Server, bruker Azure Key Vault for sikkerhet, håndterer planlegging av handlekurvhenting for et bestemt tidsvindu og henter ordre- og produktdata. Den byr også på en eksempelimplementering for en integrasjon med en tredjepartsleverandør av e-postmarkedsføring. Koblingen er som standard bygd for å kommunisere med [Emarsys](https://emarsys.com). Du kan imidlertid enkelt tilpasse den til integrering med andre løsninger, for eksempel Constant Contact, Mailchimp og SendGrid.

Illustrasjonen nedenfor viser komponentene i eksempelappen for kobling for forlatt handlekurv.

![Komponenter i eksempelappen for kobling for forlatt handlekurv](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> I enkelte områder må kunder kunne velge å unngå at handlekurvdata sendes til en leverandør av e-postmarkedsføring, eller å kunne be om at dataene fjernes. Microsoft tilbyr imidlertid ikke disse alternativene til kunder. Hvis du har tenkt å gjøre forretninger i områder der disse alternativene er obligatoriske, må du derfor sørge for den nødvendige infrastrukturen og tilpassingene for å spore kundenes preferanser, og bruke disse preferansene til å forhindre at kundedata sendes til e-postplattformen din. Du må også definere en prosess for å slette kundedata fra leverandøren av e-postmarkedsføring når kunden ber om det.

## <a name="obtain-the-code-sample"></a>Hente kodeeksemplet

Eksempelappen for kobling for forlatt handlekurv er tatt med i SDK-en for Retail fra og med versjon 10.0.16. Du finner koden under **\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample**. Hvis du vil ha mer informasjon om SDK-en for Retail og hvor du kan få den, kan du se [SDK (Software Development Kit) for Retail](retail-sdk/retail-sdk-overview.md).

> [!NOTE]
> Selv om eksempelkoden først ble gjort tilgjengelig i bygg i versjon 10.0.16, er den kompatibel med versjon 10.0.13 og nyere bygg av Retail Server.

## <a name="prerequisites-and-dependencies"></a>Forutsetninger og avhengigheter

Før du kan rulle ut og konfigurere eksempelkoden for kobling for forlatt handlekurv, må følgende forutsetninger oppfylles.

### <a name="access-to-commerce-resources"></a>Tilgang til Commerce-ressurser

For å kunne konfigurere og rulle ut appen for kobling for forlatt handlekurv må du ha tilgang til følgende Commerce-ressurser:

- administratortilgang til Commerce Headquarters for miljøet ditt
- Tilgang til prosjektet for Microsoft Dynamics Lifecycle Services (LCS) for miljøet ditt

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Appen for kobling for forlatt handlekurv bruker Azure Cosmos DB til å spore ID-ene og tidsstemplene for handlekurver som er hentet tidligere. Du kan bruke Azure Cosmos DB til å beholde disse dataene, eller du kan tilpasse kodeeksemplet for å integrere med et annet alternativ for datalagring. Hvis du vil ha mer informasjon om Azure Cosmos DB, kan du se [Velkommen til Azure Cosmos DB](/azure/cosmos-db/introduction).

Hvis du bruker Azure Cosmos DB, må du oppfylle følgende forutsetninger før du kan kjøre eksemplet:

- Du må ha en aktiv Azure Cosmos DB-konto. Hvis du ikke har en konto, kan du se [Opprette en databasekonto](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- Du må hente verdiene **URI** og **PRIMÆRNØKKEL** (eller **SEKUNDÆRNØKKEL**) fra **Nøkler**-bladet i Azure Cosmos DB-kontoen i Azure-portalen. Hvis du vil ha mer informasjon om hvordan du henter informasjon om endepunkt og nøkkel for Azure Cosmos DB-kontoen, kan du se [Vise og kopiere tilgangsnøkler og passord og generere dem på nytt](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure Key Vault

Appen for kobling for forlatt handlekurv bruker Key Vault til å lagre navnene på og hemmelighetene for de ulike komponentene som krever sikker tilgang.

Gjør følgende for å konfigurere et nøkkelhvelv.

1. Følg instruksjonene i [Administrere Key Vault i Azure Stack Hub ved hjelp av portalen](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true).
2. Opprett hemmeligheter for følgende informasjon:

    - API-brukernavn (Application Programming Interface) og API-hemmelighet for Emarsys
    - program-ID og hemmelighet for forlatt handlekurv

Eksempelkoden for koblingen for forlatt handlekurv bruker Azure-standardlegitimasjon til å få tilgang til Key Vault. Du må gi tillatelsene **Liste** og **Lese** til identiteten du planlegger å bruke til å få tilgang til Key Vault.

Hvis du vil ha mer informasjon om Azure-standardlegitimasjon, kan du se [Klassen DefaultAzureCredential](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Opprette en program-ID for eksempelappen for kobling for forlatt handlekurv for Azure AD-leieren

Du må opprette en program-ID for eksempelappen for kobling for forlatt handlekurv for Azure Active Directory-leieren (AD). Hvis du vil ha informasjon om hvordan du oppretter en program-ID, kan du se [Bruke portalen til å opprette en Azure AD-app og tjenestekontohaver som har tilgang til ressurser](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Legge til program-ID-en for eksempelapp for kobling for forlatt handlekurv i tillatelseslisten for API-en for Retail Server

Du må deretter legge til program-ID-en for eksempelapp for kobling for forlatt handlekurv i tillatelseslisten for API-en for Retail Server. Hvis du vil ha informasjon om hvordan du legger til en program-ID i tillatelseslisten i Azure, kan du se [Støtte for tjeneste-til-tjeneste-autentisering i Retail Server](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Konfigurere eksempelappen for kobling for forlatt handlekurv

Du konfigurerer eksempelappen for kobling for forlatt handlekurv ved å endre konfigurasjonsfilen **appSettings.json** som ligger i roten i katalogen **AbandonedCartDetectionSample**. Tabellene nedenfor beskriver egenskapene til konfigurasjonsfilen.

### <a name="keyvaultoptions"></a>KeyVaultOptions

| Egenskap    | Beskrivelse |
| ----------- | ----------- |
| KeyVaultURI | DNS-navnet (Domain Name System) for nøkkelhvelvet du bruker i Azure-portalen. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| Egenskap                                      | Beskrivelse |
| --------------------------------------------- | ----------- |
| TenantId                                      | Azure AD-leier-ID-en til Azure-leieren. |
| RetailServerAudienceId                        | Målgruppe-ID-en for Retail Server. Du kan bruke standardverdien. |
| AppIdKeyVaultSecretName                       | Navnet på hemmeligheten du opprettet for program-ID-en for eksempelappen for kobling for forlatt handlekurv. |
| AppSecretKeyVaultSecretName                   | Navnet på hemmeligheten som lagrer apphemmeligheten program-ID-en for eksempelappen for kobling for forlatt handlekurv. |
| RetailServerUrl                               | Nettadressen til Retail Server-forekomsten. Du finner denne verdien i LCS. |
| OperatingUnitNumber                           | Driftsenhetsnummeret (OUN). Du finner denne verdien i Commerce Headquarters. |
| IncludeAbandonedCartsModifiedSinceLastMinutes | Begynnelsen på tidsvinduet for de forlatte handlekurvene du vil hente. Verdien uttrykkes som et antall minutter før nåværende klokkeslett. Du kan for eksempel angi **120** for denne egenskapen hvis du vil hente alle handlekurver som sist ble endret mellom 120 minutter siden og slutten på tidsvinduet som er definert av egenskapen **ExcludeAbandonedCartsModifiedSinceLastMinutes**. |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | Slutten på tidsvinduet for de forlatte handlekurvene du vil hente. Verdien uttrykkes som et antall minutter før nåværende klokkeslett. Hvis for eksempel **120** er angitt for egenskapen **IncludeAbandonedCartsModifiedSinceLastMinutes**, angir du **30** for denne egenskapen hvis du vil hente alle handlekurver som ble endret mellom 120 minutter siden og 30 minutter siden. Denne egenskapen definerer i praksis hvor lenge du vil vente før en handlekurv deklareres som forlatt. |
| ReturnToCartUrl                               | Nettadressen til handlekurven på e-handelsområdet, i formatet som brukes i filen **app.config**. |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

Statusen for hentejobben, handlekurv-ID-ene og de endrede tidsstemplene for den forlatte handlekurven er lagret i Azure Cosmos DB. Innstillingene i konfigurasjonsfilen peker som standard mot den lokale emulatorforekomsten av Azure Cosmos DB. Når du ruller ut koblingen til produksjon, må du oppdatere disse innstillingene slik at de peker mot Azure Cosmos DB-forekomsten i Azure-abonnementet ditt. Når det gjelder lokal testing eller sandkassetesting, kan du bruke [Azure Cosmos Emulator](/azure/cosmos-db/local-emulator).

| Egenskap    | Beskrivelse |
| ----------- | ----------- |
| EndPointUri | Endepunkt-URI-en som leveres av Azure eller emulatoren. |
| PrimaryKey  | Primærnøkkelen som leveres av Azure eller emulatoren. |
| DatabaseId  | Database-ID-en. Du kan bruke standardverdien eller angi din egen. |
| ContainerId | Beholder-ID-en. Du kan bruke standardverdien eller angi din egen. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Hvis du integrerer med en annen leverandør av e-postmarkedsføring enn Emarsys, må du utvide grensesnittet **IEmailProvider** etter behov for å kommunisere med denne leverandøren.

| Egenskap                      | Beskrivelse |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | ID-en for den eksterne hendelsesposten som opprettes i Emarsys. Du finner verdien under **Utløserinnstillinger** i kampanjen du opprettet for å sende e-postvarslinger om forlatt handlekurv. |
| ApiUserNameKeyVaultSecretName | Navnet på nøkkelen der API-brukernavnet for Emarsys er lagret. |
| ApiSecretKeyVaultSecretName   | Navnet på nøkkelen der API-hemmeligheten for Emarsys er lagret. |
| EmarsysContactKeyId           | ID-en til e-postkolonnen i kontaktdatabasen for Emarsys. Standardverdien er **3** og skal ikke måtte endres. |

### <a name="mediaoptions"></a>MediaOptions

Hvis du bruker funksjonene for e-handel i Commerce, kan du bruke digital aktivastyring i Commerce til å hente produktbilder. Hvis du vil ha mer informasjon om funksjonene for endring av bildestørrelse i digital aktivastyring, kan du se [Konfigurasjon av ImageSettings-visningsport](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Egenskap                             | Beskrivelse |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | Rotnettadressen for områdets digitale aktivastyring. Du kan finne verdien i egenskapsnøkkelen **Primær URL-adresse for medieserver** i **Detaljhandel og handel \> Kanaloppsett \> Kanalprofiler** i Commerce Headquarters. |
| ImageViewPorts                       | Beholdernoden for individuelle visningsportkonfigurasjoner. |
| ImageViewPorts/viewport              | Visningsportdefinisjonen. Bruk denne egenskapen til å angi breddeområdene for visningsporten i piksler. Hvis du vil se et eksempel som viser hvordan denne egenskapen brukes, kan du se konfigurasjonsfilen **appSettings.json**. |
| ImageViewPorts/imageWidth            | Bildebredden til visningsporten i piksler. |
| imageViewPorts/imageHeight           | Bildehøyden til visningsporten i piksler. |
| imageViewPorts/useForDefaultImageTag | En **true**/**false**-verdi som angir om bildedimensjonene som er definert av visningsporten, skal brukes hvis HTML-koden `<picture>` ikke støttes for en nettleser eller e-postklient. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
