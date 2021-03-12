---
title: Arbeidspolicyer
description: Dette emnet forklarer hvordan du konfigurerer arbeidspolicyer.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 530abffb4c80a2d2f0e58e0c5a34294f7cba0b1a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998459"
---
# <a name="work-policies"></a>Arbeidspolicyer

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer systemet og lagerappen slik at de har støtte for arbeidspolicyer. Du kan bruke denne funksjonaliteten til raskt å registrere beholdning uten å opprette plasseringsarbeid når du mottar bestillinger eller overføringsordrer, eller når du fullfører produksjonsprosesser. Dette emnet gir generell informasjon. For detaljert informasjon som gjelder nummerskiltmottak, kan du se [Nummerskiltmottak via lagerappen](warehousing-mobile-device-app-license-plate-receiving.md).

En arbeidspolicy kontrollerer om lagerarbeid opprettes når en produsert vare rapporteres som ferdig, eller når varer mottas ved hjelp av lagerappen. Du definerer hver arbeidspolicy ved å definere betingelsene der den gjelder: arbeidsordretypene og -prosessene, beholdningslokasjonen og (eventuelt) produktene. For eksempel må en bestilling for produkt *A0001* mottas i lokasjonen *RECV* på lager *24*. Senere forbrukes produktet i en annen prosess på lokasjonen *RECV*. I dette tilfellet kan du definere en arbeidspolicy for å hindre at plasseringsarbeid blir opprettet når en arbeider rapporterer produkt *A0001* som mottatt på lokasjonen *RECV*.

> [!NOTE]
> - Hvis en arbeidspolicy skal være aktiv, må du definere minst én lokasjon for den på hurtigfanen **Lagerlokasjoner** på siden **Arbeidspolicyer**. 
> - Du kan ikke angi samme plassering for flere arbeidspolicyer.
> - Alternativet **Skriv ut etikett** for menyelementer på mobilenheter skriver ikke ut en nummerskiltetikett med mindre arbeid er opprettet.

## <a name="activate-the-features-in-your-system"></a>Aktivere funksjonene i systemet

Hvis du vil gjøre all funksjonalitet som er beskrevet i dette emnet, tilgjengelig i systemet, kan du aktivere følgende to funksjoner i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Forbedringer av mottak av nummerskilter
- Forbedringer for arbeidspolicy for innkommende arbeid

## <a name="the-work-policies-page"></a>Siden Arbeidspolicyer

Når du skal definere arbeidspolicyer, går du til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidspolicyer**. Deretter angir du feltene som beskrevet i følgende underdeler, på hver hurtigfane.

### <a name="the-work-order-types-fasttab"></a>Hurtigfanen Arbeidsordretyper

På hurtigfanen **Arbeidsordretyper** legger du til alle arbeidsordretyper og de tilknyttede arbeidsprosessene som arbeidspolicyen gjelder for. Følgende arbeidsordretyper og relaterte arbeidsprosesser støttes for arbeidspolicyer.

| Arbeidsordretype | Arbeidsprosess |
|---|---|
| Råvareplukking| Alle relaterte prosesser |
| Plasser koprodukt og biprodukt | Alle relaterte prosesser |
| Plasser ferdigvarer | Alle relaterte prosesser |
| Overføringsmottak | Mottak (og plassering) av nummerskilt |
| Bestillinger | <ul><li>Mottak (og plassering) av nummerskilt</li><li>Mottak (og plassering) av lastvare</li><li>Mottak (og plassering) av bestillingslinje</li><li>Mottak (og plassering) av bestillingsvarer</li></ul> |

Hvis du vil definere en arbeidspolicy slik at den gjelder flere arbeidsprosesser i samme arbeidsordretype, legger du til en egen linje for hver arbeidsprosess i rutenettet.

For hver linje i rutenettet angir du feltet **Arbeidsopprettelsesmetode** til én av følgende verdier:

- **Aldri** – Arbeidspolicyen hindrer at lagerarbeid opprettes for den valgte arbeidsordretypen og den relaterte arbeidsprosessen.
- **Direkteoverføring** – Arbeidspolicyen vil opprette direkteoverføringsarbeid ved hjelp av policyen du velger i feltet **Navn på direkteoverføringspolicy**.

### <a name="the-inventory-locations-fasttab"></a>Hurtigfanen Lagerlokasjoner

På hurtigfanen **Lagerlokasjoner** legger du til alle lokasjoner der denne arbeidspolicyen skal brukes. Hvis ingen lokasjon er knyttet til en arbeidspolicy, brukes ikke arbeidspolicyen for noen prosesser.

Du kan ikke angi samme plassering for flere arbeidspolicyer.

Du kan bruke en lagerlokasjon som er tilordnet en lokasjonsprofil, der **Bruk sporing av nummerskilt** er deaktivert. I dette tilfellet vil arbeidere registrere lagerbeholdningen direkte.

### <a name="the-products-fasttab"></a>Hurtigfanen Produkter

På **Produkter**-fanen angir du feltet **Produktvalg** for å kontrollere hvilke produkter policyen skal gjelde for:

- **Alle** – Policyen skal gjelde for alle produkter.
- **Valgt** – Policyen skal bare gjelde for produkter som er oppført i rutenettet. Bruk verktøylinjen på hurtigfanen **Produkter** til å legge til produkter i rutenettet eller fjerne dem fra rutenettet.

## <a name="default-and-custom-to-locations"></a>Standard og egendefinerte "til"-lokasjoner

> [!NOTE]
> Hvis du vil gjøre funksjonaliteten som er beskrevet i denne delen, tilgjengelig i systemet, må du aktivere funksjonene *Forbedringer for nummerskiltmottak* og *Arbeidspolicyforbedringer for innkommende arbeid* i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tidligere støttet systemet bare mottak på standardlokasjonen som er definert for hvert lager. Menyelementer for mobilenheter som bruker følgende arbeidsprosesser, inneholder imidlertid nå alternativet **Bruk standarddata**. Ved hjelp av dette alternativet kan du tilordne en egendefinert "til"-plassering til ett eller flere menyelementer. (Dette alternativet var allerede tilgjengelig for enkelte andre typer menyelementer.)

- Mottak (og plassering) av nummerskilt
- Mottak (og plassering) av lastvare
- Mottak (og plassering) av bestillingslinje
- Mottak (og plassering) av bestillingsvarer

Innstillingen **Til-plassering** for et menyelement overstyrer standard mottakslokasjon for lageret, for alle ordrer som er behandlet med dette menyelementet.

Følg denne fremgangsmåten for å konfigurere et menyelement for en mobilenhet for å støtte mottak til en egendefinert plassering.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg eller opprett et menyelement som bruker en av arbeidsopprettingsprosessene som er oppført tidligere i denne delen.
1. På **Generelt**-hurtigfanen angir du **Bruk standarddata**-alternativet til **Ja**.
1. I handlingsruten velger du **Standarddata**.
1. Angi følgende verdier på siden **Standarddata**:

    - **Feltet Standarddata:** Sett dette feltet til *Til lokasjon*.
    - **Lager:** Velg hvilket mållager som skal brukes med dette menyelementet.
    - **Lokasjon:** Dette feltet inneholder alle lokasjons-ID-ene som er tilgjengelige for det valgte lageret. Innstillingen i dette feltet har imidlertid ingen virkning. Du kan derfor la det stå tomt. Du kan likevel bruke listen til å bekrefte ID-en du må angi, i feltet **Hardkodet verdi**.
    - **Hardkodet verdi:** Angi lokasjons-ID-en for mottakslokasjonen som gjelder for dette menyelementet.

> [!TIP]
> En arbeidspolicy kan bare brukes hvis alle mottakslokasjonene er oppført i det relevante arbeidspolicyoppsettet. Dette kravet gjelder uansett om du bruker standard lagermottakslokasjon eller en egendefinert "til"-lokasjon.

## <a name="example-scenario-warehouse-receiving"></a>Eksempelscenario: Lagermottak

Alle produkter som mottas ved hjelp av prosessen *Mottak (og plassering) av bestillingsvare*, må registreres på lokasjonen *FL-001*, og de må være tilgjengelige på lager *24*. Arbeid bør imidlertid ikke opprettes. Produkter som er mottatt av en annen prosess (det vil si ved hjelp av andre menyelementer for mobilenheter), bør registreres ved standard mottakslokasjon (*RECV*), og arbeid bør opprettes som vanlig. (Dette scenariet viser ikke standard mottaksoppsett.)

Dette scenariet krever følgende elementer:

- En arbeidspolicy for prosessen *Mottak (og plassering) av bestillingsvarer* på lokasjonen *FL-001* for alle produkter
- Menyelement på mobilenhet som har standarddata, og som setter feltet **Til-lokasjon** til *FL-001*

### <a name="prerequisites"></a>Forutsetninger

Hvis du vil gjøre funksjonaliteten som er beskrevet i dette scenarioet, tilgjengelig i systemet, må du aktivere funksjonene *Forbedringer for nummerskiltmottak* og *Arbeidspolicyforbedringer for innkommende arbeid* i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Dette scenarioet bruker standard demonstrasjonsdata. Hvis du vil arbeide deg gjennom det ved å bruke verdiene som presenteres her, må du derfor arbeide på et system der standard demodata er installert. Du må også velge den juridiske enheten **USMF**.

### <a name="set-up-a-work-policy"></a>Definere en arbeidspolicy

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidspolicyer**.
1. Velg **Ny**.
1. I feltet **Arbeidspolicynavn** angir du *Ikke plasseringsarbeid for innkjøpsvare*.
1. Velg **Lagre**.
1. På hurtigfanen **Arbeidsordretyper** velger du **Legg til** for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:

    - **Arbeidsordretype:** *Bestillinger*
    - **Arbeidsprosess:** *Mottak (og plassering) av bestillingsvarer*
    - **Arbeidsopprettelsesmetode:** *Aldri*
    - **Navn på direkteoverføringspolicy:** La dette feltet stå tomt.

1. På hurtigfanen **Lagerlokasjoner** velger du **Legg til** for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:

    - **Lager:** *24*
    - **Lokasjon:** *FL-001*

1. På hurtigfanen **Produkter** angir du feltet **Produktvalg** til *Alle*.
1. Velg **Lagre**.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Definere et menyelement for mobilenhet for å endre mottakslokasjonen

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg det eksisterende menyelementet **Kjøpsmottak** i den venstre ruten.
1. På **Generelt**-hurtigfanen angir du **Bruk standarddata**-alternativet til *Ja*.
1. Velg **Lagre**.
1. I handlingsruten velger du **Standarddata**.
1. På siden **Standarddata** velger du **Ny** i handlingsruten for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:

    - **Feltet Standarddata:** *Til-plassering*
    - **Lager:** *24*
    - **Lokasjon:** La dette feltet stå tomt.
    - **Hardkodet verdi:** *FL-001*

1. Velg **Lagre**.

### <a name="receive-a-purchase-order-without-creating-work"></a>Motta en bestilling uten å opprette arbeid

Eksemplet i denne delen viser hvordan du mottar en bestillingsvare, men uten å opprette arbeid, på en lokasjon som er forskjellig fra standard mottakslokasjon som er definert for lageret. Dette eksemplet bruker arbeidspolicyen og varen fra mobilenheten som du opprettet tidligere i dette scenariet.

#### <a name="create-a-purchase-order"></a>Opprette en bestilling

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Ny**.
1. I **Opprett bestilling**-dialogboksen angir du følgende verdier:

    - **Leverandørkonto:** *US-101*
    - **Område:** *2*
    - **Lager:** *24*

1. Velg **OK** for å lukke dialogboksen og opprette den nye bestillingen.
1. På hurtigfanen **Bestillingslinjer** angir du følgende verdier for den tomme raden:

    - **Varenummer:** *A0001*
    - **Antall:** *1*

1. Velg **Lagre**.
1. Noter deg bestillingsnummeret.

#### <a name="receive-a-purchase-order"></a>Motta en bestilling

1. På mobilenheten logger du deg på lager *24* ved å bruke *24* som bruker-ID og *1* som passord.
1. Velg **Innkommende**.
1. Velg **Kjøpsmottak**. **Lokasjon**-feltet bør settes til *FL-001*.
1. Angi bestillingsnummeret for bestillingen som du opprettet i den forrige fremgangsmåten.
1. I **VarenummerI**-feltet angir du *A0001*.
1. Velg **OK**.
1. I feltet **Antall** angi *1*.
1. Velg **OK**.

Bestillingen er nå mottatt, men intet arbeid er tilknyttet den. Lagerbeholdningen er oppdatert, og et antall på *1* for vare *A0001* er nå tilgjengelig på lokasjonen *FL-001*.

## <a name="example-scenario-manufacturing"></a>Eksempelscenario: Produksjon

I eksemplet nedenfor er det to produksjonsordrer, *PRD-001* og *PRD-002*. Produksjonsordren *PRD-001* har en operasjon kalt *Montering*, der produktet *SC1* rapporteres som ferdig til lokasjonen *001*. Produksjonsordren *PRD-002* er en operasjon kalt *Maling*, og den bruker *SC1*-produktet fra lokasjonen *001*. Produksjonsordren *PRD-002* bruker også råvaren *RM1* fra lokasjonen *001*. Råmaterialet *RM1* er lagret i lagerlokasjonen *BULK-001* og blir plukket til lokasjon *001* av lagerarbeid for plukking av råvarer. Plukkarbeidet blir generert når produksjonen *PRD-002* frigis.

[![Arbeidspolicyer for lager](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Når du planlegger å konfigurere en arbeidspolicy for lageret i dette scenariet, bør du vurdere følgende punkter:

- Lagerarbeid for plassering av ferdigvarer er ikke nødvendig når du rapporterer produktet *SC1* som ferdig fra produksjonordren *PRD-001* til lokasjonen *001*. Årsaken til dette er at operasjonen *Maling* for produksjonsordre *PRD-002* bruker produktet *SC1* på samme lokasjon.
- Lagerarbeid for plukking av råvarer kreves for å flytte råvaren *RM1* fra lagerlokasjonen *BULK-001* til lokasjonen *001*.

Her er et eksempel på en arbeidspolicy som du kan sette opp, basert på disse hensynene:

- **Arbeidspolicynavn:** *Ikke plasseringsarbeid*
- **Arbeidsordretyper:** *Plasser ferdigvarer* og *Plasser koprodukt og biprodukt*
- **Lagerlokasjoner:** Lager *51* og lokasjon *001*
- **Produkter:** *SC1*

Eksempelscenarioet nedenfor inneholder trinnvise instruksjoner om hvordan du definerer lagerarbeidspolicyen i dette scenariet.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Eksempelscenario: Rapportere som ferdig til en lokasjon som ikke er nummerskiltkontrollert

Dette scenarioet viser et eksempel der en produksjonsordre rapporteres som ferdig til en lokasjon som ikke er nummerskiltkontrollert.

Dette scenarioet bruker standard demonstrasjonsdata. Hvis du vil arbeide deg gjennom det ved å bruke verdiene som presenteres her, må du derfor arbeide på et system der standard demodata er installert. Du må også velge den juridiske enheten **USMF**.

### <a name="set-up-a-warehouse-work-policy"></a>Definere en lagerarbeidspolicy

Lagerprosesser inkluderer ikke alltid lagerarbeid. Ved å definere en arbeidspolicy, kan du hindre oppretting av arbeid for råvareplukking og plassering av ferdige varer for et sett med produkter på bestemte lokasjoner.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidspolicyer**.
1. Velg **Ny**.
1. I feltet **Arbeidspolicynavn** angir du *Ikke plasseringsarbeid*.
1. Velg **Lagre** i handlingsruten.
1. På hurtigfanen **Arbeidsordretyper** velger du **Legg til** for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:

    - **Arbeidsordretype:** *Plasser ferdigvarer*
    - **Arbeidsprosess:** *Alle relaterte arbeidsprosesser*
    - **Arbeidsopprettelsesmetode:** *Aldri*
    - **Navn på direkteoverføringspolicy:** La dette feltet stå tomt.

1. Velg **Legg til** på nytt for å legge til nok en rad i rutenettet, og angi deretter følgende verdier for den nye raden:

    - **Arbeidsordretype:** *Plasser koprodukt og biprodukt*
    - **Arbeidsprosess:** *Alle relaterte arbeidsprosesser*
    - **Arbeidsopprettelsesmetode:** *Aldri*
    - **Navn på direkteoverføringspolicy:** La dette feltet stå tomt.

1. På hurtigfanen **Lagerlokasjoner** velger du **Legg til** for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:

    - **Lager:** *51*
    - **Lokasjon:** *001*

1. På hurtigfanen **Produkter** angir du feltet **Produktvalg** til *Valgt*.
1. På **Produkter**-hurtigfanen velger du **Legg til** for å legge til en rad i rutenettet.
1. I den nye raden setter du **Varenummer**-feltet til *L0101*.
1. Velg **Lagre** i handlingsruten.

### <a name="set-up-an-output-location"></a>Definere en utleveringslokasjon

1. Gå til **Organisasjonsstyring \> Ressurser \> Ressursgrupper**.
1. Velg ressursgruppe **5102** i den venstre ruten.
1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Utleveringslager:** *51*
    - **Utleveringssted:** *001*

1. Velg **Lagre** i handlingsruten.

> [!NOTE]
> Lokasjonen *001* er ikke en nummerskiltkontrollert lokasjon. Du kan definere en utleveringslokasjon som ikke er nummerskiltkontrollert, hvis det finnes en gjeldende arbeidspolicy for lokasjonen.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Opprette en produksjonsordre og rapportere den som avsluttet

1. Gå til **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer**.
1. Velg **Ny produksjonsordre** i handlingsruten.
1. I dialogboksen **Opprett produksjonsordre** setter du **Varenummer**-feltet til *L0101*.
1. Velg **Opprett** for å opprette orden og lukke dialogboksen.

    Det legges til en ny produksjons ordre i rutenettet på siden **Alle produksjonsordrer**.

    La den nye produksjonsordren være valgt.

1. I handlingsruten, i fanen **Produksjonsordre**, i **Prosess**-gruppen, velger du **Estimat**.
1. I dialogboksen **Estimat** leser du estimatet og velger deretter **OK** for å lukke dialogboksen.
1. I handlingsruten, i fanen **Produksjonsordre**, i **Prosess**-gruppen, velger du **Start**.
1. I dialogboksen **Start**, på **Generelt**-fanen, angir du feltet **Automatisk stykklisteforbruk** til *Aldri*.
1. Velg **OK** for å lagre innstillingen og lukke dialogboksen.
1. I handlingsruten, i fanen **Produksjonsordre**, i **Prosess**-gruppen, velger du **Ferdigmeld**.
1. I dialogboksen **Ferdigmeld**, på **Generelt**-fanen, setter du **Godtar feil** til *Ja*.
1. Velg **OK** for å lagre innstillingen og lukke dialogboksen.
1. Velg **Arbeidsdetaljer** i gruppen **Generelt** i fanen **Lager** i handlingsruten.

Når produksjonsordren rapporteres som fullført, genereres det ikke arbeid for plassering. Dette skjer fordi en arbeidspolicy er definert som hindrer at arbeidet blir generert når produktet *L0101* rapporteres som ferdig til lokasjon *001*.

## <a name="more-information"></a>Mer informasjon

Hvis du vil ha mer informasjon om menyelementer for mobilenheter, kan du se [Definere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md).

For mer informasjon om nummerskiltmottak og arbeidspolicyer, se [Nummerskiltmottak via lagerappen](warehousing-mobile-device-app-license-plate-receiving.md).

For mer informasjon om innkommende lastadministrasjon for lagerstyring, se [Lagerhåndtering av innkommende laster for bestillinger](inbound-load-handling.md).
