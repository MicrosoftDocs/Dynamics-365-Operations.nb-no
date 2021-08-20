---
title: Server-til-server-godkjenning for ATS-integrerings-API
description: Dette emnet beskriver hvordan du konfigurerer server-til-server-godkjenning for integrasjoner mot Dynamics 365 Human Resources API for søkersporingssystemintegrering.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aabe2cd9fd962c8f1c5bbf7fe911e7c6ceeae082f61fc4359aaf7bf197531eff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778085"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>Server-til-server-godkjenning for ATS-integrerings-API

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver hvordan du konfigurerer server-til-server-godkjenning for programintegrasjoner mot Dynamics 365 Human Resources API for søkersporingssystemintegrering. Det er et par lag med sikkerhet som må administreres for at tjenestekontohaveren skal få tilgang til den virtuelle Microsoft Dataverse-tabellen og tilknyttede data. Brukeren må ha tilgang til den virtuelle Dataverse-tabellen i Microsoft Power Platform og tilgang til dataene i Dynamics 365 Human Resources.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Aktiver tilgang til virtuelle Dataverse-tabeller i Power Platform

Det første trinnet som gir tilgang til de virtuelle Dataverse-tabellene i Power Platform er å konfigurere programmet i Power Platform for godkjenning mot virtuelle Dataverse-tabellendepunkt. Trinnene for å gjøre dette, finner du i [Microsoft Dataverse-utviklerhåndboken](/powerapps/developer/data-platform).

  - For enkeltstående appregistreringer: [Bruk server-til-server-godkjenning for én leietaker](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - For appregistreringer med flere leietakere: [Bruk server-til-server-godkjenning for flere leietakere](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>Opprette en sikkerhetsrolle for ATS-integreringer

Ett av trinnene etter at programbrukeren er opprettet, er å tilordne brukeren til en sikkerhetsrolle som definerer tilgangen programmet skal ha til sluttpunktene. Dette er trinn 7 i [Oppretting av programbruker](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) for enkeltstående appregistreringer, og [Opprett en sikkerhetsrolle for programbrukeren for registreringer med flere leietakere](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user). 

Rollen du tilordner programbrukeren, bør ha tilgang til dataenhetene som brukes i ATS-integreringen. Dette eksisterer ikke ut av boksen, så en ny sikkerhetsrolle må opprettes. Den nye rollen kan opprettes etter trinnene som er beskrevet i [Opprett en sikkerhetsrolle](/power-platform/admin/create-edit-security-role#create-a-security-role).

For den nye rollen må passende tilgang tilordnes til, som et minimum, følgende enheter i kategorien **Egendefinerte enheter** for den nye rollen. Merk at det kan være flere enheter du kan må legge til hvis integreringen bruker mer omfattende programdata. Når den nye rollen er opprettet, kan den tilordnes til programbrukeren.

  - Basisarbeider (mshr)
  - Ansettelseskandidat (mshr)
  - Sertifikatkompetanse (mshr)
  - Sertifikattype (mshr)
  - Bedrift
  - Kompensasjonsjobbfunksjon (mshr)
  - Kompensasjonsjobbtype (mshr)
  - Land/regioner (mshr)
  - Avdeling (mshr)
  - Utdanningskompetanse (mshr)
  - Utdannelsesgrad (mshr)
  - Utdanningsdisipliner (mshr)
  - Krav til utdanning (mshr)
  - Identifikasjon (mshr)
  - Identifikasjonstype (mshr)
  - Institusjon (mshr)
  - Utstedende byrå (mshr)
  - Jobbkompensasjon (mshr)
  - Jobber (mshr)
  - Utdannelsesnivå (mshr)
  - Partskontakter (mshr)
  - Personer (mshr)
  - Personadresser (mshr)
  - Personscreening (mshr)
  - Stillingstype (mshr)
  - Stillinger V2 (mshr)
  - Yrkeserfaringskompetanse (mshr)
  - Vurderingsnivå (mshr)
  - Vurderingsmodeller (mshr)
  - Årsakskoder (mshr)
  - Rekrutteringsforespørsel (mshr)
  - Rekrutteringsforespørselssted (mshr)
  - Rekrutteringsforespørselsstilling (mshr)
  - Rekrutteringsforespørselskompetanse (mshr)
  - Screeningtype (mshr)
  - Kompetanse (mshr)
  - Kompetanse (mshr)
  - Titler (mshr)
  - Veteranstatus (mshr)
  - Arbeider (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Gi programtillatelser til personaledata

Det andre trinnet er å sikre at programmet får nødvendige tillatelser til dataene i Human Resources ved å koble dem til en bruker i Human Resources-programmet. For en programbruker utføres server-til-server-kall via virtuelle Dataverse-tabeller i sammenheng med identiteten til brukeren (appen) i Dataverse som starter handlingen. Tjenesten for det virtuelle tabellkortet slår deretter opp den tilknyttede brukeren i Human Resources, og kjører spørringen i denne brukerens kontekst. Det betyr at en bruker må opprettes i Human Resources med de riktige rollene som er tilordnet, for å gi tilgang til dataene som det integrerende programmet trenger.

Human Resources-brukeren må også tilordnes de riktige tillatelsene til dataene i Human Resources. Rollen **Rekrutteringsprogram** (HcmRecruitingIntegrator) er tilgjengelig med rettigheter for de primære enhetene som kreves for integrasjon med rekrutteringsdata. Denne rollen kan tilordnes programbrukeren på **Brukere**-siden for å gi passende tilgang til dataene. Hvis du vil ha mer informasjon om sikkerhetsroller for Human Resources, kan du se [Rollebasert sikkerhet](/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Angi den nye brukeren med de nødvendige tillatelsene

Følg denne fremgangsmåten for å angi den nye brukeren med de nødvendige tillatelsene:

  1. Åpne **Brukere**-siden i Human Resources, og velg **Ny**.
  2. Angi en **bruker-ID** og et **brukernavn** for den nye programbrukeren. Du kan for eksempel skrive inn "RekrutteringIntegrasjon".

      > [!NOTE]
      > Hvis appen ikke har en Microsoft Azure Active Directory (Azure AD)-brukerkonto eller e-postadresse, kan du f.eks. angi "RekrutteringApp" i e-postadressen og leverandørfeltene for brukeren.

  3. På hurtigfanen **Brukerens roller** velger du handlingen **Tilordne roller**.
  4. I ruten **Tilordne roller til bruker** velger du **Rekrutteringsprogram** og deretter **OK**.
  5. Lagre den nye brukerposten.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Koble den nye Human Resources-brukeren til programmet

Når brukeren er opprettet, må det opprettes en post for programmet i skjemaet **Azure Active Directory-programmer** for å koble appen til Human Resources-brukeren.

  1. Åpne skjemaet **Azure Active Directory-programmer**, og velg **Ny**.
  2. I feltet **Klient-ID** angir du klient-IDen til programbrukeren som er opprettet for programmet.
  3. I **Navn**-feltet angir du navnet på det integrerende programmet.
  4. Velg den nye Human Resources-brukeren som er opprettet for rekrutteringsintegrasjon, i **Bruker-ID**-feltet.
  5. Lagre den nye posten.

Programmet vil da ha tilgang til Human Resources-data, begrenset bare til dataene som kreves for rekruttering av programintegrasjoner.

## <a name="see-also"></a>Se også

[Rekruttere jobbkandidater](hr-personnel-recruit.md)<br>
[Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Bruke Microsoft Dataverse-web-API-en](/powerapps/developer/data-platform/webapi/overview)<br>
[Opprette og oppdatere alternativsett ved hjelp av web-API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
