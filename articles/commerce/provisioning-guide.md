---
title: Klargjøre et miljø for forhåndsvisning av Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø.
author: psimolin
manager: annbe
ms.date: 04/10/2020
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
ms.openlocfilehash: d54db89372a0f9ef5b267d25e14067e3243a803c
ms.sourcegitcommit: 4254acb3cf8c6299fc2f3818ea6c499f058320d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/09/2020
ms.locfileid: "3254754"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>Klargjøre et miljø for forhåndsvisning av Dynamics 365 Commerce


[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du klargjør et Dynamics 365 Commerce-forhåndsvisningsmiljø.

Før du begynner, anbefaler vi at du tar en rask titt på dette emnet for å få en pekepinn på hva prosessen krever.

> [!NOTE]
> Hvis du ikke har fått tilgang til Dynamics 365 Commerce-forhåndsvisningen, kan du be om forhåndsvisningstilgang fra [Dynamics 365 Commerce-nettstedet](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Oversikt

For å kunne klargjøre Commerce Preview-miljøet må du opprette et prosjekt som har et bestemt produktnavn og type. Miljøet og Commerce Scale Unit (CSU) har også bestemte parametere du må bruke når du skal klargjøre e-handel senere. Instruksjonene i dette emnet beskriver alle nødvendige trinn for å fullføre klargjøringen og parameterne du må bruke.

Når klargjøringen av Commerce-forhåndsvisningsmiljøet er fullført, er det noen få trinn du må ta i etterkant for å klargjøre det. Noen trinn er valgfrie, avhengig av hvilke aspekter av systemet du vil evaluere. Du kan alltid fullføre de valgfrie trinnene senere.

Hvis du vil ha informasjon om hvordan du konfigurerer Commerce-forhåndsvisningsmiljøet etter klargjøring, kan du se [Konfigurere et Commerce-forhåndsvisningsmiljø](cpe-post-provisioning.md). Hvis du vil ha informasjon om hvordan du konfigurerer valgfrie funksjoner for Commerce-forhåndsvisningsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-forhåndsvisningsmiljø](cpe-optional-features.md).

Hvis du har spørsmål om klargjøringstrinnene eller du får problemer, kan du fortelle Microsoft i [Yammer-gruppen for Microsoft Dynamics 365 Commerce-forhåndsvisningen](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger må være på plass før du kan klargjøre Commerce-forhåndsvisningsmiljøet:

- Du har tilgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).
- Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan opprette et Dynamics 365 Commerce-prosjekt.
- Du er godtatt i Dynamics 365 Commerce-forhåndsvisningsprogrammet.
- Du har de nødvendige tillatelsene til å opprette et prosjekt for **Overfør, opprett løsninger og finn ut mer om**.
- Du er medlem av **Miljøadministrator**- eller **Prosjekteier**-rollen i prosjektet der du skal klargjøre miljøet.
- Du har administratortilgang til Microsoft Azure-abonnementet eller kontakt med en abonnementsadministrator som kan utføre de to trinnene som krever administratortillatelser på dine vegne.
- Du har Azure Active Directory (Azure AD) tilgjengelig.
- Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som systemadministratorgruppe for e-handel, og du har ID-en tilgjengelig.
- Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som moderatorgruppe for vurderinger og omtaler, og du har ID-en tilgjengelig. (Denne sikkerhetsgruppen kan være den samme som systemadministrasjonsgruppen for e-handel.)

## <a name="provision-your-commerce-preview-environment"></a>Klargjøre Commerce-forhåndsvisningsmiljøet

Disse prosedyrene forklarer hvordan du klargjør et Commerce-forhåndsvisningsmiljø. Når du har fullført dem, vil forhåndsvisningsmiljøet for Commerce være klart for konfigurasjon. Alle aktivitetene som beskrives her, skjer i LCS-portalen.

> [!IMPORTANT]
> Forhåndsvisningstilgang er knyttet til LCS-kontoen og organisasjonen du angav i Commerce-forhåndsvisningsprogrammet. Du må bruke samme konto for å klargjøre Commerce-forhåndsvisningsmiljøet. Hvis du må bruke en annen LCS-konto eller leier for Commerce-forhåndsvisningsmiljøet, må du oppgi disse detaljene til Microsoft. Hvis du vil ha kontaktinformasjon, kan du se delen [Støtte for Commerce-forhåndsvisningsmiljøet](#commerce-preview-environment-support) senere i dette emnet.

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
> Det kan hende du ikke trenger å fullføre trinn 6, 7 og/eller 8 fordi sider som har et enkelt alternativ, hoppes over. Når du er i **Miljøparametere**-visningen, bekrefter du at teksten **Dynamics 365 Commerce - demo (10.0.* x* med Platform update *xx*)** vises rett over **Miljønavn**-feltet. For mer informasjon, se illustrasjonen som vises etter trinn 8.

1. Fra den øverste menyen velger du **Skybaserte miljøer**.
1. Klikk **Legg til** for å legge til et miljø.
1. I feltet **Programversjon** velger du den nyeste versjonen. Hvis du har et bestemt behov for å velge en annen programversjon enn den nyeste versjonen, må du ikke velge en tidligere versjon enn **10.0.8**.
1. I **Plattformversjon**-feltet bruker du plattformversjonen som automatisk velges for den valgte programversjonen. 

    ![Velge program- og plattformversjoner](./media/project1.png)

1. Velg **Neste**.
1. Velg **Demo** som miljøtopologien.

    ![Velge miljøtopologien 1](./media/project2.png)

1. Velg **Dynamics 365 Commerce - Demo** som miljøtopologien. Hvis du konfigurerte en enkelt Azure-kobling tidligere, vil den bli brukt for dette miljøet. Hvis du konfigurerte flere Azure-koblinger, kan du velge hvilken kontakt som skal brukes: **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**. (For den beste ende-til-ende-ytelsen anbefaler vi at du velger **USA vest 2**.)

    ![Velge miljøtopologien 2](./media/project3.png)

1. På **Distribusjonsmiljø**-siden angir du et miljønavn. La Avanserte innstillinger stå som de er.

    ![Distribusjonsmiljø-siden](./media/project4.png)

1. Juster VM-størrelsen etter behov. (Vi anbefaler VM-lagerenhet \[SKU\] **D13 v2**.)
1. Se gjennom vilkårene for prising og lisensiering, og merk deretter av i avmerkingsboksen for å angi at du godtar dem.
1. Velg **Neste**.
1. Klikk **Distribuer**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige. Du kommer tilbake til visningen **Skybaserte miljøer**, og miljøet skal vises i listen.

    Det forespurte miljøet vil vises som en kø og deretter distribueres. Miljøarbeidsflytene vil ta litt tid å fullføre. Kom derfor tilbake etter ca seks til ni timer.

1. Før du fortsetter må du kontrollere at miljøstatusen er **Distribuert**.

### <a name="initialize-the-commerce-scale-unit-csu"></a>Initialisere Commerce Scale Unit (CSU)

Hvis du vil initialisere en CSU-adresse, følger du disse trinnene.

1. Velg miljøet ditt fra listen i visningen **Skybaserte miljøer**.
1. Klikk **Detaljerte opplysninger** i miljøvisningen til høyre. Detaljerte opplysninger for miljø vises.
1. Klikk **Behandle** under **Miljøfunksjoner**.
1. Velg **Initialiser** i kategorien **Handel**. Visningen av parametere for CSU-initialisering vises.
1. I **Område**-feltet velger du **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.
1. I **Versjon**-feltet velger du **Angi en versjon** i listen, og deretter angir du **9.18.20014.4** i feltet som vises. Pass på at du angir nøyaktig hvilken versjon som er angitt her. Ellers må du oppdatere RCSU til korrekt versjon senere.
1. Aktiver alternativet **Bruk utvidelse**.
1. Velg **Miljøer for e-handelsforhåndsvisning** fra listen over utvidelser.
1. Velg **Initialiser**.
1. Klikk **Ja**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige. Visningen **Handelsadministrasjon** vises på nytt med kategorien **Handel** valgt. CSU-en din er lagt i kø for klargjøring.
1. Før du fortsetter må du kontrollere at miljøstatusen til CSU er **Vellykket**. Initialiseringen tar omtrent to til fem timer.

### <a name="initialize-e-commerce"></a>Initialisere e-handel

Hvis du vil initialisere e-handel, følger du disse trinnene.

1. I kategorien **E-handel** ser du gjennom samtykket for forhåndsvisning, og velger deretter **Oppsett**.
1. Angi et navn i feltet **Navn på e-handelsleier**. Vær imidlertid oppmerksom på at dette navnet vil vises i noen av URL-adressene som peker til e-handelsforekomsten.
1. I feltet **Commerce Scale Unit-navn** velger du CSU-en i listen. (Listen bør bare ha ett alternativ.)

    Feltet **Geografi for e-handel** angis automatisk, og verdien kan ikke endres.

1. Klikk **Neste** for å fortsette.
1. I feltet **Støttede vertsnavn** angir du et gyldig domene, for eksempel `www.fabrikam.com`.
1.  I feltet **AAD sikkerhetsgruppe for systemadministrasjon** angir du de første bokstavene i navnet på sikkerhetsgruppen du vil bruke. Velg forstørrelsesglass-ikonet for å vise søkeresultatene. Velg riktig sikkerhetsgruppe fra listen.
2.  I feltet **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler** angir du de første bokstavene i navnet på sikkerhetsgruppen du vil bruke. Velg forstørrelsesglass-ikonet for å vise søkeresultatene. Velg riktig sikkerhetsgruppe fra listen.
1. La alternativet **Aktiver tjenesten for vurderinger og omtale** være aktivert.
1. Velg **Initialiser**. Visningen **Handelsadministrasjon** vises på nytt med kategorien **E-handel** valgt. Initialiseringen av e-handel har startet.
1. Før du fortsetter må du vente til initialiseringsstatusen for e-handel er **Initialisering vellykket**.
1. Under **Koblinger** ned til høyre noterer du URL-adressene for følgende koblinger:

    * **E-handelsområde** – koblingen til roten for e-handelsområdet.
    * **Verktøy for administrasjon av e-handel-området** – koblingen til verktøyet for områdeadministrasjon.

## <a name="commerce-preview-environment-support"></a>Støtte for Commerce-forhåndsvisningsmiljø

Hvis det oppstår problemer under utføring av klargjøringstrinnene, kan du gå til [Yammer-gruppen for Microsoft Dynamics 365 Commerce forhåndsvisning](https://aka.ms/Dynamics365CommercePreviewYammer) for å få hjelp.

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen for å klargjøre og konfigurere Commerce-forhåndsvisningsmiljøet, kan du se [Konfigurere et Commerce-forhåndsvisningsmiljø](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-overview.md)

[Konfigurere et miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurere valgfrie funksjoner for et miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-optional-features.md)

[Vanlige spørsmål om miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-webområde](https://aka.ms/Dynamics365CommerceWebsite)

