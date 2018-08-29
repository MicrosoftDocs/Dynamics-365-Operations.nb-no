---
title: "Tilgang til forhåndsvisningsfunksjoner i Talent"
description: "Dette emnet beskriver hvordan en administrator kan aktivere forhåndsvisningsfunksjonene, og det viser hvilke funksjoner som er aktivert for forhåndsvisning."
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: eb99f169ada2a227ebe8e64ee56bbb38cdfda4e0
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="access-preview-features-in-talent"></a>Tilgang til forhåndsvisningsfunksjoner i Talent

[!include[banner](../includes/banner.md)]

Som en del av vår kontinuerlige distribusjonen av produktet vil vi at kunder får nye funksjoner så snart som mulig. Administratorer kan se og bruke forhåndsvisning av funksjoner i miljøet. Disse funksjonene er nesten klar for generelle tilgjengeligheten og har gjennomgått omfattende testing. Vi er bare ute etter en endelig runde med tilbakemelding og godkjenning før vi vanligvis gir dem ut.

Dette emnet beskriver hvordan en administrator kan aktivere forhåndsvisningsfunksjonene, og det viser hvilke funksjoner som er tilgjengelige for forhåndsvisning. Denne listen oppdateres etter funksjoner som er frigitt til generelle tilgjengeligheten og nye funksjoner som utgis for å forhåndsvise. Det gis ingen varsling når nye funksjoner er frigitt til å forhåndsvise. Brukere starter bare for å se funksjonene.

## <a name="enable-or-disable-preview-features"></a>Aktivere eller deaktivere forhåndsvisning av funksjoner

Du kan bruke innstillingen **Forhåndsvisningsfunksjoner** i Microsoft Dynamics 365 for Talent-administrasjonssenteret til å aktivere eller deaktivere forhåndsvisningsfunksjoner. Innstillingen er deaktivert som standard. Handlingen for å aktivere eller deaktivere forhåndsvisningsfunksjoner er miljøspesifikk.

> [!IMPORTANT]
> Ved å aktivere innstillingen **Forhåndsvisningsfunksjoner** aktiverer du forhåndsvisningsfunksjoner for alle brukere i organisasjonen som er i miljøet. Ved å deaktivere innstillingen kan du deaktivere forhåndsvisningsfunksjoner og gjøre dem utilgjengelig for brukerne. Forhåndsvisningsfunksjoner har begrenset støtte i Talent. Du kan bruke færre personverns- og sikkerhetstiltak, og de ikke er inkludert i Talent-servicenivåavtalen. Du bør ikke bruke forhåndsvisningsfunksjoner til å behandle personlige data (det vil si all informasjon som kan identifisere deg), eller til å behandle andre data som er gjenstand for juridiske eller samsvarskrav.

### <a name="enable-or-disable-preview-features-for-your-organization"></a>Aktivere eller deaktivere forhåndsvisningsfunksjoner

#### <a name="attract"></a>Attract

1. Logg på Microsoft Dynamics 365 for Talent: Attract.
2. På **Oppsett**-menyen (tannhjulssymbolet) i øvre høyre hjørne, velg **Administrasjonsinnstillinger**.
3. På fanen **Funksjonsbehandling** velger du alternativet ved siden av **Forhåndsvisningsfunksjoner**, slik at det blir blått.
4. Oppdater nettleseren for å begynne å se de nye funksjonene. (Alle brukere som allerede er pålogget, ser funksjonene neste gang de logger på, eller de kan oppdatere nettleseren for å vise funksjonene umiddelbart.)

#### <a name="core-hr"></a>Kjerne-HR

1. Logg på Talent. Arbeidsområdet for kjerne-HR åpnes, som du vil fullføre resten av trinnene fra. 
2. Velg **Systemadministrasjon \> Koblinger > Systemparametere**.
3. På siden **Systemparametere** på fanen **Forhåndsvisningsfunksjoner** angir du **Aktiver forhåndsvisningsmodus for alle brukere** til **Ja** for å gjøre forhåndsvisningsfunksjoner tilgjengelig.

> [!NOTE]
> Hvis du vil deaktivere forhåndsvisningsfunksjoner, kan du bruke de samme grunnleggende trinnene. Når du deaktiverer forhåndsvisningsfunksjoner, blir de utilgjengelige for brukerne, og det kan oppstå feil i prosesser som er knyttet til funksjonene.

## <a name="features-that-are-currently-in-preview"></a>Funksjoner som for øyeblikket forhåndsvises

### <a name="attract"></a>Attract

- **Jobbmaler** – nå kan du opprette maler for ansettelsesprosessen. Brukere kan allerede tilpasse ansettelsesprosessen for en bestemt jobb. De kan imidlertid nå opprette maler for prosessen og deretter velge ønsket mal når det opprettes en bestemt jobb. Denne funksjonen kan derfor strømlinjeforme oppsettsprosessen for jobben.
- **Karriereområde** – den gjeldende versjonen av karriereområdet viser bare alle åpne jobber. Imidlertid legges flere funksjoner til på området i fremtiden. Jobber kan merkes som enten interne eller eksterne. Interne brukere som logger på området, ser både interne jobber og eksterne jobber. Eksterne brukere og brukere som ikke er logget på, vil imidlertid bare se eksterne jobber.
- **Jobbpostering** – du kan nå postere jobber til karriereområdet.
- **LinkedIn-jobbpostering** – du kan nå postere jobber til LinkedIn.

    > [!NOTE]
    > Jobber som er postert, er synlig bare for kunder som abonnerer på ett eller flere LinkedIn-jobboversiktsprodukter. Ellers ser kunder en jobb bare hvis de eksplisitt søker etter den. Det er en forsinkelse for når jobber posteres til LinkedIn. En jobb kan ta flere timer å vises etter at den er postert fra Attract.

- **Kandidatsøknad** – både interne og eksterne kandidater kan nå søke direkte fra jobbsiden på karriereområdet.
- **Tilbudsbehandling** – brukere kan nå opprette tilbudsbrev fra maler som inneholder plassholdere. Etter hvert som kandidater går videre til tilbudstrinnet, kan rekrutteringspersoner og ansettelsesledere bruke tilbudsverktøyet til å klargjøre en kandidats formelle tilbud via maler, sende tilbudet til intern godkjenning og til slutt sende tilbudet til kandidaten for signatur. Mange nye funksjoner vil bli lagt til i tilbudsverktøyet over tid, og forhåndsvisningsfunksjonen oppdateres med disse funksjonene når vi er klar til å frigi dem for forhåndsvisning.

### <a name="core-hr"></a>Kjerne-HR

- **Åpen registrering** – åpen registrering gir ansatte en enkel, selvbetjent opplevelse for å velge fordeler. HR-administratorer kan konfigurere den åpne registreringsprosessen for fordeler for organisasjonen, og registreringsopplevelsen for ansatte, ved hjelp av en løsning med veiledning som er enkel å følge.

## <a name="feedback"></a>Tilbakemelding

Uansett om tilbakemelding er positiv eller negativ, vil vi gjerne høre fra deg om din bruk av forhåndsvisningsfunksjonene. Vi oppfordrer deg til å postere regelmessig tilbakemelding på følgende områder når du bruker denne eller andre funksjoner.

- [Fellesskap](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – dette området er en flott ressurs der brukere kan diskutere brukstilfeller, spørsmål og få hjelp til fellesskapet.
- Bruk følgende områder til å foreslå produktideer. Gi oss beskjed om funksjoner som du vil se i produktet, og også endringer som du mener bør innføres i eksisterende funksjoner.

    - [Innhente ideer](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Kjerne-HR](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

Ikke ta med personlige data (informasjon som kan identifisere deg) i tilbakemeldingene eller innsendingene av produktgjennomgang. Informasjon som samles inn, kan analyseres ytterligere, og den brukes ikke til å svare på forespørsler under gjeldende personvernlover. Personopplysninger som samles inn separat under disse programmene, er underlagt [Microsofts personvernerklæring](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Bokmerk dette emnet, og kom deretter tilbake ofte for å holde deg oppdatert om nye forhåndsvisningsfunksjoner etter hvert som vi gir dem ut.

