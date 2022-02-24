---
title: Konfigurere Human Resources-parametere
description: Innstillingene for noen Human Resources-parametere deles mellom firmaer, mens innstillingene for andre parametere er firmaspesifikke. Denne artikkelen forklarer hvordan du konfigurerer firmaspesifikke Personale-parametere.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bac50c5f302797e28df2bc792893c8a682899a93
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419837"
---
# <a name="configure-human-resources-parameters"></a>Konfigurere Human Resources-parametere

Innstillingene for noen parametere for Personale deles mellom firmaer, mens innstillingene for andre parametere er firmaspesifikke. Denne artikkelen forklarer hvordan du konfigurerer firmaspesifikke Personale-parametere.

To sider brukes til å angi Personale-parametere. For parametere som deles på tvers av firmaer, bruker du siden **Delte parametere for personaladministrasjon**. For parameterne som er firmaspesifikke (altså innstillingene gjelder ett enkelt firma), bruker du siden **Personalparametere**. På siden **Personalparametere** er innstillingene delt inn i seks kategorier:

-   Generelt
-   Rekruttering - dette er ikke inkludert i Dynamics 365 Human Resources
-   Kompensasjon
-   Nummerserier
-   Sykemelding og permisjon (FMLA)
-   Ansattselvbetjening

Hver kategori inneholder informasjon som gjelder ett enkelt firma. Innstillingene i kategorien **Generelt** definerer utseendet til informasjon om fravær, skade og sykdom og nye ansettelser. Innstillingene i denne kategorien definerer også noen standardoppføringer som vises når du arbeider. Denne kategorien lar deg spesifikt velge fargen som skal brukes på åpne fraværstransaksjoner, angi stilarket som skal brukes på rapporter, aktivere integrering mellom opplæringskurs og fraværsregistrering og velge hvilken fraværskode som skal brukes til å styre denne integreringen. Du kan også angi hvor lenge sakstilfeller for skade og sykdom skal beholdes, og angi standard ID-nummeret som vises når en ny arbeider ansettes. 

Innstillingene i kategorien **Rekruttering** definerer dokumenttypene som skal brukes korrespondanse som sendes automatisk til søkerne, og rekrutteringsprosjektet som skal brukes for uanmodede søknader (søknader som ikke er for et bestemt rekrutteringsprosjekt). Perioden som er definert for aldersfordeling for rekrutteringsprosjekt bestemmer Rekrutteringsprosjektene som er inkludert i flisen **Aldersfordelingsprosjekter** i arbeidsområdet **Rekrutteringsstyring** . Perioden som er definert for advarselen for tidsfrist for søknad brukes til å vise rekrutteringsprosjekter som nærmer seg sin Søknadsfrist på flisen **Søknadsfristen nærmer seg** i arbeidsområdet **Rekruttering**. 

Innstillingene i kategorien **Kompensasjon** definerer om brukere må bekrefte at de vil lagre informasjon for en fast eller variabel kompensasjonsplan. Hvis du merker av for **Aktiver lagring av validering**, mottar brukere en melding som spør om de vil lagre posten hver gang de lukker en kompensasjonsrelatert side. Noen av sidene i kompensasjonsstyring lar ikke brukere slette informasjon. Derfor ved å be brukerne bekrefte at de vil lagre informasjon, kan du kunne begrense mengden av informasjon som lagres, men som ikke kan slettes senere. Hvis det ikke er merket av for **Aktiver lagring av validering**, lagres alltid poster umiddelbart, muligens før brukeren er klar. Hvis du bruker ytelsesstyring, lar kategorien **Kompensasjon** deg også velge en vurderingsmodell å bruke i stedet for modellen som er tilordnet til kompensasjonsplaner når ytelse rangeres. 

### <a name="previously-released-functionality"></a>Tidligere utgitt funksjonalitet

Innstillingene i kategorien **Nummerserie** bestemmer sekvensene som brukes til å automatisk tilordne ID-er til varer i Personale, for eksempel søknader, fraværsregistreringer, kompensasjonsprosessresultatene, saksnumre, kurs og kursagendaer. Hvis du vil beholde nummerseriereferanser og -koder, kan du bruke listesiden **Nummerserier** (klikk på **Organisasjonsstyring** &gt; **Nummerserier** &gt; **Nummerserier**).

> [!NOTE]
> Antall timer arbeidet kan ikke overskride 1250, og lengden på ansettelse kan ikke overskride 12 måneder. Disse maksimumsverdier er i overensstemmelse med gjeldende lovgivning i USA. Til slutt bestemmer innstillingene i kategorien **Ansattselvbetjening** opplysningene som ledere kan angi på vegne av de ansatte.
