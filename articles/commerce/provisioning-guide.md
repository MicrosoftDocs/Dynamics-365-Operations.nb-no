---
title: Klargjøre et Dynamics 365 Commerce-sandkassemiljø
description: Denne artikkelen forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-sandkassemiljø for demonstrasjons- eller sandkassebruk med innebygde demonstrasjonsdata.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 1fc50f98055f1df72d255a5be6e863570564b183
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283648"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Klargjøre et Dynamics 365 Commerce-sandkassemiljø

[!include [banner](includes/banner.md)]

Denne artikkelen forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-sandkassemiljø for demonstrasjonsbruk med innebygde demonstrasjonsdata. Fremgangsmåten for konfigurasjon av et produksjonsmiljø ligner, men er mer omfattende siden mange av forutsetningene for sandkassemiljøet allerede er i demonstrasjonsdataene.

Før du begynner, anbefaler vi at du tar en rask titt på denne artikkelen for å få en pekepinn på hva prosessen krever.

For å kunne klargjøre et Commerce-sandkassemiljø må du angi enkelte parametere for miljøet og Commerce Scale Unit (CSU) som skal brukes når du klargjør Commerce senere. Instruksjonene i denne artikkelen beskriver alle nødvendige trinn som må fullføres for å klargjøre, og parameterne du må bruke.

Når klargjøringen av Commerce-miljøet er fullført, er det noen trinn du må utføre i etterkant for å klargjøre det for bruk. Noen trinn er valgfrie, avhengig av hvilke aspekter av systemet du vil bruke. Du kan alltid fullføre de valgfrie trinnene senere.

Hvis du vil ha informasjon om hvordan du konfigurerer Commerce-miljøet etter klargjøring, kan du se [Konfigurere et Commerce-sandkassemiljø](cpe-post-provisioning.md). Hvis du vil ha informasjon om hvordan du konfigurerer valgfrie funksjoner for Commerce-miljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-sandkassemiljø](cpe-optional-features.md).

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger må være på plass før du kan klargjøre Commerce-miljøet:

- Du har tilgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).
- Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og har et implementeringsprosjekt som allerede er opprettet og klart til bruk i LCS.  
- Du har opprettet en Azure Active Directory-sikkerhetsgruppe (Azure AD) som kan brukes som en systemadministratorgruppe for Commerce, og du har ID-en tilgjengelig.
- Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som en moderatorgruppe for vurderinger og omtaler, og du har ID-en tilgjengelig. (Denne sikkerhetsgruppen kan være den samme som systemadministratorgruppen for Commerce.)
- Du har distribuert en Headquarters-forekomst i LCS. Hvis du vil ha mer informasjon, kan du se [Distribuere et nytt miljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Legg merke til at denne listen ikke er fullstendig. Hvis du opplever problemer, kontakter du Microsoft-partnerkontakten for å få hjelp.

## <a name="provision-your-commerce-environment"></a>Klargjøre Commerce-miljøet

Følgende fremgangsmåter forklarer hvordan du klargjør et Commerce-miljø. Etter at du har fullført trinnene, er Commerce-miljøet klart til konfigurasjon. Alle trinnene som beskrives nedenfor, er i LCS-portalen.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Initialisere Commerce Scale Unit (sky)

For å initialisere CSU-en, følger du disse trinnene.

1. Velg miljøet fra listen i LCS.
1. Velg **Detaljerte opplysninger** i **MILJØER**-visningen til høyre. Detaljerte opplysninger for miljø vises.
1. Velg **Administrer** i delen **Administrer miljø** under **MILJØFUNKSJONER**.
1. Velg **Initialiser** i fanen **Commerce Scale Units**. Visningen **Legg til skalaenhet** vises.
1. I **OMRÅDE**-feltet velger du det samme området eller et område nær det du distribuerte miljøet til.
1. Velg den nyeste versjonen i rullegardinlisten **Versjon**.
1. Velg **Initialiser**.
1. Velg **Ja** advarselsdialogboksen der du blir bedt om å bekrefte initialiseringen av Commerce Scale Unit. CSU-en er nå lagt i køen for klargjøring.
1. Før du fortsetter, må du kontrollere at statusen for CSU er **VELLYKKET**. Initialiseringen tar omtrent to til fem timer.

Hvis du ikke finner **Behandle**-koblingen i miljødetaljvisningen, kontakter du Microsoft-kontakten for å få hjelp.

### <a name="initialize-e-commerce"></a>Initialisere e-handel

Følg disse trinnene for å initialisere Commerce.

1. Velg **Oppsett** i kategorien **e-handel**.
1. Angi et navn i feltet for **Navn på e-handelsmiljø**. Vær oppmerksom på at dette navnet vil vises i noen av URL-adressene som peker til e-handelsforekomsten.
1. I feltet **Commerce Scale Unit-navn** velger du CSU-en i listen. (Listen bør bare ha ett alternativ.)

    Feltet **Geografi for e-handel** angis automatisk.

1. Klikk **Neste** for å fortsette.
1. I feltet **Støttede vertsnavn** angir du et gyldig domene, for eksempel `www.fabrikam.com`.
1. Feltet **AAD-sikkerhetsgruppe for systemadministrasjon** angir de første bokstavene i navnet på sikkerhetsgruppen du vil bruke, og deretter velger du forstørrelsesglassymbolet for å vise søkeresultatene. Velg riktig sikkerhetsgruppe i listen.
1.  Feltet **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler** angir de første bokstavene i navnet på sikkerhetsgruppen du vil bruke, og deretter velger du forstørrelsesglassymbolet for å vise søkeresultatene. Velg riktig sikkerhetsgruppe i listen.
1. La alternativet **Aktiver tjenesten for vurderinger og omtale** settes til **Ja**.
1. Velg **Initialiser**. Visningen **Handelsadministrasjon** vises på nytt med kategorien **E-handel** valgt. Initialiseringen av e-handel har startet.
1. Før du fortsetter, må du vente til initialiseringsstatusen for e-handel er **INITIALISERING VELLYKKET**.
1. Under **Koblinger** ned til høyre noterer du URL-adressene for følgende koblinger:

    * **E-handelsområde** – koblingen til roten for e-handelsområdet.
    * **Commerce-områdebygger** – koblingen til verktøyet for områdeadministrasjon.

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen for å klargjøre og konfigurere Commerce-miljøet, kan du se [Konfigurere et Commerce-sandkassemiljø](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere et Dynamics 365 Commerce-sandkassemiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et Dynamics 365 Commerce-sandkassemiljø](cpe-bopis.md)

[Konfigurere valgfrie funksjoner for et Dynamics 365 Commerce-sandkassemiljø](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (sky)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-nettsted](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
