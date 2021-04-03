---
title: Klargjøre et evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du klargjør et evalueringsmiljø for Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a57cc02c6d62f288f14b65191c2f4927a019963c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478170"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Klargjøre et evalueringsmiljø for Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du klargjør et evalueringsmiljø for Microsoft Dynamics 365 Commerce.

Før du begynner, anbefaler vi at du tar en rask titt på dette emnet for å få en pekepinn på hva prosessen krever.

> [!NOTE]
> Commerce-evalueringsmiljøer er ikke generelt tilgjengelige, og gis til partnere og kunder på et per forespørsel-grunnlag. Hvis du vil ha mer informasjon, ta kontakt med din Microsoft-partnerkontakten din.

For å kunne klargjøre et Commerce-evalueringsmiljø må du opprette et prosjekt som har et bestemt produktnavn og type. Miljøet og Commerce Scale Unit (CSU) har også bestemte parametere du må bruke når du forventer å klargjøre e-handel senere. Instruksjonene i dette emnet beskriver alle nødvendige trinn som må fullføres for å klargjøre, og parameterne du må bruke.

Når klargjøringen av Commerce-evalueringsmiljøet er fullført, er det noen få trinn du må ta i etterkant for å klargjøre det for bruk. Noen trinn er valgfrie, avhengig av hvilke aspekter av systemet du vil evaluere. Du kan alltid fullføre de valgfrie trinnene senere.

Hvis du vil ha informasjon om hvordan du konfigurerer Commerce-evalueringsmiljøet etter klargjøring, kan du se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md). Hvis du vil ha informasjon om hvordan du konfigurerer valgfrie funksjoner for Commerce-evalueringsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-evalueringsmiljø](cpe-optional-features.md).

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger må være på plass før du kan klargjøre Commerce-evalueringsmiljøet:

- Du er introdusert til evalueringsprogrammet og tildelt kapasitet for et evalueringsmiljø.
- Du har tilgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).
- Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan opprette et Dynamics 365 Commerce-prosjekt.
- Du har administratortilgang til Microsoft Azure-abonnementet, eller du er i kontakt med en abonnementsadministrator som kan hjelpe deg hvis det er nødvendig.
- Du har Azure Active Directory (Azure AD) tilgjengelig.
- Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som systemadministratorgruppe for e-handel, og du har ID-en tilgjengelig.
- Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som moderatorgruppe for vurderinger og omtaler, og du har ID-en tilgjengelig. (Denne sikkerhetsgruppen kan være den samme som systemadministrasjonsgruppen for e-handel.)

Legg merke til at denne listen ikke er fullstendig. Hvis du opplever problemer, kontakter du Microsoft-partnerkontakten for å få hjelp.

## <a name="provision-your-commerce-evaluation-environment"></a>Klargjøre Commerce-evalueringsmiljøet

Disse prosedyrene forklarer hvordan du klargjør et Commerce-evalueringsmiljø. Når du har fullført dem, vil evalueringsmiljøet for Commerce være klart for konfigurasjon. Alle aktivitetene som beskrives her, skjer i LCS-portalen.

### <a name="create-a-new-project"></a>Opprett nytt prosjekt

Hvis du vil opprette et nytt prosjekt i LCS, gjør du følgende:

1. På LCS-startsiden velger du plusstegnet (**+**) for å opprette et prosjekt.
1. I den høyre ruten følger du ett av disse trinnene:

    - Hvis du er en partner, velger du **Overfør, opprett løsninger og finn ut mer om**.
    - Hvis du er kunde, velger du **Potensielt førsalg**.

1. Angi navn, beskrivelse og bransje.
1. I **Produktnavn**-feltet velger du **Dynamics 365 Commerce**.
1. I **Produktversjon**-feltet velger du **Dynamics 365 Commerce**.
1. I **Metodologi**-feltet velger du **Implementeringsmetodologi for Dynamics Retail**.
1. Valgfritt: Du kan importere roller og brukere fra et eksisterende prosjekt.
1. Velg **Opprett**. Prosjektvisningen vises.

### <a name="add-the-azure-connector"></a>Legge til Azure-koblingen

Hvis du vil legge til Azure-kobling i LCS-prosjektet, følger du fremgangsmåten i [Fullføre jobbintroduksjon for Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).

### <a name="deploy-the-environment"></a>Distribuere miljøet

Gjør følgende for å distribuere miljøet.

> [!NOTE]
> Det kan hende du ikke trenger å fullføre trinn 6, 7 og/eller 8 fordi sider som har et enkelt alternativ, hoppes over. Når du er i **Miljøparametere**-visningen, bekrefter du at teksten **Dynamics 365 Commerce - demo (10.0.* x* med Platform update *xx*)** vises rett over **Miljønavn**-feltet. For mer informasjon, se illustrasjonen som vises etter trinn 8.

1. Fra den øverste menyen velger du **Skybaserte miljøer**.
1. Klikk **Legg til** for å legge til et miljø.
1. I feltet **Programversjon** velger du den nyeste versjonen. Hvis du har et bestemt behov for å velge en annen programversjon enn den nyeste versjonen, må du ikke velge en tidligere versjon enn **10.0.14**.
1. I **Plattformversjon**-feltet bruker du plattformversjonen som automatisk velges for den valgte programversjonen. 

    ![Velge program- og plattformversjoner](./media/project1.png)

1. Velg **Neste**.
1. Velg **Demo** som miljøtopologien.

    ![Velge miljøtopologien 1](./media/project2.png)

1. På **Distribusjonsmiljø**-siden angir du et miljønavn. La Avanserte innstillinger stå som de er.

    ![Distribusjonsmiljø-siden](./media/project4.png)

1. Juster VM-størrelsen etter behov. (Vi anbefaler VM-lagerenhet \[SKU\] **D13 v2**.)
1. Se gjennom vilkårene for prising og lisensiering, og merk deretter av i avmerkingsboksen for å angi at du godtar dem.
1. Velg **Neste**.
1. Klikk **Distribuer** på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige. Du kommer tilbake til visningen **Skybaserte miljøer**, og miljøet skal vises i listen.

    Det forespurte miljøet vil vises som en kø og deretter distribueres. Miljøarbeidsflytene vil ta litt tid å fullføre. Kom derfor tilbake etter ca seks til ni timer.

1. Før du fortsetter må du kontrollere at miljøstatusen er **Distribuert**.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Initialisere Commerce Scale Unit (sky)

For å initialisere CSU-en, følger du disse trinnene.

1. Velg miljøet ditt fra listen i visningen **Skybaserte miljøer**.
1. Klikk **Detaljerte opplysninger** i miljøvisningen til høyre. Detaljerte opplysninger for miljø vises.
1. Klikk **Behandle** under **Miljøfunksjoner**.
1. Velg **Initialiser** i kategorien **Handel**. Visningen av parametere for CSU-initialisering vises.
1. I **Område**-feltet velger du det samme området eller et område nær der du distribuerte miljøet til.
1. La **Versjon**-feltet være slik det er.
1. Velg **Initialiser**.
1. Klikk **Ja** på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige. Visningen **Handelsadministrasjon** vises på nytt med kategorien **Handel** valgt. CSU-en din er lagt i kø for klargjøring.
1. Før du fortsetter må du kontrollere at miljøstatusen til CSU er **Vellykket**. Initialiseringen tar omtrent to til fem timer.

Hvis du ikke finner **Behandle**-koblingen i miljødetaljvisningen, kontakter du Microsoft-kontakten for å få hjelp.

Under distribusjonsprosessen kan du få følgende feilmelding:

> Evalueringsmiljøer (demo/test) må registrere programmet for skaleringsenhetstilkobling \<application ID\> på hovedkontoret.

Hvis CSU-initialiseringen mislykkes og du får denne feilmeldingen, noterer du deg program-IDen, som er en globalt unik ID (ASSE), og følger deretter trinnene i den neste delen for å registrere CSU-distribusjonsprogrammet i Commerce Headquarters.

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a>Registrere CSU-distribusjonsprogrammet i Commerce Headquarters (om nødvendig)

For å registrere CSU-distribusjonsprogrammet i Commerce Headquarters, følger du disse trinnene.

1. I Commerce headquarters kan du gå til **Systemadministrasjon \> Oppsett \> Azure Active Directory-programmer**.
1. Angi **Klient-ID**-kolonnen, angi program-ID fra CSU-initialiseringsfeilmeldingen du mottok.
1. I **Navn**-kolonnen angir du en beskrivende tekst (for eksempel **CSU-eval**).
1. I kolonnen **Bruker-ID** angir du **RetailServiceAccount**.
1. Forsøk på CSU-initialisering og distribusjon fra LCS.

### <a name="initialize-e-commerce"></a>Initialisere e-handel

Hvis du vil initialisere e-handel, følger du disse trinnene.

1. I kategorien **E-handel** ser du gjennom samtykket for evalueringen, og velg deretter **Oppsett**.
1. Angi et navn i feltet for **Navn på e-handelsmiljø**. Vær oppmerksom på at dette navnet vil vises i noen av URL-adressene som peker til e-handelsforekomsten.
1. I feltet **Commerce Scale Unit-navn** velger du CSU-en i listen. (Listen bør bare ha ett alternativ.)

    Feltet **Geografi for e-handel** angis automatisk.

1. Klikk **Neste** for å fortsette.
1. I feltet **Støttede vertsnavn** angir du et gyldig domene, for eksempel `www.fabrikam.com`.
1. Feltet **AAD-sikkerhetsgruppe for systemadministrasjon** angir de første bokstavene i navnet på sikkerhetsgruppen du vil bruke, og deretter velger du forstørrelsesglassymbolet for å vise søkeresultatene. Velg riktig sikkerhetsgruppe i listen.
1.  Feltet **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler** angir de første bokstavene i navnet på sikkerhetsgruppen du vil bruke, og deretter velger du forstørrelsesglassymbolet for å vise søkeresultatene. Velg riktig sikkerhetsgruppe i listen.
1. La alternativet **Aktiver tjenesten for vurderinger og omtale** settes til **Ja**.
1. Velg **Initialiser**. Visningen **Handelsadministrasjon** vises på nytt med kategorien **E-handel** valgt. Initialiseringen av e-handel har startet.
1. Før du fortsetter må du vente til initialiseringsstatusen for e-handel er **Initialisering vellykket**.
1. Under **Koblinger** ned til høyre noterer du URL-adressene for følgende koblinger:

    * **E-handelsområde** – koblingen til roten for e-handelsområdet.
    * **Commerce-områdebygger** – koblingen til verktøyet for områdeadministrasjon.

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen for å klargjøre og konfigurere Commerce-evalueringsmiljøet, kan du se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce](cpe-bopis.md)

[Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce](cpe-optional-features.md)

[Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (sky)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-webområde](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
