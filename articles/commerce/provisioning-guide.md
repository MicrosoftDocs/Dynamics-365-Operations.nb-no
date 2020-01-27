---
title: Klargjøre et Commerce-forhåndsvisningsmiljø
description: Dette emnet forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934754"
---
# <a name="provision-a-commerce-preview-environment"></a>Klargjøre et Commerce-forhåndsvisningsmiljø

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø.

Før du begynner anbefaler vi at du minst skumleser hele emnet for å få en pekepinn på hva prosessen medfører og hva dette emnet inneholder.

> [!NOTE]
> Hvis du ikke har fått tilgang til Dynamics 365 Commerce-forhåndsvisningen, kan du be om forhåndsvisningstilgang fra [nettstedet for e-handel](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Oversikt

For å kunne klargjøre Commerce Preview-miljøet må du opprette et prosjekt som har et bestemt produktnavn og type. Miljøet og Retail Cloud Scale Unit (RCSU) har også bestemte parametere du må bruke når du skal klargjøre e-handel senere. Instruksjonene i dette emnet beskriver alle nødvendige trinn du må fullføre, og parameterne du må bruke.

Når klargjøringen av Commerce-forhåndsvisningsmiljøet er fullført, er det noen få trinn du må ta i etterkant for å klargjøre det. Noen trinn er valgfrie, avhengig av hvilke aspekter av systemet du vil evaluere. Du kan alltid fullføre de valgfrie trinnene senere.

Hvis du vil ha informasjon om hvordan du konfigurerer Commerce-forhåndsvisningsmiljøet etter klargjøring, kan du se [Konfigurere et Commerce-forhåndsvisningsmiljø](cpe-post-provisioning.md). Hvis du vil ha informasjon om hvordan du konfigurerer valgfrie funksjoner for Commerce-forhåndsvisningsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-forhåndsvisningsmiljø](cpe-optional-features.md).

Hvis du har spørsmål om klargjøringstrinnene eller du får problemer, kan du fortelle Microsoft i [Yammer-gruppen for Microsoft Dynamics 365 Commerce-forhåndsvisningen](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger må være på plass før du kan klargjøre Commerce-forhåndsvisningsmiljøet:

- Du har tilgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).
- Du er godtatt i Dynamics 365 Commerce-forhåndsvisningsprogrammet.
- Du har de nødvendige tillatelsene til å opprette et prosjekt for **Potensielt førsalg** eller **Overfør, opprett løsninger og finn ut mer om**.
- Du er medlem av **Miljøadministrator**- eller **Prosjekteier**-rollen i prosjektet der du skal klargjøre miljøet.
- Du har administratortilgang til Microsoft Azure-abonnementet eller kontakt med en abonnementsadministrator som kan utføre de to trinnene som krever administratortillatelser på dine vegne.
- Du har Azure Active Directory (Azure AD) tilgjengelig.
- Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som systemadministratorgruppe for e-handel, og du har ID-en tilgjengelig.
- Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som moderatorgruppe for vurderinger og omtaler, og du har ID-en tilgjengelig. (Denne sikkerhetsgruppen kan være den samme som systemadministrasjonsgruppen for e-handel.)

### <a name="find-your-azure-ad-tenant-id"></a>Finn din Azure AD-leier-ID

Azure AD-leier-IDen er en globalt unik identifikator (GUID) som ligner på dette eksemplet: **72f988bf-86f1-41af-91ab-2d7cd011db47**.

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a>Finn din Azure AD-leier-ID ved hjelp av Azure-portalen

1. Logg på [Azure-portalen](https://portal.azure.com/).
1. Kontroller at du har valgt riktig katalog.
1. Velg **Azure Active Directory** på menyen til venstre.
1. Velg **Egenskaper** under **Behandle**. Azure AD-leier-IDen vises under **Katalog-ID**.

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a>Finn din Azure AD-leier-ID ved å bruke OpenID Connect-metadata

Opprett en OpenID-URL ved å erstatte **\{YOUR\_DOMAIN\}** med domenet ditt, for eksempel `microsoft.com`. For eksempel vil `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` bli `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.

1. Gå til OpenID-URLen som inneholder domenet ditt.

    Du kan finne din Azure AD-leier-ID i flere egenskapsverdier.

1. Søk etter **authorization\_endpoint**, og pakk ut GUID-en som vises umiddelbart etter `login.microsoftonline.com/`.

### <a name="find-your-azure-ad-security-group-id"></a>Finne Azure AD-sikkerhetsgruppe-IDen

IDen for Azure AD-sikkerhetsgruppen er en GUID som ligner på dette eksemplet: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.

Denne fremgangsmåten forutsetter at du er medlem av gruppen du prøver å finne IDen for.

1. Åpne [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).
1. Klikk **Logg på med Microsoft**, og logg på med legitimasjonen din.
1. Velg **Vis flere eksempler**til venstre.
1. Aktiver **Grupper** i høyre rute.
1. Lukk høyre rute.
1. Klikk **alle grupper jeg tilhører**.
1. Finn gruppen din i feltet **Forhåndsvis svar**. Sikkerhetsgruppe-IDen vises under egenskapen **ID**.

## <a name="provision-your-commerce-preview-environment"></a>Klargjøre Commerce-forhåndsvisningsmiljøet

Disse prosedyrene forklarer hvordan du klargjør et Commerce-forhåndsvisningsmiljø. Når du har fullført dem, vil forhåndsvisningsmiljøet for Commerce være klart for konfigurasjon. Alle aktivitetene som beskrives her, skjer i LCS-portalen.

> [!IMPORTANT]
> Forhåndsvisningstilgang er knyttet til LCS-kontoen og organisasjonen du angav i forhåndsvisningsprogrammet. Du må bruke samme konto for å klargjøre Commerce-forhåndsvisningsmiljøet. Hvis du må bruke en annen LCS-konto eller leier for Commerceforhåndsvisningsmiljøet, må du oppgi disse detaljene til Microsoft. Hvis du vil ha kontaktinformasjon, kan du se delen [Støtte for Commerce-forhåndsvisningsmiljøet](#commerce-preview-environment-support) senere i dette emnet.

### <a name="grant-access-to-e-commerce-applications"></a>Gi tilgang til e-handelsprogrammer

> [!IMPORTANT]
> Personen som logger på, må være en Azure AD-leieradministrator som har Azure AD-leier-IDen. Hvis dette trinnet ikke er fullført, vil de gjenstående klargjøringstrinnene mislykkes.

Følg denne fremgangsmåten for å autorisere e-handelsprogrammene til å få tilgang til Azure-abonnementet ditt.

1. Sett sammen en URL-adresse i følgende format:

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. Kopier og lim inn URLen i nettleseren eller tekstredigeringsprogrammet, og erstatt **\{AAD\_TENANT\_ID\}** med din Azure AD-leier-ID. Åpne deretter URLen.
1. I dialogboksen for pålogging til Azure AD logger du deg på og bekrefter at du vil gi **Dynamics 365 Commerce (forhåndsvisning)** tilgang til abonnementet. Du blir sendt til en side som angir om operasjonen var vellykket.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Kontroller at forhåndsvisningsfunksjonene er tilgjengelige og aktivert i LCS

Gjør følgende for å kontrollere at forhåndsvisningsfunksjonene er tilgjengelige og aktivert i LCS.

1. Logg på [LCS-portalen](https://lcs.dynamics.com) ved hjelp av samme LCS-konto du brukte til å be om tilgang til forhåndsvisningen.
1. På LCS-startsiden ruller du helt til høyre og klikker på flisen **Administrasjon av forhåndsvisningsfunksjoner**.

    ![Fanen Forhåndsversjonsstyring](./media/preview1.png)

1. Bla ned til **Private forhåndsvisningsfunksjoner**, og kontroller at følgende funksjoner er tilgjengelige og aktivert:

    - E-handelsevaluering
    - Programmiljøer for Commerce-forhåndsvisning

    ![Private forhåndsvisningsfunksjoner](./media/preview2.png)

1. Hvis disse funksjonene ikke vises i listen, kontakter du Microsoft og angir e-postadresse for arbeid, LCS-konto og leierinformasjon. Hvis du vil ha kontaktinformasjon, kan du se delen [Støtte for Commerce-forhåndsvisningsmiljøet](#commerce-preview-environment-support).

### <a name="create-a-new-project"></a>Opprett nytt prosjekt

Hvis du vil opprette et nytt prosjekt i LCS, gjør du følgende:

1. På LCS-startsiden velger du plusstegnet (**+**) for å opprette et prosjekt.
1. I den høyre ruten følger du ett av disse trinnene:

    - Hvis du er en partner, velger du **Overfør, opprett løsninger og finn ut mer om**.
    - Hvis du er kunde, velger du **Potensielt førsalg**.

1. Angi navn, beskrivelse og bransje.
1. I **Produktnavn**-feltet velger du **Dynamics 365 Retail**.
1. I **Produktversjon**-feltet velger du **Dynamics 365 Retail**.
1. I **Metodologi**-feltet velger du **Implementeringsmetodologi for Dynamics Retail**.
1. Valgfritt: Du kan importere roller og brukere fra et eksisterende prosjekt.
1. Velg **Opprett**. Prosjektvisningen vises.

### <a name="add-the-azure-connector"></a>Legge til Azure-koblingen

Hvis du vil legge til Azure-koblingen i LCS-prosjektet, følger du fremgangsmåten nedenfor.

1. Følg ett av disse trinnene:

    - Hvis du er en partner, velger du **Prosjektinnstillinger**-flisen helt til høyre.
    - Hvis du er en kunde, velger du **Prosjektinnstillinger** fra den øverste menyen.

1. Velg **Azure-koblinger**.
1. Klikk **Legg til** for å legge til Azure-koblingen.
1. Skriv inn et navn.
1. Angi ID for Azure-abonnement.
1. Aktiver alternativet **Konfigurer til å bruke ARM (Azure Resource Manager)**.
1. Kontroller at verdien for **AAD-leierdomene (eller ID) for Azure-abonnement** er riktig. Kontakt om nødvendig Azure-abonnementsadministratoren.
1. Velg **Neste**.
1. Følg instruksjonene på siden for å gi de nødvendige programmene tilgang til abonnementet. Kontakt om nødvendig Azure-abonnementsadministratoren.

    1. Logg på [Azure-portalen](https://portal.azure.com/).
    1. Kontroller at riktig katalog er valgt, og velg deretter **Abonnementer** på menyen til venstre.
    1. Finn det riktige abonnementet fra listen, og velg det. Bruk søkefunksjonaliteten etter behov.
    1. Velg **Tilgangskontroll (IAM)** på menyen.
    1. Klikk **Legg til** under **Legg til rolletilordning** på høyre side. **Legg til rolletilordning**-ruten åpnes.
    1. I **Rolle**-feltet velger du **Bidragsyter**.
    1. I feltet **Tilordne tilgang til** beholder du standardverdien, **Azure AD-bruker, -gruppe eller -tjenestekontohaver.**
    1. Under **Velg** angir du **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Velg **Dynamics-distribusjonstjenester \[wsfed-aktivert\]** fra listen.
    1. Velg **Lagre**.

1. Velg **Neste**.
1. Følg instruksjonene på siden for å gi de nødvendige programmene tilgang til abonnementet. Kontakt om nødvendig Azure-abonnementsadministratoren.
1. Velg **Neste**.
1. I **Azure-område**-feltet velger du **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.
1. Velg **Koble til**. Din Azure-kobling skal vises i listen.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Importere miljøer for e-handelsforhåndsvisning

Følg denne fremgangsmåten for å importere miljøer for e-handelsforhåndsvisning til prosjektet ditt.

1. Åpne startsiden for prosjektet ved å velge prosjektnavnet øverst.
1. Følg ett av disse trinnene:

    - Hvis du er en partner, velger du **Aktivabibliotek**-flisen helt til høyre.
    - Hvis du er en kunde, velger du **Aktivabibliotek** fra den øverste menyen.

1. Velg **Distribuerbar programvarepakke** fra listen til venstre.
1. Velg **Import**.
1. Velg **Miljøer for e-handelsforhåndsvisning** fra listen over aktiva under **Delt aktivabibliotek**.
1. Velg **Plukk**. Du kommer tilbake til aktivabiblioteket, og du skal se utvidelsen i listen.

Illustrasjonen nedenfor viser handlingene som må utføres på LCS-siden **Aktivabibliotek**.

![Importere miljøer for e-handelsforhåndsvisning](./media/import.png)

### <a name="deploy-the-environment"></a>Distribuere miljøet

Gjør følgende for å distribuere miljøet.

> [!NOTE]
> Det kan hende du ikke trenger å fullføre trinn 6, 7 og/eller 8 fordi sider som har et enkelt alternativ, hoppes over. Når du er i **Miljøparametere**-visningen, bekrefter du at teksten **Dynamics 365 Commerce (forhåndsvisning) - demo (10.0.6 med Platform update 30)** vises rett over **Miljønavn**-feltet. Se illustrasjonen som vises etter trinn 8.

1. Fra den øverste menyen velger du **Skybaserte miljøer**.
1. Klikk **Legg til** for å legge til et miljø.
1. I **Produktversjon**-feltet velger du **10.0.6**.
1. Velg **Platform update 30** for **Plattformversjon**.

    ![Velge program- og plattformversjoner](./media/project1.png)

1. Velg **Neste**.
1. Velg **Demo** som miljøtopologien.

    ![Velge miljøtopologien 1](./media/project2.png)

1. Velg **Dynamics 365 Commerce (forhåndsvisning) - demo** som miljøtopologien. Hvis du konfigurerte en enkelt Azure-kobling tidligere, vil den bli brukt for dette miljøet. Hvis du konfigurerte flere Azure-koblinger, kan du velge hvilken kontakt som skal brukes: **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**. (For den beste ende-til-ende-ytelsen anbefaler vi at du velger **USA vest 2**.)

    ![Velge miljøtopologien 2](./media/project3.png)

1. På **Distribusjonsmiljø**-siden angir du et miljønavn. La Avanserte innstillinger stå som de er.

    ![Distribusjonsmiljø-siden](./media/project4.png)

1. Juster VM-størrelsen etter behov. (Vi anbefaler VM-lagerenhet \[SKU\] **D13 v2**.)
1. Se gjennom vilkårene for prising og lisensiering, og merk deretter av i avmerkingsboksen for å angi at du godtar dem.
1. Velg **Neste**.
1. Klikk **Distribuer**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige. Du kommer tilbake til visningen **Skybaserte miljøer**, og miljøet skal vises i listen.

    Det forespurte miljøet vil vises som en kø og deretter distribueres. Miljøarbeidsflytene vil ta litt tid å fullføre. Kom derfor tilbake etter ca seks til ni timer.

1. Før du fortsetter må du kontrollere at miljøstatusen er **Distribuert**.

### <a name="initialize-rcsu"></a>Initialiser RCSU

Hvis du vil initialisere en RCSU-adresse, følger du disse trinnene.

1. Velg miljøet ditt fra listen i visningen **Skybaserte miljøer**.
1. Klikk **Detaljerte opplysninger** i miljøvisningen til høyre. Detaljerte opplysninger for miljø vises.
1. Klikk **Behandle** under **Miljøfunksjoner**.
1. Velg **Initialiser** i kategorien **Detaljhandel**. Visningen av parametere for RCSU-initialisering vises.
1. I **Område**-feltet velger du **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.
1. I **Versjon**-feltet velger du **Angi en versjon** i listen, og deretter angir du **9.16.19262.5** i feltet som vises. Pass på at du angir nøyaktig hvilken versjon som er angitt her. Ellers må du oppdatere RCSU til korrekt versjon senere.
1. Aktiver alternativet **Bruk utvidelse**.
1. Velg **Miljøer for e-handelsforhåndsvisning** fra listen over utvidelser.
1. Velg **Initialiser**.
1. Klikk **Ja**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige. Du returneres til visningen **Detaljhandelsstyring**, der kategorien **Detaljhandel** er valgt. RCSU-en din er lagt i kø for klargjøring.
1. Før du fortsetter må du kontrollere at miljøstatusen til RCSU er **Vellykket**. Initialiseringen tar omtrent to til fem timer.

### <a name="initialize-e-commerce"></a>Initialisere e-handel

Hvis du vil initialisere e-handel, følger du disse trinnene.

1. I kategorien **E-handel (forhåndsvisning)** ser du gjennom samtykket for forhåndsvisning, og velger deretter **Oppsett**.
1. Angi et navn i feltet **Navn på e-handelsleier**. Vær imidlertid oppmerksom på at dette navnet vil vises i noen av URL-adressene som peker til e-handelsforekomsten.
1. I feltet **Retail Cloud Scale Unit-navn** velger du RCSU-en i listen. (Listen bør bare ha ett alternativ.)

    Feltet **Geografi for e-handel** angis automatisk, og verdien kan ikke endres.

1. Klikk **Neste** for å fortsette.
1. I feltet **Støttede vertsnavn** angir du et gyldig domene, for eksempel `www.fabrikam.com`.
1.  I feltet **AAD sikkerhetsgruppe for systemadministrasjon** angir du de første bokstavene i navnet på sikkerhetsgruppen du vil bruke. Velg forstørrelsesglass-ikonet for å vise søkeresultatene. Velg en sikkerhetsgruppe fra listen.
2.  I feltet **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler** angir du de første bokstavene i navnet på sikkerhetsgruppen du vil bruke. Velg forstørrelsesglass-ikonet for å vise søkeresultatene. Velg en sikkerhetsgruppe fra listen.
1. La alternativet **Aktiver tjenesten for vurderinger og omtale** være aktivert.
1. Hvis du allerede har fullført trinnet Microsoft Azure Active Directory (Azure AD)-samtykke, som beskrevet i delen "Gi tilgang til e-handelsprogrammer", merker du av i avmerkingsboksen for å bekrefte ditt samtykke. Hvis du ennå ikke har fullført dette trinnet, må du gjøre det før du fortsetter med initialiseringen. Merk koblingen i teksten ved siden av avmerkingsboksen for å åpne dialogboksen for samtykke, og fullfør trinnet.
1. Velg **Initialiser**. Du returneres til visningen **Detaljhandelsstyring**, der kategorien **E-handel (forhåndsvisning)** er aktivert. Initialiseringen av e-handel har startet.
1. Før du fortsetter må du vente til initialiseringsstatusen for e-handel er **Initialisering vellykket**.
1. Under **Koblinger** ned til høyre noterer du URL-adressene for følgende koblinger:

    * **E-handelsområde** – koblingen til roten for e-handelsområdet.
    * **Verktøy for administrasjon av e-handel-området** – koblingen til verktøyet for områdeadministrasjon.

## <a name="commerce-preview-environment-support"></a>Støtte for Commerce-forhåndsvisningsmiljø

Hvis det oppstår problemer under utføring av klargjøringstrinnene, kan du gå til [Yammer-gruppen for Microsoft Dynamics 365 Commerce forhåndsvisning](https://aka.ms/Dynamics365CommercePreviewYammer) for å få hjelp.

Hvis du får problemer når du prøver å få tilgang til Yammer-gruppen, kan du kontakte Microsoft via e-post på <Dynamics365Commerce@microsoft.com>. Denne e-postadressen overvåkes ikke aktivt. Forvent derfor en forsinkelse i svaret.

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen for å klargjøre og konfigurere Commerce-forhåndsvisningsmiljøet, kan du se [Konfigurere et Commerce-forhåndsvisningsmiljø](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Commerce-forhåndsvisningsmiljø](cpe-overview.md)

[Konfigurere et Commerce-forhåndsvisningsmiljø](cpe-post-provisioning.md)

[Konfigurere valgfrie funksjoner for et Commerce-forhåndsvisningsmiljø](cpe-optional-features.md)

[Vanlige spørsmål for Commerce-forhåndsvisningsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-webområde](https://aka.ms/Dynamics365CommerceWebsite)

[Hjelperessurser for Dynamics 365 Retail](../retail/index.md)
