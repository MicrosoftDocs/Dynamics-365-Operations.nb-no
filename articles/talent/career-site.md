---
title: Karriereområde-funksjonalitet i Attract
description: Dette emnet gir en oversikt over den kandidatrettede karriereområde-funksjonaliteten i Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/13/2019
ms.locfileid: "389978"
---
# <a name="career-site-functionality-in-attract"></a>Karriereområde-funksjonalitet i Attract

[!include[banner](../includes/banner.md)]

Dette emnet gir en oversikt over den kandidatrettede karriereområde-funksjonaliteten i Microsoft Dynamics 365 for Talent: Attract. Den forklarer også hvordan du konfigurerer denne funksjonen.

Attract inneholder ett karriereområde for hvert miljø i en leier. Hvis en organisasjon for eksempel har et utviklingsmiljø og et testmiljø, klargjøres ett karriereområde for utviklingsmiljøet og et annet karriereområde klargjøres for testmiljøet. Hvert karriereområde er fullstendig isolert og har sin egen godkjenningsmekanisme. Jobber og kandidatprofiler deles ikke mellom karriereområder.

Som standard er karriereområdet offentlig. Derfor kan kandidater vise alle jobbene som er merket som eksterne, uten å måtte logge på. Alle andre handlinger krever imidlertid at kandidater logger på.

## <a name="career-site-management"></a>Karrierestedsledelse

Hvis du vil angi verdier for følgende elementer, logger du deg på Attract som administrator, velger **Administrasjonssenter** på **Innstillinger**-menyen (tannhjulsymbolet), og velger deretter **Firmainformasjon**-kategorien.

-   **Organisasjonsnavn** – Organisasjonsnavnet vises i navigasjonsfeltet øverst i karriereområdet. Ved å velge navnet på organisasjonen går kandidater til en side som viser alle åpne jobber.

-   **Organisasjonslogo** – Et bilde av organisasjonens logo vises øverst til venstre for karriereområdet. Ved å velge logobildet går kandidater til en side som viser alle åpne jobber.

    >   [!NOTE] 
    >   Logobildet som vises på karriereområdet, har en fast høyde på 20 piksler. Bildet du legger til i administrasjonssenteret, skaleres slik at det passer. Avhengig av bildet kan derfor bredden endres.
 
Hvis du vil angi verdier for følgende elementer, logger du deg på Attract som administrator, velger **Administrasjonssenter** på **Innstillinger**-menyen og velger deretter **Karrierestedsledelse**-kategorien.

-   **Optimalisering av søkemotor** – Når aktivert er alle offentlige jobber som er postert til Attract-karriereområdet, søkbare ved hjelp av søkemotorer som Bing og Google.

    >   [!NOTE] 
    >   Det kan være en forsinkelse fra aktivering av denne innstillingen til at søkeresultatene vises, avhengig av søkemotoren du bruker.
         
## <a name="career-site-urls"></a>URL-adresser for karriereområde

Følgende liste inneholder vanlige URL-adresser for karriereområde og hvordan du åpner dem.

-   **URL-adresse til hjemmeside for karriereområde** – Hvis du vil vise URL-adressen til hjemmesiden for karriereområdet, logger du på Attract som administrator, velger **Administrasjonssenter** på **Innstillinger**-menyen og velger deretter **Karrierestedsledelse**-kategorien.

-   **Søk-URL for individuell jobbutlysning** – Når du [posterer en ekstern jobb](Creating-jobs-Attract.md#postings) for første gang, kan du kopiere **Søk**-koblingen fra programmet Attract. URL-adressen for denne koblingen vil være i følgende format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **URL-adresse til jobbutlysning** – URL-adressen til jobbutlysningen er en delstreng til Søk-URL-en. Den består av alt opp til og med jobbnummeret. For den foregående Søk-URL-adressen er derfor URL-adressen for jobbutlysningen [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)

## <a name="authentication-options"></a>Godkjenningsalternativer

Kandidater har følgende alternativer for pålogging for et Attract-karriereområde:

-   Personlig konto:

    -   LinkedIn

    -   Microsoft

    -   Google

    -   Facebook

-   Jobb- eller skolekonto:

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD-påloggingen er bare beregnet for interne kandidater. Derfor fungerer den bare for interne kandidater som bruker Azure AD-legitimasjonen for firmaet. Eksempel: En kandidat som for tiden er ansatt hos Contoso Ltd., vil søke på en jobb i et ikke-relatert firma, Alpine Ski House. I dette tilfellet vil ikke påloggingen lykkes hvis den ansatte prøver å bruke Azure AD-legitimasjonen fra Contoso Ltd.

## <a name="create-and-maintain-a-profile"></a>Opprette og vedlikeholde en profil

Etter at kandidater har logget på karriereområdet, kan de velge **Min profil** i navigasjonsfeltet øverst på siden for å opprette og vedlikeholde profilen.
Profilen inneholder personlige opplysninger, informasjon om arbeidserfaring, opplysninger om utdannelse, dokumenter, koblinger og informasjon om kompetanse. Når det opprettes en profil, kan den brukes til å søke på jobber som kandidaten er interessert i. Profiler hjelper også Attract med å anbefale de rette jobbene for kandidater.

>   [!NOTE]
>   Hvis en kandidat bruker en e-post-ID til å logge på med en av godkjenningsleverandørene ovenfor, vil denne e-post-IDen som standard gå til kontaktens e-post-ID som er knyttet til profilen. Den sistnevnte endres imidlertid endres når som helst og er fullstendig uavhengig av den tidligere. Attract vil alltid bruke kontaktens e-post-ID til å knytte til profilen din for alle e-postmeldinger.

## <a name="find-the-right-job"></a>Finne riktig jobb

På jobblistesiden kan kandidater søke etter en bestemt jobb ved å skrive inn søkeord. Søkefunksjonaliteten ser etter søketermene i stillingsbetegnelser og jobbeskrivelser og viser relevante jobber som resultater. Kandidater kan filtrere resultatene når som helst basert på jobbplasseringen eller jobbfunksjonen.

Kandidater kan også vise et sett med anbefalte jobber på karriereområdet. Jobbene som anbefales til en kandidat, er basert på kandidatens tidligere søknader, profil og CVer.

>   [!NOTE] 
>   Jobbanbefalinger vises bare hvis minst 10 jobber er postert på karriereområdet og kandidaten har fullført en profil.

## <a name="apply-for-jobs"></a>Søke på stillinger

Når kandidater har funnet riktig jobb, kan de søke ved hjelp av **Søk**-knappen på siden for **Jobbdetaljer**. Nå kan kandidater opprette en ny profil eller gå gjennom informasjonen i den eksisterende profilen.
Kandidater kan også laste opp en CV, etter behov, og deretter sende inn jobbsøknaden.

## <a name="check-application-status"></a>Kontrollere søknadsstatus

Når kandidater har søkt på én eller flere jobber, kan de velge **Søknader** i navigasjonsfeltet øverst på siden for å vise åpne og lukkede søknader. Når kandidater åpner en av søknadene, ser de gjeldende stadium og ventende handlingselementer de må fullføre. Hvis en kandidat må oppgi potensielle datoer for et personlig intervju, viser for eksempel siden tilgjengelige alternativer.

## <a name="internal-jobs"></a>Interne stillinger

Jobber som er merket som interne og er postert til Attract-karriereområdet, vises for øyeblikket ikke på karriereområdet. De er bare tilgjengelige via den direkte **Søk**-URL-adressen som kan kopieres fra programmet Attract.
