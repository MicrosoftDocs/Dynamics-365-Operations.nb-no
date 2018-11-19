---
title: "Karriereområde-funksjonalitet i Attract"
description: "Denne artikkelen gir en oversikt over den kandidatrettede karrireområde-funksjonaliteten i Microsoft Dynamics 365 for Talent - Attract. Den forklarer også hvordan du konfigurerer denne funksjonen."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: nb-no
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Karriereområde-funksjonalitet i Attract

[!include [banner](includes/banner.md)]

Denne artikkelen gir en oversikt over den kandidatrettede karrireområde-funksjonaliteten i Microsoft Dynamics 365 for Talent: Attract. Den forklarer også hvordan du konfigurerer denne funksjonen.

## <a name="overview"></a>Oversikt

Attract inneholder ett karriereområde for hvert miljø i en leier. Hvis en organisasjon for eksempel har et utviklingsmiljø og et testmiljø, klargjøres ett karriereområde for utviklingsmiljøet og et annet karriereområde klargjøres for testmiljøet. Hvert karriereområde er **fullstendig isolert** og har sin egen godkjenningsmekanisme. Jobber og kandidatprofiler deles ikke mellom karriereområder.

Som standard er karriereområdet offentlig. Derfor kan kandidater vise alle jobbene som er merket som eksterne, uten å måtte logge på. Alle andre handlinger krever imidlertid at kandidater logger på.

## <a name="career-site-management"></a>Karrierestedsledelse

Følgende elementer på karriereområdet styres av innstillingene:

- **Organisasjonsnavn:** Organisasjonsnavnet vises i navigasjonsfeltet øverst i karriereområdet. Ved å velge navnet på organisasjonen går kandidater til en side som viser alle åpne jobber.
- **Organisasjonslogo:** Et bilde av organisasjonens logo vises øverst til venstre for karriereområdet. Ved å velge logobildet går kandidater til en side som viser alle åpne jobber.

Hvis du vil angi verdier for organisasjonsnavn og logo, logger du deg på Attract som administrator, velger **Administrasjonssenter** på **Innstillinger**-menyen (tannhjulsymbolet), og velger deretter den **Firmainformasjon**-kategorien.

> [!NOTE]
> Logobildet som vises på karriereområdet, har en fast høyde på 20 piksler. Bildet du legger til i administrasjonssenteret, skaleres slik at det passer. Avhengig av bildet kan derfor bredden endres.

## <a name="career-site-url"></a>URL-adresse for karriereområde

Når du [posterer en ekstern jobb](./Creating-jobs-Attract.md#postings) for første gang, kan du kopiere **Søk**-koblingen fra programmet Attract. URL-adressen for denne koblingen vil være i følgende format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

URL-adressen til karriereområdet er en delstreng av **Søk**-URL-adressen. Den består av alt opp til og med firmanavnet. For den foregående **Søk**-URL-adressen er derfor URL-adressen for karriereområdet `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Godkjenningsalternativer

Kandidater har følgende alternativer for pålogging for et Attract-karriereområde:

- Personlig konto:

    - LinkedIn
    - Microsoft 
    - Google
    - Facebook

- Jobb- eller skolekonto:

    - Microsoft Azure Active Directory (Azure AD)

Azure AD-påloggingen er bare beregnet for interne kandidater. Derfor fungerer den bare for interne kandidater som bruker den Azure AD-legitimasjonen for firmaet. Eksempel: En kandidat som for tiden er ansatt hos Contoso Ltd., vil søke på en jobb i et ikke-relatert firma, Alpine Ski House. I dette tilfellet vil ikke påloggingen lykkes hvis den ansatte prøver å bruke Azure AD-legitimasjonen fra Contoso Ltd.

## <a name="create-and-maintain-a-profile"></a>Opprette og vedlikeholde en profil

Etter at kandidater har logget på karriereområdet, kan de velge **Min profil** i navigasjonsfeltet øverst på siden for å opprette og vedlikeholde profilen. Profilen inneholder personlige opplysninger, informasjon om arbeidserfaring, opplysninger om utdannelse, dokumenter, koblinger og informasjon om kompetanse. Når det opprettes en profil, kan den brukes til å søke på jobber som kandidaten er interessert i. Profiler også hjelpe Attract med å anbefale de rette jobbene for kandidater.

## <a name="find-the-right-job"></a>Finne riktig jobb

På jobblistesiden kan kandidater søke etter en bestemt jobb ved å skrive inn søkeord. Søkefunksjonaliteten ser etter søketermene i stillingsbetegnelser og jobbeskrivelser, og viser relevante jobber som resultater. Kandidater kan filtrere resultatene når som helst basert på jobbplasseringen eller jobbfunksjonen.

Kandidater kan også vise et sett med anbefalte jobber på karriereområdet. Jobbene som anbefales til en kandidat, er basert på kandidatens tidligere søknader, profil og CVer.

> [!NOTE]
> Jobbanbefalinger vises bare hvis minst 10 jobber er postert på karriereomrdådet, og kandidaten har fullført sin profil.

## <a name="apply-for-jobs"></a>Søke på stillinger

Når kandidater har funnet riktig jobb, kan de søke ved hjelp av **Søk**-knappen øverst på siden for jobbdetaljer. Nå kan kandidater opprette en helt ny profil eller gå gjennom informasjonen i den eksisterende profilen. Kandidater kan også laste opp en CV, etter behov, og deretter sende inn jobbsøknaden.

## <a name="check-application-status"></a>Kontrollere søknadsstatus

Når kandidater har søkt på én eller flere jobber, kan de velge **Søknader** i navigasjonsfeltet øverst på siden for å vise åpne og lukkede søknader. Når kandidater åpner en av søknadene, ser de gjeldende stadium og ventende handlingselementer de må fullføre. Hvis en kandidat må oppgi potensielle datoer for et personlig intervju, viser for eksempel siden hans eller hennes alternativer.

## <a name="internal-jobs"></a>Interne stillinger

Jobber som er merket som interne og er postert til Attract-karriereområdet, vises for øyeblikket ikke på karriereområdet. De er bare tilgjengelig via den direkte **Søk**-URL-adressen som kan kopieres fra programmet Attract.

