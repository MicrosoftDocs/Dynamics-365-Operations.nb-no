---
title: Automatisering av produksjon etter ordre
description: Denne artikkelen beskriver hvordan du konfigurerer og bruker de forskjellige forbedringene som er lagt til av funksjonen Automatisering av produksjon etter ordre.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9044acb472548a797ed387b08ca6892459785793
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220604"
---
# <a name="make-to-order-supply-automation"></a>Automatisering av produksjon etter ordre

[!include [banner](../includes/banner.md)]

Funksjonen *Automatisering av produksjon etter ordre* legger til flere forbedringer i Microsoft Dynamics 365 Supply Chain Management. Disse forbedringene gjør at du kan utføre følgende oppgaver:

- Vis ressurskapasitetsbelastningen for en brukerdefinert periode, og aktiver derfor langsiktig evaluering av kapasitetsbelastningen.
- Få bedre fleksibilitet ved å styre forsinkelsestoleransen (negative dager) for hver hovedplan.
- Hold produkter tilgjengelige for ordrer i siste øyeblikk, og optimer bruken av eksisterende forsyning ved å utligne den seneste mulige forsyningen til et behov i stedet for å bruke den første mulige forsyningen.
- La komponenttildelingen være fleksibel for produksjonsordrer etter autorisering, slik at systemet kan optimalisere for endringer i etterspørselen i siste øyeblikk. Du kan med andre ord begrense merkingen til ett nivå.
- Kontroller oppfyllelsespolicyen for hver salgsordre. Standardinnstillingene tas fra kundeoppsettet.
- Forbedre konsernintern informasjonsflyt. Bestillinger oppdateres slik at de inkluderer felter for leveringsmåte, leveringsbetingelser og eksternt varenummer. Denne endringen sikrer at detaljert etterspørselsinformasjon kan flyte til det forsynende firmaet.

Denne artikkelen beskriver hvordan du definerer og bruker hver utvidelse.

> [!NOTE]
> Alle forbedringene som beskrives i denne artikkelen, gjelder for systemer som bruker innebygd hovedplanlegging. Følgende to forbedringer støttes også av tillegget for planleggingsoptimalisering for Microsoft Dynamics 365 Supply Chain Management:
>
> - Utsett toleranse på hovedplaner
> - Styr utligningssekvensen som brukes under hovedplanlegging

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Slå på funksjonen Automatisering av produksjon etter ordre

Før du kan bruke funksjonen som beskrives i denne artikkelen, må du aktivere den for systemet. Administratorer kan bruke [funksjonsadministrering](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet der denne funksjonen oppført på følgende måte:

- **Modul:** *Hovedplanlegging*
- **Funksjonsnavn:** *Automatisering av produksjon etter ordre*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Angi antall dager som skal vises på Kapasitetsbelastningsside

På **Kapasitetsbelastning**-siden kan du se gjennom tilgjengelig kapasitet for en ressurs. Funksjonen *Automatisering av produksjon etter ordre* forbedrer **Kapasitetsbelastning**-siden ved å legge til et **Antall dager**-felt. Du kan bruke dette feltet til å begrense antall dager som **oversiktsrutenettet** viser. Verdien du angir, lagres i minnet. Hvis du går ut av siden og kommer tilbake senere, vil **oversiktsrutenettet** fortsatt vise antallet dager du sist angav.

Følg denne fremgangsmåten for å åpne **Kapasitetsbelastning**-siden slik at du kan gå gjennom den tilgjengelige kapasiteten for en enkelt ressurs.

1. Gå til **Organisasjonsstyring \> Ressurser \> Ressurser**.
1. Velg en ressurs som skal undersøkes.
1. På handlingsruten, i fanen **Ressurs** i **Vis**-gruppen, velger du **Kapasitetsbelastning**.
1. Bruk filteret **Antall dager** til å begrense antall dager som **oversiktsrutenettet** viser.

Følg denne fremgangsmåten for å åpne **Kapasitetsbelastning**-siden slik at du kan gå gjennom den tilgjengelige kapasiteten for en ressursgruppe.

1. Gå til **Organisasjonsstyring \> Ressurser \> Ressursgrupper**.
1. Velg en ressursgruppe som skal undersøkes.
1. På handlingsruten, i fanen **Ressursgruppe** i **Vis**-gruppen, velger du **Kapasitetsbelastning**.
1. Bruk filteret **Antall dager** til å begrense antall dager som **oversiktsrutenettet** viser.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Bruk et enkelt merkingsnivå når du autorisere planlagte ordrer

*Merking* brukes til å koble til forsyning og behov. Det ligner på *utligning*, som indikerer hvordan hovedplanleggingen forventes å dekke behov. Merking er imidlertid mer permanent enn utligning. Funksjonen *Automatisering av produksjon etter ordre* gir muligheten til å begrense lagermerking til ett enkelt nivå når planlagte bestillinger autoriseres. Dette legger til følgende nye alternativer i feltet **Oppdater merking** i dialogboksen **Autorisering** når du autorisere en planlagt bestilling:

- *Standard på enkeltnivå* – Merking på enkeltnivå brukes. Merking på enkeltnivå merker bare hovedvaren, ikke stykklistekomponentene. Derfor kan du holde komponenttildeling for produksjonsordrer fleksible etter autorisering. Med merking på enkeltnivå kan systemet optimalisere for endringer i etterspørselen i siste øyeblikk. I *standard* merking på enkeltnivå merkes behovsordrer mot oppfyllelsesordrene, men oppfyllelsesordrer er ikke merket hvis de har restantall.
- *Utvidet på enkeltnivå* – Merking på enkeltnivå brukes. I *utvidet* merking på enkeltnivå merkes behovsordrer mot oppfyllelsesordrene, og oppfyllelsesordrer er alltid merket uansett restantall.

Disse alternativene er også tilgjengelige i **Oppdateringsmerking**-feltet i kategorien **Standardoppdatering** på siden **Hovedplanleggingsparametere**, der du definerer standardvalget for dialogboksen **Autorisering**.

Hvis du vil ha mer informasjon, se [Lagermerking med planleggingsoptimalisering](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Angi forsinkelsestoleranse (negative dager) på hovedplannivå

Funksjonen *Automatisering av produksjon etter ordre* gir deg muligheten til å konfigurere forsinkelsestoleranse (negative dager) på hovedplannivå. Innstillingen er også tilgjengelig på varedeknings- og dekningsgruppenivåene. Hvis negative dager tildeles på mer enn ett nivå, bruker systemet følgende hierarki til å bestemme hvilken innstilling som skal brukes:

- Hvis negative dager er konfigurert på **Hovedplaner**-siden, vil denne innstillingen overstyre alle andre innstillinger for negative dager når planen kjøres.
- Hvis negative dager er konfigurert på **Varedekning**-siden, vil denne innstillingen overstyre innstillingen for dekningsgruppen.
- Negative dager som er konfigurert på **Dekningsgruppe**-siden, gjelder bare hvis negative dager ikke er konfigurert for en relevant vare eller hovedplan.

Følg denne fremgangsmåten for å angi negative dager for en hovedplan.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en hovedplan i listeruten, eller opprett en ny en.
1. Angi *Ja* for alternativet **Negative dager** i hurtigfanen **Horisonter i dager**.
1. I feltet i nærheten angir du antall negative dager som skal tillates.

Hvis du vil ha mer informasjon om hvordan du bruker negative dager, kan du se [Forsinkelsestoleranse (negative dager)](planning-optimization/delay-tolerance.md).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Styr utligningssekvensen som brukes under hovedplanlegging

Hovedplanlegging bruker en *utligningssekvens* for å bestemme hvilken forsyning som vil dekke hvilket behov. Funksjonen *Automatisering av produksjon etter ordre* legger til et nytt **Bruk siste mulige forsyningsalternativ** som gir deg mer kontroll over utligningssekvensen. Det nye alternativet holder produkter tilgjengelige for ordrer i siste øyeblikk, og optimer bruken av eksisterende forsyning ved å utligne den seneste mulige forsyningen til et behov i stedet for å bruke den første mulige forsyningen.

Du kan definere utligningssekvensen på hovedplan-, varedeknings- eller dekningsgruppenivå. Hvis en utligningssekvens er konfigurert på mer enn ett nivå, bruker systemet følgende hierarki til å bestemme hvilken innstilling som skal brukes:

- Hvis det er definert en utligningssekvens på **Hovedplaner**-siden, vil denne innstillingen overstyre alle andre innstillinger for utligningssekvens når planen kjøres.
- Hvis en utligningssekvens er konfigurert på **Varedekning**-siden, vil denne innstillingen overstyre innstillingen for dekningsgruppen.
- Utligningssekvensen som er definert på **Dekningsgruppe**-siden, gjelder bare hvis innstillinger for utligningssekvens ikke er konfigurert for en relevant vare eller hovedplan.

Følg denne fremgangsmåten for å konfigurere utligning på dekningsgruppenivå.

1. Gå til **Hovedplanlegging \> Oppsett \> Dekning \> Dekningsgrupper**.
1. Velg en gruppe i listeruten, eller opprett en ny en.
1. Bruk forbruk av lagerbeholdning i **Utligningssekvens**-delen i fanen **Generelt**, og bruk feltene **Forbruk lagerbeholdning** og **Bruk siste forsyning** til å konfigurere utligningssekvensen. Tabellen senere i denne delen viser hvordan disse innstillingene kombineres for å definere utligningsrekkefølgen.

Følg denne fremgangsmåten for å konfigurere utligning på varedekningsnivået.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg et produkt i rutenettet, eller opprett et ny et.
1. Gå til **Plan**-fanen i handlingsruten, og velg deretter **Varedekning**.
1. **Varedekning**-siden inneholder rader der du kan definere dekningsregler som gjelder varen på hvert lager. Velg en eksisterende rad i rutenettet, eller velg en eksisterende.
1. Merk av for **Overstyr utligningssekvens** i fanen **Generelt**.
1. Bruk feltene **Forbruk lagerbeholdning** og **Bruk siste forsyning** til å konfigurere utligningssekvensen. Tabellen senere i denne delen viser hvordan disse innstillingene kombineres for å definere utligningsrekkefølgen.

Følg denne fremgangsmåten for å konfigurere utligning på hovedplannivået.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en hovedplan i listeruten, eller opprett en ny en.
1. I hurtigfanen **Generelt** angir du *Ja* for alternativet **Overstyr utligningssekvens**.
1. Bruk feltene **Forbruk lagerbeholdning** og **Bruk siste forsyning** til å konfigurere utligningssekvensen. Tabellen senere i denne delen viser hvordan disse innstillingene kombineres for å definere utligningsrekkefølgen.

Tabellen nedenfor viser hvordan innstillingene **Forbruk lagerbeholdning** og **Bruk siste forsyning** kombineres for å fastsette utligningsrekkefølgen.

| | Bruk siste forsyning = Ja | Bruk siste forsyning = Nei |
|---|---|---|
| **Forbruk lagerbeholdning** = *Før all forsyning* | <ol><li>Beholdning</li><li>Eksisterende forsyning som kan oppfylle etterspørselsdatoen</li><li>Eksisterende forsyning som ikke kan oppfylle behovsdatoen, men likevel innen negative dager</li><li>Opprett ny forsyning (planlagt ordre)</li></ol> | <ol><li>Beholdning</li><li>Eksisterende forsyning som kan oppfylle etterspørselsdatoen</li><li>Eksisterende forsyning som ikke kan oppfylle behovsdatoen, men likevel innen negative dager</li><li>Opprett ny forsyning (planlagt ordre)</li></ol> |
| **Forbruk lagerbeholdning** = *Etter all forsyning* | <ol><li>Eksisterende forsyning som kan oppfylle etterspørselsdatoen</li><li>Beholdning</li><li>Eksisterende forsyning som ikke kan oppfylle behovsdatoen, men likevel innen negative dager</li><li>Opprett ny forsyning (planlagt ordre)</li></ol> | <ol><li>Eksisterende forsyning som kan oppfylle etterspørselsdatoen</li><li>Eksisterende forsyning som ikke kan oppfylle behovsdatoen, men likevel innen negative dager</li><li>Beholdning</li><li>Opprett ny forsyning (planlagt ordre)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Gå gjennom og angi oppfyllelsespolicyen som gjelder hver salgsordre

Oppfyllelsespolicyer styrer prosentandel av totalprisen eller antallet av en ordre, som må være fysisk reservert før du kan frigi en salgsordre til lageret. Du kan definere en global standard oppfyllelsespolicy og deretter overstyre den for bestemte kunder etter behov. Funksjonen *Automatisering av produksjon etter ordre* gir muligheten til å vise hvilke standardpolicyer som faktisk gjelder en ordre, og bruke en ordrespesifikk overstyring etter behov.

- Hvis du vil definere standardverdier for oppfyllelsespolicy for salgsordrer, kan du gå til **Kunder \> Oppsett \> Kundeparametere**. I fanen **Lagerstyring** angir du deretter feltet **Oppfyllelsespolicy for salgsordre** til navnet på policyen du vil bruke. 
- Hvis du vil angi en kundespesifikk oppfyllelsespolicy for salgsordrer, kan du gå til **Kunder \> Kunder \> Alle kunder**. I fanen **Lager** angir du deretter feltet **Oppfyllelsespolicy** til navnet på policyen du vil bruke.

Følg denne fremgangsmåten for å vise standardpolicyen som gjelder enhver ordre, og bruke en ordrespesifikk overstyring.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Åpne salgsordren du vil inspisere eller redigere.
1. Velg **Topptekst**-visningen.
1. I hurtigfanen **Lager** gjennomgår og redigerer du følgende felter etter behov:

    - **Oppfyllelsespolicy for ordre** – Velg oppfyllelsespolicyen som skal brukes for den valgte ordren. Standardpolicyen vil bli overstyrt. Hvis du vil bruke standard oppfyllelsespolicy som vises i **Standard oppfyllelsespolicy**-feltet, lar du dette feltet stå tomt.
    - **Standard oppfyllelsespolicy** – Dette feltet viser standard oppfyllelsespolicy som gjelder hvis feltet **Oppfyllelsespolicy for ordre** er tomt. Dette feltet er skrivebeskyttet. Hvis den er tom, defineres det ingen kundespesifikk eller global standard oppfyllelsespolicy.

    Hvis både feltet **Oppfyllelsespolicy for ordre** og feltet **Standard oppfyllelsespolicy** er tomme, gjelder ingen oppfyllelsespolicy. Andre begrensninger kan imidlertid være på plass, og kan kreve at reserveringer eller andre betingelser oppfylles før salgsordren kan frigis.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Angi leveringsmåte og -betingelser for individuelle bestillingslinjer

Alle bestillinger inkluderer **leveringsbetingelser** og **leveringsmåteinnstillinger** i ordrehodet. Funksjonen *Automatisering av produksjon etter ordre* legger til disse innstillingene i hver ordrelinje. Derfor kan du definere overstyringer av **leveringsbetingelsene** eller **leveringsmåteverdien** for noen eller alle ordrelinjer etter behov. For linjer der det ikke er definert noen overstyring, brukes verdien fra hodet. Du kan angi om en endring i verdien til et av eller begge disse feltene på ordrehodet også skal oppdatere alle linjene.

Følg denne fremgangsmåten for å angi hva som skal skje med linjeinnstillingene hvis en bruker endrer **leveringsbetingelsene** eller **leveringsmåteverdien** i et ordrehode.

1. Gå til **Innkjøp og leverandører** \> Oppsett \> Parametere for innkjøp og leverandører.
1. I fanen **Generelt** velger du koblingen **Oppdater ordrelinjer** i hurtigfanen **Standardverdier og -parametere**.
1. Velg en av følgende verdier i feltene **Oppdatering av leveringsbetingelser** og **Oppdater leveringsmåte** i dialogboksen **Oppdater ordrelinjer**:

    - *Aldri* – Oppdater aldri ordrelinjene etter at innstillingene er endret på ordrehodet.
    - *Alltid* – Oppdater alltid alle ordrelinjene etter at innstillingene er endret på ordrehodet.
    - *Ledetekst* – Hvis en bruker endrer en eller begge innstillinger i ordrehodet, åpner du en dialogboks der du blir spurt om brukeren vil oppdatere alle linjene slik at de samsvarer med endringen til en eller begge innstillinger.

Følg denne fremgangsmåten for å angi leveringsinformasjon på et bestillingshode.

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Åpne bestillingen du vil redigere.
1. Velg **Topptekst**-visningen.
1. I hurtigfanen **Levering** angir du feltene **Leveringsmåte** og **Leveringsbetingelser** etter behov.
1. Avhengig av innstillingene på siden **Parametere for innkjøp og leverandører**, kan du bli spurt om du vil bruke endringene på alle ordrelinjer.

Følg denne fremgangsmåten for å angi leveringsinformasjonsoverstyringer på en bestillingshodelinje.

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Åpne bestillingen du vil redigere.
1. Velg **Linjer**-visningen.
1. I hurtigfanen **Bestillingslinjer** velger du linjen du vil redigere.
1. I hurtigfanen **Linjedetaljer** angir du feltene **Leveringsmåte** og **Leveringsbetingelser** etter behov på fanen **Levering**. Fjern merket i et eller begge felt for å bruke tilsvarende innstillinger i hodet.

Når det gjelder konserninterne ordrer, synkroniseres verdier for feltene **Leveringsmåte** og **Leveringsbetingelser** på hver bestillingslinje mellom bestillingen og den relaterte salgsordren.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Synkronisere eksterne vare-ID-er og beskrivelser for konserninterne ordrer

Når det gjelder konserninterne ordrer, gjør funksjonen *Automatisering av produksjon etter ordre* automatisk at eksterne vare-ID-er og tekstbeskrivelser på bestillingslinjer kan synkroniseres med de relaterte konserninterne salgsordrelinjene, uansett om bestillingen er for direktelevering. Funksjonen gir også muligheten til å angi den endelige eksterne kundekontoen i en konsernintern bestilling. Systemet vil automatisk ta eksterne vare-ID-er og tekstbeskrivelser fra den eksterne kundeposten i stedet for (intern) konsernintern leverandørpost.

Følg denne fremgangsmåten for å konfigurere en konsernintern leverandør til å synkronisere eksterne vare-ID-er og varenavn mellom konserninterne bestillinger og de relaterte konserninterne salgsordrene.

1. Gå til **Innkjøp og leverandører \> Leverandører \> Alle leverandører**.
1. Velg den konserninterne leverandøren du vil definere.
1. I handlingsruten i kategorien **Generelt** i **Oppsett**-gruppen, velger du **Konsernintern**.
1. På siden **Konsernintern** på fanen **Bestillingspolicyer** i delen **Konsernintern bestilling -\> Konsernintern salgsordre** merker du av for **Ekstern vare-ID og eksternt varenavn**.

Følg denne fremgangsmåten for å angi den endelige eksterne kundekontoen for en konsernintern bestilling. **Kundekonto**-feltet gjelder bare konserninterne bestillinger. Bruk det til å angi kontonummeret til kunden som til slutt vil motta varene. Når dette feltet er angitt, vil bestillingslinjer ta eksterne varebeskrivelser og -numre fra den angitte kundekontoen i stedet for den konserninterne leverandøren som er angitt på bestillingen. Hvis du endrer kundekontoen senere, oppdateres eksterne varebeskrivelser og ID-er slik at de samsvarer med verdiene for den nye kontoen. Eksterne varebeskrivelser og vare-ID-er for hver linje blir også synkronisert med den samsvarende konserninterne salgsordren.

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Åpne bestillingen du vil definere, eller opprett en ny.
1. Velg **Topptekst**-visningen.
1. I **Referanse**-delen angir du **Kundekonto**-feltettil den relevante eksterne kundekontoen.

Følg denne fremgangsmåten for å angi eksterne vare-ID-er og tekstbeskrivelser for en bestillingslinje for en konsernintern ordre. Verdiene du angir, blir synkronisert med de relaterte konserninterne salgsordrelinjene, uansett om bestillingen er for direktelevering.

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Åpne bestillingen du vil definere, eller opprett en ny.
1. Velg **Linjer**-visningen.
1. I hurtigfanen **Bestillingslinjer** velger du linjen du vil redigere.
1. I hurtigfanen **Linjedetaljer** på fanen **Generelt** gir du en ekstern beskrivelse av varen som er angitt på den valgte ordrelinjen i **Ordrelinje**-delen i fanen **Linjedetaljer**. Denne verdien synkroniseres med den relaterte konserninterne salgsordrelinjen.
1. I **Referanse**-delen i feltet **Eksternt** angir du en ekstern vare-ID for varen som er angitt på den valgte ordrelinjen. Denne verdien synkroniseres med den relaterte konserninterne salgsordrelinjen.

Hvis du vil ha mer informasjon, kan du se [Opprett og fakturer en konsernintern salgsordre for en ekstern kunde](../sales-marketing/intercompany-sales-order-for-external-customer.md).
