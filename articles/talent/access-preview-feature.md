---
title: Tilgang til forhåndsvisningsfunksjoner i Microsoft Dynamics 365 Talent
description: Dette emnet beskriver hvordan en administrator kan aktivere forhåndsvisningsfunksjonene i Microsoft Dynamics 365 Talent, og det viser hvilke funksjoner som er aktivert for forhåndsvisning.
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 0f9a83aeea3942d3c56d32956f79490c91565e9e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551613"
---
# <a name="access-preview-features-in-microsoft-dynamics-365-talent"></a>Tilgang til forhåndsvisningsfunksjoner i Microsoft Dynamics 365 Talent

[!include[banner](../includes/banner.md)]

Som en del av vår kontinuerlige distribusjonen av funksjonalitet for administrasjon av menneskelig kapital (HCM) for Microsoft Dynamics 365 Talent vil vi at kunder får nye funksjoner så snart som mulig. Administratorer kan se og bruke forhåndsvisning av funksjoner i miljøet. Disse funksjonene er nesten klar for generelle tilgjengeligheten og har gjennomgått omfattende testing. Vi er bare ute etter en endelig runde med tilbakemelding og godkjenning før vi gjør dem generelt tilgjengelige.

Dette emnet beskriver hvordan du kan aktivere forhåndsvisningsfunksjonene, og det viser hvilke funksjoner som er tilgjengelige for forhåndsvisning. Denne listen oppdateres etter funksjoner som er frigitt til generelle tilgjengeligheten og nye funksjoner som utgis for å forhåndsvise. Det gis ingen varsling når nye funksjoner er frigitt til å forhåndsvise. Brukere starter bare for å se funksjonene. Hvis du vil ha mer informasjon om nye funksjoner i Talent, kan du se [Hva er nytt eller endret i Dynamics 365 Talent](./whats-new.md) og [Produktmerknader for Dynamics 365 og Power Platform](https://docs.microsoft.com/business-applications-release-notes).

## <a name="enable-or-disable-preview-features"></a>Aktivere eller deaktivere forhåndsvisning av funksjoner

Hvis du vil ha tilgang til forhåndsvisningsfunksjoner, må du først aktivere dem i miljøet ditt. Aktivering eller deaktivering av forhåndsvisningsfunksjoner er miljøspesifikt.

> [!IMPORTANT]
> Når du aktiverer innstillingen **Forhåndsvisningsfunksjoner**, aktiverer du forhåndsvisningsfunksjoner for alle brukere i organisasjonen som er i miljøet. Når du deaktiverer innstillingen, kan du deaktivere forhåndsvisningsfunksjoner og gjøre dem utilgjengelig for brukerne. Forhåndsvisningsfunksjoner har begrenset støtte i Talent. Du kan bruke færre personvern- og sikkerhetstiltak, og de er ikke inkludert i Talent-servicenivåavtalen (SLA). Du bør ikke bruke forhåndsvisningsfunksjoner til å behandle personlige data (det vil si all informasjon som kan identifisere deg), eller til å behandle andre data som er gjenstand for juridiske eller samsvarskrav.

### <a name="attract"></a>Attract

1. Logg på Microsoft Dynamics 365 Talent: Attract.
2. På **Oppsett**-menyen (tannhjulssymbolet) i øvre høyre hjørne, velg **Administrasjonssenter**.
3. På fanen **Funksjonsbehandling** velger du alternativet ved siden av **Forhåndsvisningsfunksjoner**, slik at det blir blått og viser **På**.

    ![Aktivere forhåndsvisningsfunksjoner i Attract](./media/attract-enable-preview-features.png)

4. Velg eller avbryt valget av individuelle forhåndsvisningsfunksjoner. Hvis du ikke gjør noe, aktiveres alle tilgjengelige forhåndsvisningsfunksjoner.
5. Oppdater nettleseren for å begynne å se de nye funksjonene. Alle brukere som allerede er pålogget, ser funksjonene neste gang de logger på, eller de kan oppdatere nettleseren for å vise funksjonene umiddelbart.

> [!NOTE]
> Noen forhåndsvisningsfunksjoner kan kreve ekstra konfigurasjon. Følg koblingene ved siden av forhåndsvisningsfunksjonen for å fullføre oppsettet av den.

### <a name="core-hr"></a>Kjerne-HR

1. Logg på Talent.
2. Velg **Systemadministrasjon**, og velg deretter kategorien **Koblinger**.
3. På siden **Systemadministrasjon**, under **Oppsett**, velger du **Systemparametere**.
4. På siden **Systemparameterere** velger du kategorien **Forhåndsvisningsfunksjoner**.
5. Sett alternativet **Aktiver forhåndsvisningsmodus for alle brukere** til **Ja** for å gjøre forhåndsvisningsfunksjoner tilgjengelige.

    ![Aktivere forhåndsvisningsfunksjoner i Core HR](./media/corehr-enable-preview-features.png)

> [!NOTE]
> Følg den samme fremgangsmåten for å deaktivere forhåndsvisningsfunksjoner, men sett alternativet **Aktiver forhåndsvisningsmodus for alle brukere** til **Nei**. Når du deaktiverer forhåndsvisningsfunksjoner, blir de utilgjengelige for brukerne, og det kan oppstå feil i prosesser som er knyttet til funksjonene.

### <a name="onboard"></a>Jobbintroduksjon

Ingen forhåndsvisningsfunksjoner er tilgjengelige for Microsoft Dynamics 365 Talent: Onboard.

## <a name="features-that-are-currently-in-preview"></a>Funksjoner som for øyeblikket forhåndsvises

### <a name="attract"></a>Attract

- [Kandidatanbefaling](./intelligent-recommendations.md#candidate-recommendations) – Hvis mer enn ti kandidater har CV-er eller fullstendige profiler, vises kandidatene som oppfyller jobbkravene best, i delen **Søkere som bør vurderes** på jobbsiden.
- [Jobbanbefaling](./intelligent-recommendations.md#job-recommendations) – Hvis mer enn ti jobber er lagt inn på ditt karriereområde, gir Attract jobbanbefalinger til kandidater.
- [Broadbean-integrering](./posting-jobs-external.md#post-jobs-to-broadbean) – Du kan postere jobber fra Attract til Broadbean, et eksternt jobbposteringsområde. Når du har aktivert denne forhåndsvisningsfunksjonen, må du fullføre installasjonen ved å skrive inn Broadbean-brukernavn, klient-ID og krypteringstoken.
- [Analyse](./analytic-reports.md) – I Analysehub kan ansettelsesteam vise viktige mål for én enkelt jobb, i tillegg til aggregerte mål for alle jobber.
- [EEO](./activities-attract.md) – Nye aktivitetstyper lar deg bruke et forhåndsdefinert skjema til å samle inn EEO- og OFCCP-data fra en kandidat. Det forhåndsdefinerte skjemaet kan ikke redigeres.
- [Kandidatanbefalinger](./intelligent-recommendations.md#prospect-recommendations) – Attract gjennomgår tidligere søkere og gjeldende kandidater for å vise en liste over kandidater som stemmer overens med jobben din.
- [Relevanssøk](./attract-talent-pools.md#search-and-view-candidate-profiles) – Du kan søke i hele kandidatdatabasen etter bestemte ferdigheter, navn eller utdannelsesbakgrunner. Attract søker i hele profilen og uthever alle treff som blir funnet. Attract søker også i alle dokumenter som er tilgjengelige for en kandidat, og rangerer søkeresultatene på en intelligent måte.
- [Aktivitetsmålgruppe](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – Du kan angi målgruppen for aktiviteter (for eksempel intervju, tidsplan eller tilbakemelding) til **Alle kandidater**, **Interne kandidater** eller **Eksterne kandidater**. Du kan levere kundeaktiviteter, for eksempel YouTube-videoer, webinnhold og Microsoft Forms, til alle kandidater, bare interne kandidater, bare eksterne kandidater eller ansettelsesteamet.
- [Bruk med LinkedIn](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – Du kan angi et alternativ på Attract-karriereområdet for å la jobbkandidater søke ved hjelp av LinkedIn. Denne funksjonen effektiviserer søknadsprosessen for kandidater ved å la dem bruke sin LinkedIn-profil til automatisk å fylle ut søknadene på ditt karriereområde.
- [Sporing av kilde](./source-tracking.md) – Attract sporer kilden til kandidatsøknader for å gi verdifull informasjon som kan hjelpe deg med å identifisere rekrutteringstiltaket. Du kan også velge en søknadskilde når du legger til en kandidat til en jobb- eller talentsamling.
- [Innstilt som nummer to](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – Hvis noen kandidater passer bra i organisasjonen din, men ikke ble tilbudt den gjeldende stillingen, kan du angi dem som nummer to. Denne funksjonen bidrar til å redusere ansettelsestiden neste gang du har en lignende stilling tilgjengelig.

### <a name="core-hr"></a>Kjerne-HR

- [Valider stillingshierarki](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – Du kan validere lederhierarkiet for alle sirkelreferanser som ved en feiltakelse ble importert.
- [Angi årsakskoder for permisjonstyper](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – Du kan angi årsakskoder for permisjonstyper.
- [Kreve årsakskoder for fritidsforespørsler](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – I tillegg til å angi årsakskoder for permisjonstyper kan du kreve årsakskoder for fritidsforespørsler.
- [Angi en transaksjonsliste for permisjon og fravær for HR](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – Du kan vise en liste over permisjons- og fraværstransaksjoner for å gi innsikt i avspaseringssaldoer.

### <a name="onboard"></a>Jobbintroduksjon

Ingen forhåndsvisningsfunksjoner er tilgjengelige for Onboard.

## <a name="feedback"></a>Tilbakemelding

Vi hører gjerne fra deg om din erfaring med noen av disse forhåndsvisningsfunksjonene. Vi oppfordrer deg til å postere regelmessig tilbakemelding på følgende områder når du bruker denne eller andre funksjoner:

- [Fellesskap](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – dette området er en flott ressurs der brukere kan diskutere brukstilfeller, spørsmål og få hjelp til fellesskapet.
- Gi oss beskjed om funksjoner du vil se i produktet, eller si fra om eventuelle endringer du mener vi bør gjøre i eksisterende funksjoner. Foreslå produktideer på følgende områder:

    - [Attract-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Onboard-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

Sørg for at du ikke tar med personlige data (informasjon som kan identifisere deg) i tilbakemeldingene eller innsendingene av produktgjennomgang. Innsamlet informasjon kan analyseres ytterligere, og den brukes ikke til å svare på forespørsler under gjeldende personvernlover. Personopplysninger som samles inn separat under disse programmene, er underlagt [Microsofts personvernerklæring](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Bokmerk dette emnet, og kom deretter tilbake ofte for å holde deg oppdatert om nye forhåndsvisningsfunksjoner etter hvert som vi gir dem ut.

## <a name="see-also"></a>Se også

- [Prøv eller kjøp Talent-apper](https://dynamics.microsoft.com/talent/overview/)
- [Nyheter](./whats-new.md)
- [Produktmerknader](https://docs.microsoft.com/business-applications-release-notes/index)
- [Få kundestøtte for Talent](./talent-support.md)
