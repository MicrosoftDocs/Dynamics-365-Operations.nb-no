---
title: Sikkerhetskonfigurasjonsbegrep for virtuelle tabell-baserte integreringer
description: Denne artikkelen beskriver en arkitektur for integrering mellom Microsoft Dynamics 365 Human Resources og andre systemer.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759657"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Sikkerhetskonfigurasjonsbegrep for virtuelle tabell-baserte integreringer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver en arkitektur for bruk av [Microsoft Dataverse-virtuelle tabeller (enheter)](/dev-itpro/power-platform/virtual-entities-overview) for å bygge en integrering mellom Dynamics 365 Human Resources og et tredjepartssystem. Fokus for artikkelen er på sikkerhetskonfigurasjonen, og på godkjennings- og autorisasjonsaspekter som kreves mellom systemets behov for å bygge et funksjonelt, sikkert system.

## <a name="prerequisite-reference-articles"></a>Nødvendige referanseartikler

Følgende artikler gir mer informasjon om konsepter i denne artikkelen:

- [Oversikt over virtuelle enheter](/dev-itpro/power-platform/virtual-entities-overview)
- [Komme i gang med virtuelle tabeller (enheter)](/developer/data-platform/virtual-entities/get-started-ve)
- [Bruke server-til-server-godkjenning med flere leiere (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Bruke OAuth-godkjenning med Microsoft Dataverse (Dataverse)](/developer/data-platform/authenticate-oauth)
- [OAuth 2.0-klientlegitimasjonsflyt på Microsoft-identitetsplattformen](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Godkjenning og autorisasjon](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Arkitektur 

Diagrammene nedenfor viser de viktigste begrepene som er involvert i en integrering som bruker virtuelle tabeller (enheter).

![Virtuell tabell-basert integrering.](./media/Hosts.jpg)

Her er en forklaring på noen av elementene i det forrige diagrammet:

- **Microsoft** – Microsoft er vert for og driver de ulike Dynamics 365-produktene på vegne av kunder.

    - **Azure Active Directory-leier (Azure AD) C** – En Azure AD-leier som eies av Microsoft. Det er leieren som Dynamics 365-programmene er registrert i.

- **Integrere partner**

    - **Integreringssystem** – Systemet som integreres med Dynamics 365. Det kan være et lønnssystem eller et hvilket som helst system som er avhengig av data som er lagret i Dynamics 365.
    - **Adapter** – Programvaren eller tjenesten som er ansvarlig for samarbeid med både Dynamics 365 og integreringssystemet.

        > [!NOTE]
        > Hvis en adapter skal brukes av flere Dynamics 365-kunder, er forventningen at det vil bli registrert som et multleierprogram i Azure AD.

    - **Azure AD-leier A** – En Azure AD-leier som eies av integrasjonspartneren. Det er leieren som adapterens program-ID er registrert i.

- **Felles kunde** – En kunde som implementerer Dynamics 365 Human Resources og integreringspartnerens løsning.

    - **Dynamics 365 Finance eller Human Resources**– Den kundespesifikke forekomsten av Dynamics 365 Finance eller Human Resources som inneholder kundedataene som integreringssystemet krever.
    - **Dataverse**– Det kundespesifikke Dataverse-miljøet som er koblet til enten Finance eller Human Resources. Dataverse inneholder en web-API for samhandling med Dynamics 365-data.
    - **Azure AD-leier B** – Kundens Azure AD-leier. Det fungerer som identitetsleverandøren (autorisasjonsserver) og utsteder tokener som gir autorisasjon til å ringe kundens Dataverse-forekomst.

## <a name="basic-request-flow"></a>Grunnleggende forespørselsflyt

Denne delen beskriver den grunnleggende flyten for en vanlig forespørsel som er involvert i en integrering. Den refererer til arkitekturdiagrammet tidligere i denne artikkelen.

En vanlig forespørsel krever at adapteren spør Dynamics 365 etter data, og deretter lagrer og synkroniserer dataene til det integrerte systemet.

1. Adaspteren kaller opp Dataverse-web-API-en for å utføre en spørring etter relevante data.

    > [!NOTE]
    > Godkjenning er en forutsetning, og tokenanskaffelse er en viktig del av prosessen. Godkjenningen vil bli beskrevet i delen [Godkjenning og godkjenning ved systemgrenser](#authentication-and-authorization-at-system-boundaries).

    Dette kallet gjøres mot Dataverse-web-API for spørring etter programdata som vises gjennom en virtuell tabell. (Se 2. Første synkronisering og 3. Delta-synkronisering i diagrammet.)

2. Dataverse håndterer forespørselen ved å spørre i den virtuelle tabellen via Virtuell enhet-plugin-modulen ("Virtuell tabell-proxy" i diagrammet). Dataverse-forespørselen videresendes til den virtuelle enhetstjeneste Finance eller Human Resources for dataene som er fysisk lagret i Finance- eller Human Resources-databasen.
3. Den virtuelle tjenesten Finance or Human Resources oversetter forespørselen mot den virtuelle enheten til en spørring mot Finance- eller Human Resources-enheten som støtter den virtuelle Dataverse-enheten. Dataene hentes fra databasen, oversettes tilbake til Dataverse-enhetsrepresentasjonen og returneres til den som ringer.
4. Adapteren fullfører eventuell nødvendig tilordning og dataoversettelse, og gjør et kall til det integrerte systemet for å fastholde dataene i den integrerende systemdatabasen. (Se 4. Lagre data i diagrammet.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Godkjenning og autorisering ved systemgrenser

*Godkjenningen* validerer at brukerens eller programmets identitet er bekreftet, og bekrefter at brukeren eller programmet er den de sier de er. *Autorisasjon* gir brukeren eller programmet tilgang til bestemte tillatelser på programnivå. Hvis du vil ha mer informasjon, kan du se [Godkjenning kontra autorisasjon](/azure/active-directory/develop/authentication-vs-authorization).

De fleste kryssystemkall i arkitekturdiagrammet tidligere i denne artikkelen involverer adapteren. Adaptere må godkjenne seg selv for å utføre følgende kall:

- Kallet til Dataverse
- Kallet til integreringssystemet

Ser på systemets grenser i diagrammet. Alle webforespørsler mellom systemer må godkjennes, og autorisasjonskontroller på programnivå må godkjennes før data returneres til den som ringer. For en forespørsel mot en virtuell Dynamics 365-tabell som sikkerhetskopieres av Finance eller Human Resources, iverksettes godkjennings- og autorisasjonskontroller ved følgende systemkontroller:

- Samtalen mellom adapteren og sluttpunktet for Dataverse-web-APIen (OData)
- Kallet mellom Virtuell enhet-plugin-modulen Dataverse og Virtuell enhet-tjenesten Human Resources

I begge tilfeller utføres godkjenningskontroller først. Da utføres det autorisasjonskontroller på programnivå for å sikre at den godkjente brukeren eller programmet har de riktige rettighetene på programnivå til å hente de ønskede dataene.

Godkjenning til å kalle Dataverse håndteres via bærertokenet som må inkluderes som et HTTP-hode i webforespørselen til Dataverse. Adapteren må hente et token fra leier B Azure AD-forekomsten. (Se 1. Hent token i diagrammet.) Azure AD fungerer som identitetsleverandøren i godkjenningsflyten.

Adapteren godkjenner ved å angi applikasjons-IDen (ikke-hemmelig, som registrert i Azure AD-leier A) og et program eller et sertifikat som bare adapterprogrammet har.

Når brukeren eller programmet er godkjent for å foreta kall til Dataverse, utføres Dataverse-nivåautorisasjonkontrollene mot hver forespørsel. Disse kontrollene sørger for at den som gjør kallet (adapterprogrammets identitet, som er angitt som \<guid A\> i diagrammet), har de nødvendige programtillatelsene. Autorisasjon på programnivå administreres i Dataverse via en programbruker som representerer adapterens applikasjons-ID. Tillatelser på programnivå administreres ved å gi tilgang til bestemte Dataverse-definerte programroller. Disse rollene har mange privilegier til programmet.

For mer detaljert veiledning, se [Bruke server-til-server-godkjenning med flere leiere](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication).

Hvis programtillatelseskontroller for Dataverse-nivå er bestått, utfører Virtuell enhet-plugin-modulen et kall til Virtuell enhet-tjenesteendepunktet i Finance- eller Human Resources-miljøet. Server-til-server-godkjenning (S2S) brukes til å foreta dette kallet. Den bruker identiteten og handlingen som er konfigurert i konfigurasjonsposten for den virtuelle datakilden for Økonomi og drift.

![Konfigurasjonsposten for den virtuelle datakilden for Økonomi og drift i sandkassemiljøet.](./media/sandbox.jpg)

Hvis du vil ha mer informasjon, kan du se [Konfigurere virtuelle Dataverse-enheter](/dev-itpro/power-platform/admin-reference).

Kallet fra den virtuelle Dataverse-enhetsplugin-modulen til Finance eller Human Resources omfatter adapteridentiteten for det opprinnelige kallet til Dataverse fra adapteren (identiteten som er angitt som \<guid A\> i arkitekturdiagrammet). Hvis datakilden for den virtuelle enheten er riktig konfigurert, og S2S-godkjenningskontrollene er bestått, vil tjenesten for virtuell enhet i Finance eller Human Resources kjøre spørringen i konteksten til den opprinnelige oppkalleren (adapteren \<guid A\>). Kontroller av programtillatelse (autorisasjon) på Finance- eller Human Resources-nivå gjøres for å sikre at adapteren har de rettighetene som kreves for å få tilgang til dataenhetene som forespørselen krever via spørringen.

Sikkerhet for Finance og Human Resources administreres på følgende måter:

1. Ved å tilordne adapteridentiteten (\<guid A\>) til en bestemt Finance- eller Human Resources-bruker. Denne tilordningen gjøres på siden **Azure Active Directory-bruksområder**. Hvis du vil ha mer informasjon, kan du se [Registrere den eksterne appen](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Ved å gi Finance- eller Human Resources-brukeren de riktige rollene, rettighetene og privilegiene på programnivå. Hvis du vil ha mer informasjon, se [Rollebasert sikkerhet](/dev-itpro/sysadmin/role-based-security).

Hvis adapterprogrammet (\<guid A\>) gis de rettighetene som kreves for å få tilgang til de ønskede dataene, skjer følgende hendelser:

1. Spørringen kjøres.
2. Dataene oversettes tilbake til Dataverse-enhetssiden.
3. Dataene returneres til adapteren.

> [!IMPORTANT]
> Under utviklingen kan adapteren kjøres ved hjelp av Finance- eller Human Resources-bruker som har administratorrollen. I et produksjonsmiljø bør imidlertid adapteren aldri kjøres med administratorrettigheter.

## <a name="key-takeaways"></a>Viktige ting å ta med seg

Her er noen viktige konsekvenser av arkitekturen i den virtuelle tabellen eller enheten:

- Sikkerhetskonfigurasjonen for virtuelle tabeller som sikkerhetskopieres av Human Resources, administreres i Human Resources.
- Kunden ("Felles kunde" i arkitekturdiagrammet tidligere denne artikkelen) har full kontroll over hvilke rettigheter som gis til integreringsadapteridentiteten (angitt som \<guid A\> i diagrammet).
- Kunden er ansvarlig for riktig sikkerhetskonfigurasjon i Human Resources-miljøet. Integreringspartneren som oppretter adapteren, må gi veiledning om rettighetene som kreves for adapteren.
