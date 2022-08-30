---
title: Hovedplanlegging for produkter med begrenset holdbarhet
description: Denne artikkelen beskriver hvordan du definerer og bruker planleggingsfunksjoner som tar hensyn til holdbarheten til varer.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 95c905cbcc3c057dbccf2b7d6e894b1e99ddfba5
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337141"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Hovedplanlegging for produkter med begrenset holdbarhet

[!include [banner](../../includes/banner.md)]

Holdbarhet er den tiden et produkt kan lagres til det ikke lenger kan brukes eller selges. For produkter som har begrenset holdbarhet vil du sannsynligvis bruke en FEFO-lagerstrategi (først utløp, først ut), som prioriterer forbruket og salget av varer basert på gjenværende holdbarhet. Denne lagerstrategien er relevant for mat, medisiner og andre varer som kjennetegnes av en kort lagringstid. I henhold til FEFO lagres varer på lageret som varer på en holdbarhetshylle: Produkter som har lang holdbarhet, plasseres lengst inn i hyllene slik at produkter med kortere gjenværende holdbarhet sendes først.

## <a name="using-shelf-life-in-master-planning"></a>Bruk holdbarhet i hovedplanlegging

Denne delen beskriver hvordan hovedplanleggingen foreslår forsyning for varer med holdbarhet.

Når du kjører en hovedplan, genererer den foreslåtte planlagte ordrer (forsyning) som vil dekke behovet, og som også reduserer forsinkelsene. Hvis planen inneholder varer som har begrenset holdbarhet, blir planleggingsberegningene mer komplekse, fordi planen ikke bare må minimere forsinkelser, men også bruke eksisterende forsyning før den utløper. Planen må prøve å bruke forsyning som er nærmest utløpsdatoen, før forsyning som utløper senere. Hovedplanleggingen søker derfor å oppnå følgende mål i denne rekkefølgen:

1. Reduser summen av forsinkelser.
1. Maksimer summen av FEFO-forsyning.
1. Minimer etterfylling av lager.

I noen tilfeller kan det være en konflikt mellom de to første målene, og du må velge: Vil du utsette en forsendelse, eller vil du bruke forsyning som utløper senere, i stedet for forsyning som utløper raskere? Hvis du vil løse denne konflikten under hovedplanlegging, prioriterer systemet å minimere forsinkelser over bruk av forsyning som snart utløper. Generelt sett forekommer denne typen konflikt når det kan være forsinkelser og dekning etter periode. Vi anbefaler derfor at du bruker en dekningsperiode som er kortere enn holdbarheten til en vare. Andre typer dekning (for eksempel krav) vil sannsynligvis ikke oppleve denne typen konflikt.

## <a name="set-up-shelf-life"></a>Definer holdbarhet

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Konfigurer hver hovedplan for å vurdere holdbarhet

Hovedplaner tar som standard ikke hensyn til holdbarhet. Bruk fremgangsmåten nedenfor til å aktivere holdbarhetsberegninger for hver hovedplan som krever dem.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en eksisterende plan i listeruten, eller opprett en ny en.
1. På **Generelt**-hurtigfanen angir du **Bruk holdbarhetsdata**-alternativet til *Ja*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Konfigurer sporingsdimensjonsgrupper for å spore partidimensjon

Holdbarheten til en vare kan bare spores hvis denne varen spores i partidimensjonen. Partireferansen og de nødvendige datoene må med andre ord registreres ved mottak eller produksjon, og ved hver lagertransaksjon for varen. Hvis du vil administrere dette alternativet, kan du definere en eller flere sporingsdimensjonsgrupper for å gjøre den nødvendige sporingen, og deretter tildele de relevante varene til disse gruppene etter behov.

Bruk fremgangsmåten nedenfor til å definere en sporingsdimensjonsgruppe for å spore partidimensjonen.

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Dimensjon og variantgrupper \> Sporingsdimensjonsgrupper**.
1. Følg ett av disse trinnene:

    - I handlingsruten velger du **Ny** for å opprette en ny sporingsdimensjonsgruppe. Angi et navn og en beskrivelse og velg **Lagre** i handlingsruten.
    - I listeruten velger du den eksisterende sporingsdimensjonsgruppen du vil definere for å spore partidimensjonen.

1. I hurtigfanen **Sporingsdimensjon**, i raden **Partinummer** merker du av i avmerkingsboksene i kolonene **Aktiv** og **Fysisk lager**.

### <a name="set-up-shelf-life-for-a-product"></a>Definer holdbarhet for et produkt

Bruk fremgangsmåten nedenfor til å definere holdbarhet for et produkt.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Opprett eller åpne produktet du vil definere.
1. Hvis du vil bruke innstillingene for holdbarhet, angir du feltet **Sporingsdimensjonsgruppe** til en sporingsdimensjonsgruppe som er definert til å spore partidimensjonen, i hurtigfanen **Generelt**. Du kan bare definere dette feltet når du oppretter et produkt første gang. Du kan ikke endre verdien for eksisterende produkter.
1. På **Administrer lager**-hurtigfanen angir du følgende felter:

    - **Anbefalt holdbarhetsperiode i dager** – Angi perioden (i dager) som du vil kontrollere et parti av dette produktet innen, for å sikre at det passer for forbruk eller videresalg. Verdien til dette feltet legges til et partis *produksjonsdato* for å fastslå den anbefalte *holdbarhetsdatoen*. Du kan konfigurere systemet til å generere kvalitetsordrer når et parti nærmer seg den anbefalte holdbarhetsdatoen.
    - **Holdbarhetsperiode i dager** – Angi antall dager før et parti med dette produktet utløper. Denne verdien legges til *produksjonsdatoen* for å bestemme *utløpsdatoen*. Partiet anses som ubrukelig etter denne datoen.
    - **Best før-perioden i dager** – Angi perioden (i dager) da et parti med dette produktet fremdeles kan selges, men ikke lenger kan beholde noen av sine opprinnelige egenskaper. Denne verdien legges til *produksjonsdatoen* for å bestemme *best før*. Du kan kjøre rapporter for å identifisere lager som er over best før-datoen. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Angi en regel for Kan selges i antall dager for hver kunde

Med *Kan selges i antall dager*-funksjonalitet kan du sikre at produkter fra et parti som snart utløper, ikke sendes til kunder. Videre sikrer det at når produkter sendes til en kunde, vil et tilstrekkelig Kan selges i antall dager fremdeles forbli etter levering.

Hvis du vil bruke funksjonen Kan selges i antall dager, må du definere Kan selges i antall dager som gjelder hvert produkt (eller en gruppe produkter) for hver kunde. Du må fullføre denne prosessen manuelt fordi det ikke finnes noen dataenhet for den.

Bruk fremgangsmåten nedenfor til å angi Kan selges i antall dager for hvert produkt for hver kunde.

1. Gå til **Salg og markedsføring \> Kunder \> Alle kunder**.
1. Finn og velg kunden du vil definere.
1. I gruppen **Oppsett** i fanen **Salg** i handlingsruten velger du **Salg \> Kan selges i antall dager**.
1. På siden **Kan selges i antall dager for kunde** viser rutenettet eksisterende regler for Kan selges i antall dager for hvert produkt eller en gruppe produkter. Bruk knappene på handlingsruten til å legge til eller redigere rader i rutenettet etter behov. Det finnes et **filter** som hjelper deg med å finne eksisterende rader.
1. For hver rad angir du feltene nedenfor:

    - **Varekode** – Velg en av følgende verdier for å angi vareområdet som blir påvirket:

        - *Tabell* – Raden gjelder en bestemt vare.
        - *Gruppe* – Raden gjelder bare en bestemt varegruppe.
        - *Alle* – Raden gjelder alle varer.

    - **Varerelasjon** – Hvis du angir **Varekode**-feltet til *Tabell*, velger du en bestemt vare. Hvis du valgte **Gruppe** i *Varekode*-feltet, må du velge en varegruppe. Hvis du angir **Varekode**-feltet til *Alle*, er ikke dette feltet tilgjengelig.
    - **Kan selges i antall dager** – Angi minste antall dager kunden må ha for å selge samsvarende produkter før partiet utløper. Verdien for Kan selges i antall dager er basert på den ønskede leveringsdatoen (eller den bekreftede mottaksdatoen, hvis den er definert) for samsvarende produkter på salgsordren.
    - *(Andre produktdimensjoner)* – Hvis du vil begrense radområdet ytterligere, angir du andre dimensjonsverdier (for eksempel **Størrelse** og **Farge**) etter behov. Hvis du vil kontrollere hvilke dimensjoner som vises i rutenettet, velger du **Vis dimensjoner** i handlingsruten.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Definer alle relevante produkter slik at de er FEFO-datokontrollerte

Hvis Kan selges i antall dager skal fungere, må hver relevante vare tilhøre en varemodellgruppe der det er merket av for **FEFO-datokontrollert**.

Bruk fremgangsmåten nedenfor til å definere en varemodellgruppe slik at den støtter funksjonaliteten Kan selges i antall dager.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Varemodellgrupper**.
1. Velg en eksisterende gruppe i listeruten, eller opprett en ny en ved å velge **Ny** i handlingsruten.
1. Velg **FEFO-datokontroller** i hurtigfanen **Beholdningspolicyer**.
1. Angi andre felter for gruppen etter behov.

Bruk fremgangsmåten nedenfor til å vise eller angi varemodellgruppen som et produkt tilhører.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Åpne produktet du vil inspisere eller redigere.
1. I hurtigfanen **Generelt** angir du feltet **Varemodellgruppe** til en gruppe der det er merket av for **FEFO-datokontrollert**.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Eksempel 1: Enkel FEFO, 10-dagers periode, null dager leveringstid

Dette eksemplet viser et grunnleggende eksempel på holdbarhet, der utligning mellom forsyningsordrene og behovet oppfylles for å oppfylle følgende mål for systemet:

- Reduser summen av forsinkelser.
- Maksimer summen av FEFO-forsyning.
- Minimer etterfylling av lager.

Systemet har følgende innstillinger for vare- og hovedplan:

- **Dekningskode (etterfyllingsstrategi):** Periode 
- **Dekningsperiode:** 10 dager (er lik holdbarheten)
- **Holdbarhet:** 10 dager
- **Kan selges i antall dager:** 0 dager
- **Leveringstid:** 0 dager
- **Negative dager:** 0 dager
- **Type planlagt bestilling (standard bestillingsinnstillinger for varen):** Bestilling

Følgende salgsordrer for varen finnes i systemet:

- **SO1:** Antall (ant.) = 2, ønsket leveringsdato = i dag + 1 dag
- **SO2:** Ant. = 1, ønsket leveringsdato = i dag + 4 dager
- **SO3:** Ant. = 1, ønsket leveringsdato = i dag + 5 dager

Alle disse salgsordrene oppretter etterspørsel etter varen.

Følgende forsyning finnes for varen:

- **Lagerbeholdning:** Ant. = 1, utløpsdato = i dag + 5 dager
- **Bestilling 1 (PO1):** Mottaksdato = i dag + 2 dager, ant. = 1, utløpsdato = i dag + 4 dager

Systemet oppretter en liste over forsyninger som kan dekke dette behovet, og den sorterer listen etter utløpsdato (ved hjelp av FEFO).

Hovedplanlegging oppretter nødvendig utligning mellom tilbud og etterspørsel. Det oppretter også alle nødvendige behov basert på forsyningslisten (ved hjelp av FEFO), og vurderer tilgjengelighetsdatoen.

- SO1 kan oppfylles av beholdningsantallet, men den kan ikke oppfylles innen PO1, fordi tilgjengelighetsdatoen for PO1 er én dag senere enn SO1 krever. Derfor genererer SO1 etterspørsel etter én vareenhet.
- SO2 kan dekkes av PO1, fordi PO1 vil ankomme innen ønsket tid, og utløpsdatoen vil fortsatt være gyldig. Derfor er SO2-kravet fullstendig dekket av PO1.
- SO3 dekkes ikke, fordi ressurser ikke er tilgjengelige. Derfor genererer SO3 etterspørsel etter én vareenhet.

For å dekke alle de gjenværende behovene må systemet opprette følgende bestillingsforslag:

- **PPO1:** Mottaksdato = i dag, ant. = 2, utløpsdato = i dag + 10 dager

Følgende tabell viser en oversikt over resultatet.

| Behov | Utligning |
|---|---|
| **SO1:** Leveringsdato = i dag + 1 dag, ant. = 2 | <p>**Lager:** Ant. = 1, utløpsdato = i dag + 5 dager</p><p>**PPO1:** Mottaksdato = i dag, ant. = 1, utløpsdato = i dag + 10 dager</p> |
| **SO2:** Leveringsdato = i dag + 4 dager, ant. = 1 | **PO1:** Mottaksdato = i dag + 2 dager, 1 ant., utløpsdato = i dag + 4 dager |
| **SO3:** Leveringsdato = i dag + 5 dager, ant. = 1 | **PPO1:** Mottaksdato = i dag, ant. = 2, utløpsdato = i dag + 10 dager |

Illustrasjonen nedenfor viser hvordan tidslinjen ser ut i dette eksemplet.

![Eksempel 1: Enkel FEFO, 10-dagers periode, null dager leveringstid.](media/fefo-example-1.png "Eksempel 1: Enkel FEFO, 10-dagers periode, null dager leveringstid")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Eksempel 2: Enkel FEFO, krav, tre dagers leveringstid

Dette eksemplet viser hvordan systemets forsøk på å redusere forsinkelser noen ganger kan føre til overbestilling.

Systemet har følgende innstillinger for vare- og hovedplan:

- **Dekningskode (etterfyllingsstrategi):** Krav
- **Holdbarhet:** 10 dager
- **Kan selges i antall dager:** 0 dager
- **Leveringstid:** Fastsatt av følgende forretningsavtaler for leverandør:

    - **Forretningsavtale 1:** Hvis ant.= 1, leveringstid = 4
    - **Forretningsavtale 2:** Hvis ant.= 2, leveringstid = 3

- **Negative dager:** 0 dager
- **Type planlagt bestilling (standard bestillingsinnstillinger for varen):** Bestilling

Følgende salgsordrelinjer finnes i systemet:

- **SO1:** Ant. = 2, ønsket leveringsdato = i dag + 3 dager

Dette behovet dekkes av den eksisterende forsyningen og en bekreftet bestilling:

- **Lagerbeholdning:** Tilgjengelig = i dag, ant. = 1, utløpsdato = i dag + 2 dager
- **PO1:** Mottaksdato = i dag + 3 dager, ant. = 1, utløpsdato = i dag + 4 dager

SO1 kan ikke oppfylles ved hjelp av lagerbeholdningen, fordi utløpsdatoen for lageret er før forsendelsesdatoen. PO1 kan dekke SO1-behovet med et antall på bare 1. Derfor genererer SO1 etterspørsel etter én vareenhet. For å dekke dette behovet oppretter systemet et bestillingsforslag (PPO1).

Systemet har to forretningsavtaler (én for ant. = 1, leveringstid = 4 dager, og en for ant. = 2, leveringstid = 3 dager). Derfor forsøker systemet å redusere forsinkelsene ved å opprette et bestillingsforslag (PPO1) som oppfyller den andre forretningsavtalen. Resultatet er en overlevering (ant. = 2, utløpsdato = i dag + 10 dager).

Følgende tabell viser en oversikt over resultatet.

| Behov | Utligning |
|---|---|
| **SO1:** Leveringsdato = i dag + 3 dager, ant. = 2 | <p>**PO1:** Mottaksdato = i dag + 3 dager, ant. = 1, utløpsdato = i dag + 4 dager</p><p>**PPO1:** Mottaksdato = i dag + 3 dager, ant. = 1, utløpsdato = i dag + 10 dager</p> |

Illustrasjonen nedenfor viser hvordan tidslinjen ser ut i dette eksemplet.

![Eksempel 2: Enkel FEFO, krav, tre dagers leveringstid.](media/fefo-example-2.png "Eksempel 2: Enkel FEFO, krav, tre dagers leveringstid")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Eksempel 3: Enkel FEFO, krav, tre dagers leveringstid, fem salgbare dager

Dette eksemplet viser hvordan holdbarhet fungerer når salgbare dager legges til for en vare.

Systemet har følgende innstillinger for vare- og hovedplan:

- **Dekningskode (etterfyllingsstrategi):** Krav
- **Holdbarhet:** 10 dager
- **Kan selges i antall dager:** 5 dager
- **Leveringstid:** 5 dager
- **Negative dager:** 0 dager
- **Type planlagt bestilling (standard bestillingsinnstillinger for varen):** Bestilling

Følgende salgsordrer finnes i systemet:

- **SO1:** Ant. = 2, ønsket leveringsdato = i dag + 2 dager
- **SO2:** Ant. = 1, ønsket leveringsdato = i dag + 3 dager
- **SO3:** Ant. = 1, ønsket leveringsdato = i dag + 5 dager

Dette behovet kan dekkes av eksisterende forsyning og en bekreftet bestilling:

- **Lagerbeholdning:** Tilgjengelig = i dag, ant. = 1, utløpsdato = i dag + 6 dager
- **PO1:** Mottaksdato = i dag + 2 dager, ant. = 3, utløpsdato = i dag + 10 dager

Systemet oppretter en liste over utligningskandidater basert på forsyningslisten (FEFO) og tilgjengelighetsdatoene. SO1 kan derfor ikke oppfylles av lagerbeholdningen fordi lageret utløper før slutten av de salgbare dagene som kunden krever (ønsket mottaksdato + 5 dager). PO1 kan dekke SO1-behovet med to enheter og SO2-behovet med én enhet. Derfor har bare SO3 fortsatt udekket etterspørsel etter én vareenhet. For å dekke dette behovet oppretter systemet følgende bestillingsforslag:

- **PP01:** Mottaksdato = i dag + 5 dager, ant. = 1, utløpsdato = i dag + 10 dager

Følgende tabell viser en oversikt over resultatet.

| Behov | Utligning |
|---|---|
| **SO1:** Leveringsdato = i dag + 2 dager, ant. = 2 | **PO1:** Mottaksdato = i dag + 2 dager, ant. = 2, utløpsdato = i dag + 10 dager |
| **SO2:** Leveringsdato = i dag + 3 dager, ant. = 1 | **PO1:** Mottaksdato = i dag + 2 dager, ant. = 1, utløpsdato = i dag + 10 dager |
| **SO3:** Leveringsdato = i dag + 5 dager, ant. = 1 | **PPO1:** Mottaksdato = i dag + 5 dager, ant. = 1, utløpsdato = i dag + 10 dager |

Illustrasjonen nedenfor viser hvordan tidslinjen ser ut i dette eksemplet.

![Eksempel 3: Enkel FEFO, krav, tre dagers leveringstid, fem salgbare dager.](media/fefo-example-3.png "Eksempel 3: Enkel FEFO, krav, tre dagers leveringstid, fem salgbare dager")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Eksempel 4: Enkel FEFO, periode, leveringstid avhenger av antallet

Dette eksemplet viser hvordan systemets forsøk på å redusere forsinkelser noen ganger kan føre til overbestilling.

Systemet har følgende innstillinger for vare- og hovedplan:

- **Dekningskode (etterfyllingsstrategi):** Periode
- **Dekningsperiode:** 10 dager (er lik holdbarheten)
- **Holdbarhet:** 10 dager
- **Kan selges i antall dager:** 0 dager
- **Leveringstid:** Fastsatt av følgende forretningsavtaler for leverandør:

    - **Forretningsavtale 1:** Hvis ant.= 1, leveringstid = 5
    - **Forretningsavtale 2:** Hvis ant.= 2, leveringstid = 0

- **Negative dager:** 0 dager
- **Type planlagt bestilling (standard bestillingsinnstillinger for varen):** Bestilling

Følgende salgsordrer finnes i systemet:

- **SO1:** Ant. = 1, ønsket leveringsdato = i dag
- **SO2:** Ant. = 1, ønsket leveringsdato = i dag + 6 dager

Dette behovet kan dekkes delvis av eksisterende forsyning fra følgende bekreftede bestillinger:

- **PO1:** Mottaksdato = i dag + 1 dager, ant. = 1, utløpsdato = i dag + 2 dager
- **PO2:** Mottaksdato = i dag + 3 dager, ant. = 1, utløpsdato = i dag + 7 dager

Systemet har to forretningsavtaler (én for ant. = 1, leveringstid = 5 dager, og en for ant. = 2, leveringstid = 0 dager). Derfor forsøker systemet å redusere forsinkelse ved å opprette følgende bestillingsforslag som oppfyller den andre forretningsavtalen:

- **PP01:** Mottaksdato = i dag, ant. = 2, utløpsdato = i dag + 10 dager

SO1 blir dekket av én enhet fra PPO1. SO2 blir dekket av PO2, fordi PO2 utløper raskere enn PPO1.

Følgende tabell viser en oversikt over resultatet.

| Behov | Utligning |
|---|---|
| **SO1:** Leveringsdato = i dag, ant. = 1 | **PPO1:** Mottaksdato = i dag, ant. = 1, utløpsdato = i dag + 10 dager |
| **SO2:** Leveringsdato = i dag + 6 dager, ant. = 1 | **PO2:** Mottaksdato = i dag + 3 dager, ant. = 1, utløpsdato = i dag + 7 dager |

> [!NOTE]
> PO1 ikke brukt, fordi den vil ankomme for sent for S01 og utløper før S02 leveres. PPO1 har overbestilt av én enhet slik at leveringstiden kan være 0 (null), per forretningsavtale 2.

Illustrasjonen nedenfor viser hvordan tidslinjen ser ut i dette eksemplet.

![Eksempel 4: Enkel FEFO, periode, leveringstid avhenger av antallet.](media/fefo-example-4.png "Eksempel 4: Enkel FEFO, periode, leveringstid avhenger av antallet")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Eksempel 5: Enkel FEFO, behov, 10 negative dager

<!-- KFM: This is more of a negative days example than a shelf life example. We should point out more explicitly how shelf life affects this situation (or maybe otherwise remove this example). -->

Dette eksemplet viser hvordan holdbarhet fungerer når et stor antall negative dager legges til for en vare. Negative dager er hvor mange dager du er villig til å vente før du bestiller ny etterfylling av en vare som har negativ beholdning. Systemet oppretter ikke forsyning med mindre antall negative dager overskrides.

Systemet har følgende innstillinger for vare- og hovedplan:

- **Dekningskode (etterfyllingsstrategi):** Krav
- **Leveringstid:** 0 dager
- **Negative dager:** 10 dager
- **Type planlagt bestilling (standard bestillingsinnstillinger for varen):** Bestilling

Følgende salgsordrelinjer finnes i systemet:

- **SO1:** Ant. = 1, ønsket leveringsdato = i dag

Dette behovet kan dekkes delvis av eksisterende forsyning fra følgende bekreftet bestilling:

- **PO1:** Mottaksdato = i dag + 3 dager, ant. = 1, utløpsdato = i dag + 5 dager

Fordi systemet er konfigurert til å tillate ti negative dager, dekker det behovet for SO1 ved å bruke PO1, selv om resultatet blir en forsinkelse på tre dager, fordi SO1 oppretter negativt lager til PO1 ankommer. Det opprettes ikke et bestillingsforslag, selv om leveringstiden er 0 (null) og oppretting av et bestillingsforslag vil redusere forsinkelser.

Følgende tabell viser en oversikt over resultatet.

| Behov | Utligning |
|---|---|
| **SO1:** Leveringsdato = i dag, ant. = 1 | **PO1:** Mottaksdato = i dag + 3 dager, ant. = 1, utløpsdato = i dag + 5 dager |

Illustrasjonen nedenfor viser hvordan tidslinjen ser ut i dette eksemplet.

![Eksempel 5: Enkel FEFO, behov, 10 negative dager.](media/fefo-example-5.png "Eksempel 5: Enkel FEFO, behov, 10 negative dager")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Eksempel 6: Enkel FEFO, behov, fem negative dager

Dette eksemplet viser hvordan holdbarhet fungerer når antall negative dager for en vare er mindre en holdbarhetsperioden.

Systemet har følgende innstillinger for vare- og hovedplan:

- **Dekningskode (etterfyllingsstrategi):** Krav
- **Kan selges i antall dager:** 0 dager
- **Leveringstid:** 0 dager
- **Negative dager:** 5 dager
- **Type planlagt bestilling (standard bestillingsinnstillinger for varen):** Bestilling

Følgende salgsordrelinjer finnes i systemet:

- **SO1:** Ant. = 2, ønsket leveringsdato = i dag

Dette behovet kan dekkes delvis av eksisterende forsyning fra følgende bekreftede bestillinger:

- **PO1:** Mottaksdato = i dag, ant. = 1, utløpsdato = i dag + 1 dag
- **PO2:** Mottaksdato = i dag + 2 dager, ant. = 1, utløpsdato = i dag + 3 dager

Systemet må imidlertid følge begrensningen av at sendte varer ikke kan utløpe når forsendelsen pågår. PO2 og PO1 kan derfor ikke brukes for SO1 fordi PO1 utløper før PO2 ankommer. Systemet oppretter følgende bestillingsforslag for å fullføre dekningen av etterspørselen for SO1:

- **PPO1:** Mottaksdato = i dag, ant. = 1, utløpsdato = i dag + 10 dager

Systemet kan dra nytte av de fem negative dagene og bruke PO2 og PPO1 til å dekke SO1. Denne fremgangsmåten fører imidlertid til at leveringen blir forsinket til PO2 ankommer, og PO1 vil utløpe i mellomtiden Derfor dekker systemet SO1 ved hjelp av PPO1 og PO1.

Følgende tabell viser en oversikt over resultatet.

| Behov | Utligning |
|---|---|
| **SO1:** Leveringsdato = i dag, ant. = 2 | <p>**PO1:** Mottaksdato = i dag, ant. = 1, utløpsdato = i dag + 1 dag</p><p>**PPO1:** Mottaksdato = i dag, ant. = 1, utløpsdato = i dag + 10 dager</p> |

Illustrasjonen nedenfor viser hvordan tidslinjen ser ut i dette eksemplet.

![Eksempel 6: Enkel FEFO, behov, fem negative dager.](media/fefo-example-6.png "Eksempel 6: Enkel FEFO, behov, fem negative dager")
