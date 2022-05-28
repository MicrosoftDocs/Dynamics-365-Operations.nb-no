---
title: Definere og vedlikeholde leverandørsamarbeid
description: Dette emnet forklarer hvordan du konfigurerer leverandørsamarbeid i Dynamics 365 Supply Chain Management. Den beskriver også hvordan du klargjør nye brukere med leverandørsamarbeid og administrerer sikkerhetsrollene for disse brukerne.
author: GalynaFedorova
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4b59513d86426d3c1bfd759b9aabc331e58d5423
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677569"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Definere og vedlikeholde leverandørsamarbeid

[!include [banner](../includes/banner.md)]

Grensesnittet for leverandørsamarbeid viser begrenset informasjon om bestillinger, fakturaer og forsendelseslager til eksterne leverandørbrukere. Fra dette grensesnittet kan en leverandør også svare på forespørsler om tilbud, og vise og redigere grunnleggende firmainformasjon.

Dette emnet forklarer hvordan du konfigurerer leverandørsamarbeid i Dynamics 365 Supply Chain Management. Den beskriver også hvordan du setter opp en arbeidsflyt for å klargjøre nye brukere med leverandørsamarbeid og administrerer sikkerhetsrollene for disse brukerne.

> [!NOTE]
> Informasjonen om oppsett av sikkerhetsroller for leverandørsamarbeid gjelder bare for gjeldende versjon av Finance and Operations. I Microsoft Dynamics AX 7.0 (februar 2016) og Microsoft Dynamics AX programversjon 7.0.1 (mai 2016) kan du samarbeide med leverandører ved hjelp av modulen **Leverandørportal**. Hvis du vil ha informasjon om brukertillatelser for leverandørportalen i Microsoft Dynamics AX, kan du se [Brukersikkerhet for leverandørportal](configure-security-vendor-portal-users.md).

## <a name="set-up-vendor-collaboration-security-roles"></a>Definere sikkerhetsroller for leverandørsamarbeid

En innkjøpsmedarbeider eller en leverandør som har tilstrekkelige tillatelser, kan be om at en kontaktperson blir klargjort som en bruker ved å aktivere **Klargjør leverandørbruker** i kontaktpersonposten. Under klargjøringsprosessen velges brukertillatelser for den nye eksterne brukeren, og den nye leverandørbrukerforespørselen sendes. Det er viktig at du konfigurerer brukertillatelsene som kan velges i leverandørbrukerforespørselen, riktig. Ellers kan leverandører få tilgang til informasjon som de ikke skal ha tilgang til i Supply Chain Management.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>Definere sikkerhetsrollene som kan velges når en ny brukerforespørsel brukes for en kontaktperson

1. Velg **Systemadministrasjon** &gt; **Sikkerhet** &gt; **Eksterne roller**.
2. Velg **Ny**, og velg deretter en sikkerhetsrolle og **Leverandør**-partsrollen.

Det kan hende at du vil legge til rollene **Leverandøradministrasjon (ekstern)** og **Leverandør (ekstern)** som finnes i Supply Chain Management. Du kan også bruke sikkerhetsroller som firmaet har opprettet.

Du bør bare gjøre rollen **Leverandøradministrasjon (ekstern)** tilgjengelig hvis leverandørene skal kunne opprette nye kontakter, sende brukerforespørsler for leverandørsamsamarbeid for nye brukere og endringer i brukerinformasjon, og håndtere disse forespørslene via en arbeidsflyt.

Hvis du planlegger å definere leverandørkontakter og brukere manuelt, kan du gjøre bare **leverandørrollen (ekstern)** tilgjengelig. Denne rollen vil da være den eneste rollen som kan forespørres via en leverandørbrukerforespørsel.

> [!NOTE]
> Rollen **SystemUser** tildeles manuelt når du oppretter en ny brukerkonto. Derfor må du fjerne rollen og tilordne rollen **SystemExternalUser**. Hvis det opprettes nye brukerkontoer via arbeidsflyten som startes av en leverandørbrukerforespørsel om å klargjøre en ny bruker, tilordnes én eller flere av rollene du har definert for leverandørsamarbeid, og **SystemExternalUser**-rollen tilordnes.

#### <a name="vendor-admin-external-security-role"></a>Sikkerhetsrolle for leverandøradministrator (ekstern)

Rollen **Leverandøradministrasjon (ekstern)** kan brukes for eksterne leverandører som vedlikeholder kontaktinformasjon for leverandøren og kommer med forespørsler om å klargjøre nye samarbeidsbrukere for leverandører. Eksterne brukere som har denne sikkerhetsrollen, kan utføre følgende oppgaver:

- Vise og endre kontaktinformasjon, for eksempel personens tittel, e-postadresse og telefonnummer.
- Legge til en ny eller eksisterende kontakt i leverandørkontoene de er en kontakt for.
- Slette eventuell kontaktperson de har opprettet.
- Aktivere eller deaktivere tilknytningen mellom en kontaktperson og en leverandørkonto. Når tilknytningen mellom en kontaktperson og en leverandørkonto er deaktivert, kan ikke kontaktpersonen refereres til på nye bestillinger eller andre dokumenter.
- Avslå eller tillat en kontaktpersons tilgang til dokumenter i leverandørsamarbeidsgrensesnittet som gjelder spesielt for leverandørkontoen. Når tilknytningen mellom en kontaktperson og en leverandørkonto er deaktivert, nektes alltid tilgang til dokumenter som er spesifikke for leverandørkontoen.
- Be om en ny brukerkonto for en kontaktperson ved hjelp av **Klargjør bruker**-handlingen.
- Be om at kontaktpersonens brukerkonto skal deaktiveres.
- Be om at en kontaktpersons brukerkonto endres for å legge til eller fjerne sikkerhetsroller.
- Vis tilbudsforespørsler.

#### <a name="vendor-external-security-role"></a>Sikkerhetsrolle for leverandør (ekstern)

**Leverandørrollen (ekstern)** kan brukes for eksterne leverandører som vil arbeide med bestillinger. Eksterne brukere som har denne sikkerhetsrollen, kan utføre følgende oppgaver:

- Svare på og vise informasjon om bestillinger.
- Vedlikeholde leverandørsamarbeidsfakturaer.
- Vise forsendelseslager.
- Vise og svare på tilbudsforespørsler.
- Vise leverandøropplysninger.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Definere sikkerhetsroller som brukes når kundeemneleverandører er introdusert

Hvis du vil introdusere leverandører som startes via en registreringsforespørsel for en kundeemneleverandør, må du definere en ekstern sikkerhetsrolle. Denne rollen blir tilordnet nye brukere i løpet av klargjøringsprosessen som styres av arbeidsflyten for typen **Arbeidsflyt for brukerforespørsel (plattform)**. Hvis du vil ha mer informasjon, kan du se delen [Konfigurere arbeidsflyter for å behandle brukerforespørsler for leverandørsamarbeid](#set-up-workflows-to-process-vendor-collaboration-user-requests) senere i dette emnet.

Hvis du vil ha mer informasjon om hvordan du introduserer potensielle leverandører, kan du [Ønske leverandører velkommen](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Definer en sikkerhetsrolle som skal brukes når en ny forespørsel fra en kundeemneleverandørbruker blir sendt

1. Velg **Systemadministrasjon** > **Sikkerhet** > **Eksterne roller**.
2. Velg **Ny**, og velg deretter en sikkerhetsrolle og **Potensiell leverandør**-partsrollen.

Du bør legge til rollen **Potensiell leverandør (ekstern)** som finnes i Supply Chain Management.

Sikkerhetsrollen gir bare tilgang til den nye leverandørregistreringsveiviseren.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Konfigurere arbeidsflyter for å behandle brukerforespørsler for leverandørsamarbeid

Hvis du vil garantere at alle relevante oppgaver er fullført, og at de riktige godkjenningene er gitt, må du definere arbeidsflyter for å håndtere brukerforespørsler for leverandørsamarbeid.

Brukerforespørsler for leverandørsamsamsvar sendes enten av eksterne leverandører som har sikkerhetsrollen **Leverandøradministrasjon (ekstern)** eller lignende tillatelser, eller av innkjøpsmedarbeidere i firmaet. De kan også genereres fra forespørsler om leverandørregistrering under leverandørintroduksjonsprosessen.

Det finnes tre typer forespørsler:

- Forespørsler om å klargjøre en ny bruker
- Forespørsler om å deaktivere en eksisterende bruker
- Forespørsler om å endre sikkerhetsrollene til en eksisterende bruker

Hvis du vil ha mer informasjon om brukerforespørsler om leverandørsamarbeid, kan du se [Administrere brukere av leverandørsamarbeid](manage-vendor-collaboration-users.md).

Du må opprette to eller flere arbeidsflyter for å behandle alle tre typene brukerforespørsler for leverandørsamarbeid. Nye arbeidsflyter opprettes på **Brukerarbeidsflyt**-siden.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Eksempel på en arbeidsflyt for klargjøring av nye brukere og endring av sikkerhetsroller

Hvis du vil behandle leverandørbrukerforespørsler om å opprette nye brukere og endre sikkerhetsroller, kan du definere en betingelse for grener i begynnelsen av arbeidsflyten. På denne måten brukes det en annen gren i arbeidsflyten, avhengig av om forespørselen er å opprette en ny bruker eller endre en eksisterende bruker.

Hvis du vil definere denne grenen, oppretter du en ny arbeidsflyt av typen **Brukerforespørselsarbeidsflyt (platform)**. Grenene i denne arbeidsflyten kan inneholde følgende elementer.

#### <a name="branch-to-provision-new-users"></a>Grener for å klargjøre nye brukere

1. Tilordne en godkjenningsoppgave til personen som er ansvarlig for å godkjenne at nye brukere skal få tilgang til informasjon om leverandørsamarbeid.
2. Tilordne en oppgave til personen som er ansvarlig for å be om nye Microsoft Azure Active Directory (Azure AD)-brukerkontoer i Azure Portal. Bruk den forhåndsdefinerte oppgaven **Send Azure B2B-brukerinvitasjon** for dette trinnet. B2B-brukere kan automatisk eksporteres til Azure AD. Bruk den forhåndsdefinerte **Klargjøring Azure AD B2B-bruker**. Hvis du vil ha mer informasjon, kan du se [Eksportere B2B-brukere til Azure AD](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Tilordne en godkjenningsoppgave til personen som laster opp til Azure. Hvis en kontooppretting ikke har blitt opprettet, avviser denne personen oppgaven og avslutter arbeidsflyten. Denne godkjenningsoppgaven kan hoppes over hvis du har tatt med trinnet som automatisk eksporterer nye brukerkontoer til Azure via B2B-programmeringsgrensesnittet (API).
4. Legg til en automatisert oppgave som klargjør en ny bruker. Bruk den forhåndsdefinerte oppgaven **Automatisk klargjøring av bruker** for dette trinnet.
5. Legg til en oppgave som varsler den nye brukeren. Det kan hende at du vil sende en velkomst-e-post til den nye brukeren som inneholder en URL-adresse for Supply Chain Management. Denne e-posten kan bruke en mal du oppretter på **E-postmeldinger**-siden velger deretter på siden **Parametere for brukerarbeidsflyt**. Malen kan inneholde **%portalURL%**-taggen. Når velkomst-e-posten genereres, erstattes denne taggen av URL-adressen til leietakeren for Supply Chain Management.

    > [!NOTE]
    > Denne arbeidsflyten kan brukes i flere scenarier som omfatter brukerintroduksjon. Den kan for eksempel brukes når mulige leverandører eller kontaktpersoner krever en samarbeidskonto for leverandører. Derfor bør du uttrykke e-posten som en generell erklæring som kan brukes til flere formål.

#### <a name="branch-to-modify-security-roles"></a>Gren for å endre sikkerhetsroller

1. Tilordne en godkjenningsoppgave til personen som er ansvarlig for å godkjenne endringer i sikkerhetsroller.
2. Legg til en automatisert oppgave som legger til eller fjerner de relevante sikkerhetsrollene. Bruk oppgaven **Automatisk klargjøring av bruker** for dette trinnet.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Eksempel på en arbeidsflyt for deaktivering av en bruker

Opprett en arbeidsflyt av typen **Deaktiver arbeidsflyt for brukerforespørsel**, og legg deretter til følgende oppgaver.

1. Tilordne en godkjenningsoppgave til personen som er ansvarlig for å godkjenne forespørsler om å deaktivere brukere. Du kan legge til betingelser for å automatisere dette godkjenningstrinnet.
2. Legg til en automatisert oppgave som deaktiverer brukeren. Bruk oppgaven **Automatisk deaktivering av bruker** for dette trinnet.
3. Legg til eventuelle oppryddingsoppgaver som er nødvendige. Du kan for eksempel legge til en oppgave som fjerner kontoen fra katalogen i Azure Portal.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Aktiver leverandørsamarbeid for en bestemt leverandør

Før du oppretter en brukerkonto for en person som skal bruke leverandørsamarbeid, må du definere leverandøren for å tillate leverandørsamarbeid. På siden **Leverandører**, på fanen **Generelt** angir du feltet **Samarbeidsaktivering**. Følgende alternativer er tilgjengelige:

- **Aktive (bestilling bekreftes automatisk)** – Bestillinger bekreftes automatisk hvis leverandøren godtar dem uten å be om endringer.
- **Aktive (bestilling bekreftes ikke automatisk)** – Organisasjonen din må bekrefte bestillinger manuelt etter at leverandøren har godtatt dem.

> [!NOTE]
> Innkjøpsteknikere i firmaet kan også fullføre denne oppgaven.

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Feilsøke klargjøring av nye leverandørsamarbeidsbrukere

Nye brukere i leverandørsamarbeid klargjøres via arbeidsflyten du angir for å behandle brukerforespørsler for leverandørsamarbeid av typen **Klargjør leverandørbruker**.

Hvis e-postadressen til en ny leverandørsamarbeidsbruker tilhører et domene som er registrert med Azure som en leietaker (det vil si en administrert domenekonto), må e-postadressen være en eksisterende Azure AD-konto. Hvis ikke kan ikke klargjøringsprosessen fullføres.

Hvis du vil ha mer informasjon om prosessen som brukes i oppgaven **Send Azure B2B-brukerinvitasjon** i arbeidsflyten for Azure AD-kontoadministrasjon, kan du se [Azure Active Directory B2B-samarbeid](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Tilleggsressurser

[Leverandørsamarbeid med eksterne leverandører](vendor-collaboration-work-external-vendors.md)

Se en kort video om leverandørintroduksjonsprosessen: [Introdusere en ny leverandør](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
