---
title: Definere firmaspesifikke parametere for Personale
description: Innstillingene for noen parametere for Personale deles mellom firmaer, mens innstillingene for andre parametere er firmaspesifikke. Denne artikkelen forklarer hvordan du konfigurerer firmaspesifikke Personale-parametere.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: b4c362ecb6134158cb9f00d3670232043c7d619d
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-company-specific-hr-parameters"></a>Definere firmaspesifikke parametere for Personale

[!include[banner](includes/banner.md)]


Innstillingene for noen parametere for Personale deles mellom firmaer, mens innstillingene for andre parametere er firmaspesifikke. Denne artikkelen forklarer hvordan du konfigurerer firmaspesifikke Personale-parametere.

To sider brukes til å angi Personale-parametere. For parametere som deles på tvers av firmaer, bruker du siden **Delte parametere for personaladministrasjon**. For parameterne som er firmaspesifikke (altså innstillingene gjelder ett enkelt firma), bruker du siden **Personalparametere**. På siden **Personalparametere** er innstillingene delt inn i seks kategorier:

-   Generelt
-   Rekruttering
-   Kompensasjon
-   Nummerserier
-   Sykemelding og permisjon (FMLA)
-   Ansattselvbetjening

Hver kategori inneholder informasjon som gjelder ett enkelt firma. Innstillingene i kategorien **Generelt** definerer utseendet til informasjon om fravær, skade og sykdom og nye ansettelser. Innstillingene i denne kategorien definerer også noen standardoppføringer som vises når du arbeider. Denne kategorien lar deg spesifikt velge fargen som skal brukes på åpne fraværstransaksjoner, angi stilarket som skal brukes på rapporter, aktivere integrering mellom opplæringskurs og fraværsregistrering og velge hvilken fraværskode som skal brukes til å styre denne integreringen. Du kan også angi hvor lenge sakstilfeller for skade og sykdom skal beholdes, og angi standard ID-nummeret som vises når en ny arbeider ansettes. 

Innstillingene i kategorien **Rekruttering** definerer dokumenttypene som skal brukes korrespondanse som sendes automatisk til søkerne, og rekrutteringsprosjektet som skal brukes for uanmodede søknader (søknader som ikke er for et bestemt rekrutteringsprosjekt). Perioden som er definert for aldersfordeling for rekrutteringsprosjekt bestemmer Rekrutteringsprosjektene som er inkludert i flisen **Aldersfordelingsprosjekter** i arbeidsområdet **Rekrutteringsstyring** . Perioden som er definert for advarselen for tidsfrist for søknad brukes til å vise rekrutteringsprosjekter som nærmer seg sin Søknadsfrist på flisen **Søknadsfristen nærmer seg** i arbeidsområdet **Rekruttering**. 

Innstillingene i kategorien **Kompensasjon** definerer om brukere må bekrefte at de vil lagre informasjon for en fast eller variabel kompensasjonsplan. Hvis du merker av for **Aktiver lagring av validering**, mottar brukere en melding som spør om de vil lagre posten hver gang de lukker en kompensasjonsrelatert side. Noen av sidene i kompensasjonsstyring lar ikke brukere slette informasjon. Derfor ved å be brukerne bekrefte at de vil lagre informasjon, kan du kunne begrense mengden av informasjon som lagres, men som ikke kan slettes senere. Hvis det ikke er merket av for **Aktiver lagring av validering**, lagres alltid poster umiddelbart, muligens før brukeren er klar. Hvis du bruker ytelsesstyring, lar kategorien **Kompensasjon** deg også velge en vurderingsmodell å bruke i stedet for modellen som er tilordnet til kompensasjonsplaner når ytelse rangeres. 

Innstillingene i kategorien **Nummerserie** bestemmer sekvensene som brukes til å automatisk tilordne ID-er til varer i Personale, for eksempel søknader, fraværsregistreringer, kompensasjonsprosessresultatene, saksnumre, kurs og kursagendaer. Hvis du vil beholde nummerseriereferanser og -koder, kan du bruke listesiden **Nummerserier** (klikk på **Organisasjonsstyring** &gt; **Nummerserier** &gt; **Nummerserier**). 

Innstillingene i kategorien **FMLA** definerer hvor mange timer en ansatt må arbeide for å være kvalifisert for FMLA-fordeler, lengden på ansettelse som er nødvendig for berettigelse, og ansettelsesforholdets startdato som brukes til å fastslå lengden på ansettelse. Innstillingene definerer også antallet FMLA-timer som ansatte er berettiget til og FMLA-kalenderen som brukes til å beregne hvor mange FMLA-timer ansatte har brukt. Kategorien **FMLA** er bare tilgjengelig for firmaer i USA. 

**Obs!** Antall timer arbeidet kan ikke overskride 1 250, og lengden på ansettelse kan ikke overskride 12 måneder. Disse maksimumsverdier er i overensstemmelse med gjeldende lovgivning i USA. Til slutt bestemmer innstillingene i kategorien **Ansattselvbetjening** opplysningene som en leder kan angi på vegne av hans eller hennes ansatte.

<a name="see-also"></a>Se også
--------

[Definere parametere for Personale på tvers av juridiske enheter](set-up-hr-parameters-across-legal-entities.md)




