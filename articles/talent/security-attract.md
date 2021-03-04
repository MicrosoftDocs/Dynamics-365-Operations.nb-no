---
title: Angi brukertillatelser i Attract
description: Dette emnet inneholder informasjon om rollesikkerhet i Microsoft Dynamics 365 Talent – Attract.
author: andreabichsel
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: efac512cfa07bb2183f06b8be45f74bef9af0767
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462102"
---
# <a name="set-user-permissions-in-attract"></a>Angi brukertillatelser i Attract

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract bruker rollebasert sikkerhet. Med andre ord gis ikke tilgang til individuelle brukere, men til sikkerhetsrollene som brukere er tilordnet. En bruker som er tilordnet en sikkerhetsrolle, har tilgang til settet med rettigheter som er knyttet til denne rollen.

Attract inneholder fem grunnleggende brukerroller:

- Administrator
- Ansettelsesansvarlig
- Rekrutterer
- Intervjuer
- Skrivebeskyttet

Administratorrollen er den eneste rollen som har tillatelse til å legge til andre brukere og endre tillatelsene deres.

- **Legg til** – I administrasjonssenteret, i fanen **Brukertillatelser**, velger du **Tilordne roller**, søker etter brukeren du vil legge til, og deretter tilordner tillatelser til denne brukeren.
- **Rediger** – Søk etter brukeren, eller finn brukeren i listen, og velg deretter **Rediger** for å endre vedkommendes tillatelser.
- **Slett** – Hvis du sletter en brukers tillatelser, fjerner du ikke brukeren fra systemet. Du begrenser imidlertid brukerens tilgang og tillatelser i Attract. For eksempel er Hilda tilordnet rollen som ansettelsesansvarlig, og hun legges til en jobb som ansettelsesansvarlig. Hvis Hilda senere blir fjernet fra rollen som ansettelsesansvarlig, forblir hun ansettelsesansvarlig for jobben og har fremdeles tilgang til denne jobben. Hun kan imidlertid ikke opprette andre jobber.

Delene nedenfor gir en beskrivelse på høyt nivå av hver rolle. Tabellene senere i emnet gir mer detaljert informasjon.

> [!NOTE]
> Noen funksjoner er bare tilgjengelige med tillegget for omfattende ansettelse for Attract.

## <a name="administrator"></a>Administrator

Brukere som er tilordnet rollen som administrator, kan få tilgang til og endre alle dataene i Attract. Administratorer kan opprette, lese, oppdatere og slette data. De har også tilgang til administrasjonssenteret, der de kan konfigurere Attract og sette opp brukerinformasjon. Vi anbefaler at minst én person tilordnes til administratorrollen. Som standard settes miljøadministratoren i Microsoft Power Apps som administrator i Attract. Hvis du har registrert deg for prøveversjonen av Attract, tilordnes automatisk administratorrollen til deg. For å opprette jobber, må brukere som har rollen administrator, for øyeblikket også ha rekruttererrollen eller rollen som ansettelsesansvarlig

## <a name="hiring-manager"></a>Ansettelsesansvarlig

Brukere som er tilordnet rollen som ansettelsesansvarlig, kan opprette jobber og oppdatere jobbene som de har opprettet tidligere. Ansettelsesansvarlige kan bare utføre et begrenset sett med handlinger i en jobb og på søknadene som er knyttet til jobben. Bare brukere som er tilordnet rollen som ansettelsesansvarlig, kan legges til et ansettelsesteam som ansettelsesansvarlige.

## <a name="recruiter-role"></a>Rekruttererrollen

Brukere som er tilordnet rekruttererrollen, har fulle lese-, opprettelses-, oppdaterings- og sletterettigheter til jobbene de har opprettet. De har også fulle opprettings-, lese-, oppdaterings- og sletterettigheter til søknadene som er knyttet til jobbene de eier. Bare brukere som er tilordnet rollen som rekrutterer, kan legges til et ansettelsesteam som rekrutterere.

## <a name="interviewer"></a>Intervjuer

Alle brukere som har Microsoft Azure Active Directory (Azure AD) i organisasjonen, kan legges til et ansettelsesteam som intervjuer. Brukere som er tilordnet rollen som intervjuer, kan vise jobbdetaljene og søkerdata for jobber som de er i ansettelsesteamet for. For disse jobbene kan intervjuere også foreta anbefalinger for ansettelse og gi tilbakemelding om kandidatene. De kan imidlertid ikke oppdatere jobbdetaljer eller søkerdata.

## <a name="read-only"></a>Skrivebeskyttet

Brukere som er tilordnet rollen Skrivebeskyttet, har lesetilgang til alle dataene i Attract-miljøet. De kan imidlertid ikke opprette eller redigere data.

## <a name="find-out-which-roles-you-have"></a>Finne ut hvilke roller du har

1.  I Attract klikker du et spørsmålstegn (**?**) i øvre høyre hjørne på siden.

2.  Klikk **Om**.

    Du vil se hvilke roller du har for Attract i vinduet som vises:

    ![Vise Attract-lisenstype](media/attract-license-types.png)
    
## <a name="delegated-roles"></a>Delegerte roller

For hver jobb de er på i ansettelsesteamet, kan rekrutterere og ansettelsesansvarlige angi én eller flere representanter for seg selv. Men de kan ikke angi representanter for andre på ansettelsesteamet.

Representanter har de samme rettighetene som personen som tilordnet dem. Hvis for eksempel en ansettelsesansvarlig angir en representant for seg selv for en jobb, vil representanten få de samme rettighetene som ansettelsesansvarlig for denne jobben. Representanter kan ikke fjerne andre representanter fra ansettelsesteamet. De kan også fjerne folk som tilordnet dem som representanter.

## <a name="job-details-and-actions"></a>Jobbdetaljer og handlinger

Brukere som har rollen som rekrutterer eller ansettelsesansvarlig, kan opprette jobber. Følgende rettigheter gjelder jobbdetaljene og handlingene som kan utføres på jobber.

| Data eller handling    | Rekrutterer | Ansettelsesansvarlig | Intervjuer |
|-------------------|-----------|----------------|-------------|
| Stillingsdetaljer       | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Skrivebeskyttet |
| Ansettelsesteam       | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Skrivebeskyttet |
| Jobbpostering       | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Skrivebeskyttet | Skrivebeskyttet |
| Prosess           | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Skrivebeskyttet |
| Legge til søkere    | Legge til søkere til jobber som brukeren er i ansettelsesteamet for | Legge til søkere til jobber som brukeren er i ansettelsesteamet for | Ikke tillatt |
| Legge til jobbkandidater     | Legge til jobbkandidater som brukeren er i ansettelsesteamet for | Et konfigurasjonsalternativ i [aktivitetsoppsett for jobbkandidat](./activities-attract.md#prospect-activity) styrer om intervjuere kan legge til og vise jobbkandidater. | Ikke tillatt |
| Aktivere jobb      | Aktivere jobber som brukeren er i ansettelsesteamet for | Aktivere jobber som brukeren er i ansettelsesteamet for | Ikke tillatt |
| Lukk jobb         | Lukke jobber som brukeren er i ansettelsesteamet for | Ikke tillatt | Ikke tillatt |
| Slett jobb        | Slette jobber som brukeren er i ansettelsesteamet for | Bare hvis ingen søkere er lagt til jobben | Ikke tillatt |
| Slett søkere | Slette søkere hvis brukeren er i ansettelsesteamet | Ikke tillatt | Ikke tillatt |

## <a name="application-details-and-actions"></a>Søknadsdetaljer og handlinger

Følgende rettigheter gjelder jobbspesifikke data for søkere og handlingene som kan utføres på søknader.

| Data eller handling          | Rekrutterer | Ansettelsesansvarlig | Intervjuer |
|-------------------------|-----------|----------------|-------------|
| Søknadsdokumenter   | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Skrivebeskyttet |
| Søknadsmerknader       | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Opprette, lese, oppdatere og slette for jobber som brukeren er i ansettelsesteamet for | Skrivebeskyttet|
| Søknadsaktivitet    | Vis hvis brukeren er i ansettelsesteamet | Vis hvis brukeren er i ansettelsesteamet | Skrivebeskyttet |
| Tilbakemelding på søknad    | Legge til og vise alle tilbakemeldinger hvis brukeren er på ansettelsesteamet | Legge til og vise alle tilbakemeldinger hvis brukeren er på ansettelsesteamet | Kan legge til tilbakemelding\*\* |
| Avvise søknad      | Kan avvise hvis brukeren er på ansettelsesteamet | Ikke tillatt | Ikke tillatt |
| Avanser stadium           | Kan avvise hvis brukeren er på ansettelsesteamet | Kan avansere hvis brukeren er på ansettelsesteamet | Ikke tillatt |
| Starte tilbudsbehandling | Kan starte tilbudsbehandling | Det er et konfigurasjonsalternativ i tilbudsaktiviteten. | Ikke tillatt |


\*\* Et konfigurasjonsalternativ i [tilbakemeldingsaktivitetoppsettet](./activities-attract.md) styrer om intervjuere kan se hverandres tilbakemelding.


## <a name="process-templates"></a>Prosessmaler

Følgende rettigheter gjelder ansettelsesprosessmaler. Muligheten for teammedlemmer å opprette og redigere maler, konfigureres i **Malbehandling** i administrasjonssenteret. Hvis malbehandling er aktivert, kan rekrutterere og ansettelsesansvarlige opprette og redigere sine egne behandlingsmaler. Hvis malbehandling er deaktivert, kan bare administratorer opprette og redigere prosessmaler. Tabellen nedenfor forutsetter at malbehandling er aktivert.

| Data              | Rekrutterer                                           | Ansettelsesansvarlig                                      | Intervjuer |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Prosessmaler | Fulle rettigheter til malene som brukeren oppretter | Fulle rettigheter til malene som brukeren oppretter | Ingen tilgang   |

## <a name="email-and-email-templates"></a>E-post og e-postmaler

Følgende rettigheter gjelder e-postmaler og handlingene som kan utføres på e-postene. Bare administratorer kan opprette og redigere e-postmaler.

| Data eller handling     | Rekrutterer          | Ansettelsesansvarlig     | Intervjuer |
|--------------------|--------------------|--------------------|-------------|
| E-postmaler    | Lesetilgang   | Lesetilgang   | Ingen tilgang   |
| Send e-post         | Sende per aktivitet  | Sende per aktivitet  | Ingen tilgang   |
| Redigere e-postinnhold | Redigere e-postinnhold | Redigere e-postinnhold | Ingen tilgang   |

## <a name="talent-pools"></a>Talentsamlinger

Følgende rettigheter gjelder talentsamlinger. Talentsamlinger er bare synlige for personen som opprettet dem, med mindre den personen velger å dele dem. Kandidatsøk kan brukes til å søke etter kandidater som ikke er lagt til i en navngitt samling.

| Data eller handling   | Rekrutterer                                       | Ansettelsesansvarlig                                  | Intervjuer |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Navngitt samling       | Fulle rettigheter til samlinger som brukeren oppretter | Fulle rettigheter til samlinger som brukeren oppretter | Ingen tilgang   |
| Dele samling       | Bare samlinger som brukeren oppretter                | Bare samlinger som brukeren oppretter                | Ingen tilgang   |
| Kandidatsøk | Fulle søkefunksjoner                        | Fulle søkefunksjoner                        | Ingen tilgang   |

## <a name="candidates"></a>Kandidater

Kandidater er personer som er lagt til i en talentsamling, men som ikke er knyttet til en jobb.

| Data                        | Rekrutterer                        | Ansettelsesansvarlig                   | Intervjuer |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Profil – kandidatdetaljer | Opprette, lese, oppdatere og slette | Opprette, lese, oppdatere og slette | Ingen tilgang   |
| Dokumenter                   | Opprette, lese, oppdatere og slette | Opprette, lese, oppdatere og slette | Ingen tilgang   |


[!INCLUDE[footer-include](../includes/footer-banner.md)]