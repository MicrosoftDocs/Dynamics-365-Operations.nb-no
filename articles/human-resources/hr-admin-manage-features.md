---
title: Behandle funksjoner
description: Lær hvordan du aktiverer eller deaktiverer nye funksjoner i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84ff11e8237ce0669f7f6ac70c5b4411c5d4b466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010041"
---
# <a name="manage-features"></a>Behandle funksjoner

Som en del av vår kontinuerlige distribusjonen av ny funksjonalitet for Microsoft Dynamics 365 Human Resources vil vi at kunder får nye funksjoner så snart som mulig. Vi tilbyr forhåndsversjon av funksjoner, som nesten er klar for generelle tilgjengeligheten og har gjennomgått omfattende testing. Vi er bare ute etter en endelig runde med tilbakemelding og godkjenning før vi gjør dem generelt tilgjengelige.

Hvis du vil ha mer informasjon om nye funksjoner i Human Resources, kan du se [Hva er nytt i Human Resources](hr-admin-whats-new.md) og [lanseringsplan for Dynamics 365 og Power Platform ](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

Arbeidsområdet **Funksjonsbehandling** inneholder en liste over funksjoner som leveres i hver utgivelse. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem. Hvis du vil ha mer informasjon om funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager. Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden. Så snart du ser nye funksjoner i arbeidsområdet for **funksjonsbehandling**, kan du aktivere dem. Det kan hende at noen funksjoner er aktivert som standard.

Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer. Arbeidsområdet for **funksjonsbehandling** angir når en forhåndsvisningsfunksjon blir obligatorisk. Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene. De kan ikke deaktivere obligatoriske funksjoner. Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.

## <a name="enable-or-disable-preview-features"></a>Aktivere eller deaktivere forhåndsvisning av funksjoner

Hvis du vil ha tilgang til forhåndsvisningsfunksjoner, må du først aktivere dem i miljøet ditt. Aktivering eller deaktivering av forhåndsvisningsfunksjoner er miljøspesifikt.

> [!IMPORTANT]
> Forhåndsvisningsfunksjoner er bare tilgjengelige i **Sandkasse**-miljøer. Når du aktiverer en forhåndsversjon av en funksjon, aktiverer du den for alle brukere i organisasjonen som er i miljøet. Når du slår av funksjonen, kan du deaktivere den og gjøre den utilgjengelig for brukerne. Forhåndsvisningsfunksjoner har begrenset støtte i Human Resources. Du kan bruke færre personvern- og sikkerhetstiltak, og de er ikke inkludert i Human Resources-servicenivåavtalen (SLA). Du bør ikke bruke forhåndsvisningsfunksjoner til å behandle personlige data (det vil si all informasjon som kan identifisere deg), eller til å behandle andre data som er gjenstand for juridiske eller samsvarskrav.

1. Velg **Systemadministrasjon**i Human Resources.

2. Velg flisen **Funksjonsbehandling**.

3. Hvis du vil aktivere en forhåndsversjon av en funksjon, velger du den fra listen og velger deretter **Aktiver**. Hvis du vil deaktivere en forhåndsversjon av en funksjon, velger du den fra listen og velger deretter **Deaktiver**.

## <a name="preview-feature-benefits-management"></a>Forhåndsversjon av funksjon: Fordelsbehandling

Med fordelsbehandling får du en fleksibel løsning som støtter et bredt utvalg av fordelsalternativer, sammen med en brukervennlig ansattopplevelse som viser tilbudene dine. Hvis du vil ha mer informasjon om konfigurasjon og bruk av Fordelsbehandling, kan du se [Oversikt over fordelsbehandling](hr-benefits-management-overview.md).

Fordelsbehandling erstatter funksjonalitet i arbeidsområdet **Fordeler**. Når du aktiverer forhåndsversjonen av funksjonen Fordelsbehandling, har du ikke lenger tilgang til følgende skjemaer i arbeidsområdet **Fordeler**:

- **Fordeler**
- **Fordelselementer**
- **Bidragsberegningssatser**
- **Resultater av fordelsregistrering**
- **Resultater for utløp og utvidelse av fordel**
- **Policyregeltyper for fordelsrettigheter**
- **Policyer for fordelsrettigheter**
- **Rettighetshendelser**

Du kan vise informasjonen i disse skjemaene i skrivebeskyttet modus. Hvis du vil redigere informasjonen, må du først deaktivere forhåndsversjonen av funksjonen for Fordelsbehandling.

### <a name="benefits-management-known-issues"></a>Kjente problemer med Fordelsbehandling

#### <a name="life-events"></a>Levetidshendelser

Ved behandling av levetidshendelser vil brukeren få en feilmelding:

Startdatoen for dekning må være mellom *begynnelsen av abonnementsperioden* og *slutten av abonnementsperioden*. 

Levetidshendelsen vil fortsette å bli behandlet som forventet.

#### <a name="eligibility-processing"></a>Rettighetsbehandling

Ved pågående rettighet for fordeler som bruker et dekningsbeløp av typen 1–5 ganger lønn, prosent av lønn og flatt beløp, må datoen for fordelsdetaljer settes til den ansattes startdato i **Ansettelseshistorikk**, med antall arbeids timer, betalingsfrekvens og årlig lønnsbeløp for fordeler. Hvis det finnes fast kompensasjon for arbeideren, angir du antall timer som er arbeidet sammen med betalingsfrekvensen, og det årlige lønnsbeløpet blir beregnet. Hvis den ansatte har fast lønn, er ikke arbeidstimene nødvendig. Det anbefales at du angir fast kompensasjon først når du oppretter nye arbeidere. Slik oppdaterer du posten med fordelsdetaljer: Gå til **Arbeider > Arbeiderlogg > Ansettelsesdetaljer**. Juster datoen til arbeiderens startdato.

#### <a name="employee-self-service"></a>Ansattselvbetjening

Ansatte kan velge en plan som de ikke er kvalifisert for, og sjekke denut. For eksempel: En arbeider har ingen underordnede, men kan velge en medisinsk plan med et familiedekningsalternativ.

Den ansattes beløp beregnes ikke ved oppdatering av dekningsbeløpet for livsforsikring. Når en ansatt for eksempel blir tilbudt en livsforsikringsplan, kan de velge opptil $50 000 i dekning med en kost på $0,36 per $1000 dekning.  Når den ansatte oppdaterer dekningsbeløpet, forblir den ansattes tilknyttede kostpris null.

For en fordelsplan som bare tillater ett valg av denne plantypen, vil brukeren få en feilmelding hvis de prøver å frafalle en plan etter å ha valgt en plan. En bruker velger for eksempel en medisinsk plan og setter den inn i handlekurven. Brukeren velger deretter **Frafall** for en annen medisinsk plan. Brukeren vil motta en feil.

## <a name="preview-features-in-leave-and-absence"></a>Forhåndsversjonsfunksjoner i Permisjon og fravær

Funksjoner for Permisjon og fravær inkluderer:

- **Permisjons- og fraværskalender** – Permisjons- og fraværsparametere flyttes fra **Personalparametere** til en ny skjerm kalt for **Permisjons- og fraværsparametere**. Den nye skjermen inneholder en ny **Kalender**-kategori. Denne forhåndsversjonen aktiverer bare et delsett av parameterne. Du får tilgang til den nye skjermen fra kategorien **Koblinger** i arbeidsområdet **Permisjon og fravær**. Kalenderne omfatter:
  - **Firmakalender** – viser alle fritidsforespørsler for ansatt. Personer med **Personal**-rollen kan få tilgang til denne kalenderen fra kategorien **Koblinger** i arbeidsområdet **Permisjon og fravær**.
  - **Kalender for lederteam** – viser alle fritidsforespørsler i direkterapporter. Ledere kan få tilgang til kalenderen fra kategorien **Mitt team** i Ansattselvbetjening under **Permisjon og fravær**. 

- **Feriekalendere i Permisjon og fravær** – Permisjonstyper inkluderer et nytt **Ferid**-alternativ, brukt i sammenheng med arbeidstidskalenderen. Dager som er definert av ferier og lukkinger, er nå angitt som **Ferie** når arbeidsdager genereres. Når avsetninger behandles, gjøres justeringer i ansatte som er tilordnet kalenderen, for å planlegge for helligdager som faller på arbeidsdager.

- **Revisjon av permisjonsavsetning** – En ny skjerm lar deg seg gjennom når avsetninger er behandlet og slettet, både av alle ansatte og enkeltansatte. Du får tilgang til denne nye skjermen fra kategorien **Koblinger** i arbeidsområdet **Permisjon og fravær**.

- **Sletting av permisjonsavsetning** – Du kan nå slette avsetningsposter for bestemte permisjonsplaner. Du får tilgang til dette nye alternativet fra kategorien **Koblinger** i arbeidsområdet **Permisjon og fravær**. For enkeltansatte vises dette alternativet i gruppen **Permisjon og fravær** i ansattprofilen. 

- **Avrunding for permisjonsavsetning** – Nye alternativer for **Permisjonstype** definerer hvilken type avrunding som avsetningen skal bruke, pluss desimalpresisjonen for avrundingen under avsetningsprosessen. Når avsetninger behandles, brukes avrundingen og presisjonen på avsetningspostene. 

- **Konfigurer flere permisjonstyper i en enkelt permisjonsplan** – En ny kolonne i tidsplanen for permisjonsavsetning lar deg definere flere permisjonstyper for en permisjons- og fraværsplan med forskjellige avsetningsplaner. Det forrige **Permisjonstype**-feltet er fjernet. I den ansattes registrering vises saldoene for permisjonstypene nå i en tabell i stedet for øverst på skjermen.

  > [!IMPORTANT]
  > Du kan ikke deaktivere denne funksjonen etter at du har aktivert den.

- **Bruk en ansatts fulltidsekvivalens (FTE) for avsetning** – En ny kolonne i tidsplanen for permisjonsavsetning tillater bruk av FTE for avsetning. Når avsetninger behandles, bruker programmet den ansattes primære stilling og FTE-en som er definert, til å bestemme avsetningsbeløpet som er fordelt.

  > [!NOTE]
  > Denne funksjonen er bare tilgjengelig hvis du aktiverer **Konfigurer flere permisjonstyper per permisjonsplan**. 

## <a name="feedback"></a>Tilbakemelding

Vi hører gjerne fra deg om din erfaring med forhåndsvisningsfunksjoner. Vi oppfordrer deg til å postere regelmessig tilbakemelding på følgende områder når du bruker denne eller andre funksjoner:

- [Fellesskap](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – dette området er en flott ressurs der brukere kan diskutere brukstilfeller, spørsmål og få hjelp til fellesskapet.
- Gi oss beskjed om funksjoner du vil se i produktet, eller si fra om eventuelle endringer du mener vi bør gjøre i eksisterende funksjoner. Foreslå produktideer på [Human Resources-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    
Ikke ta med personlige data (informasjon som kan identifisere deg) i tilbakemeldingene eller innsendingene av produktgjennomgang. Innsamlet informasjon kan analyseres ytterligere, og den brukes ikke til å svare på forespørsler under gjeldende personvernlover. Personopplysninger som samles inn separat under disse programmene, er underlagt [Microsofts personvernerklæring](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Se også

- [Hva er nytt i Human Resources](hr-admin-whats-new.md)
- [Lanseringsplan for Dynamics 365 og Power Platform](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)